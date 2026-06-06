# doc-format-gbt9704

`doc-format-gbt9704` is a Codex skill for formatting Chinese official documents according to GB/T 9704-2012《党政机关公文格式》. It helps Codex turn Word documents, legacy `.doc` files, plain text drafts, summaries, notices, reports, letters, commands, and meeting minutes into standardized official-document layouts.

## What It Does

This skill guides Codex to apply the core GB/T 9704-2012 formatting requirements, including:

- A4 page setup and official document text block geometry.
- Standard margins: top 37 mm, left 28 mm, right 26 mm, bottom 35 mm.
- Default 3号仿宋 body text.
- 2号小标宋-style centered document titles.
- Official heading hierarchy: `一、`, `（一）`, `1.`, `（1）`.
- Font treatment for hierarchy: first level 黑体, second level 楷体, lower levels 仿宋.
- Official page numbers outside the text block, alternating by odd/even pages.
- Signature and date placement for common no-seal documents.
- Rules for attachments, imprint blocks, letter format, command format, and minutes format.
- Render-and-review workflow for Word documents so layout issues are caught before delivery.

## When To Use

Use this skill when you ask Codex to:

- 按《党政机关公文格式》排版 Word 文档。
- Convert a `.doc` or `.docx` into GB/T 9704-2012 format.
- Normalize a Chinese official document draft.
- Check whether a document follows GB/T 9704 formatting.
- Create or revise a 公文、通知、报告、总结、函、命令、纪要.
- Apply official page margins, fonts, line spacing, page numbers, signature/date layout, attachments, or imprint rules.

Example prompts:

```text
Use $doc-format-gbt9704 to format this Word document according to GB/T 9704-2012.
```

```text
用 $doc-format-gbt9704 把这个 .doc 按党政机关公文格式重新排版。
```

```text
Use $doc-format-gbt9704 to audit this document and tell me which GB/T 9704 layout rules it violates.
```

## Repository Structure

```text
doc-format-gbt9704/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
├── references/
│   └── format_rules.md
└── scripts/
    └── format_docx_gbt9704.py
```

### `SKILL.md`

The Codex skill entrypoint. It describes when the skill should trigger and the workflow Codex should follow.

### `references/format_rules.md`

A compact, automation-friendly reference for GB/T 9704-2012 rules. It covers page geometry, typography, headers, body layout, signatures, seals, attachments, imprint blocks, page numbers, landscape tables, and special formats.

### `scripts/format_docx_gbt9704.py`

A reusable helper script for common no-seal DOCX formatting tasks. It is intended for straightforward reports and summaries where the source text has:

- a document title,
- body paragraphs,
- optional section headings,
- optional final issuing authority,
- optional final date.

For complex official documents with red headers, seals, attachments, imprint blocks, letter format, command format, or minutes-specific requirements, Codex should read `references/format_rules.md` and patch or extend the implementation.

## Installation

Clone or copy this folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/huanda1988/doc-format-gbt9704.git ~/.codex/skills/doc-format-gbt9704
```

Restart Codex or start a new conversation so the skill list is refreshed.

## Basic Usage In Codex

After installation, mention the skill in your prompt:

```text
$doc-format-gbt9704 请把这份 Word 文档按 GB/T 9704-2012 公文格式排版。
```

For Word files, this skill is designed to work with the Documents skill. Codex should:

1. Convert legacy `.doc` files to `.docx` when necessary.
2. Preserve original content unless rewriting is explicitly requested.
3. Apply GB/T 9704 layout rules.
4. Render the DOCX to page images.
5. Inspect every page for clipping, overlap, missing glyphs, broken page numbers, and bad signature placement.
6. Deliver the final `.docx`.

## Script Usage

The script can be run directly for simple no-seal documents:

```bash
python scripts/format_docx_gbt9704.py input.docx --out output.docx
```

Keep source metadata if needed:

```bash
python scripts/format_docx_gbt9704.py input.docx --out output.docx --keep-metadata
```

The input must be `.docx`. Convert `.doc` first, for example with LibreOffice:

```bash
soffice --headless --convert-to docx --outdir /path/to/out input.doc
```

Or on macOS:

```bash
textutil -convert docx -output input.docx input.doc
```

## Formatting Defaults

The helper script applies these defaults:

| Item | Default |
|---|---|
| Paper | A4, 210 mm × 297 mm |
| Margins | Top 37 mm, left 28 mm, right 26 mm, bottom 35 mm |
| Body font | 3号仿宋-style, 16 pt |
| Title font | 2号小标宋-style, 22 pt |
| Line pitch | Exact 29 pt |
| Body indent | First line indented by 2 Chinese characters |
| First-level heading | 黑体 |
| Second-level heading | 楷体 |
| Lower-level heading/body | 仿宋 |
| Page number | 4号宋体-style `— PAGE —`; odd pages right, even pages left |

## Important Notes

- The script is a practical formatter, not a complete legal/typographic engine for every possible GB/T 9704 case.
- Always inspect rendered pages before final delivery.
- Do not rely only on text extraction or XML inspection for layout quality.
- If a document contains seals, red issuing authority marks, imprint blocks, attachments, or special formats, use the reference rules and adjust the document manually or extend the script.
- The bundled rules are designed for AI-assisted formatting and should be checked against the official standard when strict compliance is required.

## Validation Checklist

Before publishing or delivering a formatted document, confirm:

- The page is A4.
- Margins match the standard layout.
- The first page contains正文.
- The title is centered and visually appropriate.
- Paragraphs use two-character first-line indentation.
- Heading levels follow `一、`, `（一）`, `1.`, `（1）`.
- Dates do not use leading zeroes in month/day.
- Page numbers sit outside the text block and alternate left/right.
- Signature and date are visible and correctly aligned.
- Rendered pages have no overlap, clipping, missing glyph boxes, or broken spacing.

## License

No license has been specified yet. Add a license file before public reuse if needed.
