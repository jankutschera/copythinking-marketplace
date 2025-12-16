---
description: Vintage 70s Polaroid style image
argument-hint: [scene description]
---

Generate a vintage 1970s Polaroid-style image using Nano Banana Pro.

Scene request: $ARGUMENTS

Build a vintage prompt using these authentic 70s Polaroid characteristics:
- **Film**: Authentic Polaroid instant film look
- **Exposure**: Slightly overexposed with warm color cast
- **Focus**: Soft focus, especially around edges
- **Texture**: Nostalgic film grain, faded edges
- **Colors**: Warm oranges and yellows, lifted blacks, muted highlights

Prompt template:
```
Generate an authentic 1970s Polaroid instant photograph of [SCENE DESCRIPTION]. Slightly overexposed with warm amber color cast, soft focus around edges, authentic instant film grain and texture. Faded colors with lifted blacks, nostalgic vintage atmosphere. [If reference photo: Use uploaded reference photo exactly for subject's likeness.]
```

If the user wants themselves in the photo, ask for a reference photo.

Use `mcp__fal-ai__generate` with model `fal-ai/nano-banana-pro` and `image_size: "square"` for authentic Polaroid dimensions.
