# Social Media Design

Complete design system for social media posts, stories, OG images, and meta tags.

---

## Social Media Post Formats

### Platform Size Reference

| Format | Size (px) | Aspect | Best For |
|--------|-----------|--------|----------|
| **Story/Reel** | 1080 × 1920 | 9:16 | Instagram Stories, Reels, TikTok, YouTube Shorts |
| **Square** | 1080 × 1080 | 1:1 | Instagram Feed, LinkedIn, Facebook |
| **Portrait** | 1080 × 1350 | 4:5 | Instagram Feed (optimal), Pinterest |
| **Landscape** | 1200 × 675 | 16:9 | Twitter/X, LinkedIn, Facebook |
| **YouTube Thumb** | 1280 × 720 | 16:9 | YouTube Thumbnails |
| **Pinterest** | 1000 × 1500 | 2:3 | Pinterest Pins |
| **LinkedIn Carousel** | 1080 × 1080 | 1:1 | LinkedIn Document Posts |
| **Twitter Header** | 1500 × 500 | 3:1 | Twitter Profile Banner |

---

## 9:16 Story/Reel Templates (1080 × 1920)

### Safe Zones

```
┌────────────────────────────┐
│  ↑ 250px (Username/Icons)  │
│  ┌────────────────────┐    │
│  │                    │    │
│  │                    │    │
│  │   SAFE ZONE        │    │
│  │   (1080 × 1420)    │    │
│  │                    │    │
│  │   Keep all text    │    │
│  │   and key visuals  │    │
│  │   in this area     │    │
│  │                    │    │
│  └────────────────────┘    │
│  ↓ 250px (CTA/Swipe up)    │
└────────────────────────────┘
        1080 × 1920
```

### Bold Statement Story

```html
<div style="
  width: 1080px;
  height: 1920px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 80px;
  background: linear-gradient(180deg, #0a0a0a 0%, #1a1a2e 100%);
  font-family: system-ui, sans-serif;
">
  <h1 style="
    font-size: 96px;
    color: #fff;
    text-align: center;
    line-height: 1.0;
    font-weight: 800;
    text-transform: uppercase;
    letter-spacing: -0.02em;
    margin: 0;
  ">Your Bold<br/>Statement<br/>Here</h1>
  <p style="
    font-size: 32px;
    color: rgba(255,255,255,0.7);
    text-align: center;
    margin-top: 48px;
    max-width: 800px;
  ">Supporting text that adds context</p>
</div>
```

### Quote Story

```html
<div style="
  width: 1080px;
  height: 1920px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 100px;
  background: #faf9f6;
  font-family: Georgia, serif;
">
  <div style="
    font-size: 200px;
    color: #e5e5e5;
    line-height: 0.5;
    margin-bottom: 20px;
  ">"</div>
  <p style="
    font-size: 64px;
    color: #1a1a1a;
    line-height: 1.3;
    font-style: italic;
    margin: 0 0 48px 0;
  ">The inspiring quote that resonates with your audience goes here.</p>
  <div style="
    font-size: 28px;
    color: #666;
    font-family: system-ui, sans-serif;
    font-style: normal;
  ">— Author Name</div>
</div>
```

### Tips/List Story

```html
<div style="
  width: 1080px;
  height: 1920px;
  display: flex;
  flex-direction: column;
  padding: 120px 80px;
  background: #fff;
  font-family: system-ui, sans-serif;
">
  <div style="
    font-size: 24px;
    color: #666;
    text-transform: uppercase;
    letter-spacing: 0.2em;
    margin-bottom: 32px;
  ">5 Tips</div>
  <h1 style="
    font-size: 64px;
    color: #0a0a0a;
    line-height: 1.1;
    font-weight: 700;
    margin: 0 0 64px 0;
  ">How to improve your [topic]</h1>

  <!-- Tip items -->
  <div style="display: flex; flex-direction: column; gap: 40px;">
    <div style="display: flex; align-items: flex-start; gap: 24px;">
      <div style="
        min-width: 56px;
        height: 56px;
        background: #0a0a0a;
        color: #fff;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 28px;
        font-weight: 700;
      ">1</div>
      <p style="font-size: 36px; color: #1a1a1a; margin: 8px 0 0 0; line-height: 1.3;">First tip with actionable advice</p>
    </div>
    <!-- Repeat for tips 2-5 -->
  </div>
</div>
```

### Product Showcase Story

```html
<div style="
  width: 1080px;
  height: 1920px;
  display: flex;
  flex-direction: column;
  background: #f5f5f5;
  font-family: system-ui, sans-serif;
">
  <!-- Product Image Area -->
  <div style="
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 60px;
  ">
    <img src="product.png" style="max-width: 90%; max-height: 100%; object-fit: contain;">
  </div>

  <!-- Info Area -->
  <div style="
    padding: 60px 80px 120px;
    background: #fff;
  ">
    <div style="
      font-size: 20px;
      color: #10b981;
      font-weight: 600;
      margin-bottom: 16px;
    ">NEW ARRIVAL</div>
    <h2 style="
      font-size: 48px;
      color: #0a0a0a;
      font-weight: 700;
      margin: 0 0 16px 0;
    ">Product Name</h2>
    <p style="
      font-size: 32px;
      color: #666;
      margin: 0 0 24px 0;
    ">Brief product description</p>
    <div style="
      font-size: 40px;
      color: #0a0a0a;
      font-weight: 700;
    ">$99.00</div>
  </div>
</div>
```

---

## 1:1 Square Templates (1080 × 1080)

### Minimal Announcement

```html
<div style="
  width: 1080px;
  height: 1080px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 100px;
  background: #0a0a0a;
  font-family: system-ui, sans-serif;
">
  <div style="
    font-size: 18px;
    color: #666;
    text-transform: uppercase;
    letter-spacing: 0.3em;
    margin-bottom: 32px;
  ">Announcing</div>
  <h1 style="
    font-size: 72px;
    color: #fff;
    text-align: center;
    line-height: 1.1;
    font-weight: 700;
    margin: 0;
  ">Your Big<br/>News Here</h1>
  <p style="
    font-size: 28px;
    color: #888;
    text-align: center;
    margin-top: 32px;
  ">Supporting details • Date • Link</p>
</div>
```

### Carousel Slide (Educational)

```html
<div style="
  width: 1080px;
  height: 1080px;
  display: flex;
  flex-direction: column;
  padding: 100px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  font-family: system-ui, sans-serif;
">
  <div style="
    font-size: 20px;
    color: rgba(255,255,255,0.8);
    margin-bottom: 24px;
  ">Slide 1 of 5</div>
  <h2 style="
    font-size: 56px;
    color: #fff;
    line-height: 1.2;
    font-weight: 700;
    margin: 0 0 48px 0;
  ">The key insight or teaching point</h2>
  <p style="
    font-size: 32px;
    color: rgba(255,255,255,0.9);
    line-height: 1.5;
    flex: 1;
  ">Detailed explanation that provides value and context. Keep it scannable with short paragraphs.</p>
  <div style="
    display: flex;
    align-items: center;
    gap: 16px;
    margin-top: auto;
  ">
    <img src="avatar.jpg" style="width: 56px; height: 56px; border-radius: 50%;">
    <span style="color: #fff; font-size: 24px;">@username</span>
  </div>
</div>
```

### Stats/Data Square

```html
<div style="
  width: 1080px;
  height: 1080px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 100px;
  background: #fff;
  font-family: system-ui, sans-serif;
">
  <div style="
    font-size: 200px;
    font-weight: 800;
    color: #0a0a0a;
    line-height: 1;
    margin-bottom: 24px;
  ">73%</div>
  <p style="
    font-size: 36px;
    color: #666;
    text-align: center;
    line-height: 1.4;
    max-width: 700px;
  ">of users prefer brands that communicate authentically</p>
  <div style="
    margin-top: 48px;
    font-size: 20px;
    color: #999;
  ">Source: Research Study 2024</div>
</div>
```

---

## 4:5 Portrait Templates (1080 × 1350)

### Instagram Optimal Feed Post

```html
<div style="
  width: 1080px;
  height: 1350px;
  display: flex;
  flex-direction: column;
  background: #fafafa;
  font-family: system-ui, sans-serif;
">
  <!-- Visual Area (60%) -->
  <div style="
    flex: 0 0 810px;
    background: url('image.jpg') center/cover;
  "></div>

  <!-- Text Area (40%) -->
  <div style="
    flex: 1;
    padding: 48px 60px;
    display: flex;
    flex-direction: column;
    justify-content: center;
  ">
    <h2 style="
      font-size: 40px;
      color: #0a0a0a;
      font-weight: 700;
      line-height: 1.2;
      margin: 0 0 20px 0;
    ">Compelling headline that grabs attention</h2>
    <p style="
      font-size: 28px;
      color: #666;
      line-height: 1.4;
      margin: 0;
    ">Brief supporting text that adds context and encourages engagement.</p>
  </div>
</div>
```

---

## 16:9 Landscape Templates (1200 × 675 / 1920 × 1080)

### YouTube Thumbnail

```html
<div style="
  width: 1280px;
  height: 720px;
  display: flex;
  align-items: center;
  padding: 60px;
  background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%);
  font-family: system-ui, sans-serif;
  position: relative;
">
  <!-- Background Image with Overlay -->
  <div style="
    position: absolute;
    inset: 0;
    background: url('background.jpg') center/cover;
    opacity: 0.3;
  "></div>

  <!-- Content -->
  <div style="position: relative; z-index: 1; max-width: 70%;">
    <h1 style="
      font-size: 84px;
      color: #fff;
      font-weight: 800;
      line-height: 1.0;
      text-transform: uppercase;
      margin: 0;
      text-shadow: 0 4px 20px rgba(0,0,0,0.5);
    ">ATTENTION<br/>GRABBING<br/>TITLE</h1>
  </div>

  <!-- Face/Element on Right -->
  <div style="
    position: absolute;
    right: 0;
    bottom: 0;
    width: 500px;
    height: 100%;
  ">
    <img src="face.png" style="height: 100%; object-fit: contain; object-position: bottom;">
  </div>
</div>
```

### Twitter/LinkedIn Post

```html
<div style="
  width: 1200px;
  height: 675px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 80px;
  background: #fff;
  font-family: system-ui, sans-serif;
">
  <div style="max-width: 600px;">
    <div style="
      display: inline-block;
      padding: 8px 20px;
      background: #e8f5e9;
      color: #2e7d32;
      font-size: 16px;
      font-weight: 600;
      border-radius: 100px;
      margin-bottom: 24px;
    ">CATEGORY</div>
    <h1 style="
      font-size: 52px;
      color: #0a0a0a;
      font-weight: 700;
      line-height: 1.1;
      margin: 0 0 24px 0;
    ">Your key message or announcement</h1>
    <p style="
      font-size: 24px;
      color: #666;
      line-height: 1.5;
      margin: 0;
    ">Supporting text that provides context and encourages clicks.</p>
  </div>
  <div style="
    width: 320px;
    height: 320px;
    background: #f5f5f5;
    border-radius: 24px;
    display: flex;
    align-items: center;
    justify-content: center;
  ">
    <!-- Icon or Image -->
  </div>
</div>
```

---

## Typography Guidelines by Format

### 9:16 Stories/Reels
```
HEADLINES:
- Size: 72-120px
- Weight: 700-800
- Max lines: 3-4
- All caps for impact

BODY TEXT:
- Size: 28-36px
- Weight: 400-500
- Max lines: 4-5

REMEMBER:
- People scroll FAST
- 3 seconds to hook
- Less text = better
```

### 1:1 Square
```
HEADLINES:
- Size: 48-72px
- Weight: 600-700
- Max lines: 2-3

BODY TEXT:
- Size: 24-32px
- Weight: 400
- Max lines: 3-4
```

### 4:5 Portrait
```
HEADLINES:
- Size: 36-48px
- Weight: 600-700

BODY TEXT:
- Size: 24-28px
- Generous line height (1.4-1.5)
```

### 16:9 Landscape
```
HEADLINES:
- Size: 48-84px (YouTube can go bigger)
- High contrast essential

BODY TEXT:
- Size: 20-28px
- Keep minimal
```

---

## Color Psychology for Social

| Color | Emotion | Best For |
|-------|---------|----------|
| **Red** | Urgency, excitement | Sales, alerts, food |
| **Orange** | Friendly, energetic | CTAs, youth brands |
| **Yellow** | Optimism, attention | Highlights, warnings |
| **Green** | Growth, health | Eco, finance, wellness |
| **Blue** | Trust, calm | Tech, corporate, health |
| **Purple** | Luxury, creativity | Beauty, premium |
| **Pink** | Playful, feminine | Lifestyle, beauty |
| **Black** | Luxury, power | Fashion, premium |
| **White** | Clean, minimal | Tech, lifestyle |

### Platform Color Vibes

```
INSTAGRAM:
- Warm, lifestyle-oriented
- Soft gradients work well
- Earthy tones trending

LINKEDIN:
- Professional blues
- Clean backgrounds
- High contrast text

TWITTER/X:
- Bold, attention-grabbing
- Dark mode friendly
- Strong contrast

TIKTOK:
- Vibrant, saturated
- Neon accents
- Dark backgrounds popular
```

---

## Open Graph Image Specifications

### Platform Requirements

| Platform | Recommended Size | Aspect Ratio | Max File Size |
|----------|------------------|--------------|---------------|
| Twitter/X | 1200 × 630 | 1.91:1 | 5MB |
| Facebook | 1200 × 630 | 1.91:1 | 8MB |
| LinkedIn | 1200 × 627 | 1.91:1 | 5MB |
| Discord | 1200 × 630 | 1.91:1 | 8MB |
| Slack | 1200 × 630 | 1.91:1 | 5MB |

### Safe Zone

```
┌──────────────────────────────────────────────────────────┐
│  ┌──────────────────────────────────────────────────┐   │
│  │                                                   │   │
│  │              SAFE ZONE (1080 × 566)              │   │
│  │         Keep important content here              │   │
│  │                                                   │   │
│  └──────────────────────────────────────────────────┘   │
│                  60px padding on all sides              │
└──────────────────────────────────────────────────────────┘
              Full image: 1200 × 630
```

---

## Meta Tags

### Complete Meta Tag Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Primary Meta Tags -->
  <title>Page Title - Brand Name</title>
  <meta name="title" content="Page Title - Brand Name">
  <meta name="description" content="Brief description of the page content. Keep under 160 characters for best display.">

  <!-- Open Graph / Facebook -->
  <meta property="og:type" content="website">
  <meta property="og:url" content="https://example.com/page">
  <meta property="og:title" content="Page Title - Brand Name">
  <meta property="og:description" content="Brief description of the page content.">
  <meta property="og:image" content="https://example.com/og-image.png">
  <meta property="og:image:width" content="1200">
  <meta property="og:image:height" content="630">
  <meta property="og:image:alt" content="Description of the image for accessibility">

  <!-- Twitter -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:url" content="https://example.com/page">
  <meta name="twitter:title" content="Page Title - Brand Name">
  <meta name="twitter:description" content="Brief description of the page content.">
  <meta name="twitter:image" content="https://example.com/og-image.png">

  <!-- Optional: Twitter handles -->
  <meta name="twitter:site" content="@brandhandle">
  <meta name="twitter:creator" content="@authorhandle">
</head>
</html>
```

### Twitter Card Types

```html
<!-- Summary (small image) -->
<meta name="twitter:card" content="summary">

<!-- Summary with large image (most common) -->
<meta name="twitter:card" content="summary_large_image">

<!-- App card -->
<meta name="twitter:card" content="app">

<!-- Player card (video/audio) -->
<meta name="twitter:card" content="player">
```

### Article-Specific Tags

```html
<!-- For blog posts / articles -->
<meta property="og:type" content="article">
<meta property="article:published_time" content="2024-01-15T08:00:00Z">
<meta property="article:modified_time" content="2024-01-16T10:30:00Z">
<meta property="article:author" content="Author Name">
<meta property="article:section" content="Technology">
<meta property="article:tag" content="Design">
<meta property="article:tag" content="Web Development">
```

---

## OG Image Templates

### Brand Hero Template

```html
<div style="
  width: 1200px;
  height: 630px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 80px;
  background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%);
  font-family: system-ui, sans-serif;
">
  <div style="max-width: 650px;">
    <div style="
      font-size: 16px;
      color: #888;
      text-transform: uppercase;
      letter-spacing: 0.2em;
      margin-bottom: 24px;
    ">Brand Name</div>
    <h1 style="
      font-size: 56px;
      color: #fff;
      line-height: 1.1;
      margin: 0 0 24px 0;
      font-weight: 700;
    ">Your compelling headline goes here</h1>
    <p style="
      font-size: 22px;
      color: #a0a0a0;
      line-height: 1.4;
      margin: 0;
    ">A brief supporting description that adds context.</p>
  </div>
  <div style="
    width: 200px;
    height: 200px;
    background: #fff;
    border-radius: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
  ">
    <!-- Logo here -->
  </div>
</div>
```

### Article Card Template

```html
<div style="
  width: 1200px;
  height: 630px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding: 60px;
  background: linear-gradient(180deg, transparent 0%, rgba(0,0,0,0.8) 100%),
              url('background-image.jpg') center/cover;
  font-family: system-ui, sans-serif;
">
  <div style="
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 24px;
  ">
    <img src="author-avatar.jpg" style="
      width: 48px;
      height: 48px;
      border-radius: 50%;
    ">
    <div>
      <div style="color: #fff; font-weight: 600;">Author Name</div>
      <div style="color: #a0a0a0; font-size: 14px;">Jan 15, 2024 · 5 min read</div>
    </div>
  </div>
  <h1 style="
    font-size: 48px;
    color: #fff;
    line-height: 1.2;
    margin: 0;
    font-weight: 700;
    max-width: 800px;
  ">Article title that captures attention and curiosity</h1>
</div>
```

### Product Launch Template

```html
<div style="
  width: 1200px;
  height: 630px;
  display: flex;
  align-items: center;
  padding: 80px;
  background: #fafafa;
  font-family: system-ui, sans-serif;
">
  <div style="flex: 1;">
    <div style="
      display: inline-block;
      padding: 8px 16px;
      background: #10b981;
      color: #fff;
      font-size: 14px;
      font-weight: 600;
      border-radius: 100px;
      margin-bottom: 24px;
    ">NEW</div>
    <h1 style="
      font-size: 52px;
      color: #0a0a0a;
      line-height: 1.1;
      margin: 0 0 20px 0;
      font-weight: 700;
    ">Product Name</h1>
    <p style="
      font-size: 20px;
      color: #666;
      line-height: 1.5;
      margin: 0;
      max-width: 400px;
    ">Brief product description highlighting the key value proposition.</p>
  </div>
  <div style="
    width: 450px;
    height: 450px;
    display: flex;
    align-items: center;
    justify-content: center;
  ">
    <!-- Product image -->
    <img src="product.png" style="max-width: 100%; max-height: 100%;">
  </div>
</div>
```

### Minimal Quote Template

```html
<div style="
  width: 1200px;
  height: 630px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 80px;
  background: #fff;
  font-family: Georgia, serif;
">
  <div style="text-align: center; max-width: 900px;">
    <div style="
      font-size: 72px;
      color: #e5e5e5;
      margin-bottom: -20px;
    ">"</div>
    <p style="
      font-size: 36px;
      color: #0a0a0a;
      line-height: 1.4;
      margin: 0 0 32px 0;
      font-style: italic;
    ">The inspiring quote or key message that you want to share.</p>
    <div style="
      font-size: 16px;
      color: #666;
      font-family: system-ui, sans-serif;
    ">— Author Name, Title</div>
  </div>
</div>
```

---

## Dynamic OG Image Generation

### Using Vercel OG (React/Next.js)

```tsx
// app/api/og/route.tsx
import { ImageResponse } from 'next/og';

export const runtime = 'edge';

export async function GET(request: Request) {
  const { searchParams } = new URL(request.url);
  const title = searchParams.get('title') || 'Default Title';

  return new ImageResponse(
    (
      <div
        style={{
          width: '100%',
          height: '100%',
          display: 'flex',
          alignItems: 'center',
          justifyContent: 'center',
          backgroundColor: '#0a0a0a',
          padding: 80,
        }}
      >
        <h1
          style={{
            fontSize: 64,
            color: '#fff',
            textAlign: 'center',
          }}
        >
          {title}
        </h1>
      </div>
    ),
    {
      width: 1200,
      height: 630,
    }
  );
}
```

### Usage in Next.js

```tsx
// app/blog/[slug]/page.tsx
export async function generateMetadata({ params }) {
  const post = await getPost(params.slug);

  return {
    title: post.title,
    description: post.excerpt,
    openGraph: {
      title: post.title,
      description: post.excerpt,
      images: [
        {
          url: `/api/og?title=${encodeURIComponent(post.title)}`,
          width: 1200,
          height: 630,
        },
      ],
    },
  };
}
```

---

## Design Guidelines

### Typography for OG Images

```
HEADLINES:
- Size: 48-64px
- Weight: 600-700
- Max characters: ~60 for readability
- Line height: 1.1-1.2

BODY TEXT:
- Size: 20-24px
- Weight: 400-500
- Max characters: ~150

LABELS/BADGES:
- Size: 14-16px
- Weight: 500-600
- All caps with letter-spacing
```

### Color Considerations

```
HIGH CONTRAST:
- Text must be readable at small sizes
- Test at 400px wide (preview size)
- Dark bg + light text or light bg + dark text

AVOID:
- Low contrast combinations
- Thin fonts on busy backgrounds
- Text without background treatment over images

SAFE CHOICES:
- Dark: #0a0a0a, #1a1a1a
- Light: #ffffff, #fafafa
- Text on dark: #ffffff, #f5f5f5
- Text on light: #0a0a0a, #171717
```

### Composition Rules

```
HIERARCHY:
1. Brand/Logo (optional, subtle)
2. Main headline (largest, most prominent)
3. Supporting text (secondary)
4. Visual element (product, illustration)

ALIGNMENT:
- Left-aligned text is most readable
- Centered works for short headlines
- Right-aligned rarely works

BALANCE:
- Don't center everything
- Use asymmetric layouts
- Leave breathing room (don't fill every pixel)
```

---

## Testing Tools

### Preview Your OG Images

| Tool | URL | Purpose |
|------|-----|---------|
| Twitter Card Validator | cards-dev.twitter.com/validator | Test Twitter cards |
| Facebook Debugger | developers.facebook.com/tools/debug | Test Facebook OG |
| LinkedIn Inspector | linkedin.com/post-inspector | Test LinkedIn cards |
| OpenGraph.xyz | opengraph.xyz | General preview |
| Metatags.io | metatags.io | Multi-platform preview |

### Common Issues

```
IMAGE NOT SHOWING:
- Check image URL is absolute (https://...)
- Verify image dimensions
- Check file size limits
- Clear platform cache (use debug tools)

WRONG IMAGE:
- Platform may have cached old image
- Use debug tools to refresh cache
- Add version query string: ?v=2

TEXT TRUNCATED:
- Title: Keep under 60 characters
- Description: Keep under 160 characters
```

---

## Quick Reference

### Minimum Requirements

```html
<!-- Absolute minimum for social sharing -->
<meta property="og:title" content="Title">
<meta property="og:description" content="Description">
<meta property="og:image" content="https://example.com/image.png">
<meta name="twitter:card" content="summary_large_image">
```

### Checklist

- [ ] OG image is 1200×630
- [ ] Image file size under 5MB
- [ ] Image URL is absolute (https://)
- [ ] Title under 60 characters
- [ ] Description under 160 characters
- [ ] All URLs are valid
- [ ] Tested on Twitter, Facebook, LinkedIn
- [ ] Image looks good at small size (preview)
