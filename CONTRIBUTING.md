# Contributing to Awesome AI Photo Restoration Prompts

Thank you for helping make AI photo restoration more accurate and identity-preserving!

## Prompt Submission Guidelines

Every prompt PR should include:

1. **Clear Target Degradation**: Specify the exact problem (e.g., severe fold creases, high-ISO concert blur, 1940s sepia fading, e-commerce JPEG ringing).
2. **Explicit Preservation Guardrails**: State what must *not* change (identity, gaze, age markers, monochrome tone, layout, text).
3. **Model Compatibility Notes**: Note which models you tested (e.g., GPT Image, Gemini, Flux Kontext, Qwen-Image-Edit, ComfyUI).
4. **JSON Sync**: If adding a new prompt, also add an entry to `prompts/prompts.json` with `id`, `category`, `title`, `bestFor`, and `prompt`.

## What We Do Not Accept

- Generic one-liners like *"make it 8K ultra realistic masterpiece"* without preservation constraints.
- Prompts that promote deepfakes, non-consensual edits, or misleading document forgery.
