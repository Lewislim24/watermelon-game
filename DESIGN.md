---
name: Game Hub
description: A handcrafted browser arcade — five mini-games, one clean lounge.
colors:
  navy-deep: "#1a1a2e"
  navy-surface: "#16213e"
  navy-canvas: "#0d1117"
  navy-border: "#0f3460"
  amber-gold: "#f9ca24"
  ink-primary: "#eeeeee"
  ink-secondary: "#aaaaaa"
  ink-muted: "#888888"
  ink-ghost: "#444444"
  game-teal: "#16a085"
  game-green: "#27ae60"
  game-orange: "#e67e22"
  game-purple: "#9b59b6"
  game-blue: "#3498db"
typography:
  display:
    fontFamily: "system-ui, -apple-system, sans-serif"
    fontSize: "2.8rem"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: "normal"
  headline:
    fontFamily: "system-ui, -apple-system, sans-serif"
    fontSize: "1.6rem"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "0.05em"
  title:
    fontFamily: "system-ui, -apple-system, sans-serif"
    fontSize: "1.05rem"
    fontWeight: 700
    lineHeight: 1.3
  body:
    fontFamily: "system-ui, -apple-system, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "system-ui, -apple-system, sans-serif"
    fontSize: "0.625rem"
    fontWeight: 400
    letterSpacing: "0.2em"
rounded:
  pill: "99px"
  card: "14px"
  surface: "8px"
  canvas: "4px"
spacing:
  xs: "8px"
  sm: "16px"
  md: "20px"
  lg: "28px"
  xl: "48px"
components:
  game-card:
    backgroundColor: "{colors.navy-surface}"
    textColor: "{colors.ink-primary}"
    rounded: "{rounded.card}"
    padding: "28px 20px 20px"
  play-button:
    textColor: "#ffffff"
    rounded: "{rounded.pill}"
    padding: "6px 22px"
  score-box:
    backgroundColor: "{colors.navy-surface}"
    textColor: "{colors.ink-primary}"
    rounded: "{rounded.surface}"
    padding: "6px 16px"
  restart-button:
    textColor: "#ffffff"
    rounded: "{rounded.surface}"
    padding: "10px 28px"
  nav-link:
    textColor: "{colors.amber-gold}"
---

# Design System: Game Hub

## 1. Overview

**Creative North Star: "The Handcrafted Lounge"**

This is a place someone made, not a product that was launched. The Game Hub has a quiet, focused energy — deep space navy surfaces, a warm amber-gold glow on the things that matter, and enough restraint that each game gets its own identity when you step into it. The hub defers to the games. The games defer to the player.

The system is built on a **committed dark strategy**: the navy palette spans three depth layers (page, surface, canvas), separated not by shadows but by tonally distinct blues. Depth here is geological, not architectural. Color appears only where it earns its place: amber-gold on the hub's heading and navigation; per-game accents on each game's title and score. Motion is quiet at rest and snappy on interaction — cards lift on hover, everything else stays still.

The typography is native system-ui throughout. It doesn't announce itself; it disappears. Personality lives in weight contrast, color, and the glow that follows accent headings — not in typeface choices.

**What this system explicitly rejects:**
- AI slop: generic card grids, cream backgrounds, pastel palettes, eyebrow labels on every section, AI scaffolding patterns
- Cheap mobile-ad game aesthetics: flashy banners, gradient overload, fake progress bars, aggressive CTAs
- Dark gamer cliché: neon-on-black aggression, toxic visual energy, overwrought glow effects
- Kids' site: chunky primary colors, cartoon mascots, patronizing UX

**Key Characteristics:**
- Three-layer dark depth (page → surface → canvas) via tonal navy, not shadows
- Amber-gold as the single shared hub accent; each game gets its own distinct accent on its own page
- System-ui typography — legible, neutral, never competes with the games
- Hover interactions are snappy (0.1–0.15s) and physical-feeling (lift + shadow)
- No decorative elements — layout, color, and motion only

## 2. Colors: The Deep Space Navy Palette

A committed dark palette in three tonal navy depths, unified by amber-gold and five per-game identity colors.

### Primary
- **Amber Gold** (`#f9ca24`): The hub's sole accent. Hub h1, back-navigation links, score values in games that don't have their own accent. Applied with a soft glow text-shadow (`0 0 12px rgba(249,202,36,0.4)`) on display headings. Its rarity is the point.

### Secondary
- **Game Teal** (`#16a085`): Watermelon game identity — heading, score values, play button, hover border.
- **Game Green** (`#27ae60`): Snake.
- **Game Orange** (`#e67e22`): Breakout.
- **Game Purple** (`#9b59b6`): 2048.
- **Game Blue** (`#3498db`): Flappy Bird.

These five are not interchangeable. They are per-game identity marks, not a shared palette.

### Neutral
- **Deep Space Navy** (`#1a1a2e`): Page body background. The lowest layer; the room itself.
- **Surface Navy** (`#16213e`): Card and panel background. The second layer; the furniture.
- **Canvas Dark** (`#0d1117`): Game canvas background. The deepest layer; the game world.
- **Border Deep Blue** (`#0f3460`): All border and divider lines. Creates gentle separation without contrast.
- **Ink Primary** (`#eeeeee`): All body and heading text on dark backgrounds.
- **Ink Secondary** (`#aaaaaa`): Score box labels, secondary descriptions.
- **Ink Muted** (`#888888`): Hub card description text. Verify contrast at this value against `#1a1a2e` (~4.5:1 minimum).
- **Ink Ghost** (`#444444`): Footer text only.

### Named Rules

**The One Accent Rule.** Amber-gold (`#f9ca24`) is the hub's voice. On game pages, the game's accent takes over entirely. The two should never compete — there is no amber-gold text on a game page.

**The Tonal Depth Rule.** Depth is expressed through tonal navy layers, not shadows. The three background values (`#1a1a2e` → `#16213e` → `#0d1117`) separate page, surface, and canvas. Do not invent new depth layers; do not blur this into shadow-based elevation.

## 3. Typography

**Display / Body Font:** system-ui, -apple-system, sans-serif (native system stack)

**Character:** Native and immediate. The system font renders as the user's own interface — it doesn't announce itself. Typography here is about weight contrast and color, not typeface personality. The games are the personality.

### Hierarchy
- **Display** (700, 2.8rem, lh 1.1): Hub h1 — "🎮 Game Hub". The loudest typographic moment on the site. Amber-gold with soft glow. One instance only.
- **Headline** (700, 1.6rem, lh 1.2, tracking 0.05em): Game page h1. Renders in the game's accent color with a matching glow. The game name only.
- **Title** (700, 1.05rem, lh 1.3): Hub card titles. Ink primary (`#eee`).
- **Body** (400, 1rem, lh 1.5): Card descriptions and in-game instruction copy. Cap lines at 65–75ch.
- **Label** (400, 0.625rem, lh 1, tracking 0.2em): Score box labels (SCORE, HIGH, LEVEL). Uppercase by content convention only — no CSS `text-transform`.

### Named Rules

**The Glow Rule.** Headings in an accent color always pair with a matching glow (`text-shadow: 0 0 12px rgba(r,g,b,0.4)`). The glow follows the accent, not the layout. A glow on neutral text is decoration; only accent headings earn it.

## 4. Elevation

This system uses **tonal layering**, not shadows. The three dark backgrounds create visual depth through color alone. Surfaces do not float — they rest in their layer.

The exception is **hover state on interactive cards**: the lift (`translateY(-5px)`) and dark ambient shadow (`box-shadow: 0 10px 28px rgba(0,0,0,0.5)`) signal that a card is a link. This is a response to interaction, not a resting state.

### Shadow Vocabulary
- **Hover lift** (`box-shadow: 0 10px 28px rgba(0,0,0,0.5)`): Hub game cards on hover only. Paired with `translateY(-5px)`. Transition: 0.15s ease-out.
- **Game overlay backdrop** (`background: rgba(10,10,20,0.9)`): Absolutely-positioned overlay for start/end game screens. Not a box-shadow; a tonal veil.

### Named Rules

**The Flat-by-Default Rule.** Resting surfaces have no box-shadow. Shadows appear only as a response to hover interaction. A shadowed card at rest is trying too hard.

## 5. Components

### Buttons

Two button contexts in this system: the **play button** on hub cards (pill, per-game accent, compact) and **restart buttons** in game overlays (larger, same game accent, more presence).

- **Shape:** Pill (99px) for play buttons; surface-rounded (8px) for restart buttons
- **Play Button:** `background: var(--accent)`; white text; padding `6px 22px`; 0.8rem bold; 700 weight
- **Restart Button:** Game accent background; white text; padding `10px 28px`; 1rem bold
- **Hover:** `opacity: 0.9` + `transform: scale(1.04)`; 0.1s transition — snappy and physical
- **No ghost, no outlined, no disabled styling needed.** Every button in this system has a filled background.

### Cards (Hub Game Cards)

The hub's primary component. Dark navy surface with per-game accent injected via CSS `--accent` custom property.

- **Corner Style:** Gently rounded (14px)
- **Background:** Surface navy (`#16213e`)
- **Shadow Strategy:** None at rest. Hover: lift + dark ambient shadow (see Elevation)
- **Border:** `1px solid #0f3460` at rest; transitions to `1px solid var(--accent)` on hover
- **Internal Padding:** 28px 20px 20px (generous top breathing room for the icon)
- **Structure:** Emoji icon (3.2rem, lh 1) → game title (1.05rem bold) → description (0.78rem, `#999`) → play button
- **Transition:** `transform 0.15s, box-shadow 0.15s, border-color 0.15s` — all three properties together

**The Accent Injection Pattern.** Hub cards set `style="--accent:#16a085"` inline, making the game's identity color available to all child elements via `var(--accent)`. One component; five visual identities; no per-game CSS classes.

### Score Boxes

The game UI's score readout. Tonal surface, uppercase label, large value in game accent color.

- **Shape:** Surface-rounded (8px)
- **Background:** Surface navy (`#16213e`)
- **Border:** `1px solid #0f3460`
- **Padding:** `6–8px 16px`; minimum width 80px; text centered
- **Label:** 0.625rem, tracking 0.2em, ink-secondary (`#aaa`)
- **Value:** 1.3–1.4rem bold, game accent color (always matches the page's headline glow)

### Navigation

One text link per game page, returning to the hub. No nav bar, no breadcrumb.

- **Style:** Amber-gold (`#f9ca24`), 0.85rem, no underline, opacity 0.8 at rest
- **Hover:** Opacity 1.0, transition 0.1s ease
- **Placement:** Full-width constrained container (max-width matching canvas), left-aligned, above game content

### Game Canvas Wrapper

The most important structural element in every game page. The canvas is not just a tag — it's surrounded by a positional wrapper that hosts the overlay.

- **Canvas background:** Canvas dark (`#0d1117`) — darker than the page, creates the game world
- **Canvas border:** `2px solid #0f3460`, 4px corner radius
- **Overlay (start/end screen):** `position: absolute; inset: 0; background: rgba(10,10,20,0.9)`; flex-centered content; matching 4px corner radius. Show with class toggle; hide by setting `display: none` via `.hidden` class.

## 6. Do's and Don'ts

### Do:
- **Do** use amber-gold (`#f9ca24`) only on the hub page (h1 and nav links). On game pages, the game accent takes its place entirely.
- **Do** inject per-game color via `style="--accent:#hex"` on the card or page root — not via per-game CSS classes.
- **Do** apply the glow text-shadow whenever a heading uses an accent color: `text-shadow: 0 0 12px rgba(r,g,b,0.4)`.
- **Do** use the three tonal navy layers (`#1a1a2e` → `#16213e` → `#0d1117`) as the depth system. Depth comes from tone, not shadow.
- **Do** keep hover transitions at 0.1–0.15s. The system should feel immediate and physical, not animated.
- **Do** make every element feel like a decision was made about it — not the first thing a template would produce.

### Don't:
- **Don't** use AI slop patterns: cream backgrounds, pastel card grids, gradient text (`background-clip: text`), glassmorphism as default, hero metrics, numbered section eyebrows (01/02/03), small uppercase tracked labels above every heading.
- **Don't** use cheap mobile-ad game aesthetics: flashing banners, gradient overload, fake progress bars, aggressive CTAs, visual noise.
- **Don't** use dark gamer cliché aesthetics: neon-on-black aggression, purple-and-cyan neon schemes, dragon-logo energy, toxic visual tone.
- **Don't** use kids' site design: chunky primary colors, cartoon mascots, patronizing copy, oversimplified layouts.
- **Don't** add box-shadow to resting surfaces. Shadows appear only as a hover-state response.
- **Don't** use `border-left` or `border-right` as a colored stripe accent on cards or panels.
- **Don't** use gradient text. Headings are solid accent colors with a single glow, never gradients.
- **Don't** introduce new accent colors. The palette has one hub accent (amber-gold) and five per-game accents. All are defined; none should be extended without purpose.
- **Don't** use `text-transform: uppercase` in CSS. Uppercase labels are uppercase by content ("SCORE"), never forced by CSS.
