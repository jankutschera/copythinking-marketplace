---
name: lead-magnet-architect
description: Create lead magnets, landing pages, and email sequences. Use when user asks to "create a lead magnet", "build a landing page", "design an opt-in", "email sequence", or "freebie".
---

# Lead Magnet Architect for Dominant Guide

Design and create lead magnets, landing pages, and email sequences that convert.

## Current Lead Magnets

| Name | Type | File | Landing Page |
|------|------|------|--------------|
| The Dom's Odyssey | PDF Guide | `/documents/the-doms-odyssey.pdf` | `/21-day-dominance-challenge/` |
| BDSM Kink Checklist | PDF Checklist | `/documents/The-BDSM-Checklist.pdf` | - |
| Emotional Roadmap Template | PDF Template | `/documents/Emotional-Roadmap-Template.pdf` | - |
| Pervertibles Safety Checklist | PDF Checklist | `/documents/Pervertibles-Safety-Checklist.pdf` | - |
| Scene Safety Bundle | PDF Bundle | `/documents/scene-safety-bundle.pdf` | - |

## Lead Magnet Types

### 1. PDF Guides (High Value)
- Comprehensive guides (20-50 pages)
- Professional design
- Actionable content
- Example: "The Dom's Odyssey"

### 2. Checklists (Quick Win)
- 1-3 pages
- Immediately actionable
- Print-friendly
- Example: "BDSM Kink Checklist"

### 3. Templates (Practical Tools)
- Fill-in-the-blank formats
- Reusable tools
- Example: "Emotional Roadmap Template"

### 4. Email Courses (Nurture)
- 5-7 day sequences
- Daily lessons
- Builds relationship
- Example: "7-Day Dominance Foundations"

### 5. Quizzes (Engagement)
- Personality-style results
- Shareable
- Segmentation tool
- Example: Current Dom Type Quiz

### 6. Video Training (Premium)
- Short video series
- Higher perceived value
- Personal connection

## Landing Page Framework

### Structure

```
[HERO SECTION]
├── Headline (Problem → Promise)
├── Subheadline (Specific benefit)
├── Lead Magnet Visual (mockup/preview)
└── Primary CTA Button

[PAIN POINTS]
├── "You're tired of..."
├── Bullet list of struggles
└── Empathy statement

[THE SOLUTION]
├── "Introducing [Lead Magnet Name]"
├── What's inside (specific deliverables)
└── Preview/table of contents

[SOCIAL PROOF]
├── Testimonials (if available)
├── Numbers ("Join 5,000+ Doms")
└── Trust indicators

[WHAT YOU'LL LEARN]
├── Benefit-focused bullets
├── Specific outcomes
└── Time frame if applicable

[ABOUT THE AUTHOR]
├── Linus photo
├── Brief credibility
└── Personal connection

[FINAL CTA]
├── Repeat offer
├── Email form
└── Privacy note
```

### Headline Formulas

**Problem-Solution:**
"Stop Second-Guessing. Start Leading with Confidence."

**Specific Promise:**
"The 5 Principles That Transform Nervous Beginners into Trusted Doms"

**Curiosity:**
"What 90% of 'How to Be a Dom' Guides Get Wrong"

**Direct Benefit:**
"Build Unshakeable Confidence in 21 Days"

### CTA Button Copy

Good examples:
- "Get Free Access"
- "Download Now (Free)"
- "Start Your Training"
- "Send Me the Guide"

Avoid:
- "Submit"
- "Sign Up"
- "Subscribe"

## Email Sequence Framework

### Welcome Sequence (After Opt-in)

**Email 1: Immediate Delivery**
- Subject: "Your [Lead Magnet] is here"
- Download link
- Quick win from the content
- Set expectations for future emails

**Email 2: Day 1 - Value Add**
- Subject: "[First lesson/tip from lead magnet]"
- Expand on one concept
- Personal story or example
- Soft quiz mention

**Email 3: Day 3 - Deeper Dive**
- Subject: "[Common question/misconception]"
- Address a struggle
- Provide framework or solution
- Related article link

**Email 4: Day 5 - Case Study/Story**
- Subject: "[Transformation story]"
- Before/after narrative
- What made the difference
- Invitation to reply

**Email 5: Day 7 - Next Step**
- Subject: "What's next for you?"
- Summarize the journey
- Quiz CTA if haven't taken
- Invite to explore more content

### Email Copy Guidelines

**Subject Lines:**
- 40-50 characters ideal
- Curiosity or benefit-focused
- Avoid spam triggers
- Test emoji sparingly

**Body Copy:**
- Short paragraphs (2-3 sentences)
- Conversational tone
- One main idea per email
- Single clear CTA

**Sign-off:**
```
Stay dangerous,
Linus

P.S. [Secondary thought or CTA]
```

## Lead Magnet Creation Process

### Step 1: Topic Selection

Criteria for good lead magnet topics:
- [ ] Solves a specific problem
- [ ] Quick to consume (20 min max)
- [ ] Immediately actionable
- [ ] Natural segue to paid offerings
- [ ] Not freely available elsewhere

### Step 2: Outline

```markdown
# [Lead Magnet Title]

## Quick Win
[What they can do/learn in 5 minutes]

## Core Content
### Section 1: [Topic]
### Section 2: [Topic]
### Section 3: [Topic]

## Action Steps
[Specific next actions]

## Additional Resources
[Links to articles, quiz, etc.]
```

### Step 3: Content Creation

Using copythinking skills:
1. `/analyze-copy` - Review for conversion
2. `/write-hook` - Generate compelling headlines
3. `/awareness-check` - Ensure right awareness level

### Step 4: Design

For PDF creation, use:
- `example-skills:pdf` - Generate PDF documents
- Brand colors: Use Dominant Guide palette
- Typography: Clean, readable
- Include: Logo, website URL, social links

### Step 5: Landing Page

Create Astro page at:
- `/src/pages/[lead-magnet-slug].astro`

Include:
- Kit form embed
- Proper meta tags
- noindex if gated

### Step 6: Email Integration

Kit (ConvertKit) setup:
1. Create form for lead magnet
2. Add tag for segmentation
3. Create automation sequence
4. Set up delivery email

## Lead Magnet Ideas Pipeline

### Based on Content Pillars

| Pillar | Lead Magnet Idea | Format |
|--------|------------------|--------|
| Dominance | "The Confident Dom Playbook" | PDF Guide |
| Communication | "50 Dom Commands Cheat Sheet" | PDF Checklist |
| Consent | "Negotiation Script Templates" | PDF Templates |
| Aftercare | "Aftercare Essentials Kit" | PDF Checklist |
| Safety | "Scene Planning Worksheet" | PDF Template |
| Techniques | "Beginner Bondage Guide" | PDF Guide |

### Based on Funnel Stage

| Stage | Lead Magnet Type | Goal |
|-------|------------------|------|
| Awareness | Quiz | Identify type, capture email |
| Interest | Checklist | Quick win, build trust |
| Consideration | Guide | Demonstrate expertise |
| Decision | Templates | Show practical value |

## Output Templates

### Landing Page (Astro)

```astro
---
import BaseLayout from '../layouts/BaseLayout.astro';
import Header from '../components/Header.astro';
import Footer from '../components/Footer.astro';

const title = "[Lead Magnet Name] | Dominant Guide";
const description = "[Meta description with benefit]";
---

<BaseLayout title={title} description={description}>
  <Header />
  <main class="landing-page">
    <!-- Hero, content sections, form -->
  </main>
  <Footer />
</BaseLayout>
```

### Email Sequence (for Kit)

```markdown
## Email 1: Delivery
**Subject:** Your [Lead Magnet] is ready
**Send:** Immediately

[Content]

---

## Email 2: First Value
**Subject:** [Curiosity hook]
**Send:** Day 1

[Content]
```

## Integration Points

### Input From
- **content-strategist** - Topic opportunities
- **competitor-monitor** - Competitor lead magnet analysis

### Output To
- **article-writer** - Related content to drive traffic
- Kit/ConvertKit - Email automation

### Skills to Use
- `copythinking-skills:analyze-copy` - Optimize landing page
- `copythinking-skills:write-hook` - Headlines and subject lines
- `example-skills:pdf` - PDF generation

## Quick Commands

**Create new lead magnet:**
"Create a lead magnet about [topic]"

**Design landing page:**
"Build a landing page for [lead magnet]"

**Write email sequence:**
"Create a 5-email welcome sequence for [lead magnet]"

**Analyze existing:**
"Review the conversion potential of [landing page URL]"
