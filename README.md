# tng-plugins

Personal plugin marketplace 

## Install

```bash
# One-time
claude plugin marketplace add https://github.com/nmtrang29/tng-plugins

# Install a plugin
claude plugin install writing@tng-plugins

# Reload Claude Code to pick it up
/reload-plugins
```

## Plugins

| Plugin | Skill | Description |
|---|---|---|
| ✍️ writing | [analyse-writing-style-blog](plugins/writing/skills/analyse-writing-style-blog/) | Sample posts from a blog and produce a structured style guide for the author's voice. |
| | [analyse-writing-style-gdrive](plugins/writing/skills/analyse-writing-style-gdrive/) | Read a person's Drive docs in parallel and produce a structured style guide for their voice. |
| | [write-with-me](plugins/writing/skills/write-with-me/) | Collaborative drafting in a target voice: outline, write in sections, audience-aware critique, iterate. |
| 📊 reporting | [activity-report](plugins/reporting/skills/activity-report/) | Time-estimate breakdown of Claude Code activity by tag and day, with optional ticket drill-down and chat delivery. |
| 🎨 design | [create](plugins/design/skills/create/) | Design a UI from scratch — brief → craft passes (typography, layout, color, style) → usability + accessibility → hand-off. |
| | [critique](plugins/design/skills/critique/) | Review an existing UI through visual-craft, usability, and accessibility passes; returns prioritized, specific feedback. |

More coming.

## Updating

When plugins are updated upstream, run:

```bash
/plugin update
```
