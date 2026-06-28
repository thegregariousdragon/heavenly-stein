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

## Collaboration preferences

Use [`ai-workflows/ASSISTANT_COLLABORATION_RULES.md`](ASSISTANT_COLLABORATION_RULES.md) for standing collaboration preferences, including:

- asking decision questions one at a time;
- using branch-and-PR workflow for repo changes;
- checking conflicts and mergeability before merging;
- asking before merge unless merge was explicitly authorized;
- using squash merge as the default merge method;
- keeping generated local artifacts out of the repo unless requested.

Use [`ai-workflows/EPUB_PUBLISHING.md`](EPUB_PUBLISHING.md) when generating reader-facing EPUB files from publishable story Markdown.

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

If the scene is on Der Himmelskrug, the assistant should use [`ai-workflows/STATION_SCENE_CHECK.md`](STATION_SCENE_CHECK.md).

If the scene is away from the station, the assistant should use [`ai-workflows/OFF_STATION_SCENE_CHECK.md`](OFF_STATION_SCENE_CHECK.md).

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
