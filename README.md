# Claude Skills Marketplace

A curated collection of skills for Claude Code. Each skill teaches Claude a specialized workflow — drop any skill folder into `~/.claude/skills/` and it becomes immediately available.

## What is a Claude Skill?

A skill is a folder inside `~/.claude/skills/` containing markdown files that give Claude deep, domain-specific knowledge and workflow instructions. When you trigger a skill (by asking Claude to do something in that domain), Claude reads the skill files and operates as an expert in that area.

Skills are:
- **Portable** — copy a folder, get the capability
- **Composable** — use multiple skills in one session
- **Updatable** — edit the markdown, Claude learns instantly
- **Shareable** — this repo

## Installation

### Install a single skill
```bash
cp -r skills/presentation-builder ~/.claude/skills/
```

### Install all skills
```bash
cp -r skills/. ~/.claude/skills/
```

## Skill Registry

| Skill | Description | Trigger |
|-------|-------------|---------|
| [presentation-builder](./skills/presentation-builder/) | Transform scripts into Apple-inspired HTML presentations with animations, color psychology, and lead magnet CTAs | "create a presentation", "build slides", "in the style of..." |

## Skill Structure

Each skill follows this convention:

```
skill-name/
├── skill.md           # Main entry point — trigger conditions, workflow, core rules
├── [topic].md         # Supporting context files (as many as needed)
└── ...
```

The `skill.md` file is the orchestrator. Supporting files hold deep reference content (style catalogs, boilerplates, examples) that would be too large to keep in one file.

## Contributing a Skill

A well-formed skill includes:

1. **`skill.md`** — trigger conditions, step-by-step workflow, non-negotiable rules, and a pre-delivery checklist
2. **Context files** — reference material Claude needs without searching externally (catalogs, templates, examples)
3. **Specificity** — the more concrete and example-driven, the better Claude performs

### Skill Quality Standards
- Trigger conditions must be unambiguous
- Rules must be stated as constraints, not suggestions
- Examples beat descriptions — show the input and the expected output
- Include a checklist Claude can self-verify against before delivering

## License

MIT — use, modify, and share freely.
# mamad-challenge-skills
