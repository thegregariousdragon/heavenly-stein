# Branching Model

Purpose: keep `main` stable as the active source of truth while allowing safe AI-assisted development, story drafting, planning, and canon review.

## Stable branch

`main` is the stable source of truth unless the user explicitly names another branch.

Rules for `main`:

- It should always represent current active canon and current accepted workflow guidance.
- It should not contain half-finished canon updates.
- It should not receive non-canon story drafts unless the repo later creates a clearly marked draft area and process.
- It should not revive old plots, chronology, scene blocking, one-off incidents, or old prose by accident.
- Changes should enter through pull requests.

## Standard branch types

Use predictable branch names so humans and AI assistants can understand the purpose of the work.

### `canon-update/<topic>`

Use for changes to active canon.

Examples:

- `canon-update/green-room-policy`
- `canon-update/starship-garage-rules`
- `canon-update/feli-public-arc`

Use when editing:

- `canon/`
- `quick-reference/CANON_LOCKS.md`
- `quick-reference/RECENT_CHANGES.md`
- `quick-reference/MECHANICS_CHEATSHEET.md`
- `quick-reference/STATION_BLOCKING_GUIDE.md`
- `quick-reference/CHARACTER_QUICK_CARDS.md`
- other quick-reference files that summarize active canon

Rule: if the change affects what is true in the world, use this branch type.

### `ai-workflow/<topic>`

Use for AI process, prompt workflow, audit, context pack, template, or repo-operation changes.

Examples:

- `ai-workflow/context-packs`
- `ai-workflow/continuity-audits`
- `ai-workflow/branch-and-pr-templates`

Use when editing:

- `ai-workflows/`
- `.github/pull_request_template.md`
- `.github/ISSUE_TEMPLATE/`

Rule: AI workflow changes guide how assistants use canon. They should not change active canon by accident.

### `story-dev/<story-or-arc>`

Use for story drafting, scene experiments, outlines, beat sheets, or arc development.

Examples:

- `story-dev/spare-tap-after-hours`
- `story-dev/himmelskrug-run`
- `story-dev/green-room-inspection`

Rule: story-dev branches do not automatically become canon. New reusable facts created in story development should be marked as candidate canon and promoted deliberately through `canon-update/...` or the canon promotion process.

### `planning/<topic>`

Use for planning boards, story queues, roadmaps, and non-canon development organization.

Examples:

- `planning/arc-board-refresh`
- `planning/story-queue-v1`
- `planning/canon-maintenance`

Rule: planning files can guide future work, but they do not override active canon.

### `archive-review/<topic>`

Use only when reviewing old material for possible re-promotion.

Examples:

- `archive-review/relay-haven-precedents`
- `archive-review/omniway-residue`
- `archive-review/old-himmelskrug-run-material`

Rule: nothing from archive review becomes canon by merge alone. If something is worth restoring, rewrite it into active canon through canon promotion.

## Pull request expectations

Every pull request should answer:

- What type of change is this?
- Does it change active canon?
- What files were checked?
- Does it preserve the continuity rebuild boundary?
- What should AI assistants do differently after it merges?

Use `.github/pull_request_template.md` for the required checklist.

## Merge practice

Prefer squash merges for normal work so `main` history reads as intentional changes.

Good merge titles:

- `Add AI workflow context packs`
- `Clarify Green Room destination-law screening`
- `Update Starship Garage and Restricted Works routing`
- `Add continuity audit checklist`

Avoid vague merge titles:

- `fix stuff`
- `misc`
- `updates`
- `final`

## AI assistant behavior

When asked to work in the repo, an AI assistant should:

1. Confirm the intended branch or infer the correct branch type.
2. Use `main` as the base unless told otherwise.
3. Create or use a topic branch.
4. Make focused commits.
5. Read back changed files when possible.
6. Open a pull request into `main` unless the user asks not to.
7. Never silently write non-canon story material into active canon.

## Naming rules

Use lowercase branch names with hyphens.

Preferred pattern:

```text
branch-type/short-topic
```

Examples:

```text
canon-update/flight-control-race-rules
ai-workflow/canon-promotion
story-dev/feli-heinz-proposal-pressure
planning/story-pipeline
archive-review/tested-precedents-cleanup
```

Avoid names that do not show intent:

```text
new-stuff
branch2
greg-edits
misc
final-final
```

## Safety principle

Branch names are part of continuity control. They should make it obvious whether a change is active canon, AI workflow, planning, draft story, or archive review.