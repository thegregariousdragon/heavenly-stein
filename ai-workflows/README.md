# AI Workflows

Purpose: make The Heavenly Stein easier and safer to use for AI-assisted story creation, revision, continuity checking, and canon maintenance.

These files do not replace canon. They tell an AI how to choose, use, and report on the existing canon files before drafting or revising.

## Source of truth

Use `main` as the stable source of truth unless the user explicitly names another branch.

For all AI-assisted story or canon work, preserve the existing source order:

1. Current chat instructions.
2. GitHub `main` unless another branch is named.
3. `README.md`, `CANON_INDEX.md`, and `MANIFEST.md`.
4. `ACCESSIBILITY.md`.
5. Quick-reference files.
6. Numbered canon files.
7. Planning files.

## Core operating rule

Keep the world. Reset the old events.

Old story plots, chronology, scene blocking, one-off incidents, and old prose are not active canon unless a later canon update explicitly re-promotes them. Character specifics, worldbuilding systems, station layout, mechanics, law, labor, governance, ships, transport, weapons, communications, media, clean/restricted routing, and system precedents remain active.

## Workflow files

- `CONTEXT_PACKS.md` — choose the smallest sufficient file set for the task.
- `DRAFT_SCENE.md` — draft new story material from active canon.
- `CONTINUITY_AUDIT.md` — check a draft, outline, or proposed canon update for drift.

## Required AI behavior

Before drafting or revising, the AI should:

1. Identify the task type.
2. Load the matching context pack.
3. Check current continuity locks relevant to the scene.
4. Draft or revise.
5. Provide a short continuity report when helpful.
6. Name uncertainties instead of inventing canon.

## Accessibility

Outputs should remain screen-reader friendly by default:

- Use real Markdown headings.
- Prefer short paragraphs and simple lists.
- Avoid dense tables unless they genuinely help.
- Do not rely on color-only meaning.
- For station scenes, include surface, sound, air/smell, lighting mode, access, and route class when relevant.

## Non-canon draft rule

Story drafts, outlines, experiments, and planning notes do not become active canon by existing in the repository. New facts become canon only through deliberate canon promotion or explicit canon updates.