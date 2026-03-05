# Script Transformation & Content Examples

## The Ran Nahmany Narrative Formula

Apply this arc to every presentation, regardless of topic:

```
1. HOOK        — Open with controversy, shock, or a surprising fact
2. VALIDATE    — Acknowledge their current struggle or belief ("you're right to feel this way")
3. REVEAL      — Show the hidden opportunity they're missing
4. PROVE       — Back it up with real data, examples, social proof
5. URGENCY     — "The window is open now" — without being pushy
6. TRANSITION  — Organic move to the CTA ("if you want to go further...")
```

---

## Script-to-Slide Transformation Rules

### The Core Translation Principle
**Features → Benefits. Technical → Human. Abstract → Concrete.**

| Wrong (feature) | Right (benefit) |
|----------------|----------------|
| "124GB storage" | "10,000 photos in your pocket" |
| "74.5% SWE benchmark" | "As good as a senior developer" |
| "Zero to one in 18 months" | "$1.5 billion from nothing" |
| "API costs dropped 97%" | "Enterprise AI for the price of lunch" |
| "55% faster task completion" | "Get home 2 hours earlier, every day" |

---

## Slide Pattern Library

### Pattern 1: Big Stat Slide
**When**: Script has a single powerful number
```
Script: "ChatGPT reached 100 million users in 2 months"

Slide:
  h1: "100 Million Users"
  .huge (with count-up animation): "2 Months"
  h2: "Fastest technology adoption in human history"
  badge-primary: "For context: TikTok took 9 months"
```

### Pattern 2: Comparison Slide (Old vs New)
**When**: Script contrasts two approaches, costs, or methods
```
Script: "Instead of hiring a developer at $120k/year, you build it yourself for $20/month"

Slide:
  h1: "The Real Cost Difference"
  .comparison-grid:
    .comparison-old (left):
      h3: "Hiring a Developer"
      .huge: "$120K/yr"
      badges: badge-danger "Full-time salary"
               badge-danger "Benefits & overhead"
               badge-danger "2-week notice to change anything"
    .comparison-new (right):
      h3: "Building It Yourself"
      .huge: "$20/mo"
      badges: badge-success "On demand"
               badge-success "Changes in hours"
               badge-success "You own it forever"
```

### Pattern 3: Three-Pill Formula
**When**: Script gives a 3-step process or a memorable triad
```
Script: "Build once, hand them the keys, sell forever"

Slide:
  Three side-by-side pill/card elements:
  [Build Once] → [Hand Over Keys] → [Sell Forever]
  Each as a .badge-primary or styled card
```

### Pattern 4: Quote Slide
**When**: Script has a powerful single statement / "mic drop"
```
Script: "I'm not a developer. I'm a problem solver who uses Claude Code."

Slide:
  Full width, vertically centered, two lines:
  "I'm not a developer."
  "I'm a problem solver."
  Subheadline (smaller, muted): "— Ran Nahmany"
```

### Pattern 5: Timeline
**When**: Script describes a progression over time
```
Script: "Amazon launched 1995 → eBay 1995 → Google 1998 → now AI"

Slide:
  Horizontal timeline:
  [1995 Amazon] → [1995 eBay] → [1998 Google] → [2022 ChatGPT] → [NOW: YOU]
  Each node reveals sequentially via animation
  Color code: early entries muted/gray, "NOW" in cyan with glow
```

### Pattern 6: Problem List → Solution Reveal
**When**: Script lists pain points then reveals the solution
```
Script: "You're using 5 different apps — Excel for tracking, WhatsApp for communication,
         email for invoices, Google Sheets for reports, Slack for team..."

Slide A (Problem):
  h1: "5 Apps for 1 Job"
  Grid of 5 cards: [Excel] [WhatsApp] [Email] [Google Sheets] [Slack]
  All with badge-danger red accents
  Animate in one by one (building frustration)

Slide B (Bridge):
  h1: "There's a Better Way"
  — transition slide, minimal content —

Slide C (Solution):
  h1: "One System"
  Single centered card with badge-success green accents
  "Everything in one place. Built for you."
```

### Pattern 7: Data Bar Chart
**When**: Script has comparative quantities
```
Script: "Midjourney makes $200M with 11 employees vs Adobe's $20B with 30,000"

Slide:
  h1: "Revenue Per Employee"
  Two bars, animated growing from 0:
  [Midjourney] bar (green/tall) → $18M per person
  [Adobe] bar (red/short) → $667K per person
  Headline below: "27x More Efficient"
```

### Pattern 8: Before/After World
**When**: Script contrasts the old world with the new world
```
Slide:
  h1: "Two Worlds"
  .comparison-grid:
    Left card (OLD WORLD — red accents):
      "The Old Way"
      badge-danger items: fragmented, manual, expensive, slow
    Right card (NEW WORLD — green accents):
      "The New Way"
      badge-success items: unified, automated, affordable, instant
```

### Pattern 9: Opportunity Window
**When**: Script creates urgency about a limited-time opportunity
```
Script: "We're in the deployment gap. Companies need AI but don't have it yet."

Slide A:
  h1: "The Gap"
  .huge: "75%"
  h2: "of CEOs say AI is critical..."

Slide B (immediate follow):
  h1: "...but only"
  .huge: "28%"  (in red or amber)
  h2: "have actually deployed it"
  badge-primary: "That gap = your opportunity"
```

### Pattern 10: Social Proof / Proof Slide
**When**: Script references real companies or results
```
Script: "Jasper AI went from zero to $1.5B valuation in 18 months"

Slide:
  h1: "It's Already Happening"
  Three metric cards (animate in):
  [Jasper AI: $0 → $1.5B in 18 months]
  [Midjourney: $200M revenue, 11 employees]
  [Perplexity: Challenging Google, 1/1000th the team]
  h2: "These aren't accidents. There's a pattern."
```

---

## Slide Trigger Words

Watch for these in the script — they always mean a new slide:

| Trigger | Action |
|---------|--------|
| "But..." | New slide — transition/contrast |
| "Here's the thing..." | New slide — new idea |
| "Therefore..." / "So..." | New slide — conclusion |
| "The real question is..." | New slide — reframe |
| "Picture this..." | New slide — scenario opening |
| New paragraph after data | New slide — digestion break |
| Emotional shift (fear → hope) | New slide — tone shift |
| Contrast phrase ("Instead of X...") | New slide — comparison begins |

---

## Slide Count Planning

| Script Length | Target Slides | Max Slides |
|--------------|--------------|-----------|
| Short (< 500 words) | 10-12 | 15 |
| Medium (500-1500 words) | 15-18 | 25 |
| Long (1500-3000 words) | 18-25 | 35 |
| Very long (3000+ words) | Suggest splitting | — |

**If script is too long**: Identify natural act breaks, suggest splitting into a series.

---

## Lead Magnet CTA Templates

### Template A: Playbook (best for strategy content)
```html
<h1>Get The Complete <span class="glow-text">Playbook</span></h1>
<h2>Everything you need to [close your first client / launch your first product / etc.]</h2>
<div class="glass-card">
    <h3 style="color: #22d3ee;">The [Topic] Playbook Includes:</h3>
    <div style="text-align: left; gap: 12px; display: flex; flex-direction: column;">
        <div><span style="color: #22d3ee; font-weight: 700;">✓</span> 20+ Discovery Questions (copy-paste ready)</div>
        <div><span style="color: #22d3ee; font-weight: 700;">✓</span> Exact Pricing Formula (3-tier structure)</div>
        <div><span style="color: #22d3ee; font-weight: 700;">✓</span> 30-Day Launch Roadmap</div>
        <div><span style="color: #22d3ee; font-weight: 700;">✓</span> 50+ AI Prompts for Client Work</div>
        <div><span style="color: #22d3ee; font-weight: 700;">✓</span> The Objection Handling Script</div>
    </div>
</div>
<a href="#" class="cta-button">Download The Playbook →</a>
<p style="font-size: 13px; opacity: 0.4; margin-top: 10px;">Free instant download. No spam, ever.</p>
```

### Template B: Guide (best for educational content)
```html
<h1>Download The Free <span class="glow-text">Guide</span></h1>
<h2>Your complete roadmap to [achieving the specific result]</h2>
<!-- same structure with guide-specific benefits -->
<a href="#" class="cta-button">Get The Guide →</a>
```

### Template C: Toolkit (best for tactical/tool content)
```html
<h1>Get The <span class="glow-text">Toolkit</span></h1>
<h2>All the tools and templates to [take action today]</h2>
<!-- benefits focused on templates, tools, frameworks -->
<a href="#" class="cta-button">Download The Toolkit →</a>
```

### CTA Content Rules
**ALWAYS include:**
- Specific numbers: "20+ questions", "50+ prompts", "7-step framework"
- Action words: "copy-paste", "fill-in-the-blank", "ready to use"
- Time references: "30-Day Plan", "in 48 hours"

**NEVER include:**
- "Learn the secrets" (vague)
- "Join 500+ members" (unless verified)
- "Become successful" (too generic)
- More than ONE main CTA button

---

## Tone by Content Type

### Urgent / Warning Tone
Used when: the audience is at risk of missing something or making a costly mistake
- Dark backgrounds (black)
- Red accents throughout
- Short, punchy sentences
- Stark, high-contrast slides
- Example headline: "The Window Is Closing"

### Opportunity / Exciting Tone
Used when: revealing a positive opportunity or new path
- Light/white backgrounds
- Blues and greens dominant
- Smooth, welcoming pacing
- "Breath of fresh air" feeling
- Example headline: "You're Earlier Than You Think"

### Educational / Methodical Tone
Used when: teaching a process or explaining a concept
- Clean, neutral backgrounds
- Purple or blue accents
- Clear hierarchical reveals
- One concept per slide, never rush
- Example headline: "Here's Exactly How It Works"

---

## Common Pitfalls & Fixes

| Problem | Fix |
|---------|-----|
| Slide feels crowded | Split into 2 slides OR add `.dense` class |
| Opening feels generic | Start with a shocking number, not a title |
| Data feels abstract | Add human context ("that's larger than the UK's GDP") |
| Comparisons feel flat | Animate left card first, then right — build the contrast |
| CTA feels salesy | Change language to "if you want to go further" framing |
| Animations feel disconnected | Add a bridge/transition slide between sections |
| Presentation feels too long | Cut any slide that doesn't advance the narrative |

---

## The Real Estate Rule

**Every slide earns its place by doing ONE of these:**
1. Hooks attention (opening slides)
2. Validates the problem (empathy slides)
3. Reveals the opportunity (insight slides)
4. Proves it's real (proof slides)
5. Creates stakes / urgency (tension slides)
6. Shows the path forward (solution slides)
7. Calls to action (CTA slide)

If a slide doesn't fit one of these jobs, cut it or merge it.
