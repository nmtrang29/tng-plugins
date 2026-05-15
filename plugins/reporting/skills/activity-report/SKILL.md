---
name: activity-report
description: Use when the user asks for a summary of their Claude Code activity, time tracking, session history, or daily/weekly work report. Invoked as /activity-report with an optional date range or ticket argument.
allowed-tools: Bash(python3:*), Read, Grep
user-invocable: true
---

# Activity Report

Generate a time-estimate breakdown of Claude Code usage, grouped by **tag** (from `/tag`) and day. Sessions without a tag are grouped under `(untagged)`.

## Invocation

`/activity-report <argument>` where `<argument>` is natural language:

| Input | Meaning |
|-------|---------|
| `today` | Current date |
| `yesterday` | Previous date |
| `last 3 days` | Today and 2 days prior |
| `last week` | Mon–Fri of previous week |
| `this week` | Mon through today |
| `this month` | 1st of current month through today |
| `march 4-6` | Specific date range |
| *(empty)* | Default to `today` |
| `ABC-123` | Escalation mode — report time for a specific ticket |
| `ABC-123 last 2 weeks` | Escalation mode with date range (default: last 30 days) |

A "ticket" is anything matching the generic pattern `[A-Z]{2,}-\d+` (Jira, Linear, GitHub project keys, etc.). If your tracker uses a different scheme, adjust the regex in the implementation.

## Data Source

`~/.claude/history.jsonl` — one JSON object per line, each representing a **user message**. Schema:

```json
{"display": "message text", "timestamp": 1772789318435, "project": "/Users/.../repo-name", "sessionId": "uuid", "pastedContents": {}}
```

- `timestamp`: Unix epoch in **milliseconds**
- `project`: Full path to the working directory — use the last path component as the project name
- `sessionId`: Groups messages into sessions (one session = one Claude Code conversation)
- `display`: The user's message text (use to infer task descriptions)

`~/.claude/tags.jsonl` — optional, created by `/tag`. One JSON object per line with manual session tags:

```json
{"sessionId": "uuid", "tag": "ABC-123", "timestamp": 1773000000000}
```

## Time Estimation Algorithm

1. Group messages by `sessionId`, sorted by `timestamp`
2. For each consecutive pair of messages in a session, compute the gap
3. If gap <= 15 minutes: add it to session time
4. If gap > 15 minutes: cap at 15 minutes (assumes context switch)
5. A session with only one message: count as 5 minutes
6. Round each tag-day total up to the nearest 5-minute increment
7. Sum per tag per day (sessions without a tag go under `(untagged)`)

## Output Format

Produce TWO outputs:

### 1. Per-tag detail (by day)

For each day, for each tag active that day:
- Estimated time
- Project(s) where work happened
- Brief task description (inferred from message content — 1 line max)

Sessions without a `/tag` are grouped under `(untagged)`.

### 2. Summary table

A markdown table with **tags** as rows, days as columns, and time per cell. Include a Project(s) column showing which repos were used. Include row and column totals.

Example:

```
| Tag | Project(s) | Mar 4 | Mar 5 | Mar 6 | Total |
|---|---|---|---|---|---|
| ABC-123 | service-api | 30min | — | 2h 45min | 3h 15min |
| refactor-auth | webapp | — | 3h 15min | 40min | 3h 55min |
| (untagged) | webapp, notes | 30min | 2h | 1h | 3h 30min |
| Daily total | | 1h | 5h 15min | 4h 25min | ~10h 40min |
```

Tags come **only** from `/tag` entries in `tags.jsonl`. Do NOT auto-detect ticket patterns from message content.

## Escalation Mode

When the argument matches a ticket pattern (e.g. `ABC-123`), switch to escalation mode.

### Step 1: Find tagged sessions

Use a `python3 -c` command to:
1. Read `~/.claude/tags.jsonl` and find all sessions tagged with the target ticket
2. Default date range: last 30 days (override with an explicit range, e.g. `ABC-123 last 2 weeks`)
3. For each tagged session, compute time using the standard algorithm from `~/.claude/history.jsonl`

Only sessions explicitly tagged via `/tag` are included — no auto-detection from message content.

### Step 2: Escalation report output

```
## Escalation Report — ABC-123

### Sessions

| Date | Project | Time | Classification | Summary |
|------|---------|------|----------------|---------|
| Mar 8 | service-api | 1h 30min | active-work | Reproduced reported issue |
| Mar 9 | webapp | 45min | partial (50%) | Debugging UI, partially related |
| Mar 10 | runbooks | 20min | reference-only | — |

### Total time: 1h 52min
(excluding reference-only sessions)
```

## Implementation (standard mode)

Use a single `python3 -c` command via Bash to:
1. Parse the date range argument into start/end dates
2. Read and filter `~/.claude/history.jsonl`
3. Read `~/.claude/tags.jsonl` (if it exists) to get manual tags per session
4. Output structured JSON with per-session, per-tag, per-day data, including project names and the first 10 messages (truncated to 150 chars) per session
5. Sessions with multiple tags contribute their time to **each** tag
6. Sessions without any tag are grouped under the key `(untagged)`

Then:
1. Format the results as markdown using the output format above, with tags as the primary grouping
2. Infer task descriptions from the `display` fields

## Optional: Chat delivery

After displaying the report in the terminal, the user may want to send the **summary table** (output #2) to a chat tool (Slack, Teams, Discord, etc.) as a DM or channel post.

This step is opt-in and tool-agnostic. If the user has a chat MCP server configured and wants delivery:

1. Ask which tool / recipient / channel to send to (or read it from a config the user has set up)
2. Wrap the summary table in a code block (triple backticks) so it renders as monospace
3. Format the message as: `*Activity Report — <date range>*\n\n` followed by the table inside triple backticks
4. Add the relevant chat MCP tool to `allowed-tools` in this skill's frontmatter before invoking it

If no chat tool is configured or the user doesn't ask for delivery, skip this step — the terminal output is the report.

## Common Mistakes

- **Wrong file**: Do NOT look in `~/.claude/projects/` or `~/.claude/conversations/` — all history is in `~/.claude/history.jsonl`
- **Timestamp units**: Timestamps are in **milliseconds**, not seconds — divide by 1000 for Python `datetime.fromtimestamp()`
- **Multi-day sessions**: A session can span multiple days — split time at midnight boundaries
- **Project name**: Extract from the last path component of the `project` field, not the full path
