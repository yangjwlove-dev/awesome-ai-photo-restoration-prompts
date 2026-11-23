# 06. Text, Receipts & Document Sharpening Prompts

All prompts below enforce strict identity, tone, and fidelity guardrails.

## 1. Blurry Document & Screenshot OCR Legibility Recovery

- **ID**: `doc-general-ocr-prep`
- **Best for**: Blurry phone photos of contracts, lecture slides, whiteboards, or low-res web screenshots.

```text
Enhance the legibility and stroke sharpness of this blurry document/screenshot without changing, rewriting, or inventing a single letter, number, or symbol.

Repair priorities:
- Remove JPEG compression ringing, faint shadow gradients, and minor out-of-focus softness.
- Increase crisp local contrast between ink/text and the page background while keeping clean character outlines.

Strict constraints:
- If any character is genuinely ambiguous, keep faithful to the original ink strokes rather than guessing a different letter.
- Do NOT re-typeset, translate, summarize, or alter table/column layout.
```

## 2. Archival Handwritten Letter & Postcard Enhancement

- **ID**: `doc-vintage-handwriting-letter`
- **Best for**: Faded cursive letters, family diaries, and genealogy certificates on yellowed paper.

```text
Improve ink legibility on this faded archival handwritten document while preserving authentic paper character and exact cursive penmanship strokes.

Repair priorities:
- Separate faint faded ink from paper yellowing, foxing stains, and subtle bleed-through from the reverse side.
- Gently sharpen cursive pen strokes without breaking thin loops or turning handwriting into printed font.

Strict constraints:
- Do NOT alter spelling, overwrite uncertain cursive letters with modern fonts, or erase stamps/postmarks.
```

## 3. Whiteboard & Conference Slide Glare/Blur Cleanup

- **ID**: `doc-whiteboard-lecture-slide`
- **Best for**: Photos snapped from the back of a conference room or classroom.

```text
Clean up glare, uneven projector lighting, and mild zoom blur in this whiteboard/presentation slide photograph so every diagram line and text label is crisp and readable.

Repair priorities:
- Even out projector hot-spots and dim corners while preserving exact chart colors, arrows, and formulas.
- Clean up marker faintness on whiteboards without altering equations or spelling.

Strict constraints:
- Do NOT rewrite formulas, invent numbers, or rearrange diagram boxes.
```

## 4. Faded Thermal Receipt & Invoice Contrast Recovery

- **ID**: `doc-receipt-invoice-flatten`
- **Best for**: Expense reporting when thermal paper print has faded or creased.

```text
Recover maximum legibility on this faded receipt/invoice image by boosting dark-ink contrast against the paper background and cleaning up uneven phone shadows.

Strict constraints:
- Keep every digit, decimal point, date, and merchant character strictly faithful to the source image.
- Never guess or fabricate illegible digits.
```

## 5. Book Page Scan Shadow & Spine-Curve Cleanup

- **ID**: `doc-book-page-gutter`
- **Best for**: Smartphone photos of open book pages with dark spine shadows and soft margins.

```text
Even out the dark spine-gutter shadow and sharpen slightly soft printed text across this photographed book page while keeping natural paper tone and exact typography.

Strict constraints:
- Preserve exact pagination, footnotes, diagrams, and spelling without altering a single character.
```

## 6. Historical Map, Blueprint & Schematic Detail Recovery

- **ID**: `doc-vintage-map-blueprint`
- **Best for**: Low-resolution archival maps, engineering schematics, and patent drawings.

```text
Enhance fine linework, contour hatches, and small place-name labels in this archival map/blueprint while preserving exact cartographic geometry and authentic paper tones.

Strict constraints:
- Do NOT hallucinate new roads, rename labels, or distort scale bars and technical symbols.
```
