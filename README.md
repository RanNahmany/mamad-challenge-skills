# mamad-skills — Claude Code Plugin Marketplace

A curated collection of Claude Code plugins. Each plugin adds a specialized skill that Claude activates automatically for relevant tasks.

## Install via Claude Code (recommended)

Add this marketplace once, then install any plugin by name:

```shell
/plugin marketplace add RanNahmany/mamad-challenge-skills
```

Then install individual plugins:

```shell
/plugin install presentation-builder@mamad-skills
/plugin install ui-ux-pro-max@mamad-skills
/plugin install writing-linkedin-posts@mamad-skills
```

## Available Plugins

| Plugin | Description | Keywords |
|--------|-------------|----------|
| [presentation-builder](./skills/presentation-builder/) | Transform scripts into Apple-inspired HTML presentations with animations, color psychology, and lead magnet CTAs | presentation, slides, html, design |
| [ui-ux-pro-max](./skills/ui-ux-pro-max/) | UI/UX design intelligence with 50+ styles, 21 palettes, 50 font pairings, and 9 technology stacks | ui, ux, design, react, tailwind |
| [writing-linkedin-posts](./skills/writing-linkedin-posts/) | Create engaging, authentic LinkedIn posts like a Top Voice | linkedin, writing, content, social-media |

## Plugin Structure

Each plugin follows the Claude Code plugin convention:

```
skills/<plugin-name>/
├── .claude-plugin/
│   └── plugin.json     # Plugin manifest (name, version, description)
├── SKILL.md            # Skill definition with trigger conditions and workflow
└── ...                 # Supporting files (data, scripts, references)
```

The `SKILL.md` file contains the frontmatter (`name`, `description`) and the full skill instructions Claude reads when the skill is triggered.

## Contributing a Plugin

1. Create a folder under `skills/` with your plugin name
2. Add `.claude-plugin/plugin.json` with `name`, `description`, `version`
3. Add a `SKILL.md` with YAML frontmatter and skill instructions
4. Add the plugin entry to `.claude-plugin/marketplace.json`
5. Open a pull request

### plugin.json minimum

```json
{
  "name": "my-plugin",
  "description": "What it does and when it triggers",
  "version": "1.0.0"
}
```

### SKILL.md minimum

```markdown
---
name: my-plugin
description: One-line description for discovery
---

# My Plugin

## When to Activate
...

## Workflow
...
```

### Skill Quality Standards

- Trigger conditions must be unambiguous
- Rules stated as constraints, not suggestions
- Examples beat descriptions — show input and expected output
- Include a self-verifiable checklist before delivery

## License

MIT — use, modify, and share freely.
