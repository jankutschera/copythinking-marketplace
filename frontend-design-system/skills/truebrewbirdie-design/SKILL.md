---
name: truebrewbirdie-design
description: Create distinctive, production-grade frontend interfaces and social media graphics with exceptional design quality. Use this skill when the user asks to build web components, pages, artifacts, posters, landing pages, dashboards, or applications. Also triggers for Instagram posts, Stories, Reels, TikTok graphics, YouTube thumbnails, LinkedIn posts, Twitter/X graphics, OG images, or any design-related request. Generates creative, polished code and UI design that actively avoids generic AI aesthetics. Every output must be memorable and unique.
license: Complete terms in LICENSE.txt
---

# Frontend & Social Media Design System

Create distinctive, production-grade interfaces that **actively avoid generic AI aesthetics**.

## CRITICAL: Design Quality Standards

Before generating ANY design, internalize these rules:

```
YOU MUST:
✓ Create something memorable and unique
✓ Make bold creative choices
✓ Use distinctive typography (NEVER Inter, Roboto, Arial)
✓ Build a clear visual personality
✓ Surprise with at least one unexpected element

YOU MUST NOT:
✗ Generate generic "AI-looking" designs
✗ Use safe, boring color combinations
✗ Center everything with equal spacing
✗ Default to standard Tailwind styles
✗ Create something that "could be any website"
```

---

## Quick Start

1. **Context** → Who, what, mood?
2. **Inspiration** → Scrape live examples (`references/inspiration-sources.md`)
3. **Theme** → Build 5-layer theme (`references/theme-creation.md`)
4. **Implement** → Use resources below

---

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
| **All formats** | `references/social-media.md` |
| Stories/Reels (9:16) | 1080×1920 templates |
| Square (1:1) | 1080×1080 templates |
| Portrait (4:5) | 1080×1350 templates |
| Landscape (16:9) | 1280×720 / 1200×675 templates |
| OG images | 1200×630 templates |

---

## The 5-Layer Theme Architecture

Every design needs a custom theme. No defaults. No presets.

```
Layer 5: PERSONALITY   ← What makes it UNIQUE? (MOST IMPORTANT)
Layer 4: Effects       ← Shadows, transitions, easings
Layer 3: Typography    ← Font stack + type scale
Layer 2: Colors        ← Semantic token system
Layer 1: Foundation    ← Spacing scale, radii
```

**Layer 5 is mandatory.** If you can't articulate what makes this design memorable, start over.

---

## Social Media Design

For Instagram, TikTok, LinkedIn, Twitter/X, YouTube:

| Content Type | Format | Size |
|--------------|--------|------|
| Stories, Reels, TikTok | 9:16 | 1080×1920 |
| Instagram Feed | 4:5 or 1:1 | 1080×1350 or 1080×1080 |
| LinkedIn/Twitter | 16:9 | 1200×675 |
| YouTube Thumbnail | 16:9 | 1280×720 |
| Carousel | 1:1 | 1080×1080 per slide |

**Key Principles:**
- 3-second hook rule
- Less text = more impact
- High contrast for mobile
- Respect safe zones (especially Stories!)

---

## The 5 Aesthetic Pillars

### 1. Typography
- Use fonts from `assets/fonts/` - all curated for distinction
- **BLACKLIST:** Inter, Roboto, Arial, Open Sans, Lato, Montserrat, Poppins
- Pair: Display (headlines) + Body (content) + Mono (code)

### 2. Color
- Build semantic tokens, not arbitrary colors
- Dominant + sharp accent > evenly distributed palette
- Commit fully to light OR dark

### 3. Motion
- One orchestrated page load > scattered micro-interactions
- Staggered reveals with `animation-delay`
- Surprising hover states

### 4. Spatial Composition
- Asymmetry, overlap, grid-breaking
- Generous whitespace OR controlled density
- NEVER: everything centered with equal margins

### 5. Visual Details
- Textures, gradients, grain, shadows create depth
- NEVER: flat solid colors as only background
- Context-appropriate effects

---

## Anti-Patterns (NEVER Generate These)

```
❌ Inter + purple gradient on white background
❌ Everything centered with equal spacing
❌ Generic rounded corners everywhere (rounded-lg on everything)
❌ Blue primary + gray secondary (the AI default)
❌ Standard Tailwind without customization
❌ Designs that could be mistaken for AI-generated templates
❌ "Safe" choices that play it too conservative
```

---

## Quality Gate

Before delivering ANY design, verify:

- [ ] **Personality**: Does it have a clear signature element?
- [ ] **Typography**: Would a designer recognize the font choice as intentional?
- [ ] **Color**: Is there a memorable color story?
- [ ] **Motion**: Is there at least one delightful animation?
- [ ] **Uniqueness**: Would someone remember this design tomorrow?

**If you can't check all boxes, iterate until you can.**

---

## Philosophy

> "No design should be the same."

Every project gets a fresh theme built for its specific context. Extract principles from inspiration, never pixels. Bold maximalism and refined minimalism both work—the key is intentionality.

**Claude is capable of extraordinary creative work. Don't hold back. Be bold. Be distinctive. Be memorable.**
