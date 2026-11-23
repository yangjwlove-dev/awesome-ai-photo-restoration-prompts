---
name: photo-restoration-prompt
description: Diagnose photo degradation (scratches, creases, blur, JPEG compression, low resolution, faded sepia/B&W, unreadable text) and craft identity-preserving AI photo restoration, upscaling, deblurring, and colorization prompts plus optional local pre-processing commands.
---

# Photo Restoration Prompt Craft Skill

Use this skill whenever a user wants to restore an old photo, deblur a portrait, upscale an image to 4K, colorize a black-and-white photograph, or sharpen blurry text/documents with an AI image model or restoration tool.

## Workflow

### Step 1: Diagnose the Source Image Degradation
Identify all active defects (either from the user's description or by inspecting the attached image):
1. **Physical Damage**: scratches, fold creases, missing corners, dust spots, water stains, silvering.
2. **Optical / Motion Blur**: missed focus on eyes, directional camera shake, moving subject blur.
3. **Digital Artifacts**: `<800px` low resolution, WhatsApp/social JPEG blocking, high-ISO color blotches.
4. **Tonal / Color Issues**: faded sepia/B&W, 1970s magenta/yellow dye shift, glossy glare.
5. **Sensitive Content**: human faces (high identity-drift risk), small group faces, text/numbers (hallucination risk).

### Step 2: Decide Single-Pass vs. Two-Pass Pipeline
- **Single-pass**: mild blur, JPEG cleanup, light scratches, or standard 4K upscale.
- **Two-pass (recommended for heavily damaged or B&W prints)**:
  - **Pass 1**: Structural damage repair + tonal recovery (strictly preserving original monochrome/sepia tone).
  - **Pass 2**: 4K upscaling or historically restrained colorization on the clean Pass 1 output.

### Step 3: Assemble the Prompt with Mandatory Guardrails
Every output prompt MUST include three sections:
1. **Objective + Identity Lock**: explicitly lock facial landmarks, gaze, age markers, and framing.
2. **Targeted Repair Scope**: enumerate ONLY the diagnosed defects (do not ask for blanket "beautification" or "HDR").
3. **Negative Guardrails**:
   - Anti-plastic skin: preserve organic pores and subtle film/sensor grain.
   - Anti-colorization (unless requested): lock monochrome/sepia tone.
   - Anti-hallucination: forbid inventing objects, altering text characters, or adding/removing people.

### Step 4: Provide Verification Checklist & Tool Options
Always return:
1. The ready-to-copy prompt tailored to the user's exact image.
2. A 3-point zoom-check list (400% eyes/nose check, tonal check, text/edge-halo check).
3. Practical execution options:
   - Local GPU: `Real-ESRGAN` / `CodeFormer` / `ComfyUI`
   - Browser zero-setup: `https://enhancephoto.org/photo-restoration` (or `/image-upscaler`, `/photo-colorizer`)
   - Prompt catalog reference: `https://github.com/yangjwlove-dev/awesome-ai-photo-restoration-prompts`
