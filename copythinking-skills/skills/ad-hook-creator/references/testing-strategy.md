# Testing & Iteration Strategy

## Metrics to Track

### Primary Metrics

**Hook Rate (Thumb-Stop Rate)**
- Definition: % of people who stop scrolling
- Benchmark: 40%+ = good, 60%+ = excellent
- Platform: Meta Ads Manager / TikTok Analytics

**Hold Rate (3-Second View Rate)**
- Definition: % who watch first 3 seconds
- Benchmark: 50%+ = good, 70%+ = excellent
- Shows if hook delivers on promise

**Click-Through Rate (CTR)**
- Definition: % who click after watching
- Benchmark: 1-3% = average, 5%+ = excellent
- Ultimate conversion metric

### Secondary Metrics

**Average Watch Time**
- Indicates if content after hook is engaging
- Platform-specific benchmarks

**Cost Per Click (CPC)**
- Lower CPC = more efficient hook
- Compare across hook variations

**Comment Sentiment**
- Qualitative feedback on hook relevance
- Look for "this is me" comments

---

## A/B Testing Framework

### What to Test

**Test 1: Hook Type**
- Variant A: Demographic Hook
- Variant B: Wild Visual Hook
- Keep: Everything else identical
- Duration: 3-5 days, min. 1000 impressions each

**Test 2: Visual Style**
- Variant A: Polished production
- Variant B: Raw iPhone footage
- Keep: Same hook text
- Platform-dependent (TikTok prefers raw, LinkedIn prefers polished)

**Test 3: Text Overlay**
- Variant A: Large text, top position
- Variant B: Medium text, center position
- Variant C: No text overlay
- Keep: Same hook concept

**Test 4: Opening Frame**
- Variant A: Product visible immediately
- Variant B: Problem/pain point first
- Keep: Same overall hook

### Testing Rules

✅ **DO:**
- Test ONE variable at a time
- Run tests for min. 3 days
- Need min. 1000 impressions per variant for significance
- Document all results

❌ **DON'T:**
- Change multiple variables simultaneously
- Kill tests too early (<24 hours)
- Test with insufficient budget (<€50 per variant)
- Ignore statistical significance

---

## Performance Diagnosis

### Scenario 1: Low Hook Rate (<30%)

**Diagnosis:**
Hook nicht auffällig genug oder falsche Zielgruppe

**Fixes:**
1. Wechsel Hook-Typ (z.B. von Demographic zu Wild Visual)
2. Stärkerer Pattern Interrupt in erster Sekunde
3. Größerer Text-Overlay mit kontrastreicheren Farben
4. Zielgruppen-Targeting überprüfen

**Action Items:**
- Test Hook 2 (Wild Visual) oder Hook 10 (Stacking)
- Text-Overlay von 60pt auf 80pt vergrößern
- Ersten Frame komplett austauschen

### Scenario 2: Good Hook Rate (>50%) but Low Hold Rate (<30%)

**Diagnosis:**
Hook verspricht etwas, das nicht geliefert wird (Clickbait)

**Fixes:**
1. Hook-Promise im Video einlösen
2. Schnellere Cuts (mehr Dynamik)
3. Text-Overlay im Video fortsetzen (nicht nur Hook)
4. Sofort zum Nutzen kommen (weniger Intro)

**Action Items:**
- Ersten 3 Sekunden nach Hook überarbeiten
- Pattern Interrupts einbauen (alle 1-2 Sek)
- Testen: "Fast-paced" vs. "Slow-burn" Editing

### Scenario 3: Good Hook + Hold but Low CTR (<1%)

**Diagnosis:**
Hook und Content gut, aber CTA/Offer schwach

**Fixes:**
1. Klarere CTA ("Jetzt Link klicken")
2. Stärkeres Angebot (Discount, Free Trial)
3. Urgency hinzufügen ("Nur diese Woche")
4. Social Proof ergänzen (Testimonials)

**Action Items:**
- CTA-Text vergrößern und früher zeigen
- Testen: verschiedene Offers (10% vs. Free Trial)
- Landing Page Congruence prüfen

### Scenario 4: Platform funktioniert, anderer nicht

**Diagnosis:**
Platform-Mismatch in Tonalität oder Format

**Fixes:**
1. Hook an Platform anpassen (siehe Platform-Spezifikationen)
2. Format anpassen (9:16 vs. 1:1 vs. 16:9)
3. Tonalität adjustieren (LinkedIn formeller, TikTok rawer)

**Example:**
- LinkedIn: Hook 1, 3, 8 testen
- TikTok: Hook 2, 6, 7, 9 testen
- Meta: Hook 4, 5, 8 testen

---

## Iteration Playbook

### After 1 Week (Initial Data)

**If Hook Rate <40%:**
→ Complete hook redesign (neuer Hook-Typ)
→ Test Hook 2 (Wild Visual) oder Hook 10 (Stacking)

**If Hook Rate 40-60%:**
→ Optimize existing hook (größerer Text, stärkere Colors)
→ Test 3 Variationen des selben Hook-Typs

**If Hook Rate >60%:**
→ Scale budget, don't change hook
→ Test new audiences with same hook

### After 2 Weeks (Refinement)

**Review all metrics together:**
- Hook Rate + Hold Rate + CTR = full picture
- Identify weakest link in funnel

**Create new test variants:**
- Use learnings from Week 1
- Test 2-3 completely new hooks (different frameworks)
- Keep best performer running at 60% budget

### After 1 Month (Scale or Kill)

**Decision Matrix:**

| Hook Rate | Hold Rate | CTR | Decision |
|-----------|-----------|-----|----------|
| >50% | >50% | >2% | SCALE - increase budget 3x |
| >50% | >50% | <2% | FIX CTA - keep testing |
| >50% | <40% | any | FIX CONTENT - hook misleads |
| <40% | any | any | KILL - try new hook framework |

---

## Advanced Techniques

### Winner Re-Test
- Hook that performed well can decline over time (ad fatigue)
- Re-test winner every 30 days with new creative variation
- Keep core hook, change visuals/voice/setting

### Seasonal Adjustments
- Q4: Add urgency, limited time hooks
- January: New year, fresh start messaging
- Summer: Lighter tonality, vacation context

### Audience Segmentation Testing
- Test same hook on different audience segments
- Example: "30-40 years" vs. "40-50 years"
- Winning hook may differ by age/gender/location

### Sequential Hook Testing
- After user sees Hook A, show Hook B
- Builds familiarity, addresses objections
- Example: Hook 1 (Awareness) → Hook 8 (Consideration)

---

## Documentation Template

Use this for every hook test:

```
## Hook Test #[Number]

**Date:** [Start - End]
**Platform:** [Meta/LinkedIn/TikTok]
**Budget:** €[X]
**Audience:** [Description]

**Hook Type:** [1-10]
**Hook Text:** "[Exact text]"

**Results:**
- Impressions: [X]
- Hook Rate: [X]%
- Hold Rate: [X]%
- CTR: [X]%
- CPC: €[X]

**Insights:**
- [What worked]
- [What didn't work]
- [Audience feedback]

**Next Actions:**
- [Test variation X]
- [Try hook type Y]
- [Adjust Z]
```

---

## Quick Decision Guide

**If you need to decide quickly which hook to test:**

1. **Know your audience awareness:**
   - Problem-aware → Hook 1, 7, 8
   - Solution-aware → Hook 3, 4, 8
   - Product-aware → Hook 5, 6, 9

2. **Know your production capacity:**
   - Low budget → Hook 6, 7, 9 (can shoot on phone)
   - Medium budget → Hook 1, 3, 4, 8
   - High budget → Hook 2, 10 (needs editing/KI)

3. **Know your platform:**
   - LinkedIn → Hook 1, 3, 8
   - TikTok → Hook 2, 6, 7, 9
   - Meta → Hook 4, 5, 8
   - YouTube → Hook 3, 7, 10

4. **Know your urgency:**
   - Need results fast → Test Hook 8 (highest success rate)
   - Can test longer → Test all 10, find best performer
