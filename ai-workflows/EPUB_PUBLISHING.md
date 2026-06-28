# EPUB Publishing Workflow

Purpose: define how to generate reader-facing EPUB files from publishable story Markdown.

This guide is for process. It is not canon.

## Recommended publication format

For accessible reader copies, prefer EPUB over PDF unless the author requests a fixed-layout artifact.

EPUB is usually the better first publication format because it supports:

- reflowable text;
- user-controlled font size, margins, line spacing, and theme;
- screen-reader navigation;
- ebook-reader table of contents;
- semantic headings generated from Markdown.

Do not generate a PDF by default when the author asks for the most accessible reader format.

## Source file

Use the publishable Markdown file in the story package as the source.

For `Opening the Stein`, the source is [`stories/publishable/opening-the-stein/opening-the-stein.md`](../stories/publishable/opening-the-stein/opening-the-stein.md).

Do not use `story-dev/` draft files for publication unless the author explicitly asks to publish a draft or replace the publishable source.

## Author metadata

For `Opening the Stein`, use:

```text
Title: Opening the Stein
Author: Greg Lopez
Publisher: Greg Lopez
Language: en-US
```

Do not use `The Heavenly Stein` as the author unless the author explicitly asks for a project byline.

## EPUB body expectations

The EPUB body should begin cleanly with the story title and story text.

Expected visible opening:

```markdown
# Opening the Stein

## Three Hours
```

Do not insert visible front matter such as:

- duplicate title pages;
- visible generated table of contents pages;
- private-review-copy notes;
- repository-source notes;
- repeated author/publisher lines.

The ebook should still include internal EPUB navigation, but the table of contents should live in the ebook reader's navigation, not as duplicated body clutter, unless the author requests a visible table of contents.

## Local artifact workflow

When the author asks for an EPUB reader copy:

1. Fetch the current publishable Markdown from GitHub `main`.
2. Save a local working Markdown copy.
3. Generate an EPUB3 file locally.
4. Ensure metadata uses the author-approved byline.
5. Check basic EPUB structure.
6. Present the local `.epub` file for download in chat.
7. Do not commit the generated EPUB back to the repo unless the author asks.

## Basic checks

A basic EPUB check should confirm:

- the output file exists;
- the first ZIP entry is `mimetype`;
- the package includes EPUB navigation, usually `nav.xhtml`;
- the package includes OPF metadata;
- the visible book body does not include unwanted generated title-page or table-of-contents clutter;
- story headings are present and navigable.

This is not the same as a full accessibility certification. For formal validation, use a dedicated EPUB checker such as EPUBCheck or an accessibility validator.

## File naming

Use readable lowercase filenames:

```text
opening-the-stein.epub
```

If multiple local review versions are created, add a suffix:

```text
opening-the-stein-clean.epub
opening-the-stein-greg-lopez.epub
```

For final handoff, prefer the clean base filename when there is no ambiguity.

## GitHub Releases

GitHub Releases may be useful later, but do not publish private-repo story artifacts to Releases unless the author explicitly asks.

If a release is requested, treat it as a separate decision workflow:

1. Confirm whether the release should be private/internal or public-facing.
2. Confirm the tag name.
3. Confirm the title and release notes.
4. Confirm the artifact format.
5. Confirm whether the generated artifact should be attached to the release.

Ask these decisions one at a time.
