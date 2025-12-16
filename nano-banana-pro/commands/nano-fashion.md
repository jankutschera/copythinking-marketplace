---
description: Fashion editorial style image
argument-hint: [subject/outfit description]
---

Generate a high-fashion editorial image using Nano Banana Pro.

Fashion request: $ARGUMENTS

Build a fashion editorial prompt using these characteristics:
- **Style**: High-fashion editorial, Vogue/Harper's Bazaar aesthetic
- **Camera**: 85mm lens at f/2.0 (or 35mm for full body/environmental)
- **Lighting**: Professional fashion lighting with dramatic shadows
- **Color**: High contrast editorial color grading, punchy and sophisticated
- **Mood**: Powerful, aspirational, magazine-worthy

Prompt template:
```
Generate an ultra-realistic high fashion editorial photograph of [SUBJECT/OUTFIT DESCRIPTION]. Dynamic pose, powerful attitude, editorial styling. Shot with 85mm lens at f/2.0, professional fashion lighting with dramatic shadows, high contrast editorial color grading. Sharp details, magazine cover quality. [If reference photo: Use uploaded reference photo exactly for subject's likeness.]
```

If the user wants themselves in the photo, ask for a reference photo.

Use `mcp__fal-ai__generate` with model `fal-ai/nano-banana-pro` and `image_size: "portrait_4_3"` for portrait or `landscape_4_3` for full body/runway.
