# Motion Library

Ready-to-use animation patterns for distinctive interfaces.

---

## Philosophy

Motion should feel **purposeful**, not decorative.

Every animation communicates:
- **State change**: Something happened
- **Spatial relationship**: Where things are/go
- **Hierarchy**: What matters most
- **Personality**: Brand character

> "One well-orchestrated page load creates more delight than scattered micro-interactions."

---

## Foundation: Timing Variables

```css
:root {
  /* ========================================
     DURATIONS
     ======================================== */
  --duration-instant: 50ms;    /* Immediate feedback */
  --duration-fast: 150ms;      /* Micro-interactions */
  --duration-normal: 250ms;    /* Standard transitions */
  --duration-slow: 400ms;      /* Emphasis animations */
  --duration-slower: 600ms;    /* Dramatic entrances */
  --duration-slowest: 1000ms;  /* Hero animations */

  /* ========================================
     EASINGS - Natural Motion
     ======================================== */
  --ease-linear: linear;
  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
  --ease-in-out: cubic-bezier(0.4, 0, 0.2, 1);

  /* ========================================
     EASINGS - Expressive Motion
     ======================================== */
  /* Out Expo - Smooth deceleration, feels natural */
  --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);

  /* Out Quart - Slightly less dramatic than expo */
  --ease-out-quart: cubic-bezier(0.25, 1, 0.5, 1);

  /* Out Back - Slight overshoot, playful */
  --ease-out-back: cubic-bezier(0.34, 1.56, 0.64, 1);

  /* In Out Quart - Smooth both ends */
  --ease-in-out-quart: cubic-bezier(0.76, 0, 0.24, 1);

  /* Spring - Bouncy, energetic */
  --ease-spring: cubic-bezier(0.175, 0.885, 0.32, 1.275);

  /* ========================================
     DEFAULT TRANSITION
     ======================================== */
  --transition-default: var(--duration-normal) var(--ease-out);
}
```

---

## Page Load Animations

### Fade + Slide Up (Most Common)

```css
@keyframes fadeSlideUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-up {
  animation: fadeSlideUp 0.6s var(--ease-out-expo) forwards;
}

/* Usage with stagger */
.stagger-children > * {
  opacity: 0;
  animation: fadeSlideUp 0.6s var(--ease-out-expo) forwards;
}
.stagger-children > *:nth-child(1) { animation-delay: 0ms; }
.stagger-children > *:nth-child(2) { animation-delay: 75ms; }
.stagger-children > *:nth-child(3) { animation-delay: 150ms; }
.stagger-children > *:nth-child(4) { animation-delay: 225ms; }
.stagger-children > *:nth-child(5) { animation-delay: 300ms; }
.stagger-children > *:nth-child(6) { animation-delay: 375ms; }
```

### Scale + Fade

```css
@keyframes scaleIn {
  from {
    opacity: 0;
    transform: scale(0.95);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

.animate-scale-in {
  animation: scaleIn 0.4s var(--ease-out-expo) forwards;
}
```

### Clip Reveal (Hero Text)

```css
@keyframes clipReveal {
  from {
    clip-path: inset(0 100% 0 0);
  }
  to {
    clip-path: inset(0 0 0 0);
  }
}

.animate-clip-reveal {
  animation: clipReveal 0.8s var(--ease-out-expo) forwards;
}

/* Vertical reveal */
@keyframes clipRevealUp {
  from {
    clip-path: inset(100% 0 0 0);
  }
  to {
    clip-path: inset(0 0 0 0);
  }
}
```

### Blur In

```css
@keyframes blurIn {
  from {
    opacity: 0;
    filter: blur(10px);
  }
  to {
    opacity: 1;
    filter: blur(0);
  }
}

.animate-blur-in {
  animation: blurIn 0.6s var(--ease-out) forwards;
}
```

### Character Stagger (Text)

```css
.char-stagger {
  display: inline-block;
}

.char-stagger span {
  display: inline-block;
  opacity: 0;
  animation: fadeSlideUp 0.4s var(--ease-out-expo) forwards;
}

/* Apply delays via JS or nth-child */
.char-stagger span:nth-child(1) { animation-delay: 0ms; }
.char-stagger span:nth-child(2) { animation-delay: 30ms; }
.char-stagger span:nth-child(3) { animation-delay: 60ms; }
/* etc... */
```

---

## Micro-Interactions

### Button Hover - Subtle

```css
.btn {
  transition: transform var(--duration-fast) var(--ease-out),
              box-shadow var(--duration-fast) var(--ease-out);
}

.btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

.btn:active {
  transform: translateY(0);
  transition-duration: var(--duration-instant);
}
```

### Button Hover - Scale

```css
.btn-scale {
  transition: transform var(--duration-fast) var(--ease-out-back);
}

.btn-scale:hover {
  transform: scale(1.05);
}

.btn-scale:active {
  transform: scale(0.98);
}
```

### Card Hover - Lift

```css
.card {
  transition: transform var(--duration-normal) var(--ease-out-expo),
              box-shadow var(--duration-normal) var(--ease-out-expo);
}

.card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
}
```

### Card Hover - Tilt (3D)

```css
.card-tilt {
  transition: transform var(--duration-normal) var(--ease-out);
  transform-style: preserve-3d;
  perspective: 1000px;
}

/* Apply via JS based on mouse position */
/* Or use simple CSS hover: */
.card-tilt:hover {
  transform: rotateX(5deg) rotateY(-5deg);
}
```

### Link Hover - Underline Grow

```css
.link-underline {
  position: relative;
}

.link-underline::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background: currentColor;
  transition: width var(--duration-normal) var(--ease-out-expo);
}

.link-underline:hover::after {
  width: 100%;
}
```

### Link Hover - Highlight

```css
.link-highlight {
  background: linear-gradient(transparent 60%, var(--accent-muted) 60%);
  background-size: 100% 200%;
  background-position: 0 0;
  transition: background-position var(--duration-normal) var(--ease-out);
}

.link-highlight:hover {
  background-position: 0 100%;
}
```

### Input Focus

```css
.input {
  border: 2px solid var(--border-default);
  transition: border-color var(--duration-fast) var(--ease-out),
              box-shadow var(--duration-fast) var(--ease-out);
}

.input:focus {
  border-color: var(--accent-primary);
  box-shadow: 0 0 0 3px var(--accent-muted);
  outline: none;
}
```

---

## Scroll-Triggered Animations

### Using CSS scroll-driven animations (Modern)

```css
@keyframes fadeInOnScroll {
  from {
    opacity: 0;
    transform: translateY(50px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.scroll-reveal {
  animation: fadeInOnScroll linear both;
  animation-timeline: view();
  animation-range: entry 0% entry 30%;
}
```

### Using Intersection Observer (JS Required)

```html
<div class="reveal-on-scroll">Content</div>

<style>
.reveal-on-scroll {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.6s var(--ease-out-expo),
              transform 0.6s var(--ease-out-expo);
}

.reveal-on-scroll.visible {
  opacity: 1;
  transform: translateY(0);
}
</style>

<script>
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
    }
  });
}, { threshold: 0.1 });

document.querySelectorAll('.reveal-on-scroll').forEach(el => {
  observer.observe(el);
});
</script>
```

---

## Framer Motion Presets (React)

### Page Transition

```jsx
const pageVariants = {
  initial: {
    opacity: 0,
    y: 20
  },
  animate: {
    opacity: 1,
    y: 0,
    transition: {
      duration: 0.6,
      ease: [0.16, 1, 0.3, 1] // ease-out-expo
    }
  },
  exit: {
    opacity: 0,
    y: -20,
    transition: {
      duration: 0.4
    }
  }
};

// Usage
<motion.div
  variants={pageVariants}
  initial="initial"
  animate="animate"
  exit="exit"
>
  {children}
</motion.div>
```

### Stagger Container

```jsx
const containerVariants = {
  hidden: { opacity: 0 },
  visible: {
    opacity: 1,
    transition: {
      staggerChildren: 0.08,
      delayChildren: 0.1
    }
  }
};

const itemVariants = {
  hidden: {
    opacity: 0,
    y: 20
  },
  visible: {
    opacity: 1,
    y: 0,
    transition: {
      duration: 0.5,
      ease: [0.16, 1, 0.3, 1]
    }
  }
};

// Usage
<motion.ul variants={containerVariants} initial="hidden" animate="visible">
  {items.map(item => (
    <motion.li key={item.id} variants={itemVariants}>
      {item.content}
    </motion.li>
  ))}
</motion.ul>
```

### Hover Scale

```jsx
<motion.button
  whileHover={{ scale: 1.05 }}
  whileTap={{ scale: 0.98 }}
  transition={{ type: "spring", stiffness: 400, damping: 17 }}
>
  Click me
</motion.button>
```

### Scroll-Triggered

```jsx
<motion.div
  initial={{ opacity: 0, y: 50 }}
  whileInView={{ opacity: 1, y: 0 }}
  viewport={{ once: true, margin: "-100px" }}
  transition={{ duration: 0.6, ease: [0.16, 1, 0.3, 1] }}
>
  Content
</motion.div>
```

### Layout Animation

```jsx
<motion.div layout transition={{ type: "spring", stiffness: 300, damping: 30 }}>
  {/* Content that changes size */}
</motion.div>
```

---

## Specialty Animations

### Marquee (Infinite Scroll)

```css
@keyframes marquee {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}

.marquee-container {
  overflow: hidden;
}

.marquee-content {
  display: flex;
  animation: marquee 20s linear infinite;
}

.marquee-container:hover .marquee-content {
  animation-play-state: paused;
}
```

### Pulse (Attention)

```css
@keyframes pulse {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.05); }
}

.pulse {
  animation: pulse 2s var(--ease-in-out) infinite;
}
```

### Shimmer (Loading)

```css
@keyframes shimmer {
  from { background-position: -200% 0; }
  to { background-position: 200% 0; }
}

.skeleton {
  background: linear-gradient(
    90deg,
    var(--bg-secondary) 25%,
    var(--bg-tertiary) 50%,
    var(--bg-secondary) 75%
  );
  background-size: 200% 100%;
  animation: shimmer 1.5s infinite;
}
```

### Typewriter

```css
@keyframes typewriter {
  from { width: 0; }
  to { width: 100%; }
}

@keyframes blink {
  50% { border-color: transparent; }
}

.typewriter {
  overflow: hidden;
  white-space: nowrap;
  border-right: 3px solid;
  animation:
    typewriter 3s steps(30) forwards,
    blink 0.7s step-end infinite;
}
```

---

## Motion Guidelines

### Timing Recommendations

| Interaction | Duration | Easing |
|-------------|----------|--------|
| Button hover | 150ms | ease-out |
| Button press | 50ms | ease-out |
| Card hover | 250-300ms | ease-out-expo |
| Modal open | 300-400ms | ease-out-expo |
| Modal close | 200-250ms | ease-in |
| Page transition | 400-600ms | ease-out-expo |
| Scroll reveal | 500-700ms | ease-out-expo |
| Tooltip | 150ms | ease-out |

### Do's and Don'ts

```
DO:
- Use consistent timing across similar interactions
- Make animations purposeful (communicate state)
- Respect prefers-reduced-motion
- Test on slower devices

DON'T:
- Animate everything
- Use long delays that feel sluggish
- Block user interaction during animations
- Use bouncy easings for professional UIs
```

### Reduced Motion Support

```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## Quick Reference

### Easing Cheat Sheet

```
SMOOTH/NATURAL:    cubic-bezier(0.16, 1, 0.3, 1)    ease-out-expo
SNAPPY:            cubic-bezier(0.25, 1, 0.5, 1)    ease-out-quart
BOUNCY:            cubic-bezier(0.34, 1.56, 0.64, 1) ease-out-back
PROFESSIONAL:      cubic-bezier(0, 0, 0.2, 1)       ease-out
PLAYFUL:           cubic-bezier(0.175, 0.885, 0.32, 1.275) spring
```

### Copy-Paste Starter

```css
/* Add to your CSS for instant polish */
:root {
  --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
}

* {
  transition-timing-function: var(--ease-out-expo);
}

a, button {
  transition: all 150ms var(--ease-out-expo);
}

.card {
  transition: transform 250ms var(--ease-out-expo),
              box-shadow 250ms var(--ease-out-expo);
}
```
