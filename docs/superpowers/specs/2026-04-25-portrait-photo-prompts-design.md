# Portrait Photo Prompts Skill Design

## Purpose

Create a Codex skill named `portrait-photo-prompts` that helps generate professional portrait and photoshoot image prompts. The skill should produce a bilingual Chinese/English prompt pack for portrait photography concepts, with the English prompt optimized for OpenAI image models.

The skill does not call the OpenAI API, generate images, save image files, or manage API keys. Its job is to create high-quality prompts and creative direction that can be used in image generation tools.

## Location

Create the skill at:

```text
/Users/fengye/.codex/skills/portrait-photo-prompts
```

This location allows Codex to auto-discover the skill.

## Skill Structure

```text
portrait-photo-prompts/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── portrait-framework.md
    ├── openai-image-prompting.md
    └── prompt-examples.md
```

## Trigger Behavior

The skill should trigger when the user asks Codex to generate, improve, translate, structure, or vary portrait, photoshoot, headshot, fashion portrait, editorial portrait, cinematic portrait, or personal photography prompts.

The skill should support vague requests such as:

- "帮我生成一组人像写真提示词"
- "给我一个电影感肖像 prompt"
- "帮我写 OpenAI 生图用的写真提示词"
- "一键生成一套复古胶片人像 prompt"

## Interaction Rules

If the user gives enough detail, generate the prompt pack directly.

If the request is missing important creative direction, ask at most two focused questions. Useful questions include subject identity, mood, scene, styling, lighting, and final use case.

If the user explicitly says "一键生成", "直接给我", "不用问", or similar, do not ask clarification questions. Use reasonable creative defaults and proceed.

## Default Output Format

Generate a professional "Portrait Prompt Pack" with these sections:

1. Creative Direction
   - Theme intent
   - Subject temperament
   - Visual keywords

2. 中文摄影提示词
   - 主体、姿态、表情
   - 场景、服装、道具
   - 光线、镜头、构图
   - 色彩、质感、后期风格

3. English Prompt for OpenAI Image Models
   - A complete natural-language prompt
   - Clear subject, scene, lighting, lens, composition, mood, styling, texture, and photographic finish

4. Negative Constraints
   - Avoid low-quality rendering, over-smoothed skin, distorted hands, plastic texture, cluttered backgrounds, awkward anatomy, and inconsistent lighting

5. Framing and Style Suggestions
   - Aspect ratio
   - Close-up, half-body, or full-body framing
   - Lens and depth-of-field suggestions
   - Realistic photography, cinematic, editorial, or magazine-style intensity

6. Variants
   - Lighting variant
   - Composition variant
   - Mood variant
   - Styling or post-production variant

## Reference Files

### `references/portrait-framework.md`

Include reusable portrait photography language and decision frameworks:

- Subject temperament
- Pose and expression
- Wardrobe, makeup, hair, and props
- Scene and environmental context
- Lens focal lengths and depth of field
- Lighting types
- Composition patterns
- Color palettes
- Post-production texture
- Common portrait categories such as cinematic portrait, studio fashion, natural-light lifestyle, vintage film, dark emotional portrait, editorial portrait, and fine-art portrait

### `references/openai-image-prompting.md`

Include guidance for writing OpenAI image prompts:

- Prefer complete natural-language descriptions
- Describe the relationship between subject, scene, light, camera, mood, and styling
- Avoid Midjourney-specific parameters by default
- Avoid contradictory visual instructions
- Use quality and negative constraints sparingly and clearly
- Refer to the current official GPT Image model family naming rather than treating `Image-2` as a public model name

### `references/prompt-examples.md`

Include a small set of strong examples that Codex can imitate:

- Urban night emotional portrait
- Natural-light film photoshoot
- Studio high-fashion editorial
- Classical painterly portrait

Each example should include Chinese planning notes, an English OpenAI image prompt, negative constraints, and variants.

## Validation

The completed skill should pass `quick_validate.py`. If the active Python environment does not include PyYAML, run the validator from a temporary virtual environment that installs PyYAML first:

```bash
python3 -m venv /tmp/portrait-skill-validate-venv
/tmp/portrait-skill-validate-venv/bin/python -m pip install PyYAML
/tmp/portrait-skill-validate-venv/bin/python /Users/fengye/.codex/skills/.system/skill-creator/scripts/quick_validate.py /Users/fengye/.codex/skills/portrait-photo-prompts
```

Review the skill for:

- Clear YAML frontmatter with only `name` and `description`
- Concise `SKILL.md` instructions
- Useful reference files without duplicated filler
- No unrelated README, installation guide, changelog, or extra documentation

## Out of Scope

- Calling the OpenAI API
- Generating or editing image files
- Managing API credentials
- Building a UI
- Supporting every image-generation platform as a first-class target
- Writing Midjourney, Stable Diffusion, or ComfyUI-specific parameter syntax by default

## Acceptance Criteria

- Codex can discover and trigger the skill for portrait prompt requests.
- The skill reliably produces a bilingual professional prompt pack.
- The English prompt is shaped for OpenAI image models rather than Midjourney parameter syntax.
- The references provide stable photographic vocabulary, OpenAI-specific prompt guidance, and examples.
- The skill validates successfully with `quick_validate.py`.
