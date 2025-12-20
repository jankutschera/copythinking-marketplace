---
name: image-director
description: Create and manage images for Dominant Guide articles. Use when user asks to "create images", "generate article images", "make hero images", or needs visuals for content. Chooses optimal AI model and style for each use case.
---

# Image Director for Dominant Guide

Strategic image creation for dominant-guide.com articles and marketing materials.

## Brand Visual Guidelines

### Aesthetic
- **Mood:** Dark, sophisticated, intimate
- **Style:** Editorial/artistic, not pornographic
- **Colors:** Deep blacks, burgundy, gold accents, warm skin tones
- **Lighting:** Dramatic, chiaroscuro, candlelit ambiance
- **Avoid:** Explicit content, faces clearly visible, identifiable people

### Visual Themes by Category

| Category | Visual Direction |
|----------|------------------|
| **Dominance** | Power poses, leather, command presence |
| **Submission** | Graceful surrender, kneeling silhouettes, trust |
| **Communication** | Two figures, connection, eye contact (silhouette) |
| **Trust** | Hands, blindfolds, vulnerability |
| **Consent** | Negotiation imagery, agreements, balance |
| **Boundaries** | Lines, barriers, safe spaces |
| **Aftercare** | Comfort, blankets, tenderness |
| **Safety** | Equipment, preparation, care |
| **Techniques** | Tools, implements, skill |
| **Relationships** | Couples, connection, intimacy |

## Model Selection Guide

### When to Use FLUX.2 Pro (`fal-ai/flux-2-pro`)

**Best for:**
- Photorealistic imagery
- Detailed textures (leather, rope, fabric)
- Dramatic lighting effects
- High-quality hero images

**Parameters:**
```json
{
  "prompt": "[detailed prompt]",
  "image_size": "landscape_16_9",
  "num_images": 1
}
```

### When to Use Nano Banana Pro (`fal-ai/nano-banana-pro`)

**Best for:**
- Stylized/artistic images
- Specific aesthetic presets
- Quick generation
- Social media content

**Use presets:**
- `nano-cinematic` - Movie-style dramatic shots
- `nano-portrait` - Character-focused images
- `nano-vintage` - Retro/classic feel
- `nano-fashion` - Editorial style

## Prompt Framework for BDSM Content

### Structure
```
[Subject description] + [Setting] + [Lighting] + [Style] + [Technical]
```

### Safe Prompt Patterns

**For Dominance articles:**
```
A powerful silhouette of a figure in a commanding stance,
dramatic side lighting, leather jacket visible,
dark moody atmosphere, editorial photography style,
shot on Sony A7IV, 85mm f/1.4, shallow depth of field
```

**For Submission articles:**
```
Artistic silhouette of a kneeling figure in graceful pose,
warm candlelit ambiance, soft shadows,
intimate bedroom setting with dark bedding,
fine art photography, tasteful and elegant
```

**For Trust/Aftercare:**
```
Close-up of intertwined hands in soft light,
one hand gently holding the other,
warm blanket texture visible, comfort and care,
intimate lifestyle photography, soft focus background
```

**For Equipment/Techniques:**
```
Elegant still life of [equipment] on dark velvet,
dramatic spotlight, jewelry-style product photography,
rich textures, professional studio lighting
```

## Image Specifications

### Hero Images (Articles)
- **Size:** landscape_16_9 (1920x1080)
- **Format:** WebP
- **File naming:** `[article-slug].webp`
- **Location:** `/public/images/blog/`

### Social Media
- **Instagram:** square (1080x1080)
- **Stories:** portrait_16_9 (1080x1920)
- **Twitter/X:** landscape_16_9

### Thumbnails
- **Size:** 400x225
- **Auto-generated from hero image

## Workflow

### 1. Analyze Article
- Read title and first paragraphs
- Identify category and themes
- Note any specific imagery mentioned

### 2. Choose Model
- FLUX.2 Pro for hero images (quality)
- Nano Banana Pro for social/quick needs

### 3. Craft Prompt
- Use brand guidelines
- Include technical specs
- Avoid explicit content flags

### 4. Generate & Review
- Generate 1-2 options
- Check for brand alignment
- Verify no problematic content

### 5. Save & Optimize
- Convert to WebP if needed
- Save to correct location
- Update article frontmatter

## Example Prompts by Article Type

### "12 Types of Submissives"
```
Artistic composition showing twelve subtle silhouettes in
various graceful poses representing different submissive
archetypes, dark gradient background transitioning from
deep purple to black, each figure slightly different in
posture and energy, ethereal and tasteful,
editorial fashion photography style,
soft rim lighting on figures
```

### "How to Train a Submissive"
```
Elegant still life of a leather journal with handwritten
notes, a quality pen, and a single red rose on dark wood,
suggesting thoughtful guidance and structure,
warm candlelight, intimate atmosphere,
lifestyle product photography
```

### "The Bratty Submissive"
```
Silhouette of a figure with playfully defiant posture,
hands on hips, slight tilt of head suggesting mischief,
dramatic backlight creating rim glow,
dark moody background, editorial style,
capturing confident attitude
```

## Content Safety

### Always Avoid
- Explicit nudity
- Identifiable faces
- Minors or age-ambiguous figures
- Non-consensual imagery
- Weapons in threatening context
- Extreme content

### Safe Approaches
- Use silhouettes
- Focus on hands, backs, partial figures
- Emphasize atmosphere over bodies
- Still life with symbolic objects
- Abstract/artistic interpretations

## Integration

### Generate Image for Article
```
1. Read article content
2. Determine visual theme
3. Select appropriate model
4. Craft safe, brand-aligned prompt
5. Generate image
6. Save to /public/images/blog/[slug].webp
```

### Batch Generation
For multiple articles, maintain visual consistency:
- Same lighting style
- Consistent color palette
- Cohesive aesthetic across series

## Quick Commands

**Single article image:**
"Create a hero image for [article-title]"

**Batch images:**
"Generate images for all 8 submission articles"

**Social media:**
"Create Instagram posts for [article-title]"

**Style check:**
"What style should we use for [topic]?"
