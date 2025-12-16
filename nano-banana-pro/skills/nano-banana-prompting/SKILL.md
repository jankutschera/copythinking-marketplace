---
name: nano-banana-prompting
description: This skill should be used when the user asks to "generate an image with Nano Banana", "create a portrait", "make me look like", "edit my photo", "generate a photo of me", "create an image", "Instagram story", "social media content", or wants to use Nano Banana Pro (fal-ai/nano-banana-pro) for any image generation task. Use this skill to craft optimized prompts that leverage the Nano Banana philosophy.
---

# Nano Banana Pro - Prompt Engineering Mastery

## Philosophy: The Micro-Prompt Revolution

**"Small input. Precise meaning. Big outcome."**

Nano Banana represents a paradigm shift in AI image generation - the art of crafting tiny prompts that create massive impact. Unlike other models that require lengthy, complex instructions, Nano Banana Pro responds exceptionally well to concise, precise language that reads like briefing a creative director.

### Core Principles

1. **Brevity with Precision** - Every word earns its place
2. **Visual Specificity** - Use exact technical parameters (lens, aperture, lighting)
3. **Emotional Intent** - Convey mood and atmosphere clearly
4. **Reference Photo Integration** - Always specify "use uploaded reference photo exactly" when using user photos

## Prompt Structure

Write prompts as **full sentences briefing a creative director**. Include:

### Essential Components

1. **Subject Description**
   - Physical characteristics, clothing, expression
   - Position and pose
   - Relationship to environment

2. **Technical Specifications**
   - Camera and lens (e.g., "Shot with 85mm lens")
   - Aperture for depth of field (e.g., "at f/1.4")
   - Film stock or digital style reference

3. **Lighting Description**
   - Type (natural, studio, golden hour)
   - Direction and quality (soft, dramatic, chiaroscuro)
   - Named techniques (Rembrandt, high-key, low-key)

4. **Color and Mood**
   - Color grading style (cinematic warm, muted earth tones)
   - Emotional atmosphere (intimate, powerful, nostalgic)
   - Post-processing reference (film grain, vintage fade)

5. **Composition**
   - Framing (close-up, medium shot, environmental)
   - Depth of field description
   - Background treatment

## Prompt Template

```
[Context/Purpose]: For a [type of content].
[Subject]: A [detailed subject description with specific colors and details].
[Setting]: [Environment with lighting conditions].
[Technical]: Shot with [lens]mm at f/[aperture], [camera/film reference].
[Style]: [Aesthetic reference], [color grading], [mood].
[Quality]: [Resolution/detail specifications].
[Reference]: Use uploaded reference photo exactly for [subject's] likeness.
```

## Technical Parameter Guide

### Lens Selection
- **24mm** - Wide environmental shots, dramatic perspective
- **35mm** - Documentary, street photography feel
- **50mm** - Natural perspective, versatile
- **85mm** - Portrait lens, flattering compression, beautiful bokeh
- **135mm** - Compressed perspective, intimate telephoto portraits

### Aperture Guide
- **f/1.4 - f/2.0** - Extremely shallow DoF, dreamy bokeh, subject isolation
- **f/2.8** - Shallow DoF with more context, professional portrait standard
- **f/4 - f/5.6** - Balanced depth, environmental portraits
- **f/8 - f/11** - Deep focus, landscape, group shots

### Lighting Styles
- **Golden Hour** - Warm, soft, flattering natural light
- **Rembrandt** - Triangle of light under eye, dramatic but classic
- **Chiaroscuro** - Strong contrast, dramatic shadows
- **High-Key** - Bright, minimal shadows, airy feel
- **Low-Key** - Dark, moody, dramatic shadows
- **Cinematic** - Directional with color contrast (often teal shadows, warm highlights)

### Color Grading
- **Cinematic Warm** - Teal shadows, orange highlights
- **Muted Earth Tones** - Desaturated, natural palette
- **High Contrast** - Punchy blacks, vivid colors
- **Vintage Faded** - Lifted blacks, muted highlights, film grain
- **Editorial** - High contrast, clean whites, saturated

## Style Categories

### Fashion Editorial
- High-fashion, Vogue aesthetic
- Professional studio or dramatic natural lighting
- High contrast, editorial color grading
- Sharp details, aspirational mood

### Vintage/Retro
- 1970s Polaroid instant film look
- Slightly overexposed, warm color cast
- Soft focus, nostalgic grain
- Faded edges, authentic film texture

### Cinematic
- Hollywood cinematography style
- 2.39:1 widescreen feel
- Dramatic chiaroscuro or golden hour lighting
- Teal and orange grade, film grain
- Anamorphic lens flares, shallow DoF

### Portrait/Oil Painting
- Classical oil painting style
- Rich, layered colors
- Dramatic lighting reminiscent of old masters
- Canvas texture, brushstroke quality

### Celebrity Encounter
- Ultra-realistic candid photography
- Natural lighting, documentary style
- 50mm lens at f/2.0
- Authentic, believable scenarios

### Action/Dynamic
- Motion blur, sense of movement
- Dramatic angles and perspective
- High energy, vibrant colors
- Fast shutter or intentional motion effects

---

## Social Media Categories

### Instagram Stories (9:16 Vertical)
- Use `portrait_16_9` image size
- Smartphone selfie aesthetic
- Leave margins for text/stickers
- Direct flash Y2K style trending
- Mirror selfies work exceptionally well

### Instagram Feed (1:1 or 4:5)
- Use `square_hd` or `portrait_4_3`
- Clean, scroll-stopping compositions
- Rule of thirds for portraits
- Premium quality that looks effortless

### TikTok/Reels Content
- Vertical 9:16 format
- Dynamic, attention-grabbing poses
- Bright, punchy colors
- Authentic, relatable aesthetic

### Infographics & Business
- Whiteboard/glass board presentations
- Text must be legible and natural
- Presenter gesturing toward content
- Modern corporate aesthetics

### Product Photography
- Clean backgrounds for e-commerce
- Lifestyle context for social media
- Shadow play for premium brands
- Flat lay compositions

### 3D Miniatures & Creative
- Chibi-style brand stores
- Isometric weather card dioramas
- Personal avatar caricatures
- Blind-box toy aesthetic

## Social Media Aspect Ratios

| Platform | Format | Ratio | Parameter |
|----------|--------|-------|-----------|
| Stories/TikTok | Vertical | 9:16 | `portrait_16_9` |
| IG Feed Square | Square | 1:1 | `square_hd` |
| IG Feed Portrait | Portrait | 4:5 | `portrait_4_3` |
| YouTube/LinkedIn | Landscape | 16:9 | `landscape_16_9` |

## Selfie Styles

### Smartphone Selfie
- Front-camera perspective with natural distortion
- Elevated angle (most flattering)
- Natural lighting preferred

### Mirror Selfie
- Full body or three-quarter view
- Phone held naturally, slight tilt
- Show environment details

### Direct Flash (Y2K)
- Bright white flash against dark background
- High contrast, cool blue tone
- Canon IXY/IXUS digital camera style
- Early 2000s aesthetic

### Car Selfie
- Golden hour through windows
- Side mirror reflections optional
- Warm, intimate atmosphere

## Reference Files

For detailed prompt examples and patterns, see:
- **`references/prompt-patterns.md`** - 200+ categorized prompts from the masterclass
- **`references/technical-specs.md`** - Complete camera, lighting, and color guides
- **`references/style-presets.md`** - Ready-to-use style templates
- **`references/social-media-templates.md`** - Instagram, TikTok, Infographics, Product shots

## Using This Skill

When generating images with Nano Banana Pro:

1. **Read the user's request** - Understand subject, mood, and purpose
2. **Select appropriate style** - Match style category to intent
3. **Build the prompt** - Use template with all technical components
4. **Include reference photo instruction** - If user provides a photo, add "Use uploaded reference photo exactly"
5. **Call fal.ai MCP** - Use `mcp__fal-ai__generate` with model `fal-ai/nano-banana-pro`

## Example Transformation

**User says:** "Make me look like a CEO"

**Optimized prompt:**
```
Generate an ultra-realistic corporate portrait of a confident executive in a tailored navy suit with subtle pinstripes, sitting in a modern corner office with floor-to-ceiling windows overlooking a city skyline. Shot with 85mm lens at f/1.8, soft Rembrandt lighting from large windows, professional corporate color grading with warm skin tones and cool background. Shallow depth of field with bokeh on city lights. Use uploaded reference photo exactly for subject's likeness.
```
