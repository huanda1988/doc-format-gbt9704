# GB/T 9704-2012 Official Document Rules

This reference condenses GB/T 9704-2012《党政机关公文格式》 into automation-friendly rules. Use it when exact dimensions, typography, element order, or special format behavior is needed.

## Table of Contents

1. Page Geometry
2. Typography
3. Regions
4. Header Area
5. Body Area
6. Signature, Date, and Seal
7. Notes and Attachments
8. Imprint
9. Page Numbers
10. Landscape Tables
11. Special Formats
12. Automation Checks

## 1. Page Geometry

| Item | Rule |
|---|---|
| Paper | A4, 210 mm × 297 mm |
| Top margin / 天头 | 37 mm ± 1 mm |
| Left margin / 订口 | 28 mm ± 1 mm |
| Text block / 版心 | 156 mm × 225 mm |
| Derived right margin | 26 mm |
| Derived bottom margin | 35 mm |
| Page number | Outside the text block |
| Print mode | Double-sided printing |

## 2. Typography

| Item | Rule |
|---|---|
| Default | 3号仿宋体 |
| Default color | Black |
| Title | Generally 2号小标宋体 |
| First-level heading | Generally 黑体 |
| Second-level heading | Generally 楷体 |
| Third/fourth-level heading | Generally 仿宋体 |
| Page number | Generally 4号半角宋体 Arabic numerals |
| Lines/chars | Generally 22 lines per page, 28 characters per line, fill the text block |

Length units:

- `字`: one Chinese character width.
- `行`: one Chinese character height plus 7/8 of a 3号 Chinese character height.

## 3. Regions

| Region | Definition |
|---|---|
| 版头 | Above the red separator line on the first page. |
| 主体 | Below the first-page red separator line and above the first imprint separator line on the final page. |
| 版记 | Below the first imprint separator and above the final imprint separator. |
| 页码 | Outside the text block. |

Generate in this order: 版头 → 主体 → 附件 → 版记 → 页码.

## 4. Header Area

### 4.1 Copy Number / 份号

- If present, use six 3号 Arabic digits.
- Place at the first line of the top-left text block, flush left.
- Example: `000001`.

### 4.2 Secrecy and Duration / 密级和保密期限

- If present, use 3号黑体.
- Place at the second line of the top-left text block, flush left.
- Use Arabic numerals in the duration.
- Example: `秘密★1年`.

### 4.3 Urgency / 紧急程度

- If present, use 3号黑体, flush left at top-left text block.
- If copy number, secrecy, and urgency all appear, stack them top-to-bottom in this order: 份号, 密级和保密期限, 紧急程度.

### 4.4 Issuing Authority Mark / 发文机关标志

- Content: full or standardized issuing authority name, optionally plus `文件`.
- Centered.
- Top edge is 35 mm below the top edge of the text block.
- Recommended font: 小标宋体.
- Color: red.
- For joint issuing, host authority generally comes first. If `文件` appears, place it to the right of authority names and vertically center it relative to the joint names.

### 4.5 Document Number / 发文字号

- Place two lines below issuing authority mark, centered.
- Use full Arabic year in `〔〕`.
- Do not add `第`; do not pad sequence numbers with zero.
- Add `号` after sequence number.
- Example: `河职院〔2019〕10号`.
- For upward documents, place document number left with one-character indent, aligned with the last signer name on the same line.

### 4.6 Signer / 签发人

- Content: `签发人：姓名`.
- Place right with one-character indent, two lines below issuing authority mark.
- `签发人`: 3号仿宋; signer name: 3号楷体.
- Multiple signers: follow issuing-authority order, left-to-right then top-to-bottom, generally two names per line; continuation aligns to the first signer on the previous line.

### 4.7 Red Separator / 版头分隔线

- Place 4 mm below document number.
- Centered and text-block width.
- Color: red.

## 5. Body Area

### 5.1 Title / 标题

- Generally 2号小标宋体.
- Place two lines below the red separator.
- Center one or more lines.
- Line breaks should preserve meaning, be symmetric, and preferably form trapezoid or diamond shapes.

### 5.2 Main Recipients / 主送机关

- Place one line below title.
- Flush left; continuation lines also flush left.
- End the final recipient with a full-width colon.
- If recipients are too long and prevent正文 from appearing on page 1, move them to the imprint as `主送`.

### 5.3 Body / 正文

- Page 1 must show正文.
- Generally 3号仿宋体.
- Place on the next line after main recipients.
- Each paragraph starts with two-character indent; continuation lines are flush left.
- Heading sequence: `一、`, `（一）`, `1.`, `（1）`.
- Font hierarchy: first level 黑体, second level 楷体, third/fourth level 仿宋体.

### 5.4 Attachment Description / 附件说明

- If attachments exist, place one line below正文, left indented two characters.
- Single: `附件：附件名称`.
- Multiple: `附件：1. XXXXX`.
- Do not add punctuation after attachment names.
- Long attachment names wrap aligned to the first character of the attachment name.

## 6. Signature, Date, and Seal

### 6.1 Date Format

- Use Arabic numerals for full year, month, and day.
- Do not pad month/day with leading zero.
- Correct: `2019年9月12日`; incorrect: `2019年09月12日`.

### 6.2 With Official Seal

- Date generally right indented four characters.
- Seal is red and must not be blank.
- Single authority: authority name above date, centered relative to date; seal centered and pressing both authority name and date; authority/date lie slightly below seal center.
- Seal top should be within one line of正文 or attachment description.
- Joint issuing: authority names arranged by issuing order; seals correspond one-to-one, neat, not overlapping/touching, and each row stays within text block. Final seal presses the final authority name and date.

### 6.3 Without Official Seal

- Single authority: place authority name one line below正文/attachment description, right indented two characters.
- Date goes one line below authority name. Its first character shifts two characters right from authority name; if date is longer, date right indent remains two characters and authority right indent increases accordingly.
- Joint issuing: host authority first; other authority names continue downward in order.

### 6.4 With Signer Signature Seal

- Single authority: place signature seal two lines below正文/attachment description, right indented four characters.
- Put signer title two characters left of signature seal and vertically center it to the seal.
- Date one line below signature seal, right indented four characters.
- Joint issuing: host title/seal first, others downward, one authority per row, titles in full.
- Signature seal generally red.

### 6.5 Insufficient Space

If the remaining blank space cannot hold the seal/signature seal and date, adjust line spacing or character spacing.

## 7. Notes and Attachments

### 7.1 Note / 附注

- If present, place on the line below date.
- Left indented two characters.
- Enclose in parentheses.

### 7.2 Attachment Body / 附件

- Start attachments on a new page before the imprint.
- Bind with正文 when possible.
- `附件` plus sequence number: 3号黑体, flush left on the first line of text block.
- Attachment title: centered on the third line of text block.
- Sequence number/title must match attachment description.
- Attachment formatting follows正文 rules.
- If attachment is not bound with正文, place document number at top-left first line of attachment followed by `附件` and sequence number.

## 8. Imprint / 版记

### 8.1 Separator Lines

- Width equals text block.
- First and final separator lines are thick, recommended 0.35 mm.
- Middle separator lines are thin, recommended 0.25 mm.
- First separator is above the first imprint element.
- Final separator coincides with lower edge of the text block on the final page.

### 8.2 CC / 抄送机关

- If present, generally 4号仿宋.
- Place one line above issuing/printing office and print date.
- Left and right indented one character.
- Format: `抄送：机关名称。`.
- Continuation aligns to the first character after the colon.
- End final CC authority with a period.

### 8.3 Moved Main Recipients

- If main recipients move to imprint, use `主送` instead of `抄送` and otherwise format like CC.
- If both main and CC recipients exist, place `主送` one line above `抄送`; do not add a separator between them.

### 8.4 Printing Office and Date

- Generally 4号仿宋.
- Place above the final separator.
- Printing office left indented one character.
- Print date right indented one character.
- Date uses full Arabic year/month/day without leading zero, followed by `印发`.
- If other imprint elements exist, separate them from printing office/date with a thin line.

## 9. Page Numbers

- Generally use 4号 half-width Song Arabic numerals.
- Place below the lower edge of the text block.
- Put a one-character dash line on each side of the page number.
- The dash line is 7 mm below the lower edge of the text block.
- Odd page numbers: right, one-character indent.
- Even page numbers: left, one-character indent.
- If a blank page appears before the imprint page, neither the blank page nor the imprint page has page numbers.
- If attachments are bound with正文, page numbers continue through attachments.

## 10. Landscape Tables

- A4 landscape tables keep page-number position consistent with other pages.
- Odd page table header is on the binding side.
- Even page table header is on the outer/cut side.

## 11. Special Formats

### 11.1 Letter Format / 信函格式

- Issuing mark uses full or standardized issuing authority name; joint issuing uses host authority mark.
- Centered, top edge 30 mm from top page edge; recommended red 小标宋.
- Red double line below mark at 4 mm: upper thick, lower thin; 170 mm long, centered.
- Red double line 20 mm above bottom page edge: upper thin, lower thick; 170 mm long, centered.
- Copy number/secrecy/urgency go flush left at text-block left below first double line in standard order; first element is 7/8 of 3号 character height below the line.
- Document number goes flush right at text-block right below first double line, also 7/8 of 3号 character height below the line.
- Title is centered two lines below the last element above it.
- If text appears above the second double line, keep it 7/8 of 3号 character height from the line.
- First page does not show page number.
- Imprint has no printing office, date, or separator lines, and sits at bottom of final page text block.

### 11.2 Command / Order Format / 命令（令）格式

- Issuing mark is authority full name plus `命令` or `令`.
- Centered; top edge 20 mm below text-block top edge.
- Recommended red 小标宋.
- Order number centered two lines below mark.
- Body starts two lines below order number.
- Signer title, signature seal, and date follow signer-signature-seal rules.

### 11.3 Minutes / 纪要格式

- Minutes mark is `XXXXX纪要`.
- Centered; top edge 35 mm below text-block top edge.
- Recommended red 小标宋.
- Attendance list: generally 3号黑体 `出席：` one line below正文/attachment description, left indented two characters; attendee unit/name after colon in 3号仿宋.
- Continuation aligns to first character after colon.
- `请假` and `列席` each start a new line and follow the same method.
- Minutes format may be adapted to actual practice.

## 12. Automation Checks

- A4 page and margins match rules.
- Text block derived from margins is 156 mm × 225 mm.
- Default body is 3号仿宋 and black.
- Title is centered 2号小标宋.
- Page 1 contains正文.
- Numbering hierarchy is consistent and not missing leading `一、`.
- Dates do not have zero-padded month/day.
- Page numbers are outside text block and alternate left/right by parity.
- Signature/date are visible and aligned according to seal/no-seal scenario.
- Attachments and attachment descriptions match.
- Imprint separator and contents follow rules when present.
- Rendered pages have no clipping, overlap, missing glyph boxes, broken table geometry, or excessive blank gaps.
