# OpenAI Image Prompting For Portraits

Use this reference when writing English prompts for OpenAI image models.

## Style

- Write complete natural-language descriptions rather than comma-only keyword strings.
- State the subject first, then describe scene, pose, styling, lighting, camera, mood, composition, and finish.
- Keep the prompt internally consistent. One clear lighting setup is better than several conflicting lighting directions.
- Use photographic terms when they change the image: lens focal length, depth of field, framing, light quality, color palette, texture, and post-production finish.
- Use negative constraints sparingly. Prefer concrete problems to avoid over broad lists.

## OpenAI-Oriented Prompt Shape

Use this pattern:

```text
Create a realistic [framing] portrait of [subject] in [scene]. The subject is [pose/expression/styling]. The image is lit with [lighting], photographed with [lens/camera feel], composed with [composition], and finished with [color/texture/post-production]. The mood should feel [mood words]. Avoid [specific negative constraints].
```

## Avoid By Default

- Midjourney flags such as `--ar`, `--style`, `--v`, `--s`, and `--q`
- Contradictory combinations such as soft natural daylight plus hard neon flash unless the interaction is clearly described
- Vague quality stacks such as "masterpiece, best quality, ultra detailed" without concrete visual direction
- Excessive celebrity references or living-artist style copying
- Prompt text that asks the model to create multiple separate images in one image

## Model Naming Note

Use public OpenAI GPT Image model family naming when discussing model targeting. Do not treat `Image-2` as a public model name unless the user explains that it is their own alias.
