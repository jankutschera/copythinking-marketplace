# Layout System

Grid patterns, spatial composition, and layout strategies.

---

## Core Philosophy

> "Unexpected layouts. Asymmetry. Overlap. Grid-breaking elements."

Layouts should be intentional, not default. Every spacing decision communicates hierarchy and guides the eye.

---

## Foundation: Container System

```css
:root {
  /* Container widths */
  --container-xs: 320px;   /* Mobile */
  --container-sm: 640px;   /* Small content */
  --container-md: 768px;   /* Medium content */
  --container-lg: 1024px;  /* Standard content */
  --container-xl: 1280px;  /* Wide content */
  --container-2xl: 1536px; /* Full width */

  /* Container padding */
  --container-padding: clamp(1rem, 5vw, 3rem);
}

.container {
  width: 100%;
  max-width: var(--container-xl);
  margin: 0 auto;
  padding: 0 var(--container-padding);
}

.container-narrow {
  max-width: var(--container-md);
}

.container-wide {
  max-width: var(--container-2xl);
}
```

---

## 12-Column Grid

### Basic Grid

```css
.grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: var(--grid-gap, 1.5rem);
}

/* Column spans */
.col-1 { grid-column: span 1; }
.col-2 { grid-column: span 2; }
.col-3 { grid-column: span 3; }
.col-4 { grid-column: span 4; }
.col-5 { grid-column: span 5; }
.col-6 { grid-column: span 6; }
.col-7 { grid-column: span 7; }
.col-8 { grid-column: span 8; }
.col-9 { grid-column: span 9; }
.col-10 { grid-column: span 10; }
.col-11 { grid-column: span 11; }
.col-12 { grid-column: span 12; }

/* Start positions */
.start-1 { grid-column-start: 1; }
.start-2 { grid-column-start: 2; }
.start-3 { grid-column-start: 3; }
.start-4 { grid-column-start: 4; }
/* ... etc */

/* Responsive */
@media (max-width: 768px) {
  .col-md-6 { grid-column: span 6; }
  .col-md-12 { grid-column: span 12; }
}

@media (max-width: 640px) {
  .col-sm-12 { grid-column: span 12; }
}
```

### Grid Usage Examples

```html
<!-- Two column 50/50 -->
<div class="grid">
  <div class="col-6">Left</div>
  <div class="col-6">Right</div>
</div>

<!-- Sidebar layout -->
<div class="grid">
  <main class="col-8">Main content</main>
  <aside class="col-4">Sidebar</aside>
</div>

<!-- Three columns -->
<div class="grid">
  <div class="col-4">One</div>
  <div class="col-4">Two</div>
  <div class="col-4">Three</div>
</div>

<!-- Offset content -->
<div class="grid">
  <div class="col-8 start-3">Centered content (starts at column 3)</div>
</div>
```

---

## Asymmetric Layouts

### Golden Ratio Split (1:1.618)

```css
.golden-split {
  display: grid;
  grid-template-columns: 1fr 1.618fr;
  gap: 2rem;
}

.golden-split-reverse {
  display: grid;
  grid-template-columns: 1.618fr 1fr;
  gap: 2rem;
}
```

### Common Asymmetric Ratios

```css
/* 40/60 split */
.split-40-60 {
  display: grid;
  grid-template-columns: 2fr 3fr;
  gap: 2rem;
}

/* 30/70 split */
.split-30-70 {
  display: grid;
  grid-template-columns: 3fr 7fr;
  gap: 2rem;
}

/* 60/40 split */
.split-60-40 {
  display: grid;
  grid-template-columns: 3fr 2fr;
  gap: 2rem;
}
```

### Editorial Offset

```css
.editorial-layout {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  gap: 2rem;
}

.editorial-layout > .main {
  grid-column: 2;
}

.editorial-layout > .aside {
  grid-column: 3;
  position: sticky;
  top: 2rem;
  height: fit-content;
}

/* Full-bleed breakout */
.editorial-layout > .full-bleed {
  grid-column: 1 / -1;
}
```

---

## Bento Grid

### Classic Bento

```css
.bento-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(180px, auto);
  gap: 1rem;
}

.bento-item { }
.bento-item.wide { grid-column: span 2; }
.bento-item.tall { grid-row: span 2; }
.bento-item.large { grid-column: span 2; grid-row: span 2; }

@media (max-width: 768px) {
  .bento-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  .bento-grid {
    grid-template-columns: 1fr;
  }

  .bento-item.wide,
  .bento-item.large {
    grid-column: span 1;
  }
}
```

### Bento Layout Example

```html
<div class="bento-grid">
  <div class="bento-item large">Featured</div>
  <div class="bento-item">Item 2</div>
  <div class="bento-item">Item 3</div>
  <div class="bento-item wide">Wide item</div>
  <div class="bento-item tall">Tall item</div>
  <div class="bento-item">Item 6</div>
</div>
```

### Named Grid Areas

```css
.bento-named {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(3, 200px);
  gap: 1rem;
  grid-template-areas:
    "featured featured stats stats"
    "featured featured chart chart"
    "recent recent recent notifications";
}

.featured { grid-area: featured; }
.stats { grid-area: stats; }
.chart { grid-area: chart; }
.recent { grid-area: recent; }
.notifications { grid-area: notifications; }
```

---

## CSS Masonry

### Column-Based Masonry

```css
.masonry {
  columns: 3;
  column-gap: 1.5rem;
}

.masonry-item {
  break-inside: avoid;
  margin-bottom: 1.5rem;
}

@media (max-width: 768px) {
  .masonry {
    columns: 2;
  }
}

@media (max-width: 480px) {
  .masonry {
    columns: 1;
  }
}
```

### Grid Masonry (Experimental)

```css
/* Future CSS - currently limited support */
.masonry-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: masonry;
  gap: 1.5rem;
}
```

---

## Overlap Patterns

### Layered Cards

```css
.layered-stack {
  position: relative;
  padding: 3rem;
}

.layered-stack > *:nth-child(1) {
  position: relative;
  z-index: 3;
}

.layered-stack > *:nth-child(2) {
  position: absolute;
  top: 0.5rem;
  left: 0.5rem;
  right: -0.5rem;
  bottom: -0.5rem;
  z-index: 2;
  opacity: 0.6;
}

.layered-stack > *:nth-child(3) {
  position: absolute;
  top: 1rem;
  left: 1rem;
  right: -1rem;
  bottom: -1rem;
  z-index: 1;
  opacity: 0.3;
}
```

### Overlapping Images

```css
.overlap-gallery {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: repeat(6, 1fr);
}

.overlap-gallery > img:nth-child(1) {
  grid-column: 1 / 8;
  grid-row: 1 / 5;
  z-index: 1;
}

.overlap-gallery > img:nth-child(2) {
  grid-column: 6 / 13;
  grid-row: 3 / 7;
  z-index: 2;
}
```

### Text Over Image

```css
.text-overlap {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
}

.text-overlap .image {
  grid-column: 1 / 3;
  grid-row: 1;
}

.text-overlap .content {
  grid-column: 2;
  grid-row: 1;
  padding: 3rem;
  background: var(--bg-primary);
  margin-left: -4rem;
  z-index: 1;
}
```

---

## Section Patterns

### Diagonal Break

```css
.diagonal-section {
  position: relative;
  padding: 6rem 0;
  background: var(--bg-secondary);
}

.diagonal-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 100px;
  background: var(--bg-primary);
  clip-path: polygon(0 0, 100% 0, 100% 0%, 0 100%);
}

.diagonal-section::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100px;
  background: var(--bg-primary);
  clip-path: polygon(0 100%, 100% 0%, 100% 100%, 0 100%);
}
```

### Wave Break

```css
.wave-section {
  position: relative;
  padding: 6rem 0;
}

.wave-section::before {
  content: '';
  position: absolute;
  top: -50px;
  left: 0;
  right: 0;
  height: 100px;
  background: var(--bg-primary);
  clip-path: ellipse(60% 100% at 50% 100%);
}
```

### Alternating Sections

```css
.section {
  padding: 6rem 0;
}

.section:nth-child(even) {
  background: var(--bg-secondary);
}

.section:nth-child(odd) {
  background: var(--bg-primary);
}
```

---

## Negative Space Patterns

### Breathable Content

```css
.breathable {
  max-width: 65ch; /* Optimal reading width */
  margin: 6rem auto;
  padding: 0 1.5rem;
}

.breathable > * + * {
  margin-top: 1.5rem;
}

.breathable > h2 {
  margin-top: 3rem;
}

.breathable > blockquote {
  margin: 2.5rem 0;
  padding-left: 1.5rem;
  border-left: 3px solid var(--accent-primary);
}
```

### Generous Sections

```css
.spacious-section {
  padding: clamp(4rem, 10vw, 8rem) 0;
}

.spacious-section > * + * {
  margin-top: clamp(2rem, 5vw, 4rem);
}
```

### Minimalist Card Grid

```css
.minimal-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 3rem; /* Generous gap */
}

.minimal-card {
  padding: 2rem;
  /* No border, minimal styling - space is the design */
}
```

---

## Responsive Strategies

### Mobile-First Breakpoints

```css
/* Base: Mobile */
.layout {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

/* Tablet */
@media (min-width: 640px) {
  .layout {
    flex-direction: row;
    gap: 1.5rem;
  }
}

/* Desktop */
@media (min-width: 1024px) {
  .layout {
    gap: 2rem;
  }
}
```

### Container Queries (Modern)

```css
.card-container {
  container-type: inline-size;
}

.card {
  display: block;
}

@container (min-width: 400px) {
  .card {
    display: flex;
    gap: 1rem;
  }
}

@container (min-width: 600px) {
  .card {
    gap: 2rem;
  }
}
```

### Fluid Spacing

```css
:root {
  --space-fluid-sm: clamp(0.75rem, 2vw, 1rem);
  --space-fluid-md: clamp(1.5rem, 4vw, 2.5rem);
  --space-fluid-lg: clamp(2rem, 6vw, 4rem);
  --space-fluid-xl: clamp(3rem, 10vw, 6rem);
}
```

---

## Quick Reference

### Common Layout Patterns

| Pattern | Use Case |
|---------|----------|
| 50/50 Split | Comparison, before/after |
| 60/40 Split | Content + sidebar |
| Golden Ratio | Editorial, hero |
| Centered Narrow | Long-form content |
| Full Bleed | Impact sections |
| Bento Grid | Feature showcase |
| Masonry | Gallery, portfolio |

### Spacing Guidelines

| Element | Spacing |
|---------|---------|
| Section padding | 4-8rem vertical |
| Card gap | 1-2rem |
| Content max-width | 65ch (prose) |
| Grid gap | 1.5-2rem |
| Component margin | 1-2rem |

### Breakpoint Reference

| Name | Width | Target |
|------|-------|--------|
| sm | 640px | Large phone |
| md | 768px | Tablet |
| lg | 1024px | Laptop |
| xl | 1280px | Desktop |
| 2xl | 1536px | Large screen |
