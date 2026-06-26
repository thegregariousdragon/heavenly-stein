# Validation Workflow

Purpose: keep The Heavenly Stein repository mechanically safe while preserving the flexibility needed for canon, planning, and story work.

This validation layer checks formatting, links, and required source-of-truth files. It does not judge story quality or decide canon.

## Current checks

The GitHub Actions workflow lives at:

```text
.github/workflows/markdown-checks.yml
```

It runs on pull requests that change Markdown or validation configuration, on pushes to `main`, and by manual dispatch.

## Check 1: Required files

This is the strict baseline check.

The workflow verifies that core source-of-truth and AI workflow files still exist.

Current required files:

- `README.md`
- `CANON_INDEX.md`
- `MANIFEST.md`
- `ACCESSIBILITY.md`
- `quick-reference/QUICK_START.md`
- `quick-reference/CANON_LOCKS.md`
- `quick-reference/RECENT_CHANGES.md`
- `ai-workflows/README.md`
- `ai-workflows/CONTEXT_PACKS.md`
- `ai-workflows/DRAFT_SCENE.md`
- `ai-workflows/CONTINUITY_AUDIT.md`
- `ai-workflows/BRANCHING_MODEL.md`
- `ai-workflows/CANON_PROMOTION.md`
- `ai-workflows/VALIDATION.md`

Why: these files define the current source-of-truth hierarchy and AI operating process.

## Check 2: Markdown lint

Uses `markdownlint-cli2` through GitHub Actions.

Configuration:

```text
.markdownlint.json
```

The current lint profile is a low-noise baseline. It catches basic mechanical Markdown issues, such as broken heading syntax, missing spaces after heading markers, tabs, trailing spaces, and missing final newlines.

It intentionally does not enforce software-project habits that are often hostile to prose and canon documents.

Examples of rules intentionally relaxed:

- Long lines are allowed.
- Bare URLs are allowed for now.
- Code fences do not need language labels.
- The first line does not have to be a top-level heading.
- The repo is not forced into a single list or table style.

Why: canon files, templates, and scene-support docs need readable Markdown without forcing software-project formatting habits onto creative documentation.

## Check 3: Link check

Uses Lychee through GitHub Actions.

Configuration:

```text
.lychee.toml
```

The first version is informational. It may report broken or unreachable links, but it is not yet a merge-blocking authority.

The link check is intentionally gentle:

- It checks Markdown links.
- It allows normal success responses and rate-limit responses.
- It excludes private GitHub repo links for now.
- It ignores mail and loopback-style example links.

Why: the goal is to learn where link checking is noisy before turning it into a strict gate.

## What validation does not do

Validation does not decide:

- whether a scene is good;
- whether a joke lands;
- whether a canon change is narratively wise;
- whether a candidate fact should be promoted;
- whether old material should be restored;
- whether a character beat is emotionally right.

Use `ai-workflows/CONTINUITY_AUDIT.md` and `ai-workflows/CANON_PROMOTION.md` for those questions.

## AI assistant behavior

When a validation check fails, an AI assistant should:

1. Identify which check failed.
2. Explain the failure in plain language.
3. Make the smallest safe fix.
4. Avoid changing canon content unless the failure is directly caused by canon-file formatting or broken links.
5. Re-check the changed file when possible.

Do not treat a validation failure as permission to rewrite prose, retcon canon, or simplify worldbuilding.

## Future validation ideas

Add these only after the basic checks are stable:

- Internal anchor validation.
- Required heading checks for issue templates.
- Markdown table formatting checks.
- File-name convention checks.
- Canon-lock keyword scans.
- Accessibility linting for color-only language or missing sensory/access fields.
- A script that warns when story drafts introduce candidate canon without marking it.
- Strict link checking once the initial link-noise profile is understood.

## Canon-safety rule

Automated validation should protect the repo from mechanical breakage. It should not become an accidental canon authority.

If a validation rule conflicts with active canon clarity or accessibility, fix the validation rule before flattening the canon.
