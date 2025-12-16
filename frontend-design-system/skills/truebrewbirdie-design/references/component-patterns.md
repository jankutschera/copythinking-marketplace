# Component Patterns

Production-ready code templates for common UI components.

---

## Hero Sections

### Asymmetric Editorial Hero

```html
<section class="hero-editorial">
  <div class="hero-content">
    <span class="hero-eyebrow">Introducing</span>
    <h1 class="hero-headline">
      Design without<br>
      compromise
    </h1>
    <p class="hero-description">
      Build interfaces that feel genuinely designed, not generated.
      Every detail matters.
    </p>
    <div class="hero-actions">
      <a href="#" class="btn btn-primary">Get Started</a>
      <a href="#" class="btn btn-ghost">Learn More</a>
    </div>
  </div>
  <div class="hero-visual">
    <img src="hero-image.jpg" alt="" class="hero-image">
  </div>
</section>

<style>
.hero-editorial {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
  gap: 4rem;
  min-height: 85vh;
  padding: 5rem 3rem;
  align-items: center;
}

.hero-content {
  max-width: 540px;
}

.hero-eyebrow {
  display: block;
  font-family: var(--font-mono);
  font-size: 0.875rem;
  text-transform: uppercase;
  letter-spacing: 0.15em;
  color: var(--text-secondary);
  margin-bottom: 1rem;
}

.hero-headline {
  font-family: var(--font-display);
  font-size: clamp(2.5rem, 6vw, 4.5rem);
  line-height: 1.1;
  font-weight: 600;
  margin-bottom: 1.5rem;
  color: var(--text-primary);
}

.hero-description {
  font-size: 1.125rem;
  line-height: 1.6;
  color: var(--text-secondary);
  margin-bottom: 2rem;
  max-width: 420px;
}

.hero-actions {
  display: flex;
  gap: 1rem;
}

.hero-visual {
  position: relative;
  border-radius: var(--radius-lg);
  overflow: hidden;
  aspect-ratio: 4/3;
}

.hero-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

@media (max-width: 768px) {
  .hero-editorial {
    grid-template-columns: 1fr;
    text-align: center;
    padding: 3rem 1.5rem;
  }

  .hero-content {
    max-width: 100%;
  }

  .hero-description {
    max-width: 100%;
  }

  .hero-actions {
    justify-content: center;
  }
}
</style>
```

### Centered Hero with Background

```html
<section class="hero-centered">
  <div class="hero-bg"></div>
  <div class="hero-content">
    <span class="hero-badge">New Release</span>
    <h1 class="hero-headline">
      The future of design<br>is here
    </h1>
    <p class="hero-description">
      Create stunning interfaces with AI-powered tools that understand your vision.
    </p>
    <div class="hero-actions">
      <a href="#" class="btn btn-primary btn-large">Start Building</a>
    </div>
    <div class="hero-social-proof">
      <div class="avatars">
        <img src="avatar1.jpg" alt="">
        <img src="avatar2.jpg" alt="">
        <img src="avatar3.jpg" alt="">
      </div>
      <span>Trusted by 10,000+ designers</span>
    </div>
  </div>
</section>

<style>
.hero-centered {
  position: relative;
  min-height: 90vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 4rem 2rem;
  overflow: hidden;
}

.hero-bg {
  position: absolute;
  inset: 0;
  background: radial-gradient(
    ellipse at 50% 0%,
    var(--accent-muted) 0%,
    transparent 70%
  );
  z-index: 0;
}

.hero-content {
  position: relative;
  z-index: 1;
  max-width: 800px;
}

.hero-badge {
  display: inline-block;
  padding: 0.5rem 1rem;
  background: var(--surface-1);
  border: 1px solid var(--border-default);
  border-radius: var(--radius-full);
  font-size: 0.875rem;
  font-weight: 500;
  margin-bottom: 2rem;
}

.hero-headline {
  font-family: var(--font-display);
  font-size: clamp(2.5rem, 8vw, 5rem);
  line-height: 1.1;
  font-weight: 700;
  margin-bottom: 1.5rem;
}

.hero-description {
  font-size: 1.25rem;
  color: var(--text-secondary);
  max-width: 600px;
  margin: 0 auto 2.5rem;
  line-height: 1.6;
}

.hero-social-proof {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.75rem;
  margin-top: 3rem;
  color: var(--text-secondary);
  font-size: 0.875rem;
}

.avatars {
  display: flex;
}

.avatars img {
  width: 32px;
  height: 32px;
  border-radius: 50%;
  border: 2px solid var(--bg-primary);
  margin-left: -8px;
}

.avatars img:first-child {
  margin-left: 0;
}
</style>
```

---

## Cards

### Hover Reveal Card

```html
<article class="card-reveal">
  <div class="card-image">
    <img src="project.jpg" alt="Project name">
  </div>
  <div class="card-overlay">
    <span class="card-category">Web Design</span>
    <h3 class="card-title">Project Name</h3>
    <p class="card-description">Brief description of the project and its impact.</p>
    <a href="#" class="card-link">View Project</a>
  </div>
</article>

<style>
.card-reveal {
  position: relative;
  border-radius: var(--radius-lg);
  overflow: hidden;
  aspect-ratio: 4/3;
  cursor: pointer;
}

.card-image {
  position: absolute;
  inset: 0;
}

.card-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.6s var(--ease-out-expo);
}

.card-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(
    to top,
    rgba(0, 0, 0, 0.9) 0%,
    rgba(0, 0, 0, 0) 60%
  );
  padding: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  color: white;
  opacity: 0;
  transition: opacity 0.4s var(--ease-out);
}

.card-reveal:hover .card-image img {
  transform: scale(1.05);
}

.card-reveal:hover .card-overlay {
  opacity: 1;
}

.card-category {
  font-size: 0.75rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  opacity: 0.8;
  margin-bottom: 0.5rem;
}

.card-title {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
}

.card-description {
  font-size: 0.875rem;
  opacity: 0.8;
  margin-bottom: 1rem;
}

.card-link {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.875rem;
  font-weight: 500;
  color: white;
  text-decoration: none;
}

.card-link::after {
  content: '→';
  transition: transform 0.2s var(--ease-out);
}

.card-link:hover::after {
  transform: translateX(4px);
}
</style>
```

### Feature Card (Bento Style)

```html
<div class="bento-card">
  <div class="bento-icon">
    <svg><!-- icon --></svg>
  </div>
  <h3 class="bento-title">Feature Name</h3>
  <p class="bento-description">
    Short description of what this feature does and why it matters.
  </p>
</div>

<style>
.bento-card {
  background: var(--surface-1);
  border: 1px solid var(--border-default);
  border-radius: var(--radius-xl);
  padding: 2rem;
  transition: border-color 0.3s var(--ease-out),
              transform 0.3s var(--ease-out);
}

.bento-card:hover {
  border-color: var(--accent-primary);
  transform: translateY(-4px);
}

.bento-icon {
  width: 48px;
  height: 48px;
  background: var(--accent-muted);
  border-radius: var(--radius-md);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
  color: var(--accent-primary);
}

.bento-title {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 0.75rem;
}

.bento-description {
  font-size: 0.9375rem;
  color: var(--text-secondary);
  line-height: 1.6;
}
</style>
```

### Stats Card

```html
<div class="stats-card">
  <div class="stat-value">
    <span class="stat-number">98</span>
    <span class="stat-unit">%</span>
  </div>
  <div class="stat-label">Customer Satisfaction</div>
  <div class="stat-trend positive">
    <svg><!-- up arrow --></svg>
    <span>+12% from last month</span>
  </div>
</div>

<style>
.stats-card {
  background: var(--surface-1);
  border: 1px solid var(--border-default);
  border-radius: var(--radius-lg);
  padding: 1.5rem;
}

.stat-value {
  display: flex;
  align-items: baseline;
  gap: 0.25rem;
  margin-bottom: 0.5rem;
}

.stat-number {
  font-family: var(--font-display);
  font-size: 3rem;
  font-weight: 700;
  line-height: 1;
}

.stat-unit {
  font-size: 1.5rem;
  color: var(--text-secondary);
}

.stat-label {
  font-size: 0.875rem;
  color: var(--text-secondary);
  margin-bottom: 1rem;
}

.stat-trend {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.875rem;
}

.stat-trend.positive {
  color: var(--success);
}

.stat-trend.negative {
  color: var(--error);
}
</style>
```

---

## Navigation

### Floating Navigation

```html
<nav class="nav-floating">
  <a href="/" class="nav-logo">Logo</a>
  <div class="nav-links">
    <a href="#" class="nav-link">Features</a>
    <a href="#" class="nav-link">Pricing</a>
    <a href="#" class="nav-link">About</a>
  </div>
  <div class="nav-actions">
    <a href="#" class="btn btn-ghost">Log in</a>
    <a href="#" class="btn btn-primary">Sign up</a>
  </div>
</nav>

<style>
.nav-floating {
  position: fixed;
  top: 1.5rem;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  align-items: center;
  gap: 2rem;
  padding: 0.75rem 1.5rem;
  background: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(10px);
  border: 1px solid var(--border-default);
  border-radius: var(--radius-full);
  z-index: 1000;
}

.nav-logo {
  font-weight: 700;
  color: var(--text-primary);
  text-decoration: none;
}

.nav-links {
  display: flex;
  gap: 1.5rem;
}

.nav-link {
  font-size: 0.875rem;
  color: var(--text-secondary);
  text-decoration: none;
  transition: color 0.2s var(--ease-out);
}

.nav-link:hover {
  color: var(--text-primary);
}

.nav-actions {
  display: flex;
  gap: 0.75rem;
}

@media (max-width: 768px) {
  .nav-floating {
    width: calc(100% - 2rem);
    justify-content: space-between;
  }

  .nav-links {
    display: none;
  }
}
</style>
```

---

## Buttons

### Button System

```html
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary">Secondary</button>
<button class="btn btn-ghost">Ghost</button>
<button class="btn btn-destructive">Delete</button>

<style>
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  font-size: 0.9375rem;
  font-weight: 500;
  border-radius: var(--radius-md);
  border: none;
  cursor: pointer;
  transition: all 0.15s var(--ease-out);
  text-decoration: none;
}

.btn:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}

/* Primary */
.btn-primary {
  background: var(--accent-primary);
  color: var(--text-on-accent);
}

.btn-primary:hover:not(:disabled) {
  background: var(--accent-primary-hover);
  transform: translateY(-1px);
}

.btn-primary:active:not(:disabled) {
  transform: translateY(0);
}

/* Secondary */
.btn-secondary {
  background: var(--surface-1);
  color: var(--text-primary);
  border: 1px solid var(--border-default);
}

.btn-secondary:hover:not(:disabled) {
  background: var(--bg-secondary);
  border-color: var(--border-strong);
}

/* Ghost */
.btn-ghost {
  background: transparent;
  color: var(--text-primary);
}

.btn-ghost:hover:not(:disabled) {
  background: var(--bg-secondary);
}

/* Destructive */
.btn-destructive {
  background: var(--error);
  color: white;
}

.btn-destructive:hover:not(:disabled) {
  opacity: 0.9;
}

/* Sizes */
.btn-sm {
  padding: 0.5rem 1rem;
  font-size: 0.875rem;
}

.btn-lg {
  padding: 1rem 2rem;
  font-size: 1rem;
}
</style>
```

---

## Forms

### Floating Label Input

```html
<div class="input-floating">
  <input type="email" id="email" placeholder=" " required>
  <label for="email">Email address</label>
</div>

<style>
.input-floating {
  position: relative;
}

.input-floating input {
  width: 100%;
  padding: 1.5rem 1rem 0.5rem;
  font-size: 1rem;
  border: 1px solid var(--border-default);
  border-radius: var(--radius-md);
  background: var(--surface-1);
  transition: border-color 0.2s var(--ease-out),
              box-shadow 0.2s var(--ease-out);
}

.input-floating label {
  position: absolute;
  left: 1rem;
  top: 50%;
  transform: translateY(-50%);
  font-size: 1rem;
  color: var(--text-secondary);
  pointer-events: none;
  transition: all 0.2s var(--ease-out);
}

.input-floating input:focus,
.input-floating input:not(:placeholder-shown) {
  border-color: var(--accent-primary);
}

.input-floating input:focus + label,
.input-floating input:not(:placeholder-shown) + label {
  top: 0.75rem;
  transform: translateY(0);
  font-size: 0.75rem;
  color: var(--accent-primary);
}

.input-floating input:focus {
  outline: none;
  box-shadow: 0 0 0 3px var(--accent-muted);
}
</style>
```

---

## Modal

### Centered Modal

```html
<div class="modal-overlay" id="modal">
  <div class="modal" role="dialog" aria-modal="true">
    <button class="modal-close" aria-label="Close">×</button>
    <div class="modal-header">
      <h2 class="modal-title">Modal Title</h2>
    </div>
    <div class="modal-body">
      <p>Modal content goes here.</p>
    </div>
    <div class="modal-footer">
      <button class="btn btn-ghost">Cancel</button>
      <button class="btn btn-primary">Confirm</button>
    </div>
  </div>
</div>

<style>
.modal-overlay {
  position: fixed;
  inset: 0;
  background: rgba(0, 0, 0, 0.5);
  backdrop-filter: blur(4px);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1rem;
  z-index: 1000;
  opacity: 0;
  visibility: hidden;
  transition: opacity 0.3s var(--ease-out),
              visibility 0.3s var(--ease-out);
}

.modal-overlay.open {
  opacity: 1;
  visibility: visible;
}

.modal {
  background: var(--surface-1);
  border-radius: var(--radius-xl);
  width: 100%;
  max-width: 480px;
  max-height: 90vh;
  overflow: auto;
  transform: scale(0.95) translateY(10px);
  transition: transform 0.3s var(--ease-out-expo);
}

.modal-overlay.open .modal {
  transform: scale(1) translateY(0);
}

.modal-close {
  position: absolute;
  top: 1rem;
  right: 1rem;
  width: 32px;
  height: 32px;
  border: none;
  background: transparent;
  font-size: 1.5rem;
  cursor: pointer;
  color: var(--text-secondary);
  transition: color 0.2s var(--ease-out);
}

.modal-close:hover {
  color: var(--text-primary);
}

.modal-header {
  padding: 1.5rem 1.5rem 0;
}

.modal-title {
  font-size: 1.25rem;
  font-weight: 600;
}

.modal-body {
  padding: 1rem 1.5rem;
  color: var(--text-secondary);
}

.modal-footer {
  padding: 0 1.5rem 1.5rem;
  display: flex;
  gap: 0.75rem;
  justify-content: flex-end;
}
</style>
```

---

## Footer

### Simple Footer

```html
<footer class="footer">
  <div class="footer-content">
    <div class="footer-brand">
      <a href="/" class="footer-logo">Brand</a>
      <p class="footer-tagline">Building the future of design.</p>
    </div>
    <nav class="footer-nav">
      <div class="footer-column">
        <h4>Product</h4>
        <a href="#">Features</a>
        <a href="#">Pricing</a>
        <a href="#">Changelog</a>
      </div>
      <div class="footer-column">
        <h4>Company</h4>
        <a href="#">About</a>
        <a href="#">Blog</a>
        <a href="#">Careers</a>
      </div>
      <div class="footer-column">
        <h4>Legal</h4>
        <a href="#">Privacy</a>
        <a href="#">Terms</a>
      </div>
    </nav>
  </div>
  <div class="footer-bottom">
    <span>© 2024 Brand. All rights reserved.</span>
    <div class="footer-social">
      <a href="#" aria-label="Twitter">𝕏</a>
      <a href="#" aria-label="GitHub">GH</a>
    </div>
  </div>
</footer>

<style>
.footer {
  background: var(--bg-secondary);
  border-top: 1px solid var(--border-default);
  padding: 4rem 2rem 2rem;
}

.footer-content {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  gap: 4rem;
  margin-bottom: 3rem;
}

.footer-brand {
  max-width: 280px;
}

.footer-logo {
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--text-primary);
  text-decoration: none;
}

.footer-tagline {
  margin-top: 0.75rem;
  color: var(--text-secondary);
  font-size: 0.9375rem;
}

.footer-nav {
  display: flex;
  gap: 4rem;
}

.footer-column {
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}

.footer-column h4 {
  font-size: 0.875rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
}

.footer-column a {
  font-size: 0.875rem;
  color: var(--text-secondary);
  text-decoration: none;
  transition: color 0.2s var(--ease-out);
}

.footer-column a:hover {
  color: var(--text-primary);
}

.footer-bottom {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 2rem;
  border-top: 1px solid var(--border-default);
  font-size: 0.875rem;
  color: var(--text-secondary);
}

.footer-social {
  display: flex;
  gap: 1rem;
}

.footer-social a {
  color: var(--text-secondary);
  text-decoration: none;
  transition: color 0.2s var(--ease-out);
}

.footer-social a:hover {
  color: var(--text-primary);
}

@media (max-width: 768px) {
  .footer-content {
    flex-direction: column;
    gap: 2rem;
  }

  .footer-nav {
    flex-wrap: wrap;
    gap: 2rem;
  }
}
</style>
```

---

## Usage Notes

1. **Adapt, don't copy** - Use these as starting points, customize for your theme
2. **Check color references** - Replace `var(--xxx)` with your theme tokens
3. **Test responsiveness** - Add breakpoints as needed
4. **Add motion** - Reference `motion-library.md` for animations
5. **Maintain consistency** - Use the same patterns across your project
