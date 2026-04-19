# YAMIICHI (闇市) Design System

## Company Overview

**YAMIICHI** (闇市, lit. "night market / underground market") is a Japanese-language e-commerce platform targeting anime and manga fans, underground idol culture, and streetwear enthusiasts. The store sells clothing, jewelry, anime merchandise, and idol goods (photobooks, CDs, limited goods).

The brand aesthetic draws from:
- Underground idol subculture (chika-idol, iDOL Street, WACK acts)
- Japanese streetwear (Harajuku dark side, layered darkness, anti-fashion)
- Cyberpunk anime visual language (Akira, Ghost in the Shell, Blame!)
- Doujinshi & indie zine culture

**Sources provided:** GitHub repo (Luimya/EC — empty at time of writing; brand built from brief). No Figma or existing assets provided.

---

## CONTENT FUNDAMENTALS

**Language:** Japanese only (ja-JP)
**Tone:** Cool, detached, slightly mysterious. Never cute or bubbly. Not aggressive — quietly confident. Think underground idol MC energy.
**Voice:** Third-person brand narration. Minimal copy. Less is more.
**Casing:** Japanese naturally handles this — no all-caps shouting, no excessive punctuation. Latin text (product codes, tags) uses ALL CAPS.
**Emoji:** Never used in UI copy. Occasionally in social/SNS context only.
**Numbers:** Full-width Japanese numerals for headings; ASCII for prices/quantities.
**Example copy style:**
- `闇に潜む、美しいものたちへ。` ("To the beautiful things lurking in the darkness.")
- `限定` (Limited) as a badge — terse, commanding
- `¥12,800` — always with yen sign, no decimals
- Product names: lowercase latin + Japanese subtitle (e.g., `void ring / 空虚の指輪`)

---

## VISUAL FOUNDATIONS

### Colors
- **Base:** `#080808` near-black (not pure black — has warmth)
- **Surface:** `#111111` (cards, panels)
- **Elevated:** `#1A1A1A` (modals, dropdowns)
- **Border:** `#2A2A2A` (default), `#3D3D3D` (bright/active)
- **Primary accent:** `#7C3AED` violet → `#A78BFA` (hover/glow)
- **CTA / highlight:** `#F0185C` neon pink
- **Secondary neon:** `#00E5CC` cyan (used sparingly — price highlights, new badges)
- **Text primary:** `#F0F0F0`
- **Text secondary:** `#9CA3AF`
- **Text muted:** `#6B7280`

### Typography
- **Display/headings:** `Noto Sans JP` weight 100–300 — impossibly thin, editorial
- **Body:** `Noto Sans JP` weight 400
- **Labels/caps:** `Space Grotesk` weight 500–700
- **Type scale:** 11, 13, 15, 18, 24, 32, 48, 72, 96px
- **Line height:** 1.2 for display, 1.6 for body
- **Letter spacing:** -0.02em for display, 0.08em for labels/uppercase

### Backgrounds & Texture
- Base is `#080808` with a subtle CSS grain noise overlay (opacity ~0.04)
- Section dividers: 1px `#2A2A2A` lines — no decorative flourishes
- Hero sections: full-bleed dark editorial photos with gradient overlay (radial, bottom-heavy)
- No gradients as backgrounds themselves — only as photo overlays

### Spacing & Layout
- Base unit: 4px
- Common spacing: 8, 16, 24, 32, 48, 64, 96, 128px
- Container max-width: 1280px
- Grid: 12-column, 24px gutter
- Generous whitespace — negative space is a design element

### Borders & Radius
- **Default radius:** `2px` (almost none — sharp, not rounded)
- **Pill:** `999px` for badges/tags only
- **Border style:** 1px solid; sometimes `0.5px` for ultra-fine lines
- **No box shadows** — instead, glow effects using `box-shadow: 0 0 20px rgba(124,58,237,0.3)`

### Animation & Motion
- **Easing:** `cubic-bezier(0.16, 1, 0.3, 1)` — fast out, slow settle
- **Duration:** 200ms for micro-interactions, 400ms for page transitions
- **Hover states:** color shift + subtle glow; no scale transforms
- **No bounces** — everything is smooth and deliberate
- **Fade-in on scroll:** opacity 0→1, translateY 16px→0

### Cards
- Background: `#111111`
- Border: `1px solid #2A2A2A`
- No shadow — glow on hover: `0 0 24px rgba(124,58,237,0.2)`
- Radius: `2px`
- Image fills top; text below with 16px padding

### Imagery
- Full-bleed editorial photos; dark, moody, high-contrast
- Color grade: desaturated with slight purple push
- Human subjects: underground idol / model aesthetic
- Never stock-photo bright or cheerful

### Icons
- See ICONOGRAPHY section

---

## ICONOGRAPHY

- **Approach:** Ultra-minimal line icons, 1px or 1.5px stroke, no fill
- **Style:** Custom SVG inline icons; geometric, sharp corners
- **System:** No third-party icon font. All icons are inline SVG `24×24` viewBox
- **Key icons used:** cart (bag), search (magnifying glass), menu (3 lines), close (×), arrow (→ ←), heart (outline), user (circle+line), filter, chevron
- **Emoji:** Never used as icons in UI
- **Logo:** Wordmark `闇市` in Noto Sans JP weight 100, with `YAMIICHI` in Space Grotesk below in small caps. See `assets/logo.svg`

---

## FILE INDEX

```
README.md                    — This file
colors_and_type.css          — All CSS design tokens + typography
SKILL.md                     — Agent skill definition

assets/
  logo.svg                   — Primary wordmark logo

preview/
  colors-base.html           — Base background/surface colors
  colors-accent.html         — Accent & neon color palette
  colors-semantic.html       — Semantic color tokens
  type-display.html          — Display type specimens
  type-body.html             — Body & label type specimens
  spacing-tokens.html        — Spacing scale tokens
  border-radius.html         — Border radius + border system
  shadows-glow.html          — Glow/shadow system
  components-buttons.html    — Button variants
  components-badges.html     — Badge/tag components
  components-cards.html      — Product card variants
  components-inputs.html     — Form inputs
  brand-logo.html            — Logo presentation

ui_kits/
  website/
    README.md                — Website UI kit overview
    index.html               — Full interactive prototype (5 screens)
```
