# Awesome AI Photo Restoration & Enhancement Prompts

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Prompts](https://img.shields.io/badge/Prompts-36%20Tested-brightgreen.svg)](prompts/)
[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-Claude%20%7C%20Codex%20%7C%20Gemini-purple.svg)](skills/photo-restoration-prompt/SKILL.md)

36 copy-paste prompts + an installable AI Agent Skill for restoring old photos, fixing blur, upscaling to 4K, colorizing B&W prints, and sharpening blurry text without facial identity drift or plastic skin.

Works with GPT Image, Gemini, Flux Kontext, Qwen-Image-Edit, and web tools such as [EnhancePhoto](https://enhancephoto.org/).

## Prompt Index

| Category | Covers | File |
| :--- | :--- | :--- |
| **01. Old Photos** | Scratches, creases, tears, water stains, faded sepia/1970s color | [01-old-photo-restoration.md](prompts/01-old-photo-restoration.md) |
| **02. Deblur** | Missed focus, camera shake, low-light ISO noise, chat compression | [02-deblur-and-sharpen.md](prompts/02-deblur-and-sharpen.md) |
| **03. 4K Upscaling** | Anti-plastic portraits, architecture, anime/art, film stills, UI | [03-4k-upscaling-texture.md](prompts/03-4k-upscaling-texture.md) |
| **04. B&W Colorization** | Natural skin undertones, 1920s–1980s streets, weddings, uniforms | [04-bw-colorization.md](prompts/04-bw-colorization.md) |
| **05. E-Commerce & Headshots** | Crisp labels, fabric weave, jewelry, LinkedIn headshots, eyeglass glare | [05-ecommerce-and-portraits.md](prompts/05-ecommerce-and-portraits.md) |
| **06. Text & Documents** | Blurry screenshots, cursive letters, whiteboards, thermal receipts | [06-text-and-documents.md](prompts/06-text-and-documents.md) |
| **JSON Catalog** | Machine-readable list for scripts & evals | [prompts.json](prompts/prompts.json) |

## Top 3 Copy-Paste Prompts

### 1. Old Photo Damage Repair (Keep Original B&W / Sepia)

```text
Restore this damaged vintage photograph while preserving 100% of every person's exact facial identity, bone structure, eye gaze, expression, hair pattern, and clothing details.

Repair scope:
- Remove physical scratches, dust specks, fold creases, surface stains, and minor paper tears.
- Recover faded shadow and mid-tone contrast without crushing blacks or clipping highlights.
- Keep authentic film grain and realistic skin pores.

Strict constraints:
- Do NOT colorize—keep the original monochrome/sepia tone.
- Do NOT smooth skin into a waxy look or erase wrinkles, freckles, glasses, or age markers.
- Do NOT add, remove, or invent background people or objects.
```

### 2. Soft-Focus Portrait Deblur

```text
Recover optical sharpness in this slightly out-of-focus portrait while keeping facial identity, skin tone, and lighting unchanged.

Focus priorities:
- Crisp eyelashes, iris catchlights, eyebrows, lip edges, and fine hair strands.
- Remove JPEG compression blocks and chroma noise without plastic smoothing.
- Keep background bokeh naturally blurred.

Constraints:
- Do NOT alter gaze, smile, pose, clothing folds, or color grading.
- Avoid HDR halos or oversharpened edge ringing.
```

### 3. Blurry Text & Document Recovery (Zero Hallucination)

```text
Sharpen this blurry document/screenshot for legibility without changing, rewriting, or inventing a single character, digit, or punctuation mark.

Repair scope:
- Remove JPEG ringing, uneven shadows, and slight motion blur.
- Boost local contrast between ink and paper while keeping clean stroke geometry.

Constraints:
- If a character is genuinely unreadable, stay faithful to the source strokes rather than guessing.
- Do NOT re-typeset, translate, or alter layout.
```

## Install the Agent Skill

Compatible with Claude Code, Codex, Gemini CLI, Antigravity, and Cursor ([`SKILL.md`](skills/photo-restoration-prompt/SKILL.md)):

```bash
git clone https://github.com/yangjwlove-dev/awesome-ai-photo-restoration-prompts.git
cp -r awesome-ai-photo-restoration-prompts/skills/photo-restoration-prompt ~/.agents/skills/
```

## Quick 5-Point Quality Check

Before saving a restored output (full guide in [docs/pitfalls-and-identity-preservation.md](docs/pitfalls-and-identity-preservation.md)):

1. **400% face check**: compare eyes, nose bridge, teeth, and glasses frames side by side with the original.
2. **Tone lock**: confirm monochrome/sepia prints did not get accidentally tinted.
3. **Texture check**: look for real pores and grain instead of flat airbrushed skin.
4. **Edge halos**: check hair and collar borders for white oversharpening outlines.
5. **Text fidelity**: confirm signs, labels, and book titles did not turn into gibberish.

## Related Tools

- **Local Open-Source**: [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) · [CodeFormer](https://github.com/sczhou/CodeFormer) · [GFPGAN](https://github.com/TencentARC/GFPGAN) · [Upscayl](https://github.com/upscayl/upscayl) · [ComfyUI](https://github.com/comfyanonymous/ComfyUI)
- **Zero-Setup Web Option**: [https://enhancephoto.org/photo-restoration](https://enhancephoto.org/photo-restoration) (browser workflow for restoration, upscaling, and colorization without local GPU setup)
- **Browser Extension**: [save-image-as-png-jpg](https://github.com/yangjwlove-dev/save-image-as-png-jpg) (convert WebP/AVIF to PNG/JPG locally and flag `<800px` images)

## Contributing & License

PRs with tested prompts are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md). Licensed under [MIT](LICENSE).
