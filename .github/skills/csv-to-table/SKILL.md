---
name: csv-to-table
description: 'Convert CSV data into a clearly formatted, color-coded Markdown table for analysis and reporting. Use when cleaning headers, selecting key columns, applying column-based color coding, and producing readable tables.'
argument-hint: 'Path to CSV and optional column order preferences'
user-invocable: true
disable-model-invocation: false
---

# CSV to Table

Convert a CSV file into a clean, presentation-ready Markdown table that is easy to scan, with column-based color mapping shown in the legend.

## When to Use
- You have raw CSV data that is hard to read in plain text.
- You need stakeholder-ready tables in chat, docs, or reports.
- You need consistent visual cues by column (for example: status column always green-tagged, priority column always amber-tagged).

## Inputs
- CSV file path.
- Optional preferences:
  - Which columns to keep.
  - Sort column and direction.
  - Column order.
  - Column color mapping.
  - Output file path (default in `data/`).

## Procedure
1. Load and inspect the CSV.
2. Validate structure:
   - Confirm delimiter and header row.
   - Detect empty columns or duplicate header names.
3. Normalize headers:
   - Trim whitespace.
   - Convert header casing to a readable standard.
   - Rename unclear headers if needed for readability.
4. Prepare rows:
   - Trim cell whitespace.
   - Handle blank cells as `N/A`.
   - Optionally sort by a key column.
5. Select display columns:
   - Keep the most decision-relevant fields.
   - Move status or metric columns near the left for faster scanning.
6. Apply color logic:
  - Create a legend first that maps each displayed column to one color.
  - Keep table cell values as plain text (no inline color tags in data cells).
7. Render output:
  - Produce a clean Markdown table with plain cell values.
  - Save the produced Markdown file in the `data/` folder by default (for example: `data/<source-name>_table.md`).
  - Preserve all input rows; do not truncate.
8. Perform quality checks before finalizing.

## Decision Points
- If row count is very large:
  - Still show all rows as requested and keep formatting consistent.
- If columns are too many:
  - Prioritize core columns and move secondary columns to an appendix table.
- If a column has no explicit color mapping:
  - Apply a neutral column color and state this in the legend.
- If colors alone may reduce accessibility:
  - Add text labels (for example: `High Risk`, `Watch`, `On Track`) in addition to color.

## Default Column Color Mapping
Use this when the user does not provide custom mapping.

- First key column -> Green
- Second key column -> Amber
- Third key column -> Red
- Remaining columns -> Blue

## Output Templates

### Markdown Style
- Start with a legend line.
- Keep each row value unchanged except normalization (for example blank values become `N/A`).
- Represent column color mapping in legend/header notes, not in each data cell.

## Completion Checks
- Headers are readable and consistent.
- Table has no misaligned columns.
- Legend matches applied column-color mapping.
- No per-cell color tags are present in the table body.
- Output is readable as Markdown.
- All input rows are included.
- Any assumptions (sorting, dropped columns) are explicitly stated.

## Prompt Starters
- `/csv-to-table data/stakeholder_interview_notes.csv`
- `/csv-to-table data/stakeholder_interview_notes.csv sort=priority desc`
- `/csv-to-table data/stakeholder_interview_notes.csv columns=stakeholder,need,priority,status`
