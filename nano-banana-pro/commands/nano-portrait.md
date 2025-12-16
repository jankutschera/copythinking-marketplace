---
description: Quick portrait with Nano Banana Pro
argument-hint: [subject description]
---

Generate a professional portrait using Nano Banana Pro with optimized portrait settings.

Subject request: $ARGUMENTS

Build a portrait prompt using these defaults:
- **Camera**: 85mm lens at f/1.8
- **Lighting**: Soft Rembrandt style with gentle fill
- **Color**: Warm natural skin tones, professional portrait grading
- **Depth**: Shallow depth of field with creamy bokeh background
- **Quality**: Ultra-realistic, fine detail visible

Prompt template:
```
Generate an ultra-realistic portrait photograph of [SUBJECT DESCRIPTION]. Shot with 85mm lens at f/1.8, soft Rembrandt lighting with gentle fill, warm natural skin tones, professional portrait color grading. Shallow depth of field with creamy bokeh background. [If reference photo: Use uploaded reference photo exactly for subject's likeness.]
```

If the user mentioned themselves or "me", ask if they have a reference photo to upload, then add the reference instruction.

Use `mcp__fal-ai__generate` with model `fal-ai/nano-banana-pro` and `image_size: "portrait_4_3"`.
