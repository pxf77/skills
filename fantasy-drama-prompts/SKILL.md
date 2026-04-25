---
name: fantasy-drama-prompts
description: Generate, adapt, improve, translate, structure, or vary OpenAI-first image prompts for popular fantasy web-novel image dramas. Use when Codex needs storyboard prompt packs, fantasy comic-drama prompts, Chinese fantasy, cultivation, xuanhuan, xianxia, short-video drama prompts, poster prompts, OpenAI image prompts, Midjourney rewrites, or Stable Diffusion tags for fantasy web-fiction scenes.
---

# Fantasy Drama Prompts

Use this skill to turn fantasy web-novel concepts, character sheets, plot excerpts, or cover requests into image-drama prompt packs. Default to OpenAI-first output: each storyboard frame must include a direct English natural-language prompt for OpenAI GPT Image models before any Midjourney or Stable Diffusion adaptation.

## Workflow

1. Identify the input type: concept, plot excerpt, character sheet, cover request, or short-video scene.
2. Choose the output form:
   - Use storyboard prompt pack by default.
   - Use poster or cover prompt when the user asks for a single strong image.
   - Add short-video narration and rhythm notes when the user asks for short-video drama output.
3. Choose the adaptation mode:
   - Use light enhancement by default: preserve the user's core facts and strengthen visual drama.
   - Use strong operation mode only when the user asks for "爆款化", "短视频化", "强运营改编", or similar.
4. Choose frame count:
   - 3-6 frames for a short concept or character setup.
   - 9-12 frames for a complete scene or plot beat.
   - Follow the user's requested frame count when specified.
5. Load only the references needed:
   - Read `references/trope-library.md` for fantasy web-fiction tropes and iconic scene logic.
   - Read `references/storyboard-framework.md` for frame rhythm, shot functions, and continuity rules.
   - Read `references/platform-prompts.md` for OpenAI, Midjourney, and Stable Diffusion prompt formats.
   - Read `references/prompt-examples.md` when the user asks for examples or a highly polished pattern.
6. Produce the output in the default structure below unless the user asks for a shorter format.

## Default Output

1. **改编策略**
   - 输入类型
   - 改编模式
   - 核心爽点
   - 分镜长度

2. **角色与世界观视觉表**
   - 主角、反派、关键配角
   - 年龄感、气质、服装、发型、武器或法器、灵力颜色、身份符号
   - 主场景与世界观关键词
   - 每帧必须复用的角色连续性锚点

3. **分镜表**
   - 镜头编号
   - 剧情功能
   - 画面描述
   - 景别、机位、构图
   - 情绪与动作
   - 法术特效与视觉符号

4. **OpenAI Image Prompt**
   - Give each frame one complete English natural-language prompt.
   - Include subject, action, scene, composition, camera, lighting, color, fantasy effects, style, and character continuity.
   - Keep OpenAI prompts free of Midjourney flags, Stable Diffusion tags, LoRA syntax, and comma-only tag blocks.
   - Add practical image notes such as aspect ratio, cover suitability, close-up or wide-shot suitability, and standalone poster potential.

5. **Cross-Platform Adaptations**
   - Midjourney prompt rewrite.
   - Stable Diffusion positive prompt, negative prompt, and token grouping.
   - Keep this section after the OpenAI prompt so platform syntax does not pollute OpenAI output.

6. **封面/海报补充**
   - 爆款主视觉
   - 强冲突角色站位
   - One OpenAI-first cover prompt.

7. **短视频漫剧补充**
   - 字幕或旁白钩子
   - 转场与节奏建议
   - 每 3-4 帧一个反转、揭示、升级或悬念点

## OpenAI Prompt Rules

- Write complete English scene descriptions suitable for the public GPT Image model family, such as `gpt-image-1.5`, `gpt-image-1`, and `gpt-image-1-mini`.
- Prefer coherent scene writing over keyword piles.
- Repeat concise character continuity anchors in every frame prompt.
- Avoid asking for multiple separate images inside one image.
- Avoid excessive visible text unless the user asks for poster typography.
- Do not claim to call image APIs or generate images. This skill creates prompts only.

## Safety And Originality

- Adapt user-provided material into new visual prompt language instead of copying long protected passages.
- Do not imitate a specific living artist or a specific copyrighted novel's protected wording.
- When the user provides a long excerpt, summarize story function and convert it into visual beats.
