# Accessibility Guide

This package is designed to be usable with screen readers such as NVDA on Windows and VoiceOver on iOS.

## Recommended reading order

1. [`README.md`](README.md)
2. [`quick-reference/QUICK_START.md`](quick-reference/QUICK_START.md)
3. [`CANON_INDEX.md`](CANON_INDEX.md)
4. [`quick-reference/CANON_LOCKS.md`](quick-reference/CANON_LOCKS.md)
5. [`quick-reference/STATION_BLOCKING_GUIDE.md`](quick-reference/STATION_BLOCKING_GUIDE.md)
6. [`quick-reference/CHARACTER_QUICK_CARDS.md`](quick-reference/CHARACTER_QUICK_CARDS.md)
7. Numbered canon files as needed.

## Navigation tips

- Use heading navigation first. Major files use real Markdown headings.
- Use search for exact terms such as `Crown`, `Hospitality Level 1`, `The Green Room`, `Grünraum`, `Starship Garage`, `Restricted Works`, `Field Carbine`, `Longbeam`, or `Scatterbeam`.
- The station layout is easiest to navigate through [`quick-reference/STATION_BLOCKING_GUIDE.md`](quick-reference/STATION_BLOCKING_GUIDE.md).
- Character lookup is fastest through [`quick-reference/CHARACTER_QUICK_CARDS.md`](quick-reference/CHARACTER_QUICK_CARDS.md) and [`quick-reference/SHORTHAND_DECODER.md`](quick-reference/SHORTHAND_DECODER.md).

## Markdown link policy

Use Markdown-compatible relative links when a file reference is meant to help the reader move through the repo.

Examples:

```markdown
Use [`quick-reference/CANON_LOCKS.md`](quick-reference/CANON_LOCKS.md).
```

```markdown
Use [`STATION_BLOCKING_GUIDE.md`](../quick-reference/STATION_BLOCKING_GUIDE.md).
```

Guidelines:

- Link file references when they are navigation instructions or recommended reading.
- Link the first file reference in a section when the reference is likely to help traversal.
- Do not link every repeated mention of the same file if doing so would make the text noisy.
- Prefer relative links over raw GitHub URLs so the repo works both locally and on GitHub.
- Keep link text descriptive enough for screen-reader link lists. A filename is acceptable when the filename itself is the useful destination label.
- Do not change canon wording, hierarchy, or meaning during a link-cleanup pass.
- Treat link cleanup as documentation/accessibility work, not canon promotion.

## Screen-reader formatting policy

- Prefer headings and short lists over dense tables.
- Do not rely on color alone. Identify lights, alarms, signs, and route states by name.
- For station descriptions, include sound, smell/air, surface, and route access when they matter.
- Avoid long unbroken paragraphs in future canon updates.
- When adding a new station area, include its public status, authority owner, route access, surface feel, lighting, air/smell rules, and sound profile.

## Useful search terms

- `continuity rebuild`
- `station interior redesign locks`
- `Interior Surface, Lighting, Air, and Sound Rules`
- `Surface, lighting, air, and sound quick guide`
- `Crown`
- `Observation`
- `Entertainment`
- `Hospitality Level 1`
- `Hospitality Level 2`
- `Retail`
- `Residential`
- `Services`
- `Starship Garage`
- `Restricted Works`
- `The Green Room`
- `Grünraum`
- `The Spare Tap`
- `Lass ma einen bauen`
