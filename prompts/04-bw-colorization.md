# 04. Realistic B&W Photo Colorization Prompts

All prompts below enforce strict identity, tone, and fidelity guardrails.

## 1. Natural Family Portrait Colorization (Realistic Skin Undertones)

- **ID**: `colorize-family-portrait-natural`
- **Best for**: 1930s–1980s B&W family portraits where natural, understated realism matters most.

```text
Colorize this black-and-white family photograph with lifelike, understated natural colors while keeping every facial feature, shadow, and texture identical to the original image.

Color direction:
- Render realistic multi-tone human skin with subtle warm highlights, gentle rosy cheeks/ears, and slightly cooler shadow transitions—never flat monochrome peach.
- Choose muted, era-authentic colors for clothing, knitwear, wood furniture, and outdoor greenery consistent with classic Kodachrome/Ektachrome film.
- Keep original luminance contrast and natural silver film grain intact.

Strict constraints:
- Do NOT alter facial geometry, eye direction, expressions, or hairstyles.
- Zero oversaturated neon hues, zero color bleeding past clothing edges.
```

## 2. 1920s–1940s Historical Street & Architecture Colorization

- **ID**: `colorize-1920s-1940s-street`
- **Best for**: Archival cityscapes, vintage cars, storefronts, and historical documentary photos.

```text
Colorize this historical black-and-white street photograph with period-accurate 1920s–1940s muted pigments and realistic atmospheric lighting.

Color direction:
- Historically accurate dark enamels for vintage automobiles (black, navy, forest green, maroon), weathered brick/limestone facades, worn asphalt, and subdued wool coats/hats.
- Natural overcast or golden-hour sky tone matching the original shadow hardness and sun angle.
- Subtle patina and weathering on metal signs, wood trim, and pavement.

Strict constraints:
- Do NOT modernize storefronts, invent contemporary signage colors, or alter historic text/numbers.
- Maintain authentic documentary contrast and analog film texture.
```

## 3. Vintage Wedding Portrait Colorization (Lace & Warm Florals)

- **ID**: `colorize-wedding-vintage`
- **Best for**: Grandparents' B&W wedding portraits with delicate white lace, tuxedos, and bouquets.

```text
Colorize this vintage black-and-white wedding photograph with delicate, timeless film colors while keeping 100% of the couple's exact facial identities and dress textures.

Color direction:
- Natural ivory/off-white wedding gown preserving intricate lace shadows (not stark digital cyan-white), charcoal/black wool tuxedo, soft botanical greens and pastel florals in the bouquet.
- Warm, lifelike skin tones with subtle tonal depth and natural eye colors.

Strict constraints:
- Do NOT alter faces, veil patterns, lace geometry, or background architectural details.
- Avoid overly rosy/saturated Instagram-style filters.
```

## 4. Archival Military & Uniform Portrait Colorization

- **ID**: `colorize-military-uniform-archival`
- **Best for**: Mid-20th-century service portraits needing restrained olive/khaki/navy uniform accuracy.

```text
Colorize this archival black-and-white uniformed portrait with historically restrained, realistic textile and brass tones.

Color direction:
- Authentic matte wool/cotton uniform colors (muted olive drab, khaki, or deep navy appropriate to the uniform cut and monochrome tone value), subtle tarnished brass buttons/insignia, and natural leather straps.
- Realistic, understated human skin tones and classic neutral studio backdrop.

Strict constraints:
- Do NOT invent new medals, alter insignia shapes, or modify facial identity and posture.
```

## 5. User-Guided Palette Colorization Template (Fill-in-the-Blanks)

- **ID**: `colorize-custom-palette-guided`
- **Best for**: When family members remember exact hair, eye, dress, or car colors.

```text
Colorize this black-and-white photograph faithfully using the specific verified color cues below while keeping every facial feature, shadow, and grain texture unchanged.

Verified color cues (replace brackets before running):
- Subject hair & eyes: [e.g., chestnut brown hair, hazel eyes]
- Main garment: [e.g., deep burgundy wool cardigan over cream blouse]
- Key prop / vehicle: [e.g., pale sage-green 1957 sedan]
- Environment / season: [e.g., late autumn afternoon, muted golden foliage, soft overcast sky]

Strict constraints:
- Keep all unspecified elements in restrained, period-authentic natural colors.
- Do NOT alter facial geometry, expressions, or original luminance contrast.
```

## 6. Combined Gentle Scratch Cleanup + Subtle Colorization

- **ID**: `colorize-restore-then-color`
- **Best for**: Moderately scratched B&W prints where you want a clean single-pass natural color version.

```text
First repair visible dust specks, fine surface scratches, and tonal fading in this black-and-white photograph, then apply understated, historically realistic natural colorization.

Priorities:
- Preserve 100% of every person's exact facial likeness, age markers, and gaze.
- Apply lifelike multi-tone skin colors and muted mid-century film hues for clothing and surroundings.
- Retain subtle organic film grain across repaired and colorized regions.

Constraints:
- Do NOT beautify or smooth skin, invent background objects, or push color saturation beyond authentic analog film.
```
