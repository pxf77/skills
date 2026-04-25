# Platform Prompt Rules

Use OpenAI prompts as the primary deliverable. Midjourney and Stable Diffusion rewrites are secondary adaptations.

## OpenAI GPT Image Prompt

Write a complete English natural-language scene prompt. Include:

- Subject and continuity anchors
- Action and emotional state
- Scene and worldbuilding context
- Shot size, camera angle, and composition
- Lighting and color palette
- Fantasy effects and visual symbols
- Desired image style and finish
- Specific negative constraints when useful

Template:

```text
Create a cinematic fantasy image-drama frame of [subject with continuity anchors] in [scene]. The subject is [action and emotion], while [supporting character or crowd reaction]. Compose the image as [shot size, angle, framing]. Use [lighting and color palette], with [magic effect and visual symbol]. Keep the style [visual style], with consistent character design across frames. Avoid [negative constraints].
```

## Midjourney Rewrite

Use concise visual phrases, then optional parameters:

```text
[subject], [scene], [action], [emotion], [magic effect], [composition], [lighting], [style keywords] --ar 16:9 --style raw
```

Use MJ parameters only in this section, never in the OpenAI prompt.

## Stable Diffusion Rewrite

Use grouped tags:

```text
Positive: [character anchors], [scene], [action], [composition], [lighting], [fantasy effects], [style]
Negative: low quality, worst quality, blurry, deformed hands, broken face, extra limbs, inconsistent costume, messy background, watermark, text artifacts, muddy magic effects
```

## Universal Negative Constraints

Use these when relevant:

- low quality
- blurry face
- deformed hands
- extra fingers
- extra limbs
- inconsistent character design
- costume drift
- messy background
- unreadable magic effects
- watermark
- random text artifacts
- duplicated characters
- plastic skin
- broken anatomy
