---
name: Story development
description: Track a non-canon story idea, scene, arc, or drafting lane
title: "Story development: "
labels: [story-dev]
body:
  - type: markdown
    attributes:
      value: |
        Use this for drafts, arcs, scene ideas, and experiments. Material here is non-canon until deliberately promoted through the canon promotion process.
  - type: textarea
    id: premise
    attributes:
      label: Premise
      description: What is the story, scene, or arc about?
    validations:
      required: true
  - type: textarea
    id: active-canon
    attributes:
      label: Active canon dependencies
      description: Which files or topics must be checked before drafting?
      placeholder: |
        - Heinz/Feli
        - Der Himmelskrug station layout
        - Flight Control
        - Green Room / Grünraum
    validations:
      required: false
  - type: checkboxes
    id: story-safety
    attributes:
      label: Story safety checks
      options:
        - label: This is not active canon yet.
        - label: Old plots, chronology, and scene blocking are not assumed active.
        - label: Character names, pronouns, roles, and relationships need checking before drafting.
        - label: Station scenes need level, route class, public/restricted status, and operational owner.
        - label: New reusable facts should be marked as candidate canon rather than silently relied on later.
  - type: textarea
    id: output
    attributes:
      label: Desired output
      description: What should the next AI or human pass produce?
      placeholder: Draft scene, outline, beat sheet, dialogue pass, continuity audit, sensory pass...
    validations:
      required: false
---
