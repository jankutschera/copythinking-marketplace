# Color System

Build semantic, intentional color systems. No random hex codes.

---

## Anti-Patterns (Never Do)

```
OVERUSED AI AESTHETICS:
- Purple/violet gradients on white (#7C3AED → #A855F7)
- Blue-purple-pink generative gradients
- Generic teal + coral combinations
- Low-contrast gray-on-white text
- Rainbow accessibility violations

DEFAULT FRAMEWORK COLORS:
- Tailwind's default blue-500
- Bootstrap's primary blue
- Any "out of the box" palette

MEANINGLESS CHOICES:
- Colors without semantic purpose
- Random accent colors
- Inconsistent usage across components
```

---

## Semantic Token Architecture

### Complete Token System

```css
:root {
  /* ========================================
     BACKGROUNDS
     ======================================== */
  --bg-primary: ;        /* Main page background */
  --bg-secondary: ;      /* Alternate sections */
  --bg-tertiary: ;       /* Nested/deeper elements */
  --bg-inverse: ;        /* Inverted (dark on light, light on dark) */

  /* ========================================
     SURFACES (Cards, Modals, Popovers)
     ======================================== */
  --surface-1: ;         /* Default card/modal */
  --surface-2: ;         /* Elevated surface */
  --surface-3: ;         /* Highest elevation */

  /* ========================================
     TEXT
     ======================================== */
  --text-primary: ;      /* Main content (high contrast) */
  --text-secondary: ;    /* Supporting text */
  --text-tertiary: ;     /* Muted/helper text */
  --text-disabled: ;     /* Disabled state */
  --text-inverse: ;      /* On inverse backgrounds */
  --text-on-accent: ;    /* On accent color backgrounds */

  /* ========================================
     BRAND / ACCENT
     ======================================== */
  --accent-primary: ;       /* Main brand/action color */
  --accent-primary-hover: ; /* Hover state */
  --accent-primary-active: ;/* Active/pressed state */
  --accent-secondary: ;     /* Supporting accent */
  --accent-muted: ;         /* Subtle accent for backgrounds */

  /* ========================================
     BORDERS
     ======================================== */
  --border-default: ;    /* Standard borders */
  --border-muted: ;      /* Subtle borders */
  --border-strong: ;     /* Emphasized borders */
  --border-focus: ;      /* Focus ring color */

  /* ========================================
     SEMANTIC / FEEDBACK
     ======================================== */
  --success: ;           /* Positive actions, confirmations */
  --success-muted: ;     /* Success backgrounds */
  --warning: ;           /* Cautions, attention needed */
  --warning-muted: ;     /* Warning backgrounds */
  --error: ;             /* Errors, destructive */
  --error-muted: ;       /* Error backgrounds */
  --info: ;              /* Informational */
  --info-muted: ;        /* Info backgrounds */

  /* ========================================
     INTERACTIVE STATES
     ======================================== */
  --interactive-default: ;
  --interactive-hover: ;
  --interactive-pressed: ;
  --interactive-disabled: ;
  --interactive-focus-ring: ;
}
```

---

## Color Relationships

### Monochromatic

Single hue with varying saturation and lightness.

```css
/* Example: Blue monochromatic */
--blue-50: hsl(210, 100%, 97%);
--blue-100: hsl(210, 100%, 94%);
--blue-200: hsl(210, 100%, 86%);
--blue-300: hsl(210, 100%, 74%);
--blue-400: hsl(210, 100%, 62%);
--blue-500: hsl(210, 100%, 50%);  /* Base */
--blue-600: hsl(210, 100%, 42%);
--blue-700: hsl(210, 100%, 34%);
--blue-800: hsl(210, 100%, 26%);
--blue-900: hsl(210, 100%, 18%);
--blue-950: hsl(210, 100%, 10%);
```

**Best for:** Sophisticated, unified designs. Luxury, editorial.

### Complementary

Opposite hues on the color wheel.

```
Blue (#3B82F6) ↔ Orange (#F97316)
Purple (#8B5CF6) ↔ Yellow (#EAB308)
Green (#22C55E) ↔ Red (#EF4444)
Teal (#14B8A6) ↔ Coral (#F43F5E)
```

**Best for:** High energy, call-to-action emphasis.

### Analogous

Adjacent hues (neighbors on the wheel).

```
Blue → Teal → Green
Purple → Blue → Teal
Orange → Yellow → Green
Red → Orange → Yellow
```

**Best for:** Harmonious, natural-feeling designs.

### Split-Complementary

One hue + two colors adjacent to its complement.

```
Blue + Yellow-Orange + Red-Orange
Purple + Yellow-Green + Yellow-Orange
```

**Best for:** Dynamic but balanced designs.

---

## Building a Palette

### Step 1: Define the Base

```
LIGHT BASE                    DARK BASE
--bg-primary: near-white      --bg-primary: near-black
--text-primary: near-black    --text-primary: near-white
```

### Step 2: Choose Temperature

```
WARM                          COOL                         NEUTRAL
Cream whites (#FAF9F5)        Blue-whites (#F8FAFC)       Pure grays (#FAFAFA)
Warm grays (#78716C)          Cool grays (#64748B)        True grays (#737373)
Earth tones                   Ocean tones                  Stone tones
```

### Step 3: Pick Accent Strategy

```
SINGLE ACCENT (Safest)
One strong color for all CTAs
Everything else neutral

DUAL ACCENT (Balanced)
Primary: Main actions
Secondary: Supporting actions

MULTI-ACCENT (Advanced)
Multiple semantic colors
Requires careful balance
```

### Step 4: Build the Scale

For each color, create a scale:

```css
/* Generate a 11-stop scale */
--color-50:  /* Lightest - backgrounds */
--color-100: /* Light backgrounds */
--color-200: /* Muted */
--color-300: /* Borders on light */
--color-400: /* Muted text on light */
--color-500: /* Base color */
--color-600: /* Hover states */
--color-700: /* Active states */
--color-800: /* Text on dark */
--color-900: /* High contrast */
--color-950: /* Darkest - backgrounds */
```

---

## Contrast Guidelines

### Minimum Ratios (WCAG AA)

| Element | Ratio | Check |
|---------|-------|-------|
| Body text | 4.5:1 | `--text-primary` vs `--bg-primary` |
| Large text (18px+) | 3:1 | Headlines |
| UI components | 3:1 | Buttons, inputs, icons |
| Decorative | No minimum | Borders, shadows |

### Quick Contrast Reference

```
ON WHITE (#FFFFFF):
- #000000 = 21:1 (max)
- #171717 = 17.4:1 (excellent)
- #404040 = 9.7:1 (great)
- #737373 = 4.6:1 (minimum body)
- #A3A3A3 = 2.6:1 (large text only)

ON BLACK (#000000):
- #FFFFFF = 21:1 (max)
- #E5E5E5 = 16.8:1 (excellent)
- #A3A3A3 = 7.6:1 (great)
- #737373 = 4.5:1 (minimum body)
```

---

## Example Palettes

### Warm Earth

```css
:root {
  /* Best for: Craft, organic, wellness, food */
  --bg-primary: #FAF7F2;
  --bg-secondary: #F5F0E8;
  --surface-1: #FFFFFF;
  --text-primary: #1C1917;
  --text-secondary: #57534E;
  --accent-primary: #B45309;  /* Amber */
  --accent-muted: #FEF3C7;
  --border-default: #E7E5E4;
}
```

### Cool Tech

```css
:root {
  /* Best for: SaaS, fintech, enterprise */
  --bg-primary: #F8FAFC;
  --bg-secondary: #F1F5F9;
  --surface-1: #FFFFFF;
  --text-primary: #0F172A;
  --text-secondary: #475569;
  --accent-primary: #0EA5E9;  /* Sky blue */
  --accent-muted: #E0F2FE;
  --border-default: #E2E8F0;
}
```

### Dark Minimal

```css
:root {
  /* Best for: Creative, portfolio, luxury */
  --bg-primary: #0A0A0A;
  --bg-secondary: #171717;
  --surface-1: #1C1C1C;
  --text-primary: #FAFAFA;
  --text-secondary: #A3A3A3;
  --accent-primary: #FFFFFF;  /* White as accent */
  --accent-muted: #262626;
  --border-default: #262626;
}
```

### Vibrant Creative

```css
:root {
  /* Best for: Agency, creative, entertainment */
  --bg-primary: #FAFAFA;
  --bg-secondary: #F5F5F5;
  --surface-1: #FFFFFF;
  --text-primary: #09090B;
  --text-secondary: #52525B;
  --accent-primary: #7C3AED;  /* Violet */
  --accent-secondary: #EC4899; /* Pink */
  --accent-muted: #F3E8FF;
  --border-default: #E4E4E7;
}
```

### Soft Sage

```css
:root {
  /* Best for: Wellness, lifestyle, eco */
  --bg-primary: #F9FAF8;
  --bg-secondary: #F3F4F1;
  --surface-1: #FFFFFF;
  --text-primary: #1A1D1A;
  --text-secondary: #4B524B;
  --accent-primary: #5F8D4E;  /* Sage green */
  --accent-muted: #E8F0E4;
  --border-default: #DFE2DB;
}
```

---

## Dark Mode Strategy

### Approach 1: Invert + Adjust

```css
:root {
  --bg-primary: #FFFFFF;
  --text-primary: #171717;
  --accent-primary: #2563EB;
}

[data-theme="dark"] {
  --bg-primary: #0A0A0A;
  --text-primary: #FAFAFA;
  --accent-primary: #3B82F6;  /* Lighter for dark bg */
}
```

### Approach 2: Semantic Persistence

Keep semantic meaning, adjust values:

```css
:root {
  --success: #16A34A;  /* Green */
  --error: #DC2626;    /* Red */
}

[data-theme="dark"] {
  --success: #22C55E;  /* Lighter green */
  --error: #EF4444;    /* Lighter red */
}
```

### Key Dark Mode Adjustments

1. **Reduce contrast slightly** - Pure white (#FFF) on pure black (#000) is harsh
2. **Lighten accent colors** - Dark backgrounds need brighter accents
3. **Adjust semantic colors** - Success/error may need more saturation
4. **Soften borders** - Dark borders on dark bg should be subtle

---

## Color Usage Patterns

### Button States

```css
.btn-primary {
  background: var(--accent-primary);
  color: var(--text-on-accent);
}
.btn-primary:hover {
  background: var(--accent-primary-hover);
}
.btn-primary:active {
  background: var(--accent-primary-active);
}
.btn-primary:disabled {
  background: var(--interactive-disabled);
  color: var(--text-disabled);
}
```

### Card Elevation

```css
.card { background: var(--surface-1); }
.card-elevated { background: var(--surface-2); }
.card-floating { background: var(--surface-3); }
```

### Status Indicators

```css
.badge-success {
  background: var(--success-muted);
  color: var(--success);
}
.badge-error {
  background: var(--error-muted);
  color: var(--error);
}
```

---

## Quick Reference

### Color Psychology

| Color | Associations | Use For |
|-------|--------------|---------|
| Blue | Trust, stability, tech | Finance, enterprise, SaaS |
| Green | Growth, health, nature | Eco, wellness, success states |
| Purple | Creativity, luxury | Creative, premium |
| Orange | Energy, warmth, action | CTAs, attention |
| Red | Urgency, passion, danger | Errors, important actions |
| Yellow | Optimism, attention | Warnings, highlights |
| Pink | Playful, modern | Lifestyle, creative |
| Teal | Balance, sophistication | Healthcare, modern brands |

### Temperature Guide

```
WARMER ← → COOLER

Warm Whites:     #FAF9F5, #FFFBEB, #FEF3C7
Neutral Whites:  #FAFAFA, #F5F5F5, #E5E5E5
Cool Whites:     #F8FAFC, #F1F5F9, #E2E8F0
```
