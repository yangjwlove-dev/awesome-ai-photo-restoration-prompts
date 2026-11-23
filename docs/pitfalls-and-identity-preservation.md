# Pitfalls & Identity Preservation Guide

Generative image models are trained to produce *plausible* images, not necessarily *faithful* reconstructions. When restoring family photographs, portraits, or archival prints, plausibility without fidelity is a failure.

## The 5 Most Common Restoration Failure Modes

### 1. Face Averaging (Identity Drift)
- **Symptom**: The restored person looks 10–15 years younger or resembles a generic stock model rather than the actual subject.
- **Root Cause**: Open-ended terms like *"beautiful portrait"*, *"studio quality"*, or *"flawless skin"* pull the diffusion trajectory toward dataset averages.
- **Fix**: Explicitly forbid beautification and enumerate immutable landmarks: *"Preserve exact eye spacing, eyelid shape, nose bridge, lip asymmetry, smile lines, eyebrows, and hairline."*

### 2. Wax-Museum Skin Smoothing
- **Symptom**: All film grain disappears and skin turns into smooth plastic.
- **Root Cause**: Asking for *"noise-free, crystal clear, ultra-smooth"* output.
- **Fix**: Request *"subtle, organic film grain and fine micro-skin texture consistent with an optical 35mm lens."*

### 3. Unwanted Colorization of Archival Monochrome
- **Symptom**: A sepia or black-and-white print comes back partially tinted or fully colorized.
- **Root Cause**: Models associate *"modern DSLR clarity"* with full RGB color.
- **Fix**: Add a hard negative constraint: *"Keep the image strictly monochrome/sepia matching the original paper tone; zero added color."*

### 4. Severe Crease / Tear Hallucination
- **Symptom**: A crease passing through an eye or button gets replaced with a distorted shape.
- **Root Cause**: Asking for restoration + upscaling + colorization in one single pass on heavily damaged areas.
- **Fix**: Use a **two-stage workflow**:
  1. **Pass 1 (Structural Repair)**: Repair scratches, tears, and stains while keeping native tone and resolution.
  2. **Pass 2 (Upscale / Colorize)**: Upscale to 2×/4× or apply colorization on the clean Pass 1 output.

### 5. Text & Background Sign Garbling
- **Symptom**: Storefront signs, newspaper headlines, or book covers turn into alien glyphs.
- **Root Cause**: Standard super-resolution treats small text as high-frequency texture.
- **Fix**: Explicitly instruct: *"Keep all visible text faithful to the original letterforms; preserve slight softness rather than inventing new characters."*

## Recommended Evaluation Rubric (5-Point Pass/Fail)

| Check | Pass Criteria |
| :--- | :--- |
| **Identity Match (400% zoom)** | Subject is immediately recognizable to someone who knows them; zero altered eye/nose geometry. |
| **Tonal Fidelity** | Exposure, white balance, and B&W/sepia preservation match intent. |
| **Natural Micro-Texture** | Hair strands, fabric weave, and pores look optical, not painted. |
| **Defect Removal** | Target scratches/stains/blur are resolved without smudged patches. |
| **Zero Hallucinations** | No invented fingers, extra jewelry, distorted glasses, or mangled text. |
