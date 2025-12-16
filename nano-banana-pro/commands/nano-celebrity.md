---
description: Create celebrity encounter scene
argument-hint: [celebrity name] [activity]
---

Generate a realistic celebrity encounter image using Nano Banana Pro.

Request: $ARGUMENTS

Parse the request to identify:
1. **Celebrity**: Who they want to meet
2. **Activity**: What they're doing together (dinner, training, chess, etc.)

Build a celebrity encounter prompt using documentary/candid style:
- **Style**: Ultra-realistic candid photography
- **Camera**: 50mm lens at f/2.0 (natural, documentary feel)
- **Lighting**: Natural available light for authenticity
- **Color**: Documentary color grading, natural and believable
- **Mood**: Authentic, candid, like a real paparazzi shot

Prompt template:
```
Generate an ultra-realistic candid photograph of [USER] with [CELEBRITY NAME], [ACTIVITY DESCRIPTION]. Natural, authentic interaction, completely believable scenario. Shot with 50mm lens at f/2.0, natural available lighting, documentary color grading for maximum authenticity. Use uploaded reference photo exactly for [USER]'s likeness.
```

**Important**: For celebrity encounters, ALWAYS ask for a reference photo since the user wants themselves in the scene.

Celebrity-specific settings to consider:
- **Warren Buffett**: Simple diner, casual business conversation
- **The Rock**: Gym setting, intense workout atmosphere
- **Elon Musk**: Modern tech office, SpaceX/Tesla memorabilia
- **Queen Elizabeth**: Palace drawing room, afternoon tea
- **Movie stars**: Red carpet, film set, or casual settings

Use `mcp__fal-ai__generate` with model `fal-ai/nano-banana-pro` and `image_size: "landscape_4_3"` for most encounters.
