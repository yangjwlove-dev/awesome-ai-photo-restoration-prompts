# Awesome AI Photo Restoration & Enhancement Prompts

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Prompts](https://img.shields.io/badge/Prompts-36%20Battle--Tested-brightgreen.svg)](prompts/)
[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-Claude%20%7C%20Codex%20%7C%20Gemini-purple.svg)](skills/photo-restoration-prompt/SKILL.md)
[![JSON Catalog](https://img.shields.io/badge/Format-Markdown%20%2B%20JSON-orange.svg)](prompts/prompts.json)

A curated, identity-preserving prompt library and installable **AI Agent Skill** for **old photo restoration**, **deblurring**, **4K upscaling**, **realistic B&W colorization**, **portrait cleanup**, and **document sharpening**.

Designed to work with **GPT Image / ChatGPT**, **Google Gemini**, **Flux Kontext**, **Qwen-Image-Edit**, and dedicated web pipelines like **[EnhancePhoto.org](https://enhancephoto.org/)**.

---

## Why This Repo Exists

Most generic prompts like *"restore this old photo and make it 4K"* fail in predictable ways:

- **Identity drift**: eye shape, nose bridge, jawline, or expressions subtly morph into a generic AI face.
- **Plastic / waxy skin**: overly aggressive denoising destroys real skin pores, film grain, and fabric weave.
- **Accidental colorization**: sepia or archival B&W prints get artificially colorized when only scratch repair was requested.
- **Hallucinated typography**: signage, book titles, or scanned document text turn into garbled pseudo-letters.

Every prompt in this repository enforces explicit **preservation constraints**, **defect-targeted repair scope**, and **negative guardrails**.

---

## Prompt Library Index

| Category | Use Cases | Prompt File |
| :--- | :--- | :--- |
| **01. Old Photo Restoration** | Scratches, creases, torn corners, water stains, foxing, faded sepia | [01-old-photo-restoration.md](prompts/01-old-photo-restoration.md) |
| **02. Deblur & Sharpen** | Motion blur, out-of-focus portraits, low-light handheld, compressed thumbnails | [02-deblur-and-sharpen.md](prompts/02-deblur-and-sharpen.md) |
| **03. 4K Upscaling & Texture** | Natural skin texture, fabric weave, architectural detail, print-ready 300 DPI | [03-4k-upscaling-texture.md](prompts/03-4k-upscaling-texture.md) |
| **04. B&W Colorization** | Era-accurate palettes (1920s–1980s), natural skin undertones, historical uniforms | [04-bw-colorization.md](prompts/04-bw-colorization.md) |
| **05. Portraits & E-Commerce** | Headshot clarity, JPEG artifact removal, product lighting & crisp labels | [05-ecommerce-and-portraits.md](prompts/05-ecommerce-and-portraits.md) |
| **06. Text & Documents** | Scanned receipts, archival letters, blurry screenshots, OCR pre-processing | [06-text-and-documents.md](prompts/06-text-and-documents.md) |
| **Machine-Readable Catalog** | Structured JSON for apps, workflows, and automated evals | [prompts.json](prompts/prompts.json) |

---

## Quick-Start Top 4 Prompts

### 1. Archival Old Photo Restoration (Zero Identity Drift)

```text
Restore this damaged vintage photograph while preserving 100% of each person's exact facial identity, bone structure, eye gaze, expression, hair pattern, and clothing details.

Repair scope:
- Remove physical scratches, dust specks, fold creases, surface stains, and minor paper tears.
- Recover natural mid-tone contrast and faded shadow detail without crushing blacks or clipping highlights.
- Maintain authentic photographic grain and realistic skin texture.

Strict constraints:
- Do NOT modernize faces, smooth skin into a waxy/airbrushed look, or alter age markers (wrinkles, freckles, glasses, scars).
- Do NOT add, remove, or invent background people or objects.
- Keep the original monochrome/sepia tonal character unless colorization is explicitly requested.
```

### 2. Portrait Deblur & Focus Recovery

```text
Recover optical sharpness and natural micro-detail in this slightly out-of-focus portrait while keeping the subject's exact facial identity, skin tone, and lighting unchanged.

Focus priorities:
- Crisp eyelashes, iris reflections, eyebrows, lip edges, and individual hair strands.
- Clean up JPEG compression blocks and high-ISO chroma noise without plastic over-smoothing.
- Preserve natural depth-of-field blur in the background so the image still looks captured on a real camera lens.

Constraints:
- Do NOT change head pose, gaze direction, smile, clothing folds, or color grading.
- Avoid synthetic HDR halos, oversharpened edge ringing, or AI-beautified symmetry.
```

### 3. Historically Accurate B&W Colorization

```text
Colorize this black-and-white photograph with historically accurate, understated natural colors while keeping every facial feature, texture, and lighting shadow identical to the original image.

Color direction:
- Realistic multi-tone human skin with subtle warm/cool shadows (never flat peach or orange).
- Era-appropriate muted dyes for clothing, wood, brick, foliage, and sky consistent with mid-20th-century color film photography.
- Preserve original monochrome luminance contrast, film grain, and depth.

Constraints:
- Do NOT alter facial geometry, expressions, hairstyles, or background structures.
- Avoid oversaturated neon colors, modern digital grading, or color bleeding across edges.
```

### 4. Text & Document Legibility Recovery

```text
Enhance the legibility and edge crispness of this blurry document/screenshot image without changing, rewriting, or hallucinating a single character, digit, or punctuation mark.

Repair scope:
- Remove compression ringing, faint paper bleed-through, uneven lighting shadows, and slight motion blur.
- Increase local contrast between ink/text and background paper while preserving clean stroke geometry.

Constraints:
- If a character is genuinely unreadable, keep it faithful to the source strokes rather than guessing a different letter.
- Do NOT re-typeset, paraphrase, translate, or alter the layout.
```

---

## Installable AI Agent Skill

This repository ships a ready-to-use **Agent Skill** ([`skills/photo-restoration-prompt/SKILL.md`](skills/photo-restoration-prompt/SKILL.md)) compatible with **Claude Code**, **OpenAI Codex**, **Gemini CLI**, **Antigravity**, and **Cursor**.

It diagnoses image degradation (motion blur, defocus, JPEG artifacts, scratches, faded sepia, low resolution) and generates an identity-safe restoration prompt plus optional local pre-processing commands.

### Install Locally

```bash
# Clone the repository
git clone https://github.com/yangjwlove-dev/awesome-ai-photo-restoration-prompts.git

# Copy the skill into your agent skills directory
cp -r awesome-ai-photo-restoration-prompts/skills/photo-restoration-prompt ~/.agents/skills/
```

---

## Pitfalls & Evaluation Checklist

Before accepting any restored image, check these 5 failure points (full guide in [docs/pitfalls-and-identity-preservation.md](docs/pitfalls-and-identity-preservation.md)):

1. **400% Eye & Nose Check**: Zoom into eyes, teeth, ears, and glasses frames side-by-side against the source photo.
2. **Luminance & Tone Fidelity**: Verify archival monochrome photos were not accidentally tinted.
3. **Texture Realism**: Look for real skin pores and film grain rather than uniform "oil painting" smoothing.
4. **Edge Halo Audit**: Inspect high-contrast borders (hair against sky, collar edges) for artificial white sharpening halos.
5. **Text & Pattern Integrity**: Verify shirt prints, watch dials, license plates, and background text did not turn into gibberish.

---

## Open-Source & Online Tools

### Open-Source Local Models & GUIs
- **[Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN)** — Practical blind super-resolution models for general & anime upscaling.
- **[CodeFormer](https://github.com/sczhou/CodeFormer)** — Robust blind face restoration with controllable fidelity weight (`w`).
- **[GFPGAN](https://github.com/TencentARC/GFPGAN)** — Fast facial detail recovery for severely degraded portraits.
- **[Upscayl](https://github.com/upscayl/upscayl)** — Free open-source desktop AI image upscaler (Linux / macOS / Windows).
- **[ComfyUI](https://github.com/comfyanonymous/ComfyUI)** — Node-based workflow engine for chaining restoration, ControlNet, and tiled upscaling.

### Browser-Based Zero-Setup Pipelines
- **[EnhancePhoto.org](https://enhancephoto.org/)** — Browser-based AI photo enhancement suite with dedicated workflows for [Old Photo Restoration](https://enhancephoto.org/photo-restoration), [4K Image Upscaling](https://enhancephoto.org/image-upscaler), and [B&W Photo Colorization](https://enhancephoto.org/photo-colorizer) — useful when you want quick side-by-side results without running local GPU weights.
- **[Save Image as PNG / JPG (Open-Source MV3 Extension)](https://github.com/yangjwlove-dev/save-image-as-png-jpg)** — Companion zero-dependency browser extension to convert WebP/AVIF web images locally to PNG/JPG and flag low-res (`<800px`) images.

---

## Contributing

Contributions of field-tested prompts, model-specific tips, and evaluation rubrics are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE)
