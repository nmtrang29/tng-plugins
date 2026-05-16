# tng-plugins

Personal plugin marketplace 

## Install

```bash
# One-time
claude plugin marketplace add https://github.com/nmtrang29/tng-plugins

# Install a plugin
claude plugin install writing-skills@tng-plugins

# Reload Claude Code to pick it up
/reload-plugins
```

## Plugins

### ✍️ writing-skills

| Skill | Description |
|---|---|
| [analyse-writing-style-blog](plugins/writing-skills/skills/analyse-writing-style-blog/) | Extract a blog's writing style from sampled posts. |
| [analyse-writing-style-gdrive](plugins/writing-skills/skills/analyse-writing-style-gdrive/) | Extract a person's writing style from their Drive docs. |
| [write-with-me](plugins/writing-skills/skills/write-with-me/) | Draft, review, and iterate in a target voice. |

### 📊 reporting

| Skill | Description |
|---|---|
| [activity-report](plugins/reporting/skills/activity-report/) | Group Claude Code usage by tag and day; optional ticket drill-down and chat delivery. |

### 🎨 design

| Skill | Description |
|---|---|
| [create](plugins/design/skills/create/) | Design a UI from scratch. |
| [critique](plugins/design/skills/critique/) | Review a UI; return prioritized feedback. |

More coming.

## Updating

When plugins are updated upstream, run:

```bash
/plugin update
```
