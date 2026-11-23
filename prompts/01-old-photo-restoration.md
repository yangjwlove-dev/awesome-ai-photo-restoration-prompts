# 01. Old & Damaged Photo Restoration Prompts

All prompts below enforce strict identity, tone, and fidelity guardrails.

## 1. Archival Damage Repair (Preserve Sepia / B&W Tone)

- **ID**: `old-photo-archival-repair`
- **Best for**: Scratched, creased, dust-spotted family photos where you want original monochrome or sepia tone preserved.

```text
Restore this damaged vintage photograph while preserving 100% of every person's exact facial identity, bone structure, expression, hair pattern, and clothing details.

Repair scope:
- Cleanly remove physical scratches, white dust specks, fold creases, minor paper tears, and foxing spots.
- Recover faded mid-tone contrast and shadow detail gently without crushing blacks or blowing out highlights.
- Preserve authentic photographic grain and realistic skin texture.

Strict constraints:
- Keep the exact original sepia/monochrome tonal character—do NOT colorize.
- Do NOT smooth skin into a waxy/airbrushed texture or erase natural wrinkles, glasses, or age markers.
- Do NOT invent new background objects or alter clothing shapes.
```

## 2. Two-Pass Heavy Tear & Fold Reconstruction (Pass 1: Structure Only)

- **ID**: `old-photo-heavy-crease-pass1`
- **Best for**: Severely folded, cracked, or water-stained photos prior to upscaling or colorizing.

```text
Perform a conservative structural restoration on this heavily creased and water-stained vintage photograph.

Priority tasks:
- Seamlessly mend deep fold lines, missing emulsion cracks, and water-ring discoloration across both foreground subjects and background.
- Reconstruct missing edges using surrounding cloth weave, paper grain, and lighting direction.
- Balance uneven yellowing across the print while keeping natural vintage contrast.

Strict constraints:
- Prioritize anatomical and identity accuracy over sharpness—do NOT over-sharpen or beautify faces.
- Preserve original monochrome tones, original framing, and background geometry.
- Keep natural silver-halide film grain uniform across repaired and original areas.
```

## 3. Multi-Person Vintage Group Portrait Restoration

- **ID**: `old-photo-group-family`
- **Best for**: Family reunions, wedding photos, and school class pictures with 3+ small faces.

```text
Restore this vintage group photograph with consistent sharpness and identity fidelity across EVERY person in the frame—including faces in the back row.

Repair scope:
- Remove print scratches, blotches, fading, and lens softness across the full frame.
- Restore subtle clarity to eyes, eyeglasses, hairlines, and collar details equally for all subjects without over-enhancing only the center faces.
- Maintain balanced vintage contrast and realistic analog film grain.

Strict constraints:
- Do NOT merge, drop, add, or swap any person's face, pose, or gaze direction.
- Avoid synthetic hyper-sharp faces floating on blurry bodies—keep sharpness optically consistent across the depth plane.
- Preserve the original B&W or vintage color palette without modernizing the look.
```

## 4. Faded 1970s–1990s Color Print Recovery (Magenta/Yellow Cast Fix)

- **ID**: `old-photo-faded-1970s-color`
- **Best for**: Old Kodak/Fujifilm prints that turned reddish-magenta, orange, or washed-out yellow.

```text
Restore this faded vintage color print by correcting dye-shift discoloration while preserving authentic analog film character and exact subject identity.

Color & tone repair:
- Neutralize heavy magenta, yellow, or cyan color casts caused by chemical print aging.
- Restore realistic natural skin undertones, neutral whites, and true shadows without making the photo look like a modern HDR smartphone shot.
- Clean up dust specks, scanner streaks, and paper surface scratches.

Strict constraints:
- Preserve original facial features, expressions, clothing patterns, and period atmosphere.
- Keep organic color film grain and subtle lens softness in out-of-focus areas.
- Do NOT oversaturate colors or apply aggressive clarity halos.
```

## 5. Remove Glossy Photo Glare & Plastic Sleeve Reflections

- **ID**: `old-photo-album-glare`
- **Best for**: Photos photographed with a phone through glass frames or glossy photo album sleeves.

```text
Remove the harsh light glare, glossy reflection patches, and uneven smartphone-capture shadows from this photographed print while restoring crisp original image detail.

Repair scope:
- Eliminate blown-out reflection streaks and hazy glare veils across faces and clothing, reconstructing underlying tones faithfully.
- Correct mild perspective skew and uneven illumination across the print surface.
- Preserve authentic print texture, exact facial identities, and original color/monochrome palette.

Strict constraints:
- Do NOT invent new facial details where subtle contrast already exists; recover from surrounding tonal cues.
- Do NOT crop out subjects or add artificial modern studio lighting.
```

## 6. 19th-Century Cabinet Card / Daguerreotype Oxidation Repair

- **ID**: `old-photo-silvering-daguerreotype`
- **Best for**: Pre-1920 studio portraits with metallic silvering, heavy tarnish, and vignette damage.

```text
Restore this 19th-century archival studio portrait affected by silvering oxidation, edge tarnish, and surface abrasions.

Repair scope:
- Remove metallic haze, tarnish spots, and fine surface scratches while recovering delicate tonal gradations in dark Victorian fabrics and facial features.
- Keep the authentic period tonal range (warm albumen/sepia or cool silver-gelatin) and original studio vignette framing.

Strict constraints:
- Do NOT colorize or modernize facial features, grooming, or posture.
- Preserve genuine archival texture and period lens falloff.
```
