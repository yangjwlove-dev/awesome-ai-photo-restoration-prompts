# 02. Deblur & Focus Recovery Prompts

All prompts below enforce strict identity, tone, and fidelity guardrails.

## 1. Soft-Focus Portrait Optical Clarity Recovery

- **ID**: `deblur-portrait-soft-focus`
- **Best for**: Portraits where the camera missed focus slightly on the eyes or face.

```text
Recover optical sharpness and natural micro-detail in this slightly out-of-focus portrait while keeping the subject's exact facial identity, skin tone, and lighting unchanged.

Focus priorities:
- Restore crisp eyelashes, iris catchlights, eyebrows, lip edges, and individual hair strands.
- Clean up subtle JPEG artifacts and sensor noise while preserving authentic skin pores.
- Keep background bokeh naturally blurred so the lens depth of field remains realistic.

Constraints:
- Do NOT alter gaze direction, expression, facial proportions, or color grading.
- Avoid synthetic HDR halos, oversharpened dark outlines, or airbrushed skin.
```

## 2. Camera Shake & Handheld Motion Blur Removal

- **ID**: `deblur-motion-handheld`
- **Best for**: Indoor, night, or candid shots blurred by slow shutter speed and directional camera shake.

```text
Remove directional camera-shake motion blur from this handheld photograph and restore clean, natural edges across both foreground subjects and architectural lines.

Repair priorities:
- Deconvolve directional ghosting around eyes, hands, hairlines, and high-contrast edges.
- Recover crisp clothing seams, jewelry, and background edges without creating double-edge ringing artifacts.
- Keep natural indoor/night ambient lighting and authentic shadow noise balance.

Constraints:
- Preserve exact subject pose, facial identity, and candid moment—do NOT freeze-pose or re-compose the scene.
- Do NOT brighten night scenes into daytime exposure.
```

## 3. Low-Light High-ISO Noise Cleanup + Detail Recovery

- **ID**: `deblur-low-light-iso-noise`
- **Best for**: Grainy concert, restaurant, or evening phone photos plagued by color blotches and muddiness.

```text
Clean up heavy high-ISO chroma noise and muddy low-light softness in this photograph while preserving natural edge detail and authentic night lighting atmosphere.

Repair priorities:
- Remove purple/green color blotches in shadow regions without turning hair or dark fabrics into flat smeared patches.
- Recover realistic eye clarity, skin texture, and specular light highlights.
- Maintain warm/cool practical light sources and natural shadow depth.

Constraints:
- Do NOT apply heavy beauty-filter skin smoothing or artificial daytime white balance.
- Preserve fine natural luminance grain so the photo retains photographic realism.
```

## 4. WhatsApp / WeChat / Social Thumbnail Compression Cleanup

- **ID**: `deblur-messenger-compressed`
- **Best for**: Heavily re-compressed chat photos suffering from 8x8 JPEG blocking, mosquito noise, and low resolution.

```text
Remove severe JPEG compression blocks, color banding, and mosquito artifacts around edges in this low-resolution shared photo, restoring clean natural sharpness.

Repair priorities:
- Eliminate blocky artifacts on faces, gradients, skies, and text edges.
- Reconstruct fine hair strands, natural skin texture, and crisp clothing patterns faithfully.
- Keep original composition, colors, and subject identities 100% unchanged.

Constraints:
- Do NOT invent new accessories, change facial expressions, or hallucinate unreadable background text.
```

## 5. Moving Subject Deblur (Kids, Pets & Sports)

- **ID**: `deblur-action-pets-kids`
- **Best for**: Candid shots of running children, dogs/cats, or sports moments with subject movement blur.

```text
Sharpen the moving subject in this candid action photo by reducing motion blur on the face, eyes, fur/hair, and clothing while maintaining a natural sense of real-camera motion.

Repair priorities:
- Restore clear focus on eyes, facial expression, and fine fur or hair detail.
- Eliminate smeared edges on moving hands/limbs without distorting anatomy or finger count.
- Keep background lighting, motion context, and natural colors intact.

Constraints:
- Do NOT alter anatomy, hand gestures, pet markings, or subject identity.
```

## 6. Landscape Atmospheric Haze & Soft Lens Sharpening

- **ID**: `deblur-landscape-haze`
- **Best for**: Travel photos shot through airplane windows, humid haze, or soft kit zoom lenses.

```text
Enhance optical micro-contrast and fine natural detail in this soft landscape photograph while keeping realistic atmospheric depth and true-to-life colors.

Repair priorities:
- Reduce hazy veil contrast loss and lens softness across foliage, rock faces, water ripples, and distant architecture.
- Restore crisp natural textures without crunchy over-sharpening halos along mountain ridges or skylines.

Constraints:
- Preserve natural aerial perspective (distant mountains should remain slightly softer than foreground).
- Do NOT add fake clouds, alter sky colors unnaturally, or apply garish HDR tone-mapping.
```
