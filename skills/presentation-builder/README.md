# Presentation Builder Skill

Transform scripts into stunning, Apple-inspired HTML presentations with sequential animations, color psychology, and lead magnet CTAs — ready to present directly in a browser.

## What It Does

Give Claude a script (or a path to one) and optionally name a visual style. Claude will:

1. Read and map the narrative arc
2. Break the script into optimally-sized slides
3. Apply the visual style (30+ built-in style references)
4. Wire up all animations with user-controlled reveals
5. End with a conversion-optimized lead magnet CTA slide
6. Save a self-contained `.html` file to `Finished Presentations/`

## Trigger Examples

```
Create a presentation using @scripts/my-script.txt in the style of glassmorphism
```
```
Build slides from this script — make it dark and dramatic
```
```
Create a presentation from the AI business script in the style of retro-synthwave
```

## Files in This Skill

| File | Purpose |
|------|---------|
| `skill.md` | Main orchestrator — workflow, core rules, checklist |
| `styles-catalog.md` | Visual DNA of all 30+ style references (colors, fonts, cards, effects) |
| `boilerplate.md` | Complete HTML scaffold with animation engine, CSS system, navigation |
| `script-examples.md` | 10 slide patterns, narrative formula, CTA templates, transformation rules |

## Key Capabilities

- **30+ Visual Styles** — from Apple Keynote to Cyberpunk Neon to Art Deco Luxury
- **Color Psychology System** — red for problems, green for solutions, cyan for technology — applied consistently
- **Sequential Animations** — user-controlled reveals via Space/Arrow keys
- **The Ran Nahmany Formula** — proven narrative arc: Hook → Validate → Reveal → Prove → Urgency → CTA
- **10 Slide Patterns** — Big Stat, Comparison, Three-Pill, Quote, Timeline, Bar Chart, Before/After, etc.
- **Lead Magnet CTA** — every presentation ends with a conversion-focused final slide
- **Safe Zone System** — content never gets cut off at any viewport size
- **Mobile Responsive** — full breakpoint system built into every output

## Installation

```bash
cp -r presentation-builder ~/.claude/skills/
```

## Output

A single self-contained `.html` file. Open in any browser, present with keyboard navigation.

```
Space / Right Arrow  →  next animation step or next slide
Left Arrow           →  previous slide (replay animations)
```

## Customization

The skill works with your existing `presentation-builder` project folder. Point it at:
- `scripts/` — your script files
- `style-references/` — custom HTML style references (Claude will read them if a style isn't in the catalog)
- `Finished Presentations/` — where output is saved
- `assets/` — images to include in slides
