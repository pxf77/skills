---
name: portrait-photo-prompts
description: Generate, improve, translate, structure, or vary professional portrait and photoshoot image prompts. Use when Codex needs to create bilingual Chinese/English prompt packs for portrait photography, headshots, fashion portraits, editorial portraits, cinematic portraits, personal photoshoots, natural-light portraits, studio portraits, vintage film portraits, or OpenAI image-model portrait prompts.
---

# Portrait Photo Prompts

Use this skill to create professional portrait and photoshoot prompt packs. Default to bilingual Chinese/English output, with the English prompt written for OpenAI image models in complete natural language.

## Workflow

1. Identify the user's portrait concept, subject, mood, scene, styling, lighting, and intended use.
2. If key creative direction is missing, ask at most two focused questions.
3. If the user says "一键生成", "直接给我", "不用问", or gives a similar instruction, skip clarification and use tasteful defaults.
4. Load only the reference files needed for the request:
   - Read `references/portrait-framework.md` when choosing photographic direction, lighting, styling, lens, composition, or visual texture.
   - Read `references/openai-image-prompting.md` when writing or refining the English prompt for OpenAI image models.
   - Read `references/prompt-examples.md` when the user asks for examples, variants, or a polished pack that should imitate a known structure.
5. Produce the prompt pack in the output format below.

## Output Format

Use this structure unless the user asks for a shorter or different format:

1. **创意方向**
   - 主题意图
   - 人物气质
   - 画面关键词

2. **中文摄影提示词**
   - 主体、姿态、表情
   - 场景、服装、道具
   - 光线、镜头、构图
   - 色彩、质感、后期风格

3. **English Prompt for OpenAI Image Models**
   - Write one complete natural-language prompt.
   - Include subject, scene, lighting, lens, composition, mood, styling, texture, and photographic finish.

4. **负面约束**
   - Name concrete issues to avoid, such as low-quality rendering, over-smoothed skin, distorted hands, plastic skin texture, cluttered backgrounds, awkward anatomy, and inconsistent lighting.

5. **画幅与风格建议**
   - Aspect ratio
   - Close-up, half-body, or full-body framing
   - Lens and depth-of-field suggestions
   - Realistic photography, cinematic, editorial, or magazine-style intensity

6. **变体**
   - Lighting variant
   - Composition variant
   - Mood variant
   - Styling or post-production variant

## Prompting Rules

- Prefer specific photographic language over generic praise.
- Keep the English prompt coherent and physically plausible.
- Do not use Midjourney parameters such as `--ar`, `--style`, or `--v` unless the user explicitly asks for Midjourney.
- Do not claim to generate or save images. This skill creates prompts only.
- Avoid overloading the prompt with contradictory styles, camera setups, or lighting directions.
- If the user mentions `Image-2`, treat it as their informal wording unless they provide an exact API model name; refer to OpenAI's public GPT Image model family when discussing model naming.
