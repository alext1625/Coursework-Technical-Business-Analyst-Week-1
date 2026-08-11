---
name: doc-to-md
description: 'Convert a source document file into an equivalent Markdown file while preserving all content, structure, and layout order. Use when migrating docs into markdown in-place with same-name output in the same directory.'
argument-hint: 'Path to source document file (for example .docx)'
user-invocable: true
disable-model-invocation: false
---

# Doc to Markdown

Convert a document file into a new Markdown file with the same base filename, saved in the same directory.

Goal:
- Preserve all source content.
- Preserve section order and document structure.
- Preserve layout semantics as closely as possible in Markdown.

## When to Use
- You need to migrate a document into markdown without losing content.
- You need markdown output in the same folder as the source document.
- You need a predictable naming rule: same base name, `.md` extension.

## Inputs
- Source document path.
- Supported source format for initial version: `.docx`.
- Optional overwrite preference (replace existing `.md` or fail safely).
- Optional conversion constraints (for example: strict tables, preserve line breaks, include image references).

## Output Rule
- Output file path must be:
  - Same directory as the input file.
  - Same base filename.
  - Extension changed to `.md`.
- Example:
  - Input: `docs/project-brief.docx`
  - Output: `docs/project-brief.md`

## Procedure
1. Validate source file.
   - Confirm file exists and is readable.
   - Confirm file extension is `.docx` for this version.
2. Compute output path.
   - Keep directory unchanged.
   - Keep filename stem unchanged.
   - Replace extension with `.md`.
3. Extract full document content.
   - Read all text, headings, lists, tables, links, and references.
   - Preserve original order.
4. Map structure to Markdown.
   - Headings -> `#` hierarchy.
   - Paragraphs -> paragraphs with spacing.
   - Bullet/numbered lists -> Markdown lists.
   - Tables -> Markdown tables.
   - Links -> Markdown links.
   - Code/preformatted blocks -> fenced code blocks.
   - Images -> markdown image references (retain relative paths where possible).
5. Preserve special content.
   - Keep callouts/notes as blockquotes or labeled sections.
   - Keep footnotes/endnotes as markdown footnotes or explicit references.
6. Write output file.
   - Create new `.md` file in source directory.
   - Do not drop content sections silently.
7. Validate fidelity.
   - Compare source and output section-by-section.
   - Confirm no section loss.
   - Confirm heading order and table/list integrity.

## Decision Points
- If output `.md` already exists:
   - Default to safe mode: do not overwrite and ask for explicit confirmation.
- If source contains unsupported styling-only elements:
  - Keep semantic content and note style-loss in a short conversion note.
- If complex layout cannot be represented exactly in Markdown:
  - Preserve text and hierarchy first.
  - Represent layout intent using headings, tables, and blockquotes.
- If embedded media paths are unclear:
  - Preserve reference text and add a TODO marker for unresolved assets.

## Quality Checks
- Output filename matches source stem exactly.
- Output file is in the same directory as source file.
- All source sections are present in output.
- Heading hierarchy is preserved.
- Lists/tables are not flattened into plain text unless unavoidable.
- Links/references are retained.
- Any unavoidable fidelity gaps are explicitly noted.

## Prompt Starters
- `/doc-to-md docs/strategy-brief.docx`
- `/doc-to-md docs/customer-research.docx overwrite=false`
- `/doc-to-md docs/week-1-summary.docx preserveTables=true`
