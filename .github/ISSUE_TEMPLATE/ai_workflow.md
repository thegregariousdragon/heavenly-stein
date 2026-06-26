---
name: AI workflow
description: Propose or improve AI process files, context packs, audits, or templates
title: "AI workflow: "
labels: [ai-workflow]
body:
  - type: markdown
    attributes:
      value: |
        Use this for AI process improvements. These changes should guide how AI assistants use canon; they should not change canon by accident.
  - type: textarea
    id: problem
    attributes:
      label: Problem or gap
      description: What should be easier, safer, or more consistent for AI-assisted story work?
    validations:
      required: true
  - type: textarea
    id: proposed-change
    attributes:
      label: Proposed workflow change
      description: What should be added or changed?
    validations:
      required: false
  - type: checkboxes
    id: workflow-safety
    attributes:
      label: Safety checks
      options:
        - label: This does not change active canon directly.
        - label: This preserves the source-of-truth hierarchy.
        - label: This points to existing canon files rather than duplicating long canon unnecessarily.
        - label: This keeps outputs screen-reader friendly.
        - label: This helps prevent accidental old-chronology resurrection.
  - type: textarea
    id: affected-files
    attributes:
      label: Likely affected workflow files
      placeholder: |
        - ai-workflows/CONTEXT_PACKS.md
        - ai-workflows/CONTINUITY_AUDIT.md
    validations:
      required: false
---
