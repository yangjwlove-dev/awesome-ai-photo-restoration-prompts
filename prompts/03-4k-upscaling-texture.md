# 03. 4K Upscaling & Natural Texture Prompts

All prompts below enforce strict identity, tone, and fidelity guardrails.

## 1. 4K Print-Ready Portrait Upscale (Anti-Plastic Skin)

- **ID**: `upscale-4k-natural-portrait`
- **Best for**: Upscaling a small portrait for framing, printing at 300 DPI, or large 4K displays.

```text
Upscale this portrait to crisp 4K print-ready resolution while strictly preserving the subject's exact facial identity, proportions, lighting, and natural skin texture.

Detail reconstruction:
- Reconstruct realistic microscopic skin pores, natural peach fuzz, individual eyelashes, eyebrows, and fine hair strands.
- Add crisp fabric weave, stitching, and knit texture to clothing consistent with the original garments.
- Maintain authentic photographic tonal roll-off and subtle organic film/sensor grain.

Strict constraints:
- Zero plastic skin smoothing, zero AI face beautification, zero age reduction.
- Do NOT change eye color, teeth alignment, jewelry design, or background objects.
```

## 2. 4K Architectural & Interior Design Upscale

- **ID**: `upscale-4k-architecture-real-estate`
- **Best for**: Real estate listings, architectural photography, and interior portfolios needing sharp straight lines.

```text
Upscale this architectural/interior photograph to clean 4K resolution with crisp geometric precision and realistic material textures.

Detail priorities:
- Sharpen straight architectural edges, window mullions, brick/stone mortar, wood grain, brushed metal, and woven upholstery.
- Clean up compression noise in painted walls and glass reflections while keeping reflections physically accurate.

Constraints:
- Do NOT warp straight vertical/horizontal lines, invent extra furniture, or alter brand logos/artwork on walls.
```

## 3. 4K Illustration, Anime & Line-Art Upscale

- **ID**: `upscale-4k-digital-art-illustration`
- **Best for**: Digital paintings, anime stills, concept art, and cel-shaded artwork without introducing photographic noise.

```text
Upscale this illustration to crisp 4K resolution while faithfully preserving the original artist's brushwork, line weight, shading style, and exact color palette.

Detail priorities:
- Reconstruct clean, anti-aliased ink lines and smooth cel/painterly gradients without JPEG ringing or stair-stepping.
- Preserve intentional paper/canvas grain or flat anime fills according to the source art style.

Constraints:
- Do NOT convert illustrated characters into photorealistic faces.
- Do NOT alter character designs, eyes, signature watermarks, or color harmony.
```

## 4. Cinematic Film Still 4K Remaster

- **ID**: `upscale-4k-old-movie-still`
- **Best for**: Low-res DVD/VHS captures and vintage cinema stills needing 35mm-style 4K remastering.

```text
Remaster and upscale this low-resolution film still to clean 4K cinema quality while honoring authentic 35mm film optics and color timing.

Detail priorities:
- Remove VHS/DVD interlacing lines, macroblocking, and chroma smear.
- Recover crisp actor facial fidelity, period costume weave, and set textures with subtle, genuine 35mm film grain.

Constraints:
- Preserve exact cinema color grading, aspect ratio framing, and actor likenesses.
- Avoid modern digital-video sharpness or sterile noise-free plastic look.
```

## 5. 4K Wildlife, Botanical & Macro Texture Upscale

- **ID**: `upscale-4k-macro-nature`
- **Best for**: Cropped wildlife shots, bird photography, and macro flower/insect images.

```text
Upscale this nature photograph to ultra-crisp 4K detail while maintaining natural optical bokeh and biologically accurate textures.

Detail priorities:
- Reconstruct individual feather barbs, animal fur fibers, leaf veins, and dewdrop specular highlights faithfully.
- Keep smooth, creamy lens background blur free from digital noise amplification.

Constraints:
- Do NOT hallucinate unnatural scales/patterns or distort animal eyes and anatomy.
```

## 6. Crisp Retina 4K UI / Logo / Diagram Upscale

- **ID**: `upscale-4k-ui-design-mockup`
- **Best for**: Blurry presentation slides, software screenshots, logos, and infographics.

```text
Upscale this graphic/UI image to razor-sharp Retina resolution with clean vector-like edges, flat solid colors, and crystal-clear typography.

Detail priorities:
- Eliminate JPEG mosquito noise around icons, buttons, borders, and text.
- Preserve exact brand colors, icon geometry, and every character of text without distortion.

Constraints:
- Do NOT rewrite labels, invent new UI buttons, or add photorealistic shading to flat vector elements.
```
