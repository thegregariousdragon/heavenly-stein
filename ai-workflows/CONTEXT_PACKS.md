# AI Context Packs

Use this file to choose the smallest sufficient canon set before drafting, revising, auditing, or planning.

Do not load the whole repo by default. Start with the common foundation, then add the task-specific pack.

## Common foundation

Use for every AI-assisted story, revision, continuity, or canon task:

1. `README.md`
2. `CANON_INDEX.md`
3. `MANIFEST.md`
4. `ACCESSIBILITY.md`
5. `quick-reference/QUICK_START.md`
6. `quick-reference/CANON_LOCKS.md`
7. `quick-reference/RECENT_CHANGES.md`

The foundation establishes package status, active/inactive canon, accessibility expectations, current locks, and latest maintenance notes.

## Pack 1: General story drafting

Use when drafting a normal scene or short story request without a narrow technical focus.

Add:

- `quick-reference/CHARACTER_QUICK_CARDS.md`
- `quick-reference/SHORTHAND_DECODER.md`
- `planning/continuity-checklist.md`
- Any numbered canon file directly named by the user.

Also add the more specific packs below when the scene touches those topics.

## Pack 2: Der Himmelskrug station scene

Use for any scene set on Der Himmelskrug or involving station movement, routing, public/restricted access, sensory design, Arrival Control, Flight Control, The Green Room / Grünraum, The Spare Tap, Starship Garage, or Restricted Works.

Add:

- `quick-reference/STATION_BLOCKING_GUIDE.md`
- `quick-reference/MECHANICS_CHEATSHEET.md`
- `canon/08-der-himmelskrug-station.md`
- `canon/06-transport-and-movement.md` when personnel movement, teleportation, docking, or controlled routes matter.
- `canon/16-economy-law-and-communications.md` when law, jurisdiction, access, devices, or public communication matter.

Required checks:

- What level is the scene on?
- What is the public/restricted status?
- Which route class applies?
- Who owns the space operationally?
- What can characters see, hear, smell, access, or be blocked from accessing?
- Are bubble elevators, service cores, Medical routes, residential routes, and dirty-side routes used correctly?

## Pack 3: Character-heavy scene

Use when character voice, relationships, family, leadership, romance, public image, stress behavior, or personal continuity is central.

Add:

- `quick-reference/CHARACTER_QUICK_CARDS.md`
- `quick-reference/SHORTHAND_DECODER.md`
- `canon/02-heinz-schmitt.md`
- `canon/03-family.md`
- `canon/04-core-relationships.md`
- `canon/09-station-leadership.md`
- `canon/17-character-personality-and-scene-fingerprints.md`

Required checks:

- Names and pronouns.
- Formal role and authority.
- Relationship status.
- Voice, stress behavior, blind spot, and scene fingerprint.
- Whether the scene lets the correct person solve the correct problem.

## Pack 4: Action, force, weapons, ships, or emergencies

Use when scenes involve weapons, shields, disabling, combat, security incidents, emergency routing, ship danger, public force, sabotage, or rescue.

Add:

- `quick-reference/MECHANICS_CHEATSHEET.md`
- `canon/05-ships.md`
- `canon/18-weapons-combat-and-force-rules.md`
- `canon/20-starship-systems.md`
- `canon/19-tested-story-precedents.md`
- `canon/16-economy-law-and-communications.md`

Required checks:

- Nonlethal does not mean harmless.
- Disabling is usually harder than destroying.
- Flight Control owns controlled approach safety.
- Emergency action is logged and reviewable.
- Tool use, utility emitters, shields, cargo, life support, heat, and collateral risk matter.
- Heinz should not automatically override assigned authority.

## Pack 5: Law, labor, governance, economy, media, or public accountability

Use when a story touches station legitimacy, worker rights, residents, PR, media feeds, fines, debt, custody, jurisdiction, audits, board politics, or public statements.

Add:

- `canon/10-governance-labor.md`
- `canon/11-media-feeds.md`
- `canon/16-economy-law-and-communications.md`
- `canon/21-corporations-cooperatives-and-institutions.md`
- `canon/19-tested-story-precedents.md`

Required checks:

- Der Himmelskrug is not sovereign and not merely Heinz's private property.
- Authority can act quickly but remains reviewable.
- Workers, residents, pilots, crews, victims, visitors, and contractors are not background costs.
- Fines and violation recoveries are not ordinary profit.
- Media interest does not erase privacy, grief, due process, or labor protection.

## Pack 6: Cannabis / The Green Room / Grünraum

Use whenever cannabis, destination law, adult-use policy, staff assignment, ventilation, intoxication, sealed takeaway, or route-specific legality appears.

Add:

- `quick-reference/MECHANICS_CHEATSHEET.md`
- `quick-reference/STATION_BLOCKING_GUIDE.md`
- `canon/08-der-himmelskrug-station.md`
- `canon/16-economy-law-and-communications.md`
- `canon/19-tested-story-precedents.md`

Required checks:

- Public name: The Green Room.
- Internal/licensing name: Grünraum.
- No cannabis/alcohol bundle promotions.
- No public use outside approved areas.
- No minors, no weapons inside, and no safety-duty impairment.
- Destination-law screening for sealed takeaway.
- No sealed takeaway to Veyr-bound passengers or crew.
- Corridor odor bleed is an engineering or policy failure.

## Pack 7: New arc, story queue, or planning work

Use when building future arcs, story queues, development lanes, or non-canon plans.

Add:

- `planning/continuity-checklist.md`
- `planning/current-arc-board.md`
- `planning/story-queue.md`
- `canon/12-story-chronology.md`
- Any topic-specific packs needed by the proposed arc.

Required checks:

- Planning notes are not automatically canon.
- No old event or one-off incident is active unless explicitly re-promoted.
- New locked facts should be routed through canon update or canon promotion.

## Pack 8: Canon update or canon promotion

Use when changing what is true in the active world.

Add:

- `README.md`
- `CANON_INDEX.md`
- `MANIFEST.md`
- `quick-reference/QUICK_START.md`
- `quick-reference/CANON_LOCKS.md`
- `quick-reference/RECENT_CHANGES.md`
- `planning/continuity-checklist.md`
- All numbered canon files directly affected.
- All quick-reference files that summarize the changed topic.

Required checks:

- Identify the canonical owner file.
- Update quick-reference summaries only after updating the owner file.
- Update `RECENT_CHANGES.md` for meaningful shifts.
- Do not create contradictions between locks, cheat sheets, station blocking, and numbered canon.
- State whether old material is being re-promoted, rejected, or ignored.

## Pack selection rule

When uncertain, load the common foundation plus the smallest likely pack, then expand only if the task touches a locked topic.