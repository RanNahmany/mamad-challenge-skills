# HTML Boilerplate

Every presentation starts from this scaffold. Replace the style block and slide content.
The JS animation system, navigation, safe zones, and responsive rules are identical in every presentation.

---

## Complete Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[PRESENTATION TITLE]</title>
    <!-- Optional: Add Google Fonts import here if the style requires it -->
    <style>
        /* ============================================================
           RESET & BASE
        ============================================================ */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html, body { height: 100%; overflow: hidden; }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'SF Pro Display', 'Inter', 'Helvetica Neue', sans-serif;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            /* REPLACE: background, color from style catalog */
            background: #000;
            color: #fff;
        }

        /* ============================================================
           LAYOUT — Stage + Slides
        ============================================================ */
        .deck {
            width: 100vw;
            height: 100vh;
            display: grid;
            place-items: center;
            position: relative;
        }

        .stage {
            width: min(1400px, calc(100vw - 80px));
            height: min(800px, calc(100vh - 160px));
            border-radius: 30px;
            position: relative;
            overflow: hidden;
            /* REPLACE: background, border, backdrop-filter from style catalog */
        }

        .slides-container {
            width: 100%;
            height: 100%;
            position: relative;
            overflow: hidden;
        }

        .slide {
            width: 100%;
            height: 100%;
            position: absolute;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            gap: 20px;
            padding: 80px 40px 100px 40px; /* NEVER exceed 100px vertical */
            max-height: calc(100vh - 220px);
            overflow: hidden;
            opacity: 0;
            /* REPLACE: transition style from style catalog */
            transform: translateY(20px);
            transition: opacity 0.6s cubic-bezier(0.16, 1, 0.3, 1),
                        transform 0.6s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .slide.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .slide .content {
            max-width: 1100px;
            width: 100%;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            max-height: calc(100vh - 260px);
        }

        /* ============================================================
           TYPOGRAPHY HIERARCHY (strict limits — never override maximums)
        ============================================================ */
        h1 {
            font-size: clamp(36px, 5vw, 60px); /* MAX 60px */
            font-weight: 900;
            line-height: 1.2;
            margin: 0 0 15px 0;
        }

        h2 {
            font-size: clamp(18px, 2.2vw, 24px); /* MAX 24px */
            font-weight: 600;
            line-height: 1.4;
            margin: 8px 0 25px 0;
        }

        .big {
            font-size: clamp(20px, 2.8vw, 28px); /* MAX 28px */
            font-weight: 700;
            line-height: 1.4;
            margin: 15px 0;
        }

        .huge {
            font-size: clamp(42px, 6vw, 72px); /* MAX 72px — use sparingly */
            font-weight: 900;
            line-height: 1.1;
            margin: 10px 0;
        }

        .glow-text {
            color: #22d3ee;
            text-shadow: 0 0 30px rgba(34, 211, 238, 0.5);
        }

        /* ============================================================
           COLOR PSYCHOLOGY BADGES
        ============================================================ */
        .badge {
            display: inline-block;
            padding: 8px 16px;
            font-size: 14px;
            font-weight: 600;
            border-radius: 50px;
            margin: 4px;
            opacity: 0; /* hidden until .animate-in */
            transform: translateY(20px);
            transition: all 0.5s cubic-bezier(0.16, 1, 0.3, 1);
        }
        .badge.animate-in { opacity: 1; transform: translateY(0); }

        .badge-danger  { background: rgba(239,68,68,0.2);   color: #f87171; border: 1px solid rgba(239,68,68,0.3); }
        .badge-success { background: rgba(34,197,94,0.2);   color: #4ade80; border: 1px solid rgba(34,197,94,0.3); }
        .badge-primary { background: rgba(6,182,212,0.2);   color: #22d3ee; border: 1px solid rgba(6,182,212,0.3); }
        .badge-warning { background: rgba(245,158,11,0.2);  color: #fbbf24; border: 1px solid rgba(245,158,11,0.3); }

        /* ============================================================
           COMPARISON CARDS
        ============================================================ */
        .comparison-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
            margin: 20px auto;
            max-width: 900px;
            width: 100%;
        }

        .comparison-card {
            padding: 25px 20px;
            border-radius: 16px;
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.5s cubic-bezier(0.16, 1, 0.3, 1);
        }
        .comparison-card.animate-in { opacity: 1; transform: translateY(0); }

        .comparison-old {
            border: 1px solid rgba(239,68,68,0.3);
            background: rgba(239,68,68,0.05);
        }
        .comparison-new {
            border: 2px solid rgba(34,197,94,0.5);
            background: rgba(34,197,94,0.05);
        }

        /* ============================================================
           EXAMPLES / FEATURES GRID
        ============================================================ */
        .examples-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin: 20px auto;
            max-width: 900px;
            width: 100%;
        }

        .example-card, .metric-card {
            padding: 25px 20px;
            border-radius: 16px;
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.5s cubic-bezier(0.16, 1, 0.3, 1);
        }
        .example-card.animate-in,
        .metric-card.animate-in { opacity: 1; transform: translateY(0); }

        /* ============================================================
           GLASS CARD (for CTA slides)
        ============================================================ */
        .glass-card {
            background: rgba(255,255,255,0.05);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 20px;
            padding: 30px 25px;
            max-width: 700px;
            width: 100%;
            margin: 20px auto;
        }

        /* ============================================================
           CTA BUTTON
        ============================================================ */
        .cta-button {
            display: inline-block;
            padding: 16px 40px;
            background: linear-gradient(135deg, #22d3ee, #0ea5e9);
            color: #000;
            font-size: 16px;
            font-weight: 700;
            border-radius: 50px;
            text-decoration: none;
            margin-top: 20px;
            box-shadow: 0 0 30px rgba(34, 211, 238, 0.4),
                        0 0 60px rgba(34, 211, 238, 0.2);
            transition: all 0.3s ease;
            cursor: pointer;
        }
        .cta-button:hover {
            transform: scale(1.04);
            box-shadow: 0 0 40px rgba(34,211,238,0.6), 0 0 80px rgba(34,211,238,0.3);
        }

        /* ============================================================
           DENSE SLIDE VARIANT (for content-heavy slides)
        ============================================================ */
        .slide.dense { gap: 10px; }
        .slide.dense h1 { font-size: clamp(32px, 4.5vw, 50px); margin: 0 0 10px 0; }
        .slide.dense h2 { font-size: clamp(16px, 2vw, 20px); margin: 5px 0 15px 0; }
        .slide.dense .badge { font-size: 12px; padding: 6px 12px; margin: 2px; }
        .slide.dense .comparison-grid { gap: 15px; margin: 15px auto; }

        /* ============================================================
           NAVIGATION CHROME
        ============================================================ */
        .progress-bar {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 1000;
            width: 200px;
            height: 3px;
            background: rgba(255,255,255,0.1);
            border-radius: 2px;
            overflow: hidden;
        }
        .progress-fill {
            height: 100%;
            background: #22d3ee;
            border-radius: 2px;
            transition: width 0.3s ease;
        }

        .nav-dots {
            position: fixed;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 1000;
            display: flex;
            gap: 8px;
            background: rgba(0,0,0,0.2);
            backdrop-filter: blur(10px);
            padding: 8px 16px;
            border-radius: 20px;
        }
        .dot {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background: rgba(255,255,255,0.3);
            cursor: pointer;
            transition: all 0.3s ease;
        }
        .dot.active {
            background: #22d3ee;
            transform: scale(1.3);
        }

        /* ============================================================
           RESPONSIVE — Mobile
        ============================================================ */
        @media (max-width: 768px) {
            .deck { padding: 20px; }
            .stage { border-radius: 20px; }
            .slide { padding: 40px 25px 60px 25px; gap: 15px; }
            h1 { font-size: clamp(28px, 8vw, 48px); margin-bottom: 10px; }
            h2 { font-size: clamp(16px, 4vw, 20px); margin: 5px 0 20px 0; }
            .big { font-size: clamp(18px, 4vw, 24px); }
            .huge { font-size: clamp(32px, 8vw, 56px); }
            .comparison-grid, .examples-grid { grid-template-columns: 1fr; gap: 20px; }
        }

        /* ============================================================
           RESPONSIVE — Short viewports
        ============================================================ */
        @media (max-height: 700px) {
            .slide { padding: 60px 30px 80px 30px; gap: 10px; }
            h1 { font-size: clamp(28px, 4vw, 44px) !important; }
            h2 { font-size: clamp(14px, 1.8vw, 18px) !important; }
            .big { font-size: clamp(16px, 2.4vw, 22px) !important; }
            .comparison-grid, .examples-grid { gap: 12px; }
        }
        @media (max-height: 600px) {
            .slide { padding: 40px 25px 60px 25px; gap: 8px; }
        }

    </style>
</head>
<body>

<!-- Optional: background layer (radial gradients, particles, grid) goes here -->

<div class="deck">
    <!-- Progress bar -->
    <div class="progress-bar"><div class="progress-fill" id="progressFill"></div></div>

    <div class="stage">
        <div class="slides-container" id="slidesContainer">

            <!-- ================================================
                 SLIDES GO HERE
                 Each slide: <div class="slide" id="slide-N"> ... </div>
                 Use .dense class for content-heavy slides
            ================================================ -->

            <!-- SLIDE 1: Opening hook -->
            <div class="slide" id="slide-1">
                <div class="content">
                    <h1>[HOOK HEADLINE]</h1>
                    <h2>[Supporting context]</h2>
                </div>
            </div>

            <!-- ... more slides ... -->

            <!-- FINAL SLIDE: Lead Magnet CTA (ALWAYS REQUIRED) -->
            <div class="slide" id="slide-final">
                <div class="content">
                    <h1>Get The Complete <span class="glow-text">[Playbook/Guide]</span></h1>
                    <h2>Everything you need to [specific outcome]</h2>
                    <div class="glass-card">
                        <h3 style="color: #22d3ee; margin-bottom: 20px; font-size: 18px;">The [Name] Includes:</h3>
                        <div style="text-align: left; display: flex; flex-direction: column; gap: 12px; font-size: 15px;">
                            <div><span style="color: #22d3ee; font-weight: 700;">✓</span> [Specific benefit — include a number if possible]</div>
                            <div><span style="color: #22d3ee; font-weight: 700;">✓</span> [Specific benefit]</div>
                            <div><span style="color: #22d3ee; font-weight: 700;">✓</span> [Specific benefit]</div>
                            <div><span style="color: #22d3ee; font-weight: 700;">✓</span> [Specific benefit]</div>
                            <div><span style="color: #22d3ee; font-weight: 700;">✓</span> [Specific benefit]</div>
                        </div>
                    </div>
                    <a href="#" class="cta-button">Download The [Resource] →</a>
                    <p style="font-size: 13px; opacity: 0.4; margin-top: 10px;">Free instant download. No spam, ever.</p>
                </div>
            </div>

        </div><!-- /slides-container -->
    </div><!-- /stage -->

    <!-- Navigation dots -->
    <div class="nav-dots" id="navDots"></div>
</div><!-- /deck -->


<script>
    // ============================================================
    // ANIMATION & NAVIGATION ENGINE
    // ============================================================
    const slides = document.querySelectorAll('.slide');
    const navDots = document.getElementById('navDots');
    const progressFill = document.getElementById('progressFill');
    let currentSlide = 0;
    let currentAnimationStep = 0;

    // ============================================================
    // DEFINE SEQUENTIAL ANIMATIONS PER SLIDE
    // Add entries for slides that need user-triggered sequential reveals.
    // Leave a slide out of this object → all elements show immediately.
    //
    // Example:
    // slideAnimations[2] = [
    //     () => slides[2].querySelectorAll('.comparison-card')[0].classList.add('animate-in'),
    //     () => slides[2].querySelectorAll('.comparison-card')[0].querySelectorAll('.badge')[0].classList.add('animate-in'),
    //     () => slides[2].querySelectorAll('.comparison-card')[0].querySelectorAll('.badge')[1].classList.add('animate-in'),
    //     () => slides[2].querySelectorAll('.comparison-card')[1].classList.add('animate-in'),
    //     () => slides[2].querySelectorAll('.comparison-card')[1].querySelectorAll('.badge')[0].classList.add('animate-in'),
    // ];
    // ============================================================
    const slideAnimations = {};

    // FILL IN ANIMATIONS HERE — one entry per animated slide
    // slideAnimations[N] = [ () => ..., () => ..., ];


    // ============================================================
    // CORE FUNCTIONS
    // ============================================================

    function initializeSlideElements(index) {
        const slide = slides[index];
        if (!slideAnimations[index]) {
            // No sequential animations: show everything immediately
            slide.querySelectorAll('.badge, .metric-card, .example-card, .comparison-card, .timeline-item')
                .forEach(el => el.classList.add('animate-in'));
        }
        // Animated slides: content stays hidden until user presses Space/Arrow
    }

    function updateProgress() {
        const pct = slides.length > 1 ? (currentSlide / (slides.length - 1)) * 100 : 100;
        progressFill.style.width = pct + '%';
    }

    function updateDots() {
        document.querySelectorAll('.dot').forEach((dot, i) => {
            dot.classList.toggle('active', i === currentSlide);
        });
        updateProgress();
    }

    function scrollToSlide(index) {
        if (index < 0 || index >= slides.length) return;
        slides[currentSlide].classList.remove('visible');
        currentSlide = index;
        currentAnimationStep = 0;
        slides[currentSlide].classList.add('visible');
        initializeSlideElements(currentSlide);
        updateDots();
    }

    function nextAction() {
        const animations = slideAnimations[currentSlide];
        if (animations && currentAnimationStep < animations.length) {
            animations[currentAnimationStep]();
            currentAnimationStep++;
        } else {
            if (currentSlide < slides.length - 1) scrollToSlide(currentSlide + 1);
        }
    }

    // ============================================================
    // KEYBOARD CONTROLS
    // ============================================================
    document.addEventListener('keydown', (e) => {
        if (e.key === ' ' || e.key === 'ArrowRight') { e.preventDefault(); nextAction(); }
        else if (e.key === 'ArrowLeft') { e.preventDefault(); if (currentSlide > 0) scrollToSlide(currentSlide - 1); }
        else if (e.key === 'ArrowUp') { e.preventDefault(); if (currentSlide > 0) scrollToSlide(currentSlide - 1); }
        else if (e.key === 'ArrowDown') { e.preventDefault(); nextAction(); }
    });

    // ============================================================
    // INIT
    // ============================================================

    // Build nav dots
    slides.forEach((_, i) => {
        const dot = document.createElement('div');
        dot.className = 'dot';
        dot.addEventListener('click', () => scrollToSlide(i));
        navDots.appendChild(dot);
    });

    // Show first slide
    scrollToSlide(0);
</script>

</body>
</html>
```

---

## Key Customization Points

When applying a style from `styles-catalog.md`, replace these sections:

### 1. `body` background and color
```css
body {
    background: [FROM CATALOG];
    color: [FROM CATALOG];
}
```

### 2. `stage` visual
```css
.stage {
    background: [glass / solid / none];
    backdrop-filter: [if glassmorphism];
    border: [if applicable];
    box-shadow: [if applicable];
}
```

### 3. `h1` treatment
```css
h1 {
    /* Option A: gradient text */
    background: linear-gradient(...);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;

    /* Option B: glow */
    text-shadow: 0 0 30px [color];

    /* Option C: plain */
    color: [color];
}
```

### 4. Slide transition
Most styles use one of:
```css
/* Scale (Apple keynote) */
.slide { transform: scale(0.95); }
.slide.visible { transform: scale(1); }

/* Slide up (most common) */
.slide { transform: translateY(20px); }
.slide.visible { transform: translateY(0); }
```

### 5. Card styling
Apply the card background/border/radius from the catalog entry.

---

## Adding Sequential Animations

For slides with 3+ elements that should reveal one-by-one:

```javascript
// After the slideAnimations = {}; declaration, add:
const s = slides; // shorthand

slideAnimations[2] = [
    () => s[2].querySelectorAll('.badge')[0].classList.add('animate-in'),
    () => s[2].querySelectorAll('.badge')[1].classList.add('animate-in'),
    () => s[2].querySelectorAll('.badge')[2].classList.add('animate-in'),
];

slideAnimations[4] = [
    // Comparison: show left card first, then its badges, then right card + its badges
    () => s[4].querySelectorAll('.comparison-card')[0].classList.add('animate-in'),
    () => s[4].querySelectorAll('.comparison-card')[0].querySelectorAll('.badge')[0].classList.add('animate-in'),
    () => s[4].querySelectorAll('.comparison-card')[0].querySelectorAll('.badge')[1].classList.add('animate-in'),
    () => s[4].querySelectorAll('.comparison-card')[1].classList.add('animate-in'),
    () => s[4].querySelectorAll('.comparison-card')[1].querySelectorAll('.badge')[0].classList.add('animate-in'),
    () => s[4].querySelectorAll('.comparison-card')[1].querySelectorAll('.badge')[1].classList.add('animate-in'),
];
```

## Counting Number Animation (for big metric slides)

```javascript
function countUp(element, target, duration = 1500, prefix = '', suffix = '') {
    const start = performance.now();
    function update(time) {
        const elapsed = time - start;
        const progress = Math.min(elapsed / duration, 1);
        const eased = 1 - Math.pow(1 - progress, 3); // ease-out cubic
        element.textContent = prefix + Math.round(target * eased).toLocaleString() + suffix;
        if (progress < 1) requestAnimationFrame(update);
    }
    requestAnimationFrame(update);
}

// Usage in slideAnimations:
slideAnimations[6] = [
    () => {
        const el = slides[6].querySelector('.huge');
        el.classList.add('animate-in');
        countUp(el, 4000000000, 2000, '$', '');
    }
];
```
