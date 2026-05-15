# tng-plugins

Personal Claude Code plugin marketplace by [Trang Nguyen](https://github.com/nmtrang29).

A growing collection of themed plugins for product design, writing analysis, and personal workflows. Each plugin is independently installable.

## Install

```bash
# One-time: register the marketplace
claude plugin marketplace add https://github.com/nmtrang29/tng-plugins

# Install a plugin
claude plugin install writing-style@tng-plugins

# Reload Claude Code to pick it up
/reload-plugins
```

## Plugins

| Plugin | Description |
|---|---|
| [`writing-style`](plugins/writing-style/) | Analyse a person's writing style at scale — Google Drive docs or blog posts. |

More coming.

## Updating

When plugins are updated upstream, run:

```bash
/plugin update
```

## Structure

```
tng-plugins/
├── .claude-plugin/
│   └── marketplace.json        # Marketplace manifest
└── plugins/
    └── <plugin-name>/
        ├── .claude-plugin/
        │   └── plugin.json     # Plugin manifest
        ├── README.md
        └── skills/
            └── <skill-name>/
                ├── SKILL.md
                └── references/
```

## License

MIT — see [LICENSE](LICENSE).
