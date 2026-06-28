# Assistant Collaboration Rules

Purpose: preserve the human author's working preferences for AI-assisted repo work.

This guide is for process. It is not canon.

## Source of truth

Use GitHub `main` as the source of truth unless the current chat explicitly says otherwise.

Uploaded ZIPs, pasted files, generated local artifacts, and temporary snapshots are not automatically authoritative unless the author explicitly promotes them.

## Decision questions

When asking the author to decide between options, ask decision questions one at a time.

Preferred pattern:

```text
Recommended next decision:

Option A: ...
Option B: ...
Option C: ...
```

Do not stack multiple unrelated decisions in one response unless the author asks for a broader menu.

## Pull request workflow

For repo changes, prefer this workflow:

1. Create a topic branch from current `main`.
2. Make the smallest coherent change set.
3. Open a pull request.
4. Check the PR for conflicts and mergeability before merging.
5. Ask before merging unless the author explicitly authorized merge in the same request.
6. Use squash merge as the default merge method for this repo, because the repo is intentionally configured for squash-style history.

If GitHub reports a PR as not yet mergeable immediately after creation, refresh or re-check PR metadata before concluding that it has a conflict. GitHub often needs a moment to calculate mergeability.

## Conflict and merge safety

Before merging any PR:

- confirm the PR targets `main` unless the author specified another base;
- confirm it is not a draft;
- confirm GitHub reports it as mergeable;
- confirm the file list matches the intended change;
- use the expected head SHA when merging if the tool supports it;
- report the merge method and resulting commit SHA.

Do not merge a PR with conflicts. If a conflict appears, summarize the conflict and ask for the next decision.

## Direct commits to main

Avoid direct commits to `main` except when the author explicitly requests them.

If a direct commit happens by mistake, repair transparently:

1. Say what happened.
2. Revert or remove the accidental direct change.
3. Re-create the intended change through branch and PR.
4. Report both the mistake and the repair.

## Branch cleanup

Merged branches may be kept for author convenience, especially if the repo may later be opened to other authors.

If branches become too unwieldy, make a cleanup plan first rather than deleting branches ad hoc.

## Local artifacts

Generated local artifacts such as EPUBs, PDFs, archives, or exports should not be pushed back to the private repo unless the author asks for that.

For reader-facing publication files, prefer generating them locally and presenting downloadable artifacts in chat unless the author asks for a GitHub Release or repository-stored build output.
