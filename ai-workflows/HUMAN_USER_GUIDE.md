# Human User Guide for AI-Assisted Story Work

Purpose: explain how a human writer can use this repo with an AI assistant after opening The Heavenly Stein project.

This guide is for process. It is not canon.

## Core idea

Use this repo like a writing cockpit, not a filing cabinet.

Start with one focused task, then ask the AI assistant to use the repo's source-of-truth files and workflow guides.

The human brings taste, intent, preference, and final judgment.

The AI assistant should handle source checking, context-pack selection, continuity risk, draft labeling, and candidate-canon discipline.

## Source-of-truth reminder

Use GitHub `main` as the source of truth unless the current chat says otherwise.

Uploaded files, pasted text, and temporary snapshots are not automatically authoritative.

Drafts, examples, and planning notes are not canon by default.

New durable facts become active canon only through canon promotion.

## The simplest starter prompt

Use this when starting real story work:

```text
Use The Heavenly Stein repo on GitHub main as source of truth.

I want to start a new draft-only story idea.

Idea:
[paste messy idea]

Please:
1. Choose the smallest context pack.
2. Tell me whether this is station, off-station, ship, or mixed.
3. Turn it into a story intake.
4. Flag continuity risks.
5. Mark candidate canon, but do not promote anything.
6. Suggest the first scene to draft.
```

## Common human tasks

### Develop a story idea

Use:

```text
Use STORY_PIPELINE.md and story-intake-template.md.

Help me turn this into a story intake:

[paste idea]

Keep it draft-only. Mark any reusable new facts as candidate canon, not active canon.
```

The assistant should produce:

- working title;
- status;
- desired output;
- premise;
- location;
- station relevance;
- characters;
- tone target;
- required context packs;
- continuity risks;
- candidate canon;
- open questions.

### Draft a scene

Use:

```text
Use the smallest sufficient context pack and DRAFT_SCENE.md.

Draft a rough scene from this intake:

[paste intake or idea]

Keep it draft-only. Do not promote new facts into canon.
```

If the scene is on Der Himmelskrug, the assistant should use `ai-workflows/STATION_SCENE_CHECK.md`.

If the scene is away from the station, the assistant should use `ai-workflows/OFF_STATION_SCENE_CHECK.md`.

### Work on an off-station story

Use:

```text
This scene is off-station. Use OFF_STATION_SCENE_CHECK.md, not station blocking unless station systems directly matter.

Idea:
[paste idea]
```

The assistant should check:

- location;
- local authority;
- jurisdiction;
- travel route;
- communications limits;
- station connection, if any;
- candidate canon.

Off-station does not mean outside canon. It means the scene uses location, jurisdiction, route, communications, and authority checks instead of station geography checks.

### Revise prose

Use:

```text
Use REVISE_SCENE.md.

Revise this for clarity, character voice, continuity, and sensory/accessibility grounding.
Preserve my intent.
Do not add canon unless you mark it as candidate canon.

[paste scene]
```

A useful revision response should include:

- revised text;
- what changed;
- continuity notes;
- candidate canon;
- remaining risks.

### Check character voice

Use:

```text
Use CHARACTER_VOICE_CHECK.md.

Check whether this scene keeps [character name] in voice and competent:

[paste scene or beat]
```

The assistant should check:

- name and pronouns;
- role and authority;
- public/private boundaries;
- relationship status;
- what the character knows;
- what the character wants;
- what the character would refuse to do;
- whether comedy comes from pressure, process, culture, or mismatch rather than stupidity.

### Run a continuity audit

Use:

```text
Run CONTINUITY_AUDIT.md on this outline or scene.

[paste material]

Report:
- hard canon conflicts;
- likely continuity risks;
- optional improvements;
- candidate canon;
- whether canon promotion is needed.
```

This is usually most useful after a rough outline or draft.

Do not run a full audit on every tiny idea unless the idea touches a locked topic.

### Promote candidate canon

Use this only when a new fact should become durable:

```text
Use CANON_PROMOTION.md.

I want to promote this candidate canon:

[detail]

Find the likely owner file, identify conflicts, and propose a canon-update branch plan.
```

Drafts are playgrounds.

Canon promotion is paperwork.

Do not promote every cool idea. Let draft-only details prove they matter first.

## How to ask for GitHub changes

When the repo itself needs to change, ask directly:

```text
Create a branch and PR for this change.
```

Examples:

```text
Create a canon-update branch for this promoted detail and open a PR into main.
```

```text
Create a planning branch for this story arc, add a planning file, and open a PR.
```

```text
Create an ai-workflow branch for this process improvement and open a PR.
```

Use branch types from `ai-workflows/BRANCHING_MODEL.md`.

## Human rhythm

A practical loop:

1. Brain-dump the idea.
2. Ask for a story intake.
3. Pick station, off-station, ship, or mixed.
4. Ask for a rough outline.
5. Ask for a scene draft.
6. Ask for a continuity audit.
7. Revise.
8. Decide whether anything deserves canon promotion.

Most story work only needs steps 1 through 6.

## What not to worry about

You do not need to manually remember all canon files.

You do not need to fill every checklist every time.

You do not need to decide every candidate canon item immediately.

You do not need to make every scene happen on the station.

You do not need to make the process heavy.

Use the smallest sufficient context pack and expand only when the task touches a locked topic.

## What the assistant should report

A good assistant response should usually include:

```text
Context used:
- <files or packs checked>

Status:
- Draft-only / candidate canon / canon promotion needed

Continuity notes:
- <important notes>

Candidate canon:
- <items, if any>

Next useful step:
- <one practical suggestion>
```

## Good human steering phrases

Use these when the assistant is close but not quite right:

```text
That's too procedural. Keep the safety logic, but make the scene warmer.
```

```text
Keep this draft-only. Do not promote the new location yet.
```

```text
This is off-station. Stop using station geography unless the route back matters.
```

```text
Check character competence. The joke should not make them stupid.
```

```text
Make the sensory grounding more accessible without adding long description.
```

```text
Give me a shorter version using only the context that matters.
```

## Final principle

The workflow should help the story move faster, not make the writer fill out forms forever.

Use enough structure to protect canon, character, access, labor, law, safety, privacy, and consequence.

Then draft the scene.