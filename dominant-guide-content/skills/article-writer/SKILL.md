---
name: article-writer
description: Write SEO-optimized articles for Dominant Guide. Use when user asks to "write an article", "create content about...", "draft a blog post", or needs new articles for the site. Incorporates brand voice and SEO best practices.
---

# Article Writer for Dominant Guide

Create SEO-optimized, brand-aligned articles for dominant-guide.com.

## Brand Voice Guidelines

**Tone:** Direct, confident, no-BS. Speaks to men who feel nervous about dominance.

**Style:**
- Practical and real, not preachy or academic
- Anti-design aesthetic (bold, breaks conventions)
- Empathetic but not soft - understands the reader's fears
- Uses "you" directly, creates dialogue feel
- Short paragraphs, scannable structure

**Avoid:**
- Generic fluff ("In this article, we will discuss...")
- Academic or clinical language
- Judgmental tone about kinks/preferences
- Clickbait without substance

## Article Structure Template

```markdown
---
title: "[Compelling Title - 50-60 chars]"
description: "[Meta description - 150-160 chars with keyword]"
pubDate: "[YYYY-MM-DD]"
author: "Linus"
category: "[One of: Dominance, Communication, Trust, Consent, Boundaries, Aftercare, Safety, Techniques, Psychology, Relationships]"
tags: ["tag1", "tag2", "tag3"]
image: "/images/blog/[slug].webp"
imageAlt: "[Descriptive alt text]"
draft: false
---

[Hook - 2-3 sentences that connect with reader's struggle/desire]

## [First H2 - Target keyword variation]

[Content - practical, actionable]

### [H3 subheading if needed]

[More specific content]

## [Second H2 - Related aspect]

[Content with examples]

> **Pro Tip:** [Actionable insight in blockquote]

## [Third H2 - Deeper exploration]

[Content addressing common concerns/questions]

## Common Questions

**[Question 1 from reader perspective]**

[Direct answer, 2-3 sentences]

**[Question 2]**

[Direct answer]

## Key Takeaways

- [Actionable point 1]
- [Actionable point 2]
- [Actionable point 3]

---

*[Closing thought that encourages practice/exploration]*
```

## SEO Requirements

### Title Optimization
- Include primary keyword near the beginning
- 50-60 characters ideal
- Create curiosity or promise value
- Avoid clickbait that doesn't deliver

### Meta Description
- 150-160 characters
- Include primary keyword naturally
- End with implicit CTA or benefit
- Match search intent

### Content Structure
- **Word count:** 1,500-2,500 words minimum for pillar content
- **H2 headings:** Every 200-300 words
- **Internal links:** 3-5 to related articles
- **External links:** 1-2 to authoritative sources (if appropriate)

### Keyword Integration
- Primary keyword in: title, first 100 words, one H2, meta description
- LSI keywords naturally throughout
- Avoid keyword stuffing - write for humans first

### FAQ Schema
Include 3-5 FAQs that can be marked up with FAQ schema. Format as:
```
**[Question]?**

[Answer in 2-3 sentences]
```

## Content Categories & Angles

### Dominance
- Building confidence as a Dom
- Leadership in D/s relationships
- Developing your dominant style
- Scene planning and execution

### Communication
- Negotiation techniques
- Expressing desires clearly
- Difficult conversations
- Check-ins during scenes

### Trust
- Building trust with a new partner
- Maintaining trust long-term
- Recovering from trust issues
- Vulnerability as strength

### Consent
- Negotiating boundaries
- Ongoing consent practices
- When to pause or stop
- Consent in established relationships

### Boundaries
- Setting your own limits
- Respecting partner limits
- When boundaries change
- Hard vs soft limits

### Aftercare
- Physical aftercare essentials
- Emotional aftercare
- Dom drop and self-care
- Aftercare for different scene types

### Safety
- Risk-aware practices
- Physical safety by activity
- Emotional safety
- Emergency protocols

### Techniques
- Specific skills and how-tos
- Beginner-friendly practices
- Advanced techniques
- Equipment and tools

### Psychology
- Understanding power dynamics
- Mental aspects of D/s
- Motivation and desire
- Processing intense experiences

### Relationships
- D/s in long-term partnerships
- Dating as a Dom
- Relationship structures
- Balancing D/s with vanilla life

## Internal Linking Strategy

Always include links to:
1. **The quiz** (`/quiz`) - when discussing self-discovery or types
2. **Related category pages** (`/articles/category/[category]`)
3. **3-5 related articles** from same or adjacent categories

Example link formats:
```markdown
If you're still figuring out your style, [take our quiz](/quiz) to discover your dominant type.

For more on this topic, see our guide to [building trust in D/s relationships](/articles/building-trust-in-a-dom-sub-relationship).
```

## Process

1. **Research Phase**
   - Identify target keyword and search intent
   - Check existing articles to avoid duplication
   - Review competitor content for gaps
   - Gather unique angles or insights

2. **Outline Phase**
   - Create H2 structure
   - Plan internal links
   - Identify FAQ opportunities
   - Note key points for each section

3. **Writing Phase**
   - Write hook first (most important)
   - Fill in sections with practical content
   - Add examples and scenarios
   - Include pro tips and callouts

4. **Optimization Phase**
   - Check keyword placement
   - Verify internal links work
   - Add meta description
   - Review for brand voice consistency

## Example Hook Styles

**The Relatable Struggle:**
"You've read the guides. Watched the tutorials. But when it's time to actually take control, something holds you back. That hesitation isn't weakness—it's awareness. And with the right approach, it becomes your strength."

**The Direct Challenge:**
"Most 'how to be a Dom' advice misses the point entirely. It focuses on what to do instead of who to become. Let's fix that."

**The Promise:**
"In the next 10 minutes, you'll learn the three principles that separate confident Doms from those who are just going through the motions."

## Output Format

When writing an article, provide:

1. **Complete markdown file** ready to save to `/src/content/articles/[slug].md`
2. **Image prompt** for generating a hero image
3. **Internal linking suggestions** based on existing content
4. **Social media snippets** (optional, for promotion)
