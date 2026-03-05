# Style References Catalog

Each entry gives you the complete visual DNA to replicate a style without reading external files.
When the user says "in the style of [name]", use the matching entry below.

---

## apple-keynote-style (dark)
**Mood**: Cinematic, premium, dramatic
**Background**: `radial-gradient(ellipse at center, #1a1a1a 0%, #000000 100%)`
**Text color**: White with gradient `linear-gradient(180deg, #ffffff 0%, #c7c7c7 100%)` on `h1`
**Font**: `-apple-system, BlinkMacSystemFont, 'SF Pro Display', 'Helvetica Neue'`
**h1**: `clamp(56px, 8vw, 96px)`, weight 700, `letter-spacing: -0.02em`
**h2**: `clamp(24px, 3vw, 36px)`, color `#a1a1a1`
**Slide transition**: `transform: scale(0.95) → scale(1)`, `opacity 0→1`, `0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94)`
**Cards**: Dark glass — `background: rgba(255,255,255,0.05)`, `border: 1px solid rgba(255,255,255,0.1)`, `border-radius: 16px`
**Accent color**: `#ff375f` (Apple red) or cyan `#22d3ee`
**Special effects**: Gradient text on h1, subtle radial glow backgrounds
**Ideal for**: Product launches, dramatic reveals, urgent topics

---

## apple-keynote-style-light
**Mood**: Clean, airy, professional Apple product feel
**Background**: `linear-gradient(135deg, #ffffff 0%, #f5f5f7 100%)`
**Text color**: `#1d1d1f` with gradient `linear-gradient(180deg, #1d1d1f 0%, #424245 100%)` on h1
**Font**: `-apple-system, 'SF Pro Display', 'Helvetica Neue'`
**h1**: `clamp(56px, 8vw, 96px)`, weight 700, `letter-spacing: -0.02em`
**h2**: `clamp(24px, 3vw, 36px)`, color `#6e6e73`
**Slide transition**: `transform: scale(0.95) → scale(1)`, `0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94)`
**Cards**: White with subtle shadow — `background: #ffffff`, `box-shadow: 0 4px 20px rgba(0,0,0,0.08)`, `border-radius: 18px`
**Accent color**: `#0071e3` (Apple blue)
**Ideal for**: Educational content, opportunity-focused, professional services

---

## glassmorphism
**Mood**: Futuristic, vibrant, immersive
**Background**: Animated gradient — `background: linear-gradient(135deg, #667eea, #764ba2, #f093fb, #f5576c, #4facfe)`, `background-size: 400% 400%`, `animation: gradientShift 15s ease infinite`
**Text color**: White
**Font**: `-apple-system, "SF Pro Display", "Helvetica Neue"`
**Stage**: `background: rgba(255,255,255,0.1)`, `backdrop-filter: blur(20px) saturate(180%)`, `border: 1px solid rgba(255,255,255,0.2)`, `border-radius: 30px`
**Cards**: Glass — `background: rgba(255,255,255,0.15)`, `backdrop-filter: blur(15px)`, `border: 1px solid rgba(255,255,255,0.25)`, `border-radius: 20px`
**Special effects**: Floating particles (small white dots animated upward)
**Ideal for**: Tech announcements, futuristic topics, high-energy content

---

## dark-glowing-style
**Mood**: Deep tech, mysterious, powerful
**Background**: `radial-gradient(ellipse at 20% 50%, rgba(120,119,198,0.2), transparent), radial-gradient(ellipse at 80% 50%, rgba(59,130,246,0.15), transparent), #000000`
**Text color**: White
**Font**: `-apple-system, 'SF Pro Display', 'Inter'`
**Slide layout**: Horizontal scroll-snap, `scroll-snap-type: x mandatory`
**Cards**: `background: rgba(255,255,255,0.03)`, `border: 1px solid rgba(255,255,255,0.08)`, `border-radius: 16px`
**Accent**: Cyan `#22d3ee` and purple `#7877c6`
**Glow effects**: `box-shadow: 0 0 30px rgba(34,211,238,0.2)` on key elements
**Special**: Animated gradient orbs in background
**Ideal for**: Software/AI topics, dark mode preference, tech-forward content

---

## minimalist-clean
**Mood**: Editorial, calm, intelligent
**Background**: Pure white `#ffffff`
**Text color**: `#111827` (near black)
**Font**: `'Inter', sans-serif` (Google Fonts import)
**h1**: `clamp(48px, 8vw, 96px)`, weight 700, line-height 1.1, color `#111827`
**h2**: `clamp(20px, 2.5vw, 32px)`, weight 400, color `#6b7280`
**Slide transition**: `translateY(20px) → 0`, `opacity 0→1`, `0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94)`
**Cards**: `background: #f9fafb`, `border: 1px solid #e5e7eb`, `border-radius: 12px`
**Accent**: `#3b82f6` (blue), `accent-light: #dbeafe`
**Dividers**: `border-top: 2px solid #111827` for section breaks
**Ideal for**: Educational content, thought leadership, B2B audiences

---

## cluely-style
**Mood**: Modern SaaS product, polished, confident
**Background**: `linear-gradient(135deg, #f8fafc 0%, #e2e8f0 50%, #cbd5e0 100%)`
**Text color**: `#1a202c`
**Font**: `-apple-system, "Inter", "Segoe UI", Roboto`
**h1**: `clamp(48px, 7vw, 72px)`, weight 700, `letter-spacing: -0.025em`, gradient `linear-gradient(135deg, #1a202c, #4a5568)`
**h2**: `clamp(20px, 2.5vw, 28px)`, color `#4a5568`
**Slide transition**: `translateY(20px) → 0`, `0.6s cubic-bezier(0.16, 1, 0.3, 1)`
**Cards**: White with shadow — `background: white`, `box-shadow: 0 4px 24px rgba(0,0,0,0.08)`, `border-radius: 16px`, `border: 1px solid rgba(0,0,0,0.06)`
**Accent**: `#667eea` (indigo-blue), `#22d3ee` (cyan)
**Special**: Product screenshot mockups, subtle gradient overlays
**Ideal for**: SaaS products, B2B tools, startup demos

---

## modern-saas-dark
**Mood**: Developer-friendly dark, enterprise, technical credibility
**Background**: `linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%)`
**Text color**: White
**Font**: `'Inter', -apple-system` (Google Fonts import)
**h1**: `clamp(40px, 6vw, 72px)`, weight 800, gradient text from white to light blue
**h2**: `clamp(18px, 2vw, 24px)`, color `rgba(255,255,255,0.7)`
**Slide animation**: `fadeInUp` — `translateY(30px) → 0`, `opacity 0→1`, `1s cubic-bezier(0.16, 1, 0.3, 1) 0.3s forwards`
**Cards**: `background: rgba(255,255,255,0.05)`, `border: 1px solid rgba(255,255,255,0.1)`, `border-radius: 12px`
**Accent**: Blue `#3b82f6`, cyan `#22d3ee`
**Ideal for**: Developer tools, APIs, technical products, AI platforms

---

## retro-synthwave
**Mood**: 80s nostalgia, high energy, bold
**Background**: `linear-gradient(135deg, #1e0a2e 0%, #0f0f23 50%, #2e1065 100%)`
**Text color**: White
**Font**: `'Orbitron'` for headlines, `'Exo 2'` for body (Google Fonts)
**Colors**: `--neon-pink: #ff00ff`, `--neon-cyan: #00ffff`, `--neon-purple: #8b00ff`, `--neon-green: #39ff14`
**Grid overlay**: Cyan grid lines at 10% opacity, 50px grid size
**Text effects**: Neon glow `text-shadow: 0 0 20px #ff00ff, 0 0 40px #ff00ff`
**Cards**: Dark with neon border glow — `border: 1px solid rgba(255,0,255,0.4)`, `box-shadow: 0 0 20px rgba(255,0,255,0.2)`
**Ideal for**: Gaming content, entertainment, Gen-X/millennial audiences, bold topics

---

## brutalist
**Mood**: Raw, confident, no-nonsense
**Background**: White `#ffffff`
**Text color**: Black `#000000`
**Font**: `'Inter'` or `'Space Grotesk'` (Google Fonts), heavy weights
**h1**: Very large, bold, black. No gradient, no effects. Pure impact.
**Border style**: Heavy `border: 4px solid #000` or `border: 3px solid #ff0000`
**Cards**: Hard borders, no border-radius, raw blocks
**Accent**: Red `#ff0000` (single accent only, used sparingly)
**No shadows**: Everything is flat. No box-shadow.
**cursor**: `crosshair`
**Ideal for**: Contrarian takes, strong opinions, provocation, bold entrepreneurial content

---

## cyberpunk-neon
**Mood**: Futuristic dystopia, high-tech, intense
**Background**: `#0a0a0f` with `radial-gradient(ellipse at center, rgba(255,0,128,0.1), transparent)`
**Text color**: White
**Font**: `'Orbitron'` for headlines, `'Rajdhani'` for body, `'Share Tech Mono'` for data (Google Fonts)
**Colors**: `--neon-pink: #ff0080`, `--neon-cyan: #00ffff`, `--neon-green: #00ff00`
**Grid**: Cyan/pink neon grid at 30% opacity
**Text effects**: Dual color neon glow — `text-shadow: 0 0 10px #00ffff, 0 0 30px #ff0080`
**Cards**: Dark glass with neon borders — `border: 1px solid rgba(0,255,255,0.3)`, `box-shadow: 0 0 15px rgba(0,255,255,0.1)`
**Ideal for**: Tech disruption topics, gaming, futurism, cybersecurity

---

## terminal-code
**Mood**: Developer terminal, hacker aesthetic, technical authority
**Background**: `#0d1117` (GitHub dark)
**Text color**: `#39ff14` (neon green) as primary, white for headlines
**Font**: `'Fira Code'`, `'JetBrains Mono'` monospace (Google Fonts)
**Prompt prefix**: Lines start with `$` or `>` for terminal feel
**Colors**: Green `#39ff14`, cyan `#00ffff`, yellow `#ffff00`, purple `#ff00ff`
**Cards**: `background: #161b22`, `border: 1px solid #30363d`, `border-radius: 6px` (GitHub-style)
**Typing animation**: Key headlines use typewriter effect
**Ideal for**: Developer content, coding education, technical deep-dives

---

## liquid-metal
**Mood**: Luxurious tech, premium, chrome
**Background**: `#0a0a0a` with animated radial color orbs (purple, pink, blue)
**Text color**: White + chrome gradient `linear-gradient(145deg, #c0c0c0, #ffffff, #c0c0c0)`
**Font**: `-apple-system, "SF Pro Display", "Helvetica Neue"`
**Animated elements**: Mercury blob divs — colorful gradient spheres floating with `mix-blend-mode: screen`
**Cards**: `background: rgba(255,255,255,0.05)`, `border: 1px solid rgba(255,255,255,0.15)`, chrome highlight borders
**Chrome effect**: `background: linear-gradient(135deg, #667eea, #764ba2, #f093fb, #f5576c, #4facfe, #00f2fe)`, `background-size: 400% 400%`
**Ideal for**: Premium products, luxury positioning, high-end services

---

## white-with-pops-of-color
**Mood**: Energetic, friendly, approachable modern
**Background**: `linear-gradient(135deg, #f5f5f0 0%, #e8e8e3 100%)` — warm off-white
**Text color**: `#1d1d1f`
**Font**: `-apple-system, 'SF Pro Display', 'Segoe UI', Roboto`
**Slide layout**: Horizontal scroll with `transform: translateX` on container
**h1**: Large, black/dark, no gradient
**Cards**: Solid color fills (not glass) — each card gets a bold background color from a palette
**Color palette for cards**: `#ff6b6b` (coral), `#4ecdc4` (teal), `#45b7d1` (sky), `#96ceb4` (sage), `#feca57` (yellow), `#ff9ff3` (pink), `#54a0ff` (blue)
**Animation**: nth-child stagger delays (OK here since content isn't sequential-reveal)
**Ideal for**: Non-technical entrepreneurs, casual educational, cheerful opportunity content

---

## simple-colors-style
**Mood**: Bold, flat, no-nonsense communication
**Background**: Full-bleed solid color per slide from a rotating palette
**Text color**: White on dark slides, dark on light slides
**Font**: System fonts, heavy weights
**Cards**: Flat color blocks with high contrast
**No gradients**: Pure solid colors only
**Ideal for**: Key messages, bold statements, social media-style content

---

## editorial-magazine
**Mood**: Print editorial, authoritative, intellectual
**Background**: Off-white `#fafaf8`
**Text color**: `#1a1a1a`
**Font**: Mix of serif (headlines) + sans-serif (body) — `'Playfair Display'` + `'Inter'`
**Layout**: Asymmetric grids, pull quotes, large drop caps
**Cards**: Paper-white with thin `1px solid #ddd` borders
**Accent**: Single accent color (usually black + one bold color)
**Ideal for**: Thought leadership, longform stories, intellectual content

---

## swiss-design
**Mood**: International modernism, grid-based, ultra-rational
**Background**: White
**Text color**: Black
**Font**: `'Helvetica Neue'` or `'Arial'`, strict grid alignment
**Grid**: 12-column strict grid visible in spacing choices
**Typography**: Large type-as-design — h1 can be 120px+ when it's the only element
**Red accent**: Pure red `#ff0000` used sparingly as a single accent
**No decorative elements**: Grids, type, and color only
**Ideal for**: Design community, rational arguments, information-dense topics

---

## neumorphism
**Mood**: Soft, tactile, UI-forward
**Background**: `#e0e5ec` (light blue-gray)
**Text color**: `#4a4a6a`
**Font**: `'Poppins'` or `'Nunito'`, soft weights
**Shadow system**: Dual shadow — `box-shadow: 8px 8px 16px #b8bec7, -8px -8px 16px #ffffff`
**Cards**: Same background as page with dual shadows (soft embossed look)
**Accent**: Soft purple-blue, no harsh colors
**Ideal for**: Soft tech products, wellness apps, consumer-friendly content

---

## black-neon-glow
**Mood**: Nightclub meets tech, vibrant, attention-grabbing
**Background**: `#000000` pure black
**Text color**: White, with key words in neon
**Font**: `-apple-system` or `'Inter'`, bold weights
**Glow system**: `text-shadow: 0 0 20px [color], 0 0 40px [color], 0 0 80px [color]`
**Neon palette**: Pink `#ff006e`, cyan `#00d4ff`, green `#39ff14`, purple `#bf00ff`
**Cards**: Black background with neon border glow
**Ideal for**: Nightlife, entertainment, bold product launches, Gen-Z audiences

---

## art-deco-luxury
**Mood**: 1920s opulence, gold, timeless luxury
**Background**: Very dark `#0a0806` or deep navy
**Text color**: Gold `#d4af37`, cream `#f5f0e8`
**Font**: `'Cormorant Garamond'` or `'Cinzel'` serif (Google Fonts)
**Gold effects**: `background: linear-gradient(135deg, #d4af37, #f5d785, #b8860b)`, `-webkit-background-clip: text`
**Borders**: Gold thin lines `1px solid rgba(212,175,55,0.4)`
**Cards**: Dark with gold borders and subtle gold gradient background
**Ornaments**: Geometric Art Deco dividers (lines, diamonds, chevrons)
**Ideal for**: Luxury brands, premium positioning, high-ticket offers

---

## animated-gradients
**Mood**: Dynamic, colorful, energetic
**Background**: `linear-gradient(270deg, #ee7752, #e73c7e, #23a6d5, #23d5ab)`, `background-size: 400% 400%`, `animation: gradientShift 15s ease infinite`
**Text color**: White
**Font**: `-apple-system`, bold
**Cards**: Semi-transparent glass over the moving gradient
**Everything moves**: Subtle parallax, floating elements, pulsing glows
**Ideal for**: Creative agencies, design studios, high-energy product launches

---

## isometric-3d
**Mood**: Playful tech, spatial, illustrative
**Background**: Light gradient `#f0f4ff → #e8eaf6`
**Text color**: Dark `#1a237e`
**Font**: `'Inter'`, rounded weights
**Visual style**: Isometric grid illustrations as slide artwork (CSS-drawn boxes, arrows)
**Cards**: Isometric perspective with depth shadows
**Colors**: Pastel blues, purples, greens
**Ideal for**: SaaS platforms, process illustrations, technical explanations

---

## memphis-design
**Mood**: 80s pop, playful, loud
**Background**: White or light with scattered geometric shapes (triangles, dots, zigzags)
**Text color**: Black with color highlights
**Font**: `'Righteous'` or `'Fredoka One'` (Google Fonts)
**Shapes**: Randomly placed geometric decorations — circles, squiggles, triangles in primary colors
**Colors**: Hot pink `#ff1493`, yellow `#ffe600`, cyan `#00bcd4`, red `#ff4444`
**No subtlety**: Everything is loud, layered, chaotic-but-intentional
**Ideal for**: Youth brands, entertainment, creative content

---

## hand-drawn-sketch
**Mood**: Casual, human, approachable
**Background**: Off-white `#fffef7` (paper-like)
**Text color**: Dark ink `#1a1a1a`
**Font**: `'Caveat'` or `'Patrick Hand'` (Google Fonts)
**Border style**: Slightly imperfect, rough — `border: 2px solid #333` with slight rotation
**Cards**: Sketch-box style with hand-drawn border effect
**Colors**: Muted, slightly desaturated
**Annotations**: Arrows, underlines, circles as decorative elements
**Ideal for**: Educational explainers, personal brands, relatable casual content

---

## modern-modal-style
**Mood**: SaaS product UI, focused, functional
**Background**: Light gray `#f3f4f6`
**Text color**: `#111827`
**Font**: `'Inter'`
**Card style**: Modal-like — centered white card with heavy shadow, `box-shadow: 0 20px 60px rgba(0,0,0,0.15)`, `border-radius: 24px`
**Each slide**: A single focused modal card in the center
**Accent**: Purple-blue `#6366f1`
**Ideal for**: Product walkthroughs, UI demos, app feature showcases

---

## blue-background-modal
**Mood**: Corporate tech, trustworthy, professional
**Background**: Rich blue `linear-gradient(135deg, #1e3a8a 0%, #1e40af 50%, #2563eb 100%)`
**Text color**: White
**Font**: `-apple-system, 'Inter'`
**Cards**: White or light glass cards against the blue
**Accent**: Yellow `#fbbf24` or cyan `#22d3ee` as contrast accent
**Ideal for**: Finance, enterprise, corporate presentations

---

## cluely-3d-style
**Mood**: 3D depth, product showcase, premium SaaS
**Background**: Dark `#0f0f0f` or deep gradient
**Text color**: White
**Font**: `'Inter'`, tight letter-spacing
**Depth effects**: Cards with 3D perspective transforms — `transform: perspective(1000px) rotateY(-5deg)`
**Shadows**: Deep layered shadows for 3D feel
**Accent**: Gradient purple-to-cyan on key elements
**Ideal for**: Premium SaaS products, 3D/spatial content, sophisticated tech demos

---

## old-video-game / old-vide-game
**Mood**: Retro 8-bit / pixel art nostalgia
**Background**: Black or deep navy
**Text color**: Bright green or white pixelated text
**Font**: `'Press Start 2P'` pixel font (Google Fonts)
**Cards**: Pixel-perfect borders with `image-rendering: pixelated`
**Animation**: Blink effects, scanlines overlay, CRT glow
**Sound cues**: Optional 8-bit sound effects on transitions
**Colors**: Pixel-art palette — lime green, bright red, yellow on dark
**Ideal for**: Gaming community, nostalgia content, tech "old school vs new school"

---

## dark-mode-pro
**Mood**: Premium productivity, focused, distraction-free
**Background**: `#111111` or `#0f172a`
**Text color**: `#f1f5f9`, muted secondaries at `rgba(255,255,255,0.6)`
**Font**: `'Inter'`, clean weights
**Cards**: `#1e293b` with `border: 1px solid rgba(255,255,255,0.08)`
**Accent**: `#6366f1` indigo or `#22d3ee` cyan
**Ideal for**: Developer tools, productivity apps, technical documentation

---

## apple-minimal
**Mood**: Ultra-minimal, single idea per screen, meditative
**Background**: White or near-white `#fafafa`
**Text color**: Black `#000`
**Font**: `-apple-system`, weights 300–900
**Principle**: One element per slide. Maximum negative space.
**h1**: Can be the entire slide content — very large, centered
**No cards**: Content floats in space
**No borders**: Pure typography and negative space
**Ideal for**: Inspirational quotes, single statistics, meditation-pace storytelling

---

# Choosing a Style by Mood

| User Says | Recommend |
|-----------|-----------|
| "Dramatic", "dark", "Apple" | `apple-keynote-style` |
| "Clean", "professional", "light" | `apple-keynote-style-light` or `minimalist-clean` |
| "Futuristic", "glass" | `glassmorphism` |
| "Tech", "SaaS", "startup" | `dark-glowing-style` or `modern-saas-dark` |
| "Retro", "80s", "nostalgic" | `retro-synthwave` or `old-video-game` |
| "Developer", "hacker", "code" | `terminal-code` |
| "Luxury", "premium", "gold" | `art-deco-luxury` or `liquid-metal` |
| "Bold", "raw", "statement" | `brutalist` |
| "Fun", "colorful", "energetic" | `white-with-pops-of-color` or `memphis-design` |
| "Minimal", "editorial" | `apple-minimal` or `swiss-design` |
| "Neon", "cyberpunk" | `cyberpunk-neon` or `black-neon-glow` |
| "Corporate", "enterprise" | `blue-background-modal` or `dark-mode-pro` |
| No preference specified | Default to `apple-keynote-style` (dark topics) or `apple-keynote-style-light` (opportunity topics) |
