---
name: analyse-writing-style-gdrive
description: Analyse the writing style of a person by reading their Google Docs at scale. Triggered when the user gives an email address and asks to characterise / analyse / extract their writing style from Google Drive. Examples — "analyse writing style of jane@example.com from Drive", "/analyse-writing-style-gdrive trang.nguyen@datadoghq.com", "characterise how X writes based on their gdrive docs".
---

# Analyse Writing Style from Google Drive

Build a comprehensive writing-style guide for a person by sampling their Google Drive docs at scale. Use parallel subagents to read ~150 prose-heavy docs, then synthesise observations into a structured style guide in the canonical section format.

## Inputs

- **Email address** of the person whose style to analyse (e.g. `trang.nguyen@datadoghq.com`)
- Optional: a list of docs to exclude

## Required tools

This skill requires a Google Drive MCP server exposing at least:
- A search tool matching `mcp__*__search_files` — Drive query syntax
- A doc-export tool matching `mcp__*__get_doc_as_markdown` (or equivalent that returns Google Doc content as markdown / plain text)

### Recommended MCP server

**Google's official remote Drive MCP server** — `https://drivemcp.googleapis.com/mcp/v1`. It's maintained by Google, uses OAuth, and inherits Google Workspace permissions. Setup:
1. Create (or reuse) a Google Cloud project
2. Enable the **Google Drive API** and **Google Drive MCP API**
3. Configure the OAuth consent screen, add scopes `drive.readonly` and `drive.file`
4. Create an OAuth 2.0 Client (Web application), add `https://claude.ai/api/mcp/auth_callback` as the authorised redirect URI
5. In Claude.ai or Claude Desktop, add a custom connector with the server URL and your OAuth client ID/secret

**Plan requirement:** Claude Enterprise, Pro, Max, or Team. The official remote server is built for Claude.ai / Claude Desktop; for Claude Code (CLI), a community Drive MCP like `piotr-agier/google-drive-mcp` is the fallback.

If no Drive MCP tools are loaded when this skill runs, stop and tell the user to install/authenticate one before re-invoking. Reference: <https://developers.google.com/workspace/drive/api/guides/configure-mcp-server>.

## Step-by-step procedure

### 1. Confirm the email and check tool availability

Confirm the email address from the user's invocation. If the email is missing or ambiguous, ask once.

Check that a `*search_files` and `*get_doc_as_markdown` tool is available. If not, tell the user which Drive MCP needs to be authenticated and stop.

### 2. Paginate to find all the user's Google Docs

Use the search tool with this query template:

```
'<email>' in owners and mimeType = 'application/vnd.google-apps.document' and trashed = false
```

Page through results using `modifiedTime < '<oldest-time-from-previous-page>'` until the result set is empty or you've reached the earliest doc. For each page request `max_results: 100`.

Persist the combined results (id, name, size, modifiedTime) to a tmp file like `/tmp/all_docs_raw.txt` if it'll exceed your context window.

### 3. Filter to prose-heavy candidates

Drop:
- `Untitled document` entries
- Docs under 3 KB (usually scratch)
- `User Interview` / `Interview Notes` / `Call Notes` / `Client call` titles (mostly verbatim quotes from others, not the user's prose)
- `Notes - X / Y` 1-1 patterns (often bullet shorthand)
- Pure `Meeting Notes` (often collaborative transcripts)

Keep the rest. Target ~150 candidates. If the corpus is larger, sample by genre diversity rather than capping at the top of the list.

### 4. Ask the user about exclusions BEFORE reading

Show the user the filtered list (count + a representative sample of titles, not the full list). Ask explicitly: **"Any docs you'd like to exclude from the analysis?"**

Wait for their answer. Common reasons users want to exclude:
- Politically sensitive docs (team dynamics, performance reviews of others)
- Personal docs they don't want characterised
- Docs they didn't actually author (collaborative drafts)

### 5. Split into batches and fan out parallel subagents

Split the candidate list into ~10 batches of ~12–15 docs each. Dispatch one general-purpose subagent per batch in parallel (single message, multiple `Agent` tool calls). Use `run_in_background: true` so you get notified as each completes.

Each subagent prompt should:
- Name the MCP tool to use (`mcp__*__get_doc_as_markdown` with the document_id)
- List the doc IDs and titles in the batch
- Say explicitly: **"DO NOT summarise doc contents. Characterise HOW she/he writes, not WHAT they write about."**
- Ask for 1200 words of structured markdown under the canonical eight sections (see Template below)
- Ask for 10–12 short direct quotes (under 200 chars each) illustrating specific moves
- Flag any genre-specific notes in the batch (e.g. if the batch is mostly peer feedback, note what's specific to that genre)

### 6. Wait for all batches, then synthesise

When all subagents have returned, consolidate their findings into a single style guide. Use the **canonical eight-section template** (see `references/style-guide-template.md` for the full template and an example).

The synthesis must:
- Cross-reference observations across batches — patterns that appear in 5+ batches are core voice; patterns in 1–2 batches are genre-specific
- Preserve direct quotes (verbatim) as evidence
- Capture specific stylistic moves with concrete examples, not generic claims
- Note British / European vs. American spelling if observed
- Note signature expressions (recurring phrases that show up in multiple docs)
- Note metaphor patterns (or their absence)
- Note anti-patterns (what the author consistently avoids)

### 7. Determine output filename

Default location: `~/Downloads/analysed-writing-style/`

Filename: `<firstname>_<lastname>_gdrive.md` (lowercase, underscore-separated). Examples:
- `trang.nguyen@datadoghq.com` → `trang_nguyen_gdrive.md`
- `jane.doe@example.com` → `jane_doe_gdrive.md`

**Always save as new version — never overwrite.** Check if `<name>_gdrive.md` already exists; if so, save as `<name>_gdrive_v2.md`. If `_v2` exists, `_v3`. Continue incrementing.

If the email's name part is ambiguous (e.g. a shared mailbox, initials only), ask the user for the person's first and last name.

### 8. Write the style guide

Write the consolidated guide to the chosen path. Confirm the path and word count to the user.

### 9. Offer to set as the active writing voice

After writing, ask the user:

> Want to add this style guide to `~/.claude/writing-style.md` so it can be picked up by `/write-with-me`?

**If no** → done.

**If yes:**
- If `~/.claude/writing-style.md` does **not** exist → write the contents of the new style guide to that file.
- If `~/.claude/writing-style.md` **already exists** → ask a second question with three options:
  - **Append** — add the new style guide to the end of the existing file, preceded by a horizontal rule and a heading like `## Added <YYYY-MM-DD>: from <source description>`. Useful for layering multiple voices over time.
  - **Replace** — overwrite the existing file with the new content. Recommended if you're consolidating into a single canonical voice.
  - **Skip** — leave `~/.claude/writing-style.md` untouched.

Confirm to the user which action was taken and the final path.

## Canonical eight-section template

The synthesis should follow this structure (see `references/style-guide-template.md` for the full spec and an example):

1. **Core Voice** — one-paragraph characterisation
2. **Voice and Perspective** — first-person/third-person/register patterns, hedge style, confidence/vulnerability balance, spelling conventions
3. **Narrative Structure** — overall arc(s) across doc types; common section patterns
4. **Structural Patterns** — heading conventions, punctuation/visual style, opening hooks, section organisation, transitions, closing style
5. **Tone Characteristics** — diagnostic vs declarative, empathy, humour style, handling disagreement
6. **Tone Shifts** — how register changes across genres (formal docs vs personal vs peer feedback vs etc.)
7. **Content Themes** — recurring topics
8. **Language Choices** — signature expressions, metaphors, emphasis techniques, technical/business writing patterns

Plus:
- **Authenticity Markers** — specifics that prove voice is real (names, dates, links, numbers, internal vocabulary)
- **What to Avoid** — anti-patterns observed
- **Practical Application** — a 12–20 step cheat sheet for writing in this voice

## Output conventions

- Use sentence case for headings if the subject uses sentence case; preserve their convention
- Preserve British / European spelling if observed in the corpus
- Do not embellish — every claim in the guide should be backed by an observed pattern or a quoted example
- Keep the file self-contained; do not require external references

## Common pitfalls

- **Don't auto-include the user's own previous analysis** if a style guide already exists in the output folder — start fresh
- **Don't reuse the doc-the-user-excluded** when re-running
- **Don't summarise doc contents in the subagent prompts** — the goal is HOW they write, not WHAT they write about
- **Don't pad with generic AI-writing-style observations** — every section should be specific to this person
- **Don't dispatch subagents serially** — they must run in parallel via a single message with multiple Agent tool calls
