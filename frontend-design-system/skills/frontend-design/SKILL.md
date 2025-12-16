---
name: frontend-design
description: Complete design system for web and UI design. Use this skill when the user mentions "design", asks for design help, wants to design something, needs UI design, UX design, web design, graphic design for web, visual design, interface design, or any design-related request. Also triggers for building websites, landing pages, dashboards, web apps, React components, HTML/CSS, styling, beautifying UI, creating layouts, or making things look good. Includes 50 curated fonts, motion library, component patterns, and live inspiration from design galleries.
license: Complete terms in LICENSE.txt
---

# Frontend Design System

A complete design system for creating distinctive, production-grade frontend interfaces.

## Quick Start

1. **Understand context** → Purpose, audience, mood
2. **Get inspiration** → Scrape live examples (see `references/inspiration-sources.md`)
3. **Create theme** → Build 5-layer theme (see `references/theme-creation.md`)
4. **Implement** → Use resources below as needed

## Resource Navigation

| Need | Reference |
|------|-----------|
| Live design inspiration | `references/inspiration-sources.md` |
| Create a unique theme | `references/theme-creation.md` |
| Typography choices | `assets/fonts/font-index.json` |
| Color tokens & palettes | `references/color-system.md` |
| Animations & transitions | `references/motion-library.md` |
| UI component templates | `references/component-patterns.md` |
| Grid & layout patterns | `references/layout-system.md` |
| OG images & social cards | `references/social-media.md` |
| Tailwind & shadcn/ui | `references/framework-integration.md` |

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
