# tng-plugins

Personal Claude Code plugin marketplace by [Trang Nguyen](https://github.com/nmtrang29).

A growing collection of themed plugins for product design, writing analysis, and personal workflows. Each plugin is independently installable.

## Install

```bash
# One-time: register the marketplace
claude plugin marketplace add https://github.com/nmtrang29/tng-plugins

# Install a plugin
claude plugin install writing-skills@tng-plugins

# Reload Claude Code to pick it up
/reload-plugins
```

## Plugins

### [`writing-skills`](plugins/writing-skills/)

Analyse someone's writing style at scale, then draft, review, and iterate prose in a target voice.

| Skill | Description |
|---|---|
| [`analyse-writing-style-blog`](plugins/writing-skills/skills/analyse-writing-style-blog/) | Analyse the writing style of a blog or blog author by sampling many posts. |
| [`analyse-writing-style-gdrive`](plugins/writing-skills/skills/analyse-writing-style-gdrive/) | Analyse the writing style of a person by reading their Google Docs at scale. |
| [`write-with-me`](plugins/writing-skills/skills/write-with-me/) | Collaborative writing assistant — drafts in a target voice, reviews through the audience's eyes, iterates until it lands. |

### [`reporting`](plugins/reporting/)

Summarise your own work from Claude Code activity logs into time breakdowns and ticket drill-downs.

| Skill | Description |
|---|---|
| [`activity-report`](plugins/reporting/skills/activity-report/) | Generate a time-estimate breakdown of Claude Code usage, grouped by tag and day. Supports ticket drill-down and optional chat delivery. |

More coming.

## Updating

When plugins are updated upstream, run:

```bash
/plugin update
```
