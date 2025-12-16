# Live Inspiration Sources

This guide enables dynamic design inspiration through live scraping of curated design galleries.

## Core Philosophy

**Don't pick from templates. Extract principles from the best.**

Every design request gets fresh inspiration from current, award-winning work. This ensures:
- Designs stay current with trends
- No two projects look the same
- Principles are adapted, not copied

---

## Curated Sources

### Tier 1: General Inspiration (Start Here)

| Source | URL | Best For | Scraping Quality |
|--------|-----|----------|------------------|
| **Aura** | https://www.aura.build/ | Modern landing pages, SaaS, startups | Excellent |
| **Godly** | https://godly.website/ | Cutting-edge web design | Excellent |
| **Awwwards** | https://www.awwwards.com/websites/ | Award-winning, high production | Good |
| **Siteinspire** | https://www.siteinspire.com/ | Minimal, editorial, clean | Good |
| **Land-book** | https://land-book.com/ | Landing pages specifically | Excellent |

### Tier 2: Specialized Galleries

| Source | URL | Specialty |
|--------|-----|-----------|
| **Refero** | https://refero.design/ | SaaS & product design |
| **Mobbin** | https://mobbin.com/browse/web | UI patterns & flows |
| **Minimal Gallery** | https://minimal.gallery/ | Minimalist designs |
| **Brutalist Websites** | https://brutalistwebsites.com/ | Brutalist aesthetic |
| **One Page Love** | https://onepagelove.com/ | Single-page designs |
| **SaaS Landing Page** | https://saaslandingpage.com/ | SaaS-specific patterns |
| **Lapa Ninja** | https://www.lapa.ninja/ | Landing page inspiration |

### Tier 3: Component-Specific

| Component | Source | URL |
|-----------|--------|-----|
| Pricing Pages | Pricing Pages | https://pricingpages.xyz/ |
| 404 Pages | 404 Gallery | https://404.gallery/ |
| Dark Mode | Dark Design | https://www.dark.design/ |
| Footers | Footer Design | https://www.footer.design/ |
| Hero Sections | Hero Examples | https://heroexamples.com/ |
| Forms | Form Design | https://www.reallygoodforms.com/ |

### Tier 4: Style-Specific

| Style | Source | URL |
|-------|--------|-----|
| Typography | Typewolf | https://www.typewolf.com/ |
| Colors | Happy Hues | https://www.happyhues.co/ |
| Gradients | UI Gradients | https://uigradients.com/ |
| Illustrations | Illustrations | https://undraw.co/illustrations |

---

## Scraping Workflow

### Step 1: Match Context to Source

```
User Request → Identify Keywords → Select Sources

Examples:
- "SaaS dashboard" → Refero, Aura, Mobbin
- "Fashion brand" → Awwwards, Siteinspire
- "Brutalist portfolio" → Brutalist Websites, Godly
- "Minimal landing page" → Minimal Gallery, Land-book
- "E-commerce" → Awwwards (filter: e-commerce), Mobbin
```

### Step 2: Fetch Examples

Use WebFetch with targeted prompts:

```
WebFetch URL: https://www.aura.build/
Prompt: "Show me the 5 most recent featured designs. For each, describe:
1. Visual style (colors, typography feel)
2. Layout approach (grid, asymmetric, etc.)
3. What makes it unique/memorable"
```

```
WebFetch URL: https://godly.website/
Prompt: "List the top designs on this page. For each:
1. Color palette description
2. Typography choices
3. Motion/animation approach
4. One unique design element"
```

### Step 3: Extract Principles (NOT Copy)

For each scraped design, document:

| Aspect | Questions to Answer |
|--------|---------------------|
| **Color Story** | Dominant color? Accent color? Light/dark? Contrast level? |
| **Type Pairing** | Display font character? Body font style? Hierarchy clarity? |
| **Motion** | Subtle or dramatic? Page load animation? Hover effects? |
| **Layout** | Grid-based or organic? Asymmetric? Use of whitespace? |
| **Signature Element** | What ONE thing makes this memorable? |

### Step 4: Synthesize for Your Design

Take the principles, NOT the pixels:

```
DON'T: "I'll use the same blue from that site"
DO: "That site uses a saturated primary + muted background. I'll apply that contrast principle."

DON'T: "I'll copy that hero layout"
DO: "That hero uses asymmetric 60/40 split. I'll use similar proportions with my own content."
```

---

## Scraping Prompts Library

### For General Inspiration

```
"Analyze the featured designs on this page. For each design, extract:
1. Overall aesthetic direction (minimal, bold, playful, etc.)
2. Color approach (palette, contrast, mood)
3. Typography style (serif/sans, weight usage)
4. Layout strategy (grid, freeform, asymmetric)
5. One standout creative choice"
```

### For Specific Components

```
"Show me examples of [hero sections / pricing tables / navigation / etc.] on this page.
For each, describe:
1. Visual hierarchy approach
2. Information density
3. Interactive elements
4. How it guides the eye"
```

### For Style Matching

```
"Find designs that feel [brutalist / luxurious / playful / minimal / etc.].
What visual elements create that feeling?
- Color choices
- Typography weight/style
- Spacing density
- Effect usage (shadows, gradients, textures)"
```

### For Technical Patterns

```
"Analyze how this site handles:
1. Responsive breakpoints
2. Animation timing
3. Component spacing
4. Color token usage"
```

---

## Analysis Framework

When you fetch a design, fill out this mental checklist:

### 1. First Impression (2 seconds)
- What's the MOOD?
- What's the ONE thing that stands out?
- Light or dark base?

### 2. Color Analysis
- [ ] Primary color (dominant)
- [ ] Secondary color (supporting)
- [ ] Accent color (calls to action)
- [ ] Background treatment (solid, gradient, texture?)
- [ ] Contrast ratio feel (high, medium, low)

### 3. Typography Analysis
- [ ] Display font category (serif, sans, display)
- [ ] Display font personality (bold, elegant, playful)
- [ ] Body font readability
- [ ] Size hierarchy (how many distinct sizes?)
- [ ] Weight usage (thin to bold range?)

### 4. Layout Analysis
- [ ] Grid system (12-col, custom, freeform?)
- [ ] Symmetry vs asymmetry
- [ ] White space density
- [ ] Content width (narrow, wide, full)
- [ ] Section rhythm (equal or varied?)

### 5. Motion Analysis
- [ ] Page load animation?
- [ ] Scroll-triggered effects?
- [ ] Hover states (subtle, dramatic?)
- [ ] Transition timing (fast, slow, bouncy?)

### 6. Unique Elements
- [ ] What would I remember tomorrow?
- [ ] What's the "signature move"?
- [ ] What breaks expected patterns?

---

## Anti-Patterns

### What NOT to do with inspiration:

```
COPYING:
- Taking exact colors hex codes
- Replicating layouts pixel-perfect
- Using the same font combinations
- Recreating specific animations

SHALLOW ANALYSIS:
- "It looks nice" (too vague)
- Noting only colors (missing principles)
- Ignoring the WHY behind choices
```

### What TO do:

```
PRINCIPLE EXTRACTION:
- "High contrast creates energy - I'll use that"
- "Asymmetric balance feels dynamic - I'll apply to my grid"
- "The subtle grain texture adds warmth - I'll add texture too"
- "Staggered animation creates rhythm - I'll time my reveals similarly"

ADAPTATION:
- Same principle, different execution
- Same structure, different aesthetics
- Same rhythm, different elements
```

---

## Quick Reference: Source Selection

```
I need inspiration for...

Landing Page → Aura, Land-book, SaaS Landing Page
Dashboard → Mobbin, Refero
Portfolio → Awwwards, Godly
E-commerce → Awwwards (commerce filter), Mobbin
Blog/Editorial → Siteinspire, Typewolf
SaaS Product → Refero, Aura
Mobile Web → Mobbin
Minimal Design → Minimal Gallery, Siteinspire
Bold/Experimental → Godly, Awwwards
Specific Component → Component-specific sources (see Tier 3)
```

---

## Example Workflow

**User Request:** "Build a landing page for an AI writing tool"

**Step 1: Select Sources**
- Primary: Aura (SaaS focus), Refero (product design)
- Secondary: Land-book (landing pages)

**Step 2: Fetch & Analyze**
```
WebFetch https://www.aura.build/
"Show AI or SaaS tool landing pages. For each:
- How do they communicate 'AI' visually?
- What creates trust/credibility?
- How is the product demo shown?"
```

**Step 3: Extract Principles**
- AI tools often use gradient accents (signals innovation)
- Trust built through social proof placement
- Product demos use floating UI mockups
- Dark modes feel more "tech"

**Step 4: Create Original Design**
- Use gradient principle → custom gradient in brand colors
- Social proof placement → adapt for our testimonials
- Floating UI concept → create our own product visualization
- Consider dark mode → test with our brand palette

**Result:** Original design inspired by principles, not copied from examples.
