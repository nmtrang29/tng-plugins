---
name: analyse-writing-style-blog
description: Analyse the writing style of a blog or blog author by sampling many posts. Triggered when the user gives a blog URL and asks to characterise / analyse / extract the author's writing style. Examples — "analyse writing style at https://example.com/blog", "/analyse-writing-style-blog https://www.noidea.dog/blog", "characterise how X writes from their blog posts".
---

# Analyse Writing Style from a Blog

Build a comprehensive writing-style guide for a blog author by sampling **many** posts (target 30+). Use parallel subagents to read posts in batches, then synthesise into a structured style guide in the canonical section format.

## Inputs

- **Blog URL** — could be the index page (`https://example.com/blog`), a Medium/Substack root (`https://author.medium.com`), or a single-post URL on a personal site (treat as a starting point and crawl from there)

## Required tools

- `WebFetch` (built-in) — fetch and parse pages
- `Agent` (built-in) — parallel subagent dispatch
- `WebSearch` (built-in, optional) — if the index page doesn't reveal enough posts, search for more from the same domain or author

## Step-by-step procedure

### 1. Crawl the blog index and collect post URLs

Fetch the blog URL. Ask the WebFetch prompt to:
- List every post title and URL on the page
- Note pagination (Older Posts / Next Page) and the URL pattern

If pagination exists, fetch the next page(s) until you have **a large pool of post URLs (target 50+)**. Don't stop at 10 — the goal of this skill is broad coverage.

For Medium / Substack, the homepage typically shows recent posts; check archive links (e.g. `/archive`) for the full list.

### 2. Filter and select a representative sample

From the pool of post URLs, select **at least 30 posts** for analysis. If the blog has fewer than 30 posts total, use all of them.

Selection criteria — aim for variety:
- Span the catalog's date range (oldest, middle, recent)
- Mix genres if the blog has them (technical, personal, conference reports, advice, etc.)
- Skip posts that are clearly trivial ("wrote some things", short link roundups) unless they reveal voice
- Skip pure interview transcripts where the author is mostly quoting others

If unclear how to pick, ask the user for their preference, but default to sampling broadly.

### 3. Fan out parallel subagents to read posts

Split the post URLs into ~6 batches of ~5–7 posts each. Dispatch one general-purpose subagent per batch in parallel (single message, multiple `Agent` tool calls). Use `run_in_background: true`.

Each subagent prompt should:
- Provide the list of post URLs and titles in the batch
- Instruct: use WebFetch on each URL, ask for opening 4–6 paragraphs verbatim, all section headings, and 2–3 representative sentences from the middle and end
- Note: WebFetch may decline to return full text verbatim due to length limits; in that case ask for short representative quotes (under 200 chars each) plus a structural summary
- Say explicitly: **"DO NOT summarise post contents. Characterise HOW the author writes, not WHAT they write about."**
- Ask for 1200 words of structured markdown under the canonical eight sections (see Template below)
- Ask for 10–12 short direct quotes (under 200 chars each) illustrating specific moves
- Flag any genre-specific differences within the batch

### 4. Wait for all batches, then synthesise

When all subagents have returned, consolidate findings into a single style guide. Use the **canonical eight-section template** (see `references/style-guide-template.md` for the full spec and an example).

The synthesis must:
- Cross-reference observations across batches — patterns appearing in 4+ batches are core voice; patterns in 1–2 batches are genre-specific or evolving over time
- Preserve direct quotes (verbatim) as evidence
- Capture specific stylistic moves with concrete examples, not generic claims
- Note signature expressions (recurring phrases that show up in multiple posts)
- Note metaphor patterns and whether they extend across posts (e.g. worldbuilding)
- Note tonal evolution across time if the date range is wide
- Note anti-patterns (what the author consistently avoids)

### 5. Determine output filename

Default location: `~/Downloads/analysed-writing-style/`

Filename: `<firstname>_<lastname>_<domain>.md` (lowercase, underscore-separated, domain dots converted to underscores). Examples:
- `https://www.noidea.dog/blog` (Tanya Reilly) → `tanya_reilly_noidea_dog.md`
- `https://steve-yegge.medium.com/` → `steve_yegge_medium_com.md`
- `https://petersouter.xyz/blog` (Peter Souter) → `peter_souter_petersouter_xyz.md`

If the author's name is **not** clearly discoverable from the blog (About page, byline, footer, URL), **ask the user** for the author's first and last name before writing. Don't guess.

Domain rules:
- Strip `www.` and protocol
- Convert dots to underscores
- For Medium subdomains (`author.medium.com`), use the full subdomain → `<firstname>_<lastname>_medium_com.md`

**Always save as new version — never overwrite.** Check if `<name>_<domain>.md` already exists; if so, save as `<name>_<domain>_v2.md`. If `_v2` exists, `_v3`. Continue incrementing.

### 6. Write the style guide

Write the consolidated guide to the chosen path. Confirm the path and word count to the user.

### 7. Offer to set as the active writing voice

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
2. **Voice and Perspective** — first-person/second-person register, hedge style, confidence/vulnerability balance, spelling conventions
3. **Narrative Structure** — overall arc(s) across post types; common section patterns
4. **Structural Patterns** — heading conventions, punctuation/visual style, opening hooks, section organisation, transitions, closing style
5. **Tone Characteristics** — confidence vs vulnerability, humour style, handling disagreement
6. **Tone Shifts** — how register changes across post genres
7. **Content Themes** — recurring topics
8. **Language Choices** — signature expressions, metaphors, emphasis techniques

Plus:
- **Authenticity Markers** — specifics that prove voice is real (names, dates, links, numbers, recurring projects, world-building vocabulary)
- **What to Avoid** — anti-patterns observed
- **Practical Application** — a 12–20 step cheat sheet for writing in this voice

## Output conventions

- Preserve the author's heading-case conventions (sentence case vs Title Case)
- Preserve spelling conventions (British/American)
- Do not embellish — every claim in the guide should be backed by an observed pattern or a quoted example
- Keep the file self-contained

## Common pitfalls

- **Don't sample too few posts** — the explicit goal of this skill is broad coverage. Target 30+; if WebFetch budget allows, push higher.
- **Don't accept WebFetch summaries as direct evidence** — when WebFetch declines to return verbatim text, the subagent should explicitly ask for short verbatim quotes instead, and flag any inference vs. observation.
- **Don't dispatch subagents serially** — they must run in parallel via a single message with multiple Agent tool calls.
- **Don't blend genres** — if the blog has very different post types (technical vs personal vs conference reports), make sure each genre is represented in the sample.
- **Don't infer biography** — if you can't confirm the author's name from the blog itself, derive the filename from the domain.

## When to recommend the gdrive skill instead

If the user mentions internal docs, Google Drive, or an email address, they probably want `analyse-writing-style-gdrive` instead. This skill is for **public web content** — personal blogs, Medium, Substack, company blogs, dev sites.
