---
name: truebrewbirdie-design
description: Complete design system for web, UI, and social media design. Use this skill when the user mentions "design", asks for design help, wants to design something, needs UI design, UX design, web design, social media design, Instagram posts, Stories, Reels, TikTok graphics, LinkedIn posts, Twitter/X graphics, YouTube thumbnails, OG images, graphic design for web, visual design, interface design, or any design-related request. Also triggers for building websites, landing pages, dashboards, web apps, React components, HTML/CSS, styling, beautifying UI, creating layouts, making things look good, or creating social media content. Includes 50 curated fonts, motion library, component patterns, social media templates (9:16, 1:1, 4:5, 16:9), and live inspiration from design galleries.
license: Complete terms in LICENSE.txt
---

# Frontend & Social Media Design System

A complete design system for creating distinctive, production-grade frontend interfaces AND social media graphics.

## Quick Start

1. **Understand context** → Purpose, audience, mood
2. **Get inspiration** → Scrape live examples (see `references/inspiration-sources.md`)
3. **Create theme** → Build 5-layer theme (see `references/theme-creation.md`)
4. **Implement** → Use resources below as needed

## Resource Navigation

### Web & UI Design
| Need | Reference |
|------|-----------|
| Live design inspiration | `references/inspiration-sources.md` |
| Create a unique theme | `references/theme-creation.md` |
| Typography choices | `assets/fonts/font-index.json` |
| Color tokens & palettes | `references/color-system.md` |
| Animations & transitions | `references/motion-library.md` |
| UI component templates | `references/component-patterns.md` |
| Grid & layout patterns | `references/layout-system.md` |
| Tailwind & shadcn/ui | `references/framework-integration.md` |

### Social Media Design
| Need | Reference |
|------|-----------|
| **All Social Media formats** | `references/social-media.md` |
| Stories/Reels (9:16) | `references/social-media.md` → 1080×1920 templates |
| Instagram/LinkedIn Square (1:1) | `references/social-media.md` → 1080×1080 templates |
| Instagram Portrait (4:5) | `references/social-media.md` → 1080×1350 templates |
| YouTube Thumbnails (16:9) | `references/social-media.md` → 1280×720 templates |
| Twitter/LinkedIn Landscape | `references/social-media.md` → 1200×675 templates |
| OG images & meta tags | `references/social-media.md` → 1200×630 templates |

## Design Workflow

### Step 1: Context Analysis
Before ANY design work:
- **Who** uses this? (audience, expertise level)
- **What** problem does it solve?
- **Where** will it live? (standalone, within app, mobile)
- **What mood** should it convey?

### Step 2: Live Inspiration
Fetch 2-3 examples from design galleries matching your context:
- Use `WebFetch` on sources listed in `references/inspiration-sources.md`
- **Analyze, don't copy**: Extract principles, not pixels
- Note: Color story, type pairing, motion philosophy, unique elements

### Step 3: Theme Creation
Build a 5-layer theme using `references/theme-creation.md`:
```
Layer 1: Foundation    → Spacing, radii
Layer 2: Colors        → Semantic tokens
Layer 3: Typography    → Font stack + scale
Layer 4: Effects       → Shadows, transitions
Layer 5: Personality   → What makes it UNIQUE?
```

### Step 4: Implementation
Reference specific guides as needed:
- Fonts: Choose from `assets/fonts/` (50 curated options)
- Motion: Use patterns from `references/motion-library.md`
- Components: Start from templates in `references/component-patterns.md`
- Layouts: Apply patterns from `references/layout-system.md`

---

## Social Media Design Workflow

For Instagram, TikTok, LinkedIn, Twitter/X, YouTube:

### Step 1: Choose Format
| Content Type | Best Format |
|--------------|-------------|
| Stories, Reels, TikTok | **9:16** (1080×1920) |
| Instagram Feed | **4:5** (1080×1350) or **1:1** (1080×1080) |
| LinkedIn Post | **1:1** (1080×1080) or **16:9** (1200×675) |
| Twitter/X | **16:9** (1200×675) |
| YouTube Thumbnail | **16:9** (1280×720) |
| Carousel | **1:1** (1080×1080) per slide |

### Step 2: Apply Template
Go to `references/social-media.md` and:
1. Pick template for your format
2. Customize colors, fonts, content
3. Respect safe zones (especially for Stories!)

### Step 3: Key Principles
- **3-second rule**: Hook attention immediately
- **Less text = more impact** (especially 9:16)
- **High contrast**: Must be readable on mobile
- **Brand consistency**: Same fonts, colors across posts
- **Platform-native**: Each platform has different vibes

---

## Core Principles

### The 5 Aesthetic Pillars

1. **Typography**
   - Use fonts from `assets/fonts/` - all curated for distinction
   - NEVER: Inter, Roboto, Arial, Open Sans, Lato, Montserrat, Poppins
   - Pair: Display font (headlines) + Body font (content) + Mono (code)

2. **Color**
   - Build semantic tokens, not random colors
   - Dominant + sharp accent > evenly distributed palette
   - Commit to light OR dark, don't hedge

3. **Motion**
   - One orchestrated page load > scattered micro-interactions
   - Staggered reveals with `animation-delay`
   - Surprising hover states
   - See `references/motion-library.md` for ready-to-use patterns

4. **Spatial Composition**
   - Asymmetry, overlap, grid-breaking
   - Generous whitespace OR controlled density
   - Never: everything centered, equal margins everywhere

5. **Visual Details**
   - Textures, gradients, grain, shadows create depth
   - Never: flat solid colors as only background
   - Context-appropriate effects (brutalist ≠ organic ≠ luxury)

## Anti-Patterns (NEVER Do)

```
❌ Inter + purple gradient on white
❌ Everything centered with equal spacing
❌ Generic rounded corners everywhere
❌ Copying scraped designs instead of extracting principles
❌ Same aesthetic across different projects
❌ Standard Tailwind without customization
❌ "Safe" choices that could be any website
```

## Quality Checklist

Before delivering, verify:
- [ ] Theme has clear personality (Layer 5)
- [ ] Typography is distinctive, not generic
- [ ] Color system uses semantic tokens
- [ ] At least one memorable motion moment
- [ ] Layout has intentional asymmetry or structure
- [ ] Would someone recognize this design as unique?

## Philosophy

> "No design should be the same."

Every project gets a fresh theme created for its specific context. We don't pick from templates - we build themes using principles and live inspiration.

**Bold maximalism and refined minimalism both work.** The key is intentionality, not intensity. Commit fully to your direction.

Claude is capable of extraordinary creative work. Don't hold back.
