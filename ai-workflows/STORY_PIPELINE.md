# Story Pipeline

Purpose: define how an idea becomes a draft, revision, audit, and possible canon candidate without accidentally changing active canon.

This workflow is for AI-assisted story creation in The Heavenly Stein.

## Core rule

Story development is not canon by default.

A story idea, outline, scene draft, beat sheet, or AI-generated detail becomes active canon only through the canon promotion workflow.

Use:

```text
ai-workflows/CANON_PROMOTION.md
```

when a draft creates a fact that should matter later.

## Station scenes are conditional

Not every story has to take place on Der Himmelskrug.

If a scene is on the station, use:

```text
ai-workflows/STATION_SCENE_CHECK.md
```

If a scene is away from the station, do not force station geography into it. Instead, check:

- where the scene takes place;
- who controls that place;
- what jurisdiction applies;
- how people got there;
- what communications or transport limits matter;
- whether station institutions, Flight Control, Arrival Control, media, law, labor, or commerce still have reach;
- whether any new location fact is candidate canon.

Off-station stories still belong in The Heavenly Stein universe. They just use location and jurisdiction checks instead of atrium, Crown, Garage, Green Room, or level-blocking checks.

## Pipeline overview

Use this order:

1. Intake the story idea.
2. Classify the scene or project.
3. Select the smallest sufficient context pack.
4. Identify setting and jurisdiction.
5. Identify character and voice constraints.
6. Draft or outline.
7. Mark candidate canon.
8. Revise.
9. Audit continuity.
10. Decide whether anything needs canon promotion.

## Step 1: Intake the story idea

Capture:

- working title;
- premise;
- desired output;
- location;
- characters;
- tone target;
- whether this is draft-only, planning, or possible canon development;
- any user-provided facts that override repo defaults for this task.

Use:

```text
planning/story-intake-template.md
```

for reusable intake notes.

## Step 2: Classify the project

Choose one or more:

- Scene draft.
- Scene revision.
- Outline.
- Beat sheet.
- Character exchange.
- Station procedure scene.
- Off-station scene.
- Ship scene.
- Media/public-reaction scene.
- Law/labor/governance scene.
- Action/emergency scene.
- Cannabis/Green Room scene.
- Archive restoration candidate.
- Canon-promotion candidate.

The classification determines which context pack and checks apply.

## Step 3: Select context pack

Use:

```text
ai-workflows/CONTEXT_PACKS.md
```

Start with the common foundation, then add only relevant packs.

Do not load the whole repo by default.

## Step 4: Identify setting and jurisdiction

Ask:

- Is the scene on Der Himmelskrug?
- Is it on a ship?
- Is it on a colony, planet, route, port, corporate site, media site, or private facility?
- Who owns or operates the location?
- Who can enforce rules there?
- What route or transport system connects it to the station?
- Are communications delayed, filtered, public, private, recorded, or monitored?
- Does destination law matter?
- Does Flight Control or another authority have operational reach?

For station scenes, use station checks.

For off-station scenes, use location, jurisdiction, transport, and communications checks.

## Step 5: Identify characters and voice constraints

Use:

```text
ai-workflows/CHARACTER_VOICE_CHECK.md
```

Check:

- names;
- pronouns;
- public/private role;
- emotional continuity;
- competence;
- relationship status;
- what the character knows;
- what the character would refuse to do;
- whether comedy comes from pressure, process, culture, or mismatch rather than stupidity.

## Step 6: Draft or outline

Use:

```text
ai-workflows/DRAFT_SCENE.md
```

Draft with active constraints visible.

Do not silently rely on old chronology, old plots, old scene blocking, or old prose.

## Step 7: Mark candidate canon

When the draft creates a reusable fact, mark it clearly:

```text
Candidate canon: <detail>
Suggested owner file: <file>
Reason: <why it may matter later>
Risk: <possible conflict or uncertainty>
```

Candidate canon is not active canon.

## Step 8: Revise

Use:

```text
ai-workflows/REVISE_SCENE.md
```

Revision should improve clarity, voice, rhythm, accessibility, continuity, and consequence without flattening character behavior or system logic.

## Step 9: Audit continuity

Use:

```text
ai-workflows/CONTINUITY_AUDIT.md
```

A useful audit should separate:

- hard canon conflicts;
- likely continuity risks;
- optional improvements;
- candidate canon;
- questions for the user.

## Step 10: Decide promotion path

If the story creates a reusable fact, decide:

- leave it as draft-only;
- mark it as candidate canon;
- promote it through a future `canon-update/<topic>` branch;
- reject it for canon;
- keep it archive-only.

Use:

```text
ai-workflows/CANON_PROMOTION.md
```

## Output modes

An AI assistant should ask for or infer the needed output:

- brainstorming notes;
- beat sheet;
- outline;
- rough scene;
- polished scene;
- continuity audit;
- revision pass;
- candidate-canon list;
- canon-promotion PR plan.

## Default report format

After drafting or revising, report:

```text
Context used:
- <files or packs checked>

Status:
- Draft-only / candidate canon / canon promotion needed

Continuity notes:
- <important notes>

Candidate canon:
- <items, if any>

Open questions:
- <questions, if needed>
```

## Safety principle

The story pipeline should make creation easier, not more bureaucratic.

The process exists so absurd Bavarian orbital beer-stein scenes can move quickly while still respecting infrastructure, safety, law, labor, access, character continuity, privacy, and consequences.