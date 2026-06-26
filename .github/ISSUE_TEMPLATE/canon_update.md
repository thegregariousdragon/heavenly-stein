---
name: Canon update
description: Propose a change or clarification to active canon
title: "Canon update: "
labels: [canon]
body:
  - type: markdown
    attributes:
      value: |
        Use this for changes to active canon. Story drafts, planning notes, and archive material do not become canon through an issue alone.
  - type: textarea
    id: summary
    attributes:
      label: Summary
      description: What should change?
    validations:
      required: true
  - type: dropdown
    id: impact
    attributes:
      label: Canon impact
      options:
        - Clarifies existing canon
        - Changes active canon
        - Promotes draft/planning material
        - Replaces obsolete wording
        - Removes accidental drift
    validations:
      required: true
  - type: textarea
    id: affected-files
    attributes:
      label: Likely affected files
      description: List canonical owner files and quick-reference summaries that may need updates.
      placeholder: |
        - canon/...
        - quick-reference/...
    validations:
      required: false
  - type: checkboxes
    id: required-checks
    attributes:
      label: Required checks
      options:
        - label: Checked `README.md`, `CANON_INDEX.md`, and `MANIFEST.md` for package status.
        - label: Checked `quick-reference/CANON_LOCKS.md` and `quick-reference/RECENT_CHANGES.md`.
        - label: Checked relevant numbered canon files.
        - label: Checked relevant quick-reference files.
        - label: This does not revive old chronology, old plots, old scene blocking, or old prose by accident.
        - label: This preserves screen-reader-friendly Markdown.
  - type: textarea
    id: ai-notes
    attributes:
      label: Notes for AI use
      description: What should AI assistants do differently if this becomes active canon?
    validations:
      required: false
---
