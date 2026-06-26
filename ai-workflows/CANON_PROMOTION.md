# Canon Promotion Workflow

Purpose: prevent drafts, planning notes, old material, or AI-generated details from becoming active canon by accident.

Canon promotion is the deliberate process of turning a candidate fact, scene consequence, system rule, character development, location detail, or restored old element into active canon.

## Core rule

Existence is not canon.

A detail is not active canon merely because it appears in:

- a story draft;
- an outline;
- a planning file;
- an issue;
- an AI response;
- a branch name;
- an archive-review note;
- an old story file;
- a pull request discussion.

A detail becomes active canon only when it is deliberately added to the relevant canonical owner file and merged into `main` through a canon-aware pull request.

## What needs promotion

Use this workflow when a change would affect future stories, such as:

- a new locked relationship status;
- a new active story event;
- a new station area, route, rule, or access policy;
- a new named recurring character;
- a new ship, corporation, institution, route, colony, or media feed;
- a new law, labor rule, fee structure, safety rule, or governance process;
- a reusable consequence from a draft scene;
- a re-promoted old event, old location, old incident, or old scene detail;
- a change to the continuity rebuild boundary.

## What does not need promotion

Ordinary scene-level details usually do not need canon promotion unless they are meant to be reused.

Examples:

- a one-time joke;
- a disposable prop;
- a guest's meal choice;
- a temporary crowd reaction;
- a non-recurring background visitor;
- a local sensory detail that does not alter station design;
- a draft-only beat that will not be relied on later.

Mark these as provisional scene details if they might be confused with canon.

## Promotion status labels

Use these labels in notes, audits, and PRs:

- `Provisional scene detail` — safe inside this draft, not reusable canon.
- `Candidate canon` — potentially reusable, needs review before future reliance.
- `Canon promotion needed` — should not be relied on until promoted.
- `Promoted canon` — added to the correct canon file and merged into `main`.
- `Rejected for canon` — deliberately not active.
- `Archive-only` — preserved for reference, not active.

## Promotion process

### Step 1: Identify the candidate detail

State the detail in one sentence.

Example:

```text
The Services Level has a Quiet Room / Memorial / Decompression district for private post-incident reflection and escorted waiting.
```

### Step 2: Classify the detail

Choose one:

- Character fact.
- Relationship fact.
- Station layout or access rule.
- Transport or movement rule.
- Ship or starship-system fact.
- Weapon or force rule.
- Law, economy, governance, labor, or media fact.
- Location, colony, route, or jurisdiction fact.
- Story chronology fact.
- Tested system precedent.
- AI workflow rule.

### Step 3: Find the canonical owner file

Use `CANON_INDEX.md` and `ai-workflows/CONTEXT_PACKS.md` to locate the file that should own the fact.

Common examples:

- Character fact: relevant character file plus `quick-reference/CHARACTER_QUICK_CARDS.md` if it affects scene use.
- Station layout/access fact: `canon/08-der-himmelskrug-station.md` plus `quick-reference/STATION_BLOCKING_GUIDE.md`.
- Transport fact: `canon/06-transport-and-movement.md` plus `quick-reference/MECHANICS_CHEATSHEET.md`.
- Ship fact: `canon/05-ships.md` or `canon/20-starship-systems.md`.
- Weapon/force fact: `canon/18-weapons-combat-and-force-rules.md` plus `quick-reference/MECHANICS_CHEATSHEET.md`.
- Governance/labor fact: `canon/10-governance-labor.md`.
- Economy/law/communications fact: `canon/16-economy-law-and-communications.md`.
- Institution/corporation fact: `canon/21-corporations-cooperatives-and-institutions.md`.
- Active chronology fact: `canon/12-story-chronology.md`.
- System precedent: `canon/19-tested-story-precedents.md`.
- AI workflow rule: `ai-workflows/`.

### Step 4: Check conflicts

Before promoting, check:

- `quick-reference/CANON_LOCKS.md`
- `quick-reference/RECENT_CHANGES.md`
- relevant quick-reference files
- relevant numbered canon files
- `ai-workflows/CONTINUITY_AUDIT.md`

Ask:

- Does this contradict current active canon?
- Does it accidentally revive old chronology?
- Does it change station geography, authority, access, law, labor, safety, or character relationships?
- Does it require a quick-reference update?
- Does it require `RECENT_CHANGES.md`?

### Step 5: Promote through a canon-aware branch

Use branch type:

```text
canon-update/<topic>
```

For archive restoration, use:

```text
archive-review/<topic>
```

first, then promote through:

```text
canon-update/<topic>
```

Do not promote directly from archive review by merge alone.

### Step 6: Update all necessary files

A promotion usually needs:

1. Canonical owner file update.
2. Quick-reference summary update if the fact affects drafting.
3. `quick-reference/RECENT_CHANGES.md` update if the change is meaningful.
4. Planning file update if the change affects active story development.
5. Continuity audit note in the PR.

### Step 7: Open a pull request

Use `.github/pull_request_template.md`.

The PR should state:

- what is being promoted;
- where it came from;
- why it should be active;
- what files were checked;
- whether old material is being re-promoted, rejected, or ignored;
- what AI assistants should do differently after merge.

## Old material restoration

Old story material is inactive by default.

When reviewing old material, do not copy it into canon unchanged unless it still fits:

- the continuity rebuild status;
- current station layout;
- current character status;
- current governance/labor/law rules;
- current mechanics;
- current accessibility and formatting standards.

Prefer preserving principles over restoring old event beats.

## Story chronology promotion

A story event should become active chronology only when the project deliberately decides it is locked.

Before updating `canon/12-story-chronology.md`, check:

- Does this event need to be true for future stories?
- Can it remain a draft-only incident?
- Does it require updates to character status, station status, law/labor consequences, media, or planning files?
- Does it create obligations for future scenes?

## AI assistant behavior

When an AI creates or notices a reusable new fact, it should mark it clearly:

```text
Candidate canon: <detail>
Reason: <why it may matter later>
Suggested owner file: <file>
Risk: <conflict or uncertainty, if any>
```

The AI should not silently add candidate canon to active canon files unless the user explicitly asks for a canon update.

## Promotion checklist

- [ ] Candidate detail stated clearly.
- [ ] Promotion type identified.
- [ ] Canonical owner file identified.
- [ ] Relevant locks checked.
- [ ] Relevant quick-reference files checked.
- [ ] Old chronology risk checked.
- [ ] Accessibility and formatting checked.
- [ ] Owner file updated.
- [ ] Quick-reference files updated if needed.
- [ ] `RECENT_CHANGES.md` updated if needed.
- [ ] Pull request explains canon impact.

## Final principle

Canon should be easy to use and hard to accidentally change.