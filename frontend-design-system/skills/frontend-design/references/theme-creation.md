# Theme Creation Framework

Build unique themes for every project. No templates. No presets. Only principles.

## Core Philosophy

> "No design should be the same."

Every theme is created fresh for its specific context. We don't pick from a list - we build themes layer by layer based on:
- Project context (audience, purpose, mood)
- Live inspiration (extracted principles)
- Intentional creative direction

---

## The 5-Layer Theme Architecture

```
Layer 5: Personality    ← What makes it UNIQUE (signature element)
Layer 4: Effects        ← Shadows, transitions, easings
Layer 3: Typography     ← Font stack + type scale
Layer 2: Colors         ← Semantic token system
Layer 1: Foundation     ← Spacing scale, radii, base units
```

Build bottom-up. Each layer builds on the previous.

---

## Layer 1: Foundation

The mathematical base of your design system.

### Spacing Scale (8px base recommended)

```css
:root {
  --space-0: 0;
  --space-1: 0.25rem;   /* 4px */
  --space-2: 0.5rem;    /* 8px */
  --space-3: 0.75rem;   /* 12px */
  --space-4: 1rem;      /* 16px */
  --space-5: 1.25rem;   /* 20px */
  --space-6: 1.5rem;    /* 24px */
  --space-8: 2rem;      /* 32px */
  --space-10: 2.5rem;   /* 40px */
  --space-12: 3rem;     /* 48px */
  --space-16: 4rem;     /* 64px */
  --space-20: 5rem;     /* 80px */
  --space-24: 6rem;     /* 96px */
  --space-32: 8rem;     /* 128px */
}
```

### Border Radius Scale

```css
:root {
  --radius-none: 0;
  --radius-sm: 0.25rem;    /* 4px - subtle */
  --radius-md: 0.5rem;     /* 8px - default */
  --radius-lg: 1rem;       /* 16px - prominent */
  --radius-xl: 1.5rem;     /* 24px - card-like */
  --radius-2xl: 2rem;      /* 32px - very rounded */
  --radius-full: 9999px;   /* pills, circles */
}
```

### Foundation Decisions

| Decision | Options | Impact |
|----------|---------|--------|
| Base unit | 4px, 8px, 10px | Affects all spacing math |
| Radius character | Sharp (0-4px), Soft (8-16px), Round (16px+) | Sets visual tone |
| Density | Spacious (larger scale), Dense (smaller scale) | Content feel |

**Example Foundations:**

```css
/* Brutalist Foundation */
--radius-default: 0;
--space-base: 8px;
/* Sharp, mathematical */

/* Soft/Organic Foundation */
--radius-default: 1rem;
--space-base: 8px;
/* Rounded, approachable */

/* Dense Dashboard Foundation */
--radius-default: 0.375rem;
--space-base: 4px;
/* Compact, information-dense */
```

---

## Layer 2: Colors

Semantic tokens, not arbitrary colors.

### Token Structure

```css
:root {
  /* === BACKGROUNDS === */
  --bg-primary: ;      /* Main page background */
  --bg-secondary: ;    /* Secondary sections */
  --bg-tertiary: ;     /* Nested elements */
  --bg-inverse: ;      /* Inverted sections */

  /* === SURFACES === */
  --surface-1: ;       /* Cards, modals */
  --surface-2: ;       /* Elevated cards */
  --surface-3: ;       /* Highest elevation */

  /* === TEXT === */
  --text-primary: ;    /* Main content */
  --text-secondary: ;  /* Supporting text */
  --text-tertiary: ;   /* Muted text */
  --text-inverse: ;    /* On dark backgrounds */

  /* === ACCENTS === */
  --accent-primary: ;     /* Main brand/action color */
  --accent-secondary: ;   /* Supporting accent */
  --accent-muted: ;       /* Subtle accent (backgrounds) */

  /* === BORDERS === */
  --border-default: ;  /* Standard borders */
  --border-muted: ;    /* Subtle borders */
  --border-strong: ;   /* Emphasized borders */

  /* === SEMANTIC === */
  --success: ;
  --warning: ;
  --error: ;
  --info: ;

  /* === INTERACTIVE === */
  --interactive-default: ;
  --interactive-hover: ;
  --interactive-pressed: ;
  --interactive-disabled: ;
}
```

### Color Decisions

| Decision | Options | Mood Created |
|----------|---------|--------------|
| Base | Light bg + dark text, Dark bg + light text | Fundamental feel |
| Temperature | Warm undertones, Cool undertones, Neutral | Emotional resonance |
| Contrast | High (vibrant), Medium (balanced), Low (subtle) | Energy level |
| Saturation | Saturated accents, Muted palette, Mixed | Visual intensity |

### Color Relationship Patterns

```
MONOCHROMATIC
Single hue, vary lightness/saturation
→ Sophisticated, unified

COMPLEMENTARY
Opposite hues (blue/orange, purple/yellow)
→ High contrast, energetic

ANALOGOUS
Adjacent hues (blue/teal/green)
→ Harmonious, natural

SPLIT-COMPLEMENTARY
One hue + two adjacent to its complement
→ Tension with safety

TRIADIC
Three evenly spaced hues
→ Balanced, playful
```

### Building a Palette

1. **Start with mood**: What emotion should the interface evoke?
2. **Choose base**: Light or dark? Warm or cool?
3. **Pick accent**: What color will draw attention?
4. **Build relationships**: How do colors interact?
5. **Test contrast**: Ensure accessibility (4.5:1 for text)

---

## Layer 3: Typography

Font stack + type scale.

### Font Stack Structure

```css
:root {
  /* Font Families */
  --font-display: 'Font Name', fallback, sans-serif;
  --font-body: 'Font Name', fallback, sans-serif;
  --font-mono: 'Font Name', fallback, monospace;

  /* Type Scale (1.25 ratio example) */
  --text-xs: 0.75rem;     /* 12px */
  --text-sm: 0.875rem;    /* 14px */
  --text-base: 1rem;      /* 16px */
  --text-lg: 1.125rem;    /* 18px */
  --text-xl: 1.25rem;     /* 20px */
  --text-2xl: 1.5rem;     /* 24px */
  --text-3xl: 1.875rem;   /* 30px */
  --text-4xl: 2.25rem;    /* 36px */
  --text-5xl: 3rem;       /* 48px */
  --text-6xl: 3.75rem;    /* 60px */
  --text-7xl: 4.5rem;     /* 72px */

  /* Line Heights */
  --leading-none: 1;
  --leading-tight: 1.25;
  --leading-snug: 1.375;
  --leading-normal: 1.5;
  --leading-relaxed: 1.625;
  --leading-loose: 2;

  /* Letter Spacing */
  --tracking-tighter: -0.05em;
  --tracking-tight: -0.025em;
  --tracking-normal: 0;
  --tracking-wide: 0.025em;
  --tracking-wider: 0.05em;
  --tracking-widest: 0.1em;
}
```

### Typography Decisions

| Decision | Options | Effect |
|----------|---------|--------|
| Display character | Serif (traditional), Sans (modern), Display (unique) | Sets tone |
| Body character | Serif (editorial), Sans (clean), Hybrid | Readability + feel |
| Scale ratio | 1.2 (tight), 1.25 (default), 1.333 (dramatic) | Hierarchy drama |
| Weight range | Light to Bold, Single weight, Heavy contrast | Visual rhythm |

### Font Selection from `font-index.json`

Reference `assets/fonts/font-index.json` for curated options:
- **Display fonts**: Headlines, hero text
- **Body fonts**: Long-form content
- **Accent fonts**: Special elements
- **Mono fonts**: Code, data

Use the `pairings` section for tested combinations.

---

## Layer 4: Effects

Shadows, transitions, and visual polish.

### Shadow Scale

```css
:root {
  /* Shadows - adjust color for theme */
  --shadow-color: 220 3% 15%;  /* HSL without alpha */

  --shadow-xs: 0 1px 2px hsl(var(--shadow-color) / 0.05);
  --shadow-sm: 0 1px 3px hsl(var(--shadow-color) / 0.1),
               0 1px 2px hsl(var(--shadow-color) / 0.06);
  --shadow-md: 0 4px 6px hsl(var(--shadow-color) / 0.1),
               0 2px 4px hsl(var(--shadow-color) / 0.06);
  --shadow-lg: 0 10px 15px hsl(var(--shadow-color) / 0.1),
               0 4px 6px hsl(var(--shadow-color) / 0.05);
  --shadow-xl: 0 20px 25px hsl(var(--shadow-color) / 0.1),
               0 10px 10px hsl(var(--shadow-color) / 0.04);
  --shadow-2xl: 0 25px 50px hsl(var(--shadow-color) / 0.25);

  /* Inner shadow for depth */
  --shadow-inner: inset 0 2px 4px hsl(var(--shadow-color) / 0.06);
}
```

### Transition Timing

```css
:root {
  /* Durations */
  --duration-instant: 50ms;
  --duration-fast: 150ms;
  --duration-normal: 250ms;
  --duration-slow: 400ms;
  --duration-slower: 600ms;

  /* Easings */
  --ease-linear: linear;
  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
  --ease-in-out: cubic-bezier(0.4, 0, 0.2, 1);

  /* Expressive easings */
  --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-out-back: cubic-bezier(0.34, 1.56, 0.64, 1);
  --ease-out-quart: cubic-bezier(0.25, 1, 0.5, 1);

  /* Default transition */
  --transition-default: var(--duration-normal) var(--ease-out);
}
```

### Effects Decisions

| Decision | Options | Feel |
|----------|---------|------|
| Shadow style | Soft (blur), Hard (no blur), Colored | Depth character |
| Animation speed | Fast (snappy), Normal, Slow (deliberate) | Energy |
| Easing character | Linear (mechanical), Smooth (natural), Bouncy (playful) | Personality |
| Hover intensity | Subtle (professional), Medium (engaging), Dramatic (expressive) | Interaction feel |

---

## Layer 5: Personality

**The most important layer.** What makes this theme UNIQUE?

### Personality Questions

Answer these before finalizing:

1. **What's the signature element?**
   - A specific color that's memorable
   - An unusual font choice
   - A distinctive animation style
   - A unique texture or pattern

2. **Would someone recognize this?**
   - If you showed someone two designs, could they tell this is yours?
   - What would they remember the next day?

3. **What breaks the expected?**
   - Where do you deviate from the "safe" choice?
   - What's surprising but intentional?

### Personality Patterns

```
SIGNATURE COLOR
One distinctive color used consistently
→ "That brand always uses that coral"

DISTINCTIVE TYPOGRAPHY
Unusual but intentional font choice
→ "That site with the Art Deco headlines"

MOTION CHARACTER
Specific animation style
→ "Everything bounces slightly on that app"

TEXTURE/PATTERN
Consistent visual texture
→ "The site with the subtle grain overlay"

SPATIAL RHYTHM
Distinctive spacing pattern
→ "The site with so much breathing room"
```

### Personality Examples

```css
/* Brutalist Joy - Personality */
--personality-shadow: 4px 4px 0 var(--border-strong); /* Hard shadows */
--personality-border: 3px solid var(--border-strong); /* Thick borders */
/* Signature: Hard shadows + chunky borders + warm accent */

/* Editorial Luxe - Personality */
--personality-letter-spacing: 0.15em; /* Wide tracking on caps */
--personality-transition: 600ms var(--ease-out-expo); /* Slow, elegant */
/* Signature: Elegant timing + refined typography */

/* Playful Tech - Personality */
--personality-radius: 2rem; /* Very rounded */
--personality-bounce: cubic-bezier(0.34, 1.56, 0.64, 1);
/* Signature: Bouncy animations + pill shapes */
```

---

## Theme Creation Workflow

### 1. Context Gathering

```
Questions to answer:
- Who is the audience? (age, expertise, expectations)
- What's the product/purpose?
- What mood should it convey?
- Any brand constraints?
- Dark or light preference?
```

### 2. Inspiration Phase

```
1. Select 2-3 sources from inspiration-sources.md
2. Fetch examples matching context
3. Analyze using the framework
4. Extract principles (not pixels)
```

### 3. Decision Documentation

For each layer, document your decision:

```markdown
## Theme Decisions: [Project Name]

### Foundation
- Base unit: 8px
- Radius character: Soft (8-16px default)
- Density: Standard
- Reasoning: SaaS product needs approachable feel

### Colors
- Base: Light with warm undertones
- Accent: Saturated teal (#0D9488)
- Approach: High contrast for CTAs
- Reasoning: Trust + action

### Typography
- Display: Clash Display (bold, modern)
- Body: Outfit (clean, readable)
- Scale: 1.25 ratio
- Reasoning: Tech-forward but friendly

### Effects
- Shadows: Soft, minimal
- Transitions: Fast (150ms), smooth easing
- Reasoning: Professional, not distracting

### Personality
- Signature: The teal accent is highly saturated against muted backgrounds
- Memorable: Bold headlines + refined body creates tension
- Unexpected: Using a display font for a B2B product
```

### 4. Implementation

Build the CSS custom properties following the structure above.

### 5. Validation Checklist

- [ ] Each layer is defined with intention
- [ ] Personality layer has a clear "signature"
- [ ] Color contrast is accessible (4.5:1 minimum)
- [ ] Typography hierarchy is clear
- [ ] Design doesn't look like "any website"
- [ ] Theme serves the specific context

---

## Anti-Patterns

### What NOT to do:

```
GENERIC:
- Using default Tailwind colors
- Not defining a personality layer
- "Safe" choices throughout
- Could-be-any-website result

INCONSISTENT:
- Mixing incompatible aesthetics
- Random radius/spacing values
- No clear design language

COPY-PASTE:
- Taking an entire theme from inspiration
- Using exact colors from other sites
- No adaptation to context
```

### What TO do:

```
INTENTIONAL:
- Every decision serves the context
- Clear reasoning for each choice
- Consistent design language

DISTINCTIVE:
- At least one memorable element
- Something unexpected but fitting
- Would be recognized as unique

ADAPTED:
- Principles from inspiration, not pixels
- Context-specific execution
- Original creative direction
```

---

## Quick Theme Starters

### If you're stuck, start here:

**Warm & Friendly**
- Foundation: Soft radii, standard spacing
- Colors: Warm light bg, earth accent
- Typography: Rounded sans + humanist body
- Effects: Soft shadows, smooth transitions
- Personality: Warm color temperature throughout

**Cool & Professional**
- Foundation: Medium radii, standard spacing
- Colors: Cool neutrals, blue accent
- Typography: Geometric sans + clean body
- Effects: Subtle shadows, fast transitions
- Personality: Precise, mathematical feel

**Bold & Creative**
- Foundation: Mixed radii (sharp + round), generous spacing
- Colors: High contrast, saturated accent
- Typography: Strong display + versatile body
- Effects: Hard shadows or none, bouncy transitions
- Personality: One dramatic element (color, type, or motion)

**Minimal & Refined**
- Foundation: Subtle radii, generous spacing
- Colors: Muted palette, single accent
- Typography: Elegant serif or refined sans
- Effects: Barely-there shadows, slow transitions
- Personality: Restraint as the signature
