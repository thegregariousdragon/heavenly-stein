# AI Continuity Audit Workflow

Use this workflow to check a draft, outline, scene plan, canon proposal, or revision for drift before treating it as safe.

The audit should be practical, not punitive. The goal is to catch contradictions early and preserve the warmth, comedy, consequence, and civic realism of The Heavenly Stein.

## Step 1: Identify audit type

Classify the material:

- Story prose.
- Outline or beat sheet.
- Scene continuation.
- Character voice pass.
- Station blocking pass.
- Action/safety pass.
- Law/labor/media pass.
- Cannabis / Green Room / Grünraum pass.
- Canon update proposal.
- Planning note.

Then choose the matching context pack from `ai-workflows/CONTEXT_PACKS.md`.

## Step 2: Check active/inactive canon boundary

Confirm:

- Active worldbuilding remains active.
- Active character specifics remain active.
- Old plots, chronology, scene blocking, one-off incidents, and old prose remain inactive unless explicitly re-promoted.
- `canon/19-tested-story-precedents.md` is used for system principles, not old event history.

Flag any sentence that implies an old event happened when the current canon does not support it.

## Step 3: Check source hierarchy

When a conflict appears, apply this order:

1. Current user instruction for this task.
2. GitHub `main` unless another branch is named.
3. `README.md`, `CANON_INDEX.md`, `MANIFEST.md`.
4. `ACCESSIBILITY.md`.
5. Quick-reference files.
6. Numbered canon files.
7. Planning files.

If the conflict is real, do not invent a reconciliation. Name it and suggest the smallest fix.

## Step 4: Station audit

For any Der Himmelskrug scene, check:

- The scene has a plausible level.
- Public/restricted status is respected.
- Route class is plausible.
- Operational owner is clear enough for the scene.
- Arrival Control handles ordinary public arrivals.
- No routine direct transport into public hospitality, Residential, school, brewery production, Command, Services, Starship Garage, or Restricted Works.
- Bubble elevators serve only Observation, Entertainment, Hospitality Level 1, Hospitality Level 2, and Retail.
- Residential is private/restricted and not a tourist plaza.
- Services is controlled staff/pilot/crew/operational support, not a public shopping floor.
- Starship Garage and Restricted Works remain physically and procedurally separate.
- Press belongs in the Hospitality Level 1 press suite, not Crown Command.
- The Crown keeps its four-quadrant civic cap structure.
- The Spare Tap remains staff-only and not public content.
- The Green Room / Grünraum stays on Retail and has eligibility, ventilation, destination-law, and staff-protection rules.

## Step 5: Mechanics audit

Check:

- Personnel transport is point-to-point.
- Personal remotes, data slates, wristpads, and earpieces carry or extend authorization; they do not create destinations or override infrastructure.
- Flight Control owns controlled approach safety.
- Clean/restricted routing is followed.
- Dirty, hazardous, undeclared, artifact-adjacent, battle-damaged, suspicious, ordnance-handling, or legally complicated traffic goes below.
- Cloaks do not permit firing while cloaked or docking while cloaked.
- Ships, shields, weapons, and systems use narrative capability profiles rather than exact old stat blocks.

## Step 6: Force and safety audit

Check:

- Nonlethal does not mean harmless.
- Disabling is usually harder than destroying.
- Public-space force includes crowd, Medical, infrastructure, legal, accessibility, and communications consequences.
- Emergency safety does not automatically decide debt, lien, contract, cargo ownership, or blame.
- Valid grievances do not excuse dangerous acts.
- Dangerous acts do not erase valid grievances.
- Cost allocation, labor impact, injury, repair, privacy, and review are considered when relevant.

## Step 7: Character audit

For every recurring or significant character, check:

- Correct name, nickname, and spelling choice.
- Pronouns checked from canon, not inferred.
- Current role and authority.
- Relationship status.
- Voice, stress behavior, and blind spot.
- Whether the character is being flattened into a joke, exposition tool, or all-purpose fixer.
- Whether the correct department or authority handles the problem.

Special attention:

- Heinz is imposing and dangerous when serious, but not a dumb brawler.
- Feli is Director of Communications and Civic Interface, not decorative PR.
- Tariq/Teriq's atmosphere work is operationally meaningful.
- Clara/Klara and Tariq/Teriq are affectionate/exasperated with growing respect, not simple harassment.
- Amara's Flight Control authority is real.
- Janelle, Medical, Dirty-Side Operations, Engineering, Compliance, Residential Life, Hospitality, Governance, and Labor should retain authority in their lanes.

## Step 8: Law, labor, media, and governance audit

Check:

- Der Himmelskrug is privately founded, partner-backed, and IFP-recognized civic/route-safety infrastructure.
- It is not a sovereign state and not merely Heinz's private beer station.
- Emergency authority acts first when needed but remains logged and reviewable.
- The Governing Board, Residents and Staff Assembly, Route Users Advisory Council, Independent Safety and Ethics Office, and Workers' Guild retain their roles when relevant.
- The Assembly speaks as a town; the Guild speaks as labor.
- Workers, residents, pilots, crews, contractors, victims, and visitors are not background costs.
- Media interest does not erase privacy, grief, due process, Medical privacy, labor rights, or active investigations.

## Step 9: Accessibility and sensory audit

Check:

- The draft does not rely on color alone for safety or wayfinding.
- Station descriptions include useful sound, surface, air/smell, lighting mode, access, or route information when relevant.
- Public warmth does not erase access controls.
- Odor bleed is treated as a failure unless the scene is about malfunction or containment stress.
- Acoustic separation is architecture, not people simply being quiet.
- Output formatting is screen-reader friendly if the audit is being returned to the user.

## Step 10: Report format

For a short audit, use:

1. Overall status.
2. Highest-risk issue.
3. Required fixes.
4. Optional improvements.

For a full audit, use:

1. Overall status.
2. Files or context packs checked.
3. Passed checks.
4. Issues found.
5. Suggested fixes.
6. Candidate canon created by the draft, if any.
7. Open questions.

## Status labels

Use these labels:

- `Pass` — no meaningful continuity issues found.
- `Pass with notes` — safe, but minor clarifications would help.
- `Needs revision` — contains fixable continuity or mechanics drift.
- `Canon conflict` — contradicts active canon and should not be treated as safe.
- `Canon promotion needed` — creates a reusable new fact that should be deliberately promoted before future reliance.

## Repair principle

Prefer the smallest repair that preserves the user's intended scene. Do not over-rewrite for style when a continuity note or one-line fix is enough.