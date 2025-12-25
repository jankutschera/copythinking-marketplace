# Generative Design System

**No templates. No style menu. Every design is born from context.**

---

## CRITICAL: How This System Works

```
OLD WAY (Template-Based):
  User request → Pick style from menu → Apply mutations → Output
  Problem: Still feels like choosing from a catalog

NEW WAY (Generative):
  User request → Analyze context → Generate dimensions → Build unique system → Output
  Result: Every design is a one-of-a-kind creation
```

---

## Phase 1: Context Extraction

Before ANY design work, extract these from the request:

### The 5 Context Questions

| Question | Extract |
|----------|---------|
| **WHO** | Who is the audience? Age, profession, culture, values |
| **WHAT** | What is the product/service? Its core function |
| **WHY** | Why does this exist? The emotional promise |
| **FEEL** | What single emotion should dominate? |
| **ANTI** | What should this explicitly NOT be? |

### Example Context Extraction

```
Request: "Personal website for a developer who loves AI and automation"

WHO: Tech-savvy developers, potential employers/clients, 25-45
WHAT: Personal portfolio showcasing skills and projects
WHY: Establish credibility and attract opportunities
FEEL: Competent but approachable, slightly edgy
ANTI: Generic dev portfolio, boring corporate, too playful
```

---

## Phase 2: Dimensional Generation

Instead of picking a "style", generate values across these 8 dimensions:

### The Design Dimensions (0-100 Scale)

| Dimension | Low (0) | High (100) | Notes |
|-----------|---------|------------|-------|
| **ORDER ↔ CHAOS** | Grid-perfect, symmetric | Broken grids, overlaps, rotations | 0-30: Corporate, 70-100: Experimental |
| **MINIMAL ↔ MAXIMAL** | Few elements, whitespace | Dense, layered, decorative | Relates to information density |
| **WARM ↔ COLD** | Earth tones, oranges | Blues, grays, teals | Emotional temperature |
| **ORGANIC ↔ GEOMETRIC** | Curves, blobs, nature | Sharp edges, grids, lines | Shape language |
| **RETRO ↔ FUTURISTIC** | Past references | Sci-fi, forward-looking | Era feeling |
| **PLAYFUL ↔ SERIOUS** | Fun, bouncy, colorful | Professional, restrained | Tone |
| **LIGHT ↔ DARK** | Light backgrounds | Dark backgrounds | Mode |
| **DENSE ↔ SPARSE** | Tight spacing | Generous whitespace | Breathing room |

### Generate Unique Dimension Values

For each project, **generate specific values** based on context:

```
Example: Tech developer portfolio (edgy but professional)

ORDER:      45  ← Some grid breaks, not chaotic
MINIMAL:    35  ← Slightly content-rich, not empty
WARM:       25  ← Cool tones dominate
ORGANIC:    20  ← Mostly geometric
RETRO:      40  ← Slight vintage tech feel
PLAYFUL:    30  ← Professional lean
LIGHT:      15  ← Dark mode
DENSE:      50  ← Balanced spacing
```

**These numbers create a UNIQUE fingerprint.** No two designs have the same dimensional profile.

---

## Phase 3: Element Generation

With your dimensions defined, generate specific design decisions:

### 3.1 Color Generation

**Never pick colors from a preset palette. Generate them from dimensions.**

```
Warm/Cold dimension → Hue range
Light/Dark dimension → Value range
Playful/Serious dimension → Saturation range
```

| Dimension Values | Color Generation Rules |
|-----------------|----------------------|
| Cold (0-30) + Dark (0-30) | Base: Deep blue-grays (#0a1628 range), Accents: Cyan/Teal |
| Warm (70-100) + Light (70-100) | Base: Cream/Warm white, Accents: Terracotta/Gold |
| Cold + Light | Base: Cool white/blue-white, Accents: Electric blue/Purple |
| Playful (70-100) | Saturated accents, possibly multiple (2-3) |
| Serious (0-30) | Desaturated, single accent color |

**Color Formula:**
1. Generate a background color from Light/Dark + Warm/Cold
2. Generate a text color with sufficient contrast
3. Generate 1-3 accent colors from Playful/Serious + Warm/Cold
4. Test: Does this palette exist in any template? If yes, shift hues.

### 3.2 Typography Generation

**Never default to Inter/Roboto. Generate from dimensions.**

| Dimension | Font Characteristics |
|-----------|---------------------|
| Order 0-30 | Geometric sans, strict weights |
| Order 70-100 | Expressive display, mixed weights |
| Retro 70-100 | Period-appropriate faces |
| Organic 70-100 | Humanist or handwritten |
| Serious 0-30 | Traditional serif or neutral sans |
| Playful 70-100 | Rounded, bouncy, or display |

**Font Pairing Formula:**
1. Display font: From Order + Playful dimensions
2. Body font: From Organic + Serious dimensions
3. Mono font (if needed): From Retro dimension

**BLACKLIST (Never use these defaults):**
Inter, Roboto, Arial, Open Sans, Lato, Montserrat, Poppins, Nunito

**Instead, pick from these curated options** (see `assets/fonts/font-index.json`):
- Display: Bebas Neue, Playfair Display, Space Grotesk, Outfit, Syne, Cabinet Grotesk
- Body: IBM Plex Sans/Mono/Serif, Source Serif, Literata, Newsreader
- Handwritten: Caveat, Patrick Hand, Indie Flower
- Retro: Orbitron, VT323, Press Start 2P, Chicago
- Experimental: Dela Gothic One, Rubik Glitch, Monoton

### 3.3 Layout Generation

**Generate layout from Order + Dense + Chaos dimensions.**

| Order Level | Layout Behavior |
|-------------|----------------|
| 0-25 | Strict 12-column grid, everything aligned |
| 26-50 | Grid with intentional breaks, asymmetry allowed |
| 51-75 | Overlapping elements, z-index play, rotations |
| 76-100 | Controlled chaos, scattered positioning |

| Dense Level | Spacing Behavior |
|-------------|------------------|
| 0-25 | Compressed, tight margins, information-dense |
| 26-50 | Balanced padding, comfortable reading |
| 51-75 | Generous whitespace, room to breathe |
| 76-100 | Extreme whitespace, almost empty |

### 3.4 Effect Generation

**Generate effects from dimensions, not from "style" presets.**

| Dimension Combination | Effect Suggestions |
|----------------------|-------------------|
| Chaos 70+ | Glitch, shake, broken elements |
| Retro 70+ | Scanlines, CRT effects, noise/grain |
| Organic 70+ | Morphing blobs, fluid animations |
| Futuristic 70+ | Neon glows, holographic, glass |
| Playful 70+ | Bounce, squash/stretch, confetti |
| Minimal 70+ | Subtle fades, micro-interactions only |

---

## Phase 4: The Signature Element

**Every design MUST have ONE completely unique element.**

This is non-negotiable. It's what makes the design memorable.

### Signature Element Categories

| Category | Examples |
|----------|----------|
| **Animation Signature** | Cursor follows with trail, text types itself, elements breathe |
| **Layout Signature** | Horizontal scroll hero, diagonal section dividers, asymmetric nav |
| **Typography Signature** | One word HUGE, mixed weights mid-sentence, vertical text |
| **Color Signature** | One shocking accent that "shouldn't work", gradient that surprises |
| **Interaction Signature** | Hover reveals hidden layer, scroll triggers unexpected |
| **Texture Signature** | Custom noise pattern, unique grain, hand-drawn elements |

### How to Find Your Signature

Ask: **"What would make someone remember this site tomorrow?"**

If you can't answer that, you haven't found your signature yet.

---

## Phase 5: Anti-Pattern Enforcement

**These patterns are BANNED. If you generate them, start over.**

### Absolute Prohibitions

```
❌ Inter font on white background with purple/blue gradient buttons
❌ Everything centered with equal spacing all around
❌ Generic rounded corners (rounded-lg on everything)
❌ Blue primary + gray secondary + white background
❌ Standard Tailwind utility classes without customization
❌ Hero with centered H1, subheading, and two buttons
❌ Three-card feature section with icons
❌ Gradient text on the headline (unless it's genuinely unique)
❌ Designs that could be output by any AI with "make me a website"
```

### The AI Detection Test

Before finalizing, ask:
1. **If I described this design in words, would another AI generate something nearly identical?**
   - If yes → Your design is too generic
2. **Does this look like a template from ThemeForest/Webflow?**
   - If yes → Push further
3. **Would a human designer say "I've seen this before"?**
   - If yes → Add more distinctiveness

---

## Phase 6: Execution Checklist

### Before Writing Any Code

- [ ] Context extracted (WHO, WHAT, WHY, FEEL, ANTI)
- [ ] 8 dimensions have specific values (not just "medium")
- [ ] Colors generated from dimensions (not picked from palette)
- [ ] Fonts selected from curated list (not defaults)
- [ ] Layout approach defined
- [ ] Signature element identified
- [ ] Anti-patterns avoided

### During Implementation

- [ ] Custom CSS properties for all design tokens
- [ ] No raw Tailwind without customization
- [ ] At least one animation/transition
- [ ] Responsive considerations
- [ ] Signature element is prominent

### After Implementation

- [ ] AI Detection Test passed
- [ ] Would I remember this tomorrow? Yes
- [ ] Is there a clear visual personality? Yes
- [ ] Does it match the extracted context? Yes

---

## Quick Reference: Dimension Presets

**Only use these as STARTING POINTS. Always customize the values.**

| Vibe | ORD | MIN | WRM | ORG | RET | PLY | LGT | DNS |
|------|-----|-----|-----|-----|-----|-----|-----|-----|
| Corporate | 15 | 50 | 40 | 20 | 30 | 20 | 70 | 45 |
| Startup | 40 | 45 | 45 | 35 | 45 | 55 | 65 | 50 |
| Creative | 65 | 30 | 50 | 55 | 50 | 60 | 50 | 40 |
| Brutal | 70 | 40 | 25 | 10 | 40 | 25 | 80 | 35 |
| Luxe | 25 | 70 | 55 | 30 | 35 | 15 | 75 | 75 |
| Tech | 35 | 55 | 20 | 15 | 55 | 30 | 20 | 50 |
| Playful | 50 | 35 | 65 | 60 | 40 | 85 | 60 | 45 |
| Editorial | 20 | 60 | 50 | 25 | 30 | 20 | 80 | 60 |
| Cyber | 55 | 40 | 10 | 15 | 70 | 35 | 5 | 40 |
| Organic | 45 | 55 | 70 | 85 | 35 | 50 | 70 | 55 |

**Remember: These are seeds. Modify every value by ±15 to create YOUR version.**

---

## The Generative Design Manifesto

```
1. No two designs should ever be the same
2. Context determines dimensions, not style menus
3. Every design has a signature that makes it memorable
4. If it looks like a template, it's not done
5. Default fonts are creative surrender
6. Whitespace is a design decision, not leftover
7. Animation should surprise, not distract
8. Color should feel inevitable, not picked from a wheel
9. Breaking rules requires knowing rules
10. The goal is: "I've never seen exactly this before"
```

---

## Appendix: Legacy Style Reference

The following are REFERENCE ONLY. Do not copy them. Use them to understand visual languages, then generate something new.

### Visual Languages (Study, Don't Copy)

| Language | Key Characteristics | When to Reference |
|----------|-------------------|-------------------|
| Brutalist | No radius, thick borders, hard shadows, mono fonts | Order 70+, Organic 0-20 |
| Vaporwave | Sunset gradients, chrome, retro grids, neon | Retro 70+, Playful 50+ |
| Swiss | Strict grid, Helvetica, single accent, functional | Order 0-25, Minimal 60+ |
| Glassmorphism | Blur, transparency, layered depth | Minimal 50+, Futuristic 50+ |
| Editorial | Serifs, drop caps, pull quotes, magazine grid | Minimal 60+, Serious 0-40 |
| Cyberpunk | Neon, glitch, scanlines, dark | Dark 0-20, Futuristic 70+ |
| Handmade | Sketchy borders, cursive fonts, paper texture | Organic 70+, Playful 60+ |
| Terminal | Monospace, syntax colors, dark, prompts | Dark 0-20, Retro 50+ |

**Study these to understand principles. Never copy their exact implementation.**

---

## Example: Full Generative Process

### Request: "Portfolio for a creative developer interested in AI"

**Phase 1: Context**
```
WHO: Tech-forward recruiters, startup founders, fellow developers
WHAT: Personal portfolio with projects and thoughts
WHY: Attract interesting opportunities, show personality
FEEL: Clever but not pretentious, slightly unconventional
ANTI: Corporate dev portfolio, basic template, too "designer-y"
```

**Phase 2: Dimensions**
```
ORDER:      55  ← Some intentional breaks, not rigid
MINIMAL:    45  ← Content present but breathing
WARM:       30  ← Cool lean, tech feel
ORGANIC:    25  ← Mostly angular with occasional softness
RETRO:      50  ← Nods to early internet but modern
PLAYFUL:    45  ← Balanced, wit over whimsy
LIGHT:      20  ← Dark mode
DENSE:      50  ← Comfortable information density
```

**Phase 3: Element Generation**
```
COLORS:
- Background: #0c0c12 (deep near-black with slight warmth)
- Text: #e8e6e3 (warm off-white)
- Accent 1: #00ff9f (unexpected mint green - the "doesn't quite fit" color)
- Accent 2: #ff4d4d (error-red for contrast moments)

FONTS:
- Display: Space Grotesk (angular but friendly)
- Body: IBM Plex Sans (readable, tech cred)
- Mono: JetBrains Mono (for code snippets)

LAYOUT:
- Asymmetric two-column on desktop
- Occasional elements breaking grid (overlapping into margins)
- Generous but not extreme whitespace

EFFECTS:
- Subtle grain overlay (Retro 50)
- Hover glitch on name (Order 55 + tech context)
- Smooth scroll with slight parallax
```

**Phase 4: Signature Element**
```
Signature: The cursor leaves a fading trail of the accent color,
like a comet. Subtle, unexpected, memorable.
```

**Phase 5: Anti-Pattern Check**
```
✓ Not using Inter
✓ Not centered-everything layout
✓ Dark mode is custom, not just "bg-gray-900"
✓ The mint green accent is unusual
✓ The cursor trail is unique
✓ Layout breaks the grid intentionally
```

**Result: A one-of-a-kind design that couldn't be generated by "make me a developer portfolio."**
