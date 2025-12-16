---
description: Cinematic movie-style image
argument-hint: [scene description]
---

Generate a Hollywood cinematic movie-style image using Nano Banana Pro.

Scene request: $ARGUMENTS

Build a cinematic prompt using these Hollywood movie characteristics:
- **Style**: Hollywood cinematography, blockbuster movie still
- **Aspect**: 2.39:1 widescreen cinematic feel
- **Camera**: 35mm lens at f/2.8 (classic cinema lens)
- **Lighting**: Dramatic chiaroscuro or golden hour, motivated sources
- **Color**: Teal and orange cinematic grade, subtle film grain
- **Effects**: Anamorphic lens characteristics, subtle flares, shallow DoF

Prompt template:
```
Generate an ultra-realistic cinematic movie still of [SCENE DESCRIPTION]. Hollywood blockbuster cinematography with dramatic lighting and epic composition. Shot with 35mm anamorphic lens at f/2.8, dramatic cinematic lighting with motivated sources, teal and orange color grading with subtle film grain. Shallow depth of field with anamorphic bokeh characteristics. [If reference photo: Use uploaded reference photo exactly for subject's likeness.]
```

Cinematic sub-styles to consider based on request:
- **Action**: High energy, explosions, dramatic angles
- **Drama**: Intimate, emotional lighting, close-ups
- **Noir**: High contrast B&W, hard shadows, mystery
- **Sci-Fi**: Cool blue tones, futuristic lighting
- **Epic/Fantasy**: Golden tones, sweeping scale

If the user wants themselves as a character, ask for a reference photo.

Use `mcp__fal-ai__generate` with model `fal-ai/nano-banana-pro` and `image_size: "landscape_16_9"` for cinematic widescreen feel.
