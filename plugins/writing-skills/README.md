# writing-skills

A growing collection of Claude Code skills for writing collaboration. Capture someone's voice from real writing samples, then draft, review, and iterate prose in that voice with audience-aware critique.

## Skills

### `/analyse-writing-style-gdrive <email>`

Analyses the writing style of a person by reading their Google Drive docs.

**Input:** an email address (e.g. `jane.doe@example.com`)

**What it does:**
1. Paginates the Drive API for all docs the user owns
2. Filters out trivial scratch docs, 1-1 notes, meeting transcripts, and user-interview transcripts
3. Asks you which docs (if any) to exclude before reading
4. Dispatches 10 parallel subagents to read ~150 prose-heavy docs and extract style observations
5. Synthesises observations into a structured style guide following the canonical 8-section template
6. Writes the guide to `~/Downloads/analysed-writing-style/<firstname>_<lastname>_gdrive.md` (always saves as a new version — never overwrites)

**Required tools:** a Google Drive MCP server exposing `*search_files` and `*get_doc_as_markdown` tools. The skill recommends Google's official remote Drive MCP (`https://drivemcp.googleapis.com/mcp/v1`) and falls back to community options like `piotr-agier/google-drive-mcp` for CLI use.

### `/analyse-writing-style-blog <blog-url>`

Analyses the writing style of a blog or its author by sampling many posts.

**Input:** a blog URL (index page, Medium/Substack root, or any post URL)

**What it does:**
1. Crawls the blog index, paginating through Older Posts
2. Selects a diverse sample of 30+ posts spanning the date range and post types
3. Dispatches parallel subagents to read posts and extract style observations
4. Synthesises into a structured style guide following the canonical 8-section template
5. Writes the guide to `~/Downloads/analysed-writing-style/<firstname>_<lastname>_<domain>.md` (always saves as a new version)

**Required tools:** only the built-in `WebFetch` and `Agent` tools.

## Output

Both skills follow the same canonical 8-section template (see [`skills/*/references/style-guide-template.md`](skills/analyse-writing-style-gdrive/references/style-guide-template.md)):

1. **Core Voice** — one-paragraph characterisation
2. **Voice and Perspective** — register, hedge style, vulnerability balance
3. **Narrative Structure** — overall arcs, common section patterns by genre
4. **Structural Patterns** — heading conventions, punctuation/visual style, opening hooks, transitions, closings
5. **Tone Characteristics** — diagnostic vs declarative, humour style, handling disagreement
6. **Tone Shifts** — how register changes across genres
7. **Content Themes** — recurring topics
8. **Language Choices** — signature expressions, metaphors, emphasis techniques

Plus: **Authenticity Markers**, **What to Avoid**, and a **Practical Application** cheat sheet.

## Output conventions

- Default location: `~/Downloads/analysed-writing-style/`
- Filename: `<firstname>_<lastname>_gdrive.md` (Drive) or `<firstname>_<lastname>_<domain>.md` (blog)
- Versioning: always save as new (`_v2`, `_v3`, ...) — never overwrite

## Why this exists

Capturing someone's writing voice from a small sample (5–10 docs) misses a lot. These skills push toward 100+ samples and parallel reading so the resulting guide reflects consistent patterns, not noise. The output is structured for use as a system prompt: when you want Claude to draft something in a specific person's voice, attach the corresponding style guide as context.
