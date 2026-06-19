# Handoff: Decorit Design System

## Overview

Decorit is an Israeli home-textile importer and manufacturer (curtains, bedding, towels, rugs, pillows, tablecloths). This design system covers the full B2B storefront and trade-portal surfaces — bilingual Hebrew/English, RTL-first.

## About the Design Files

The files in this bundle are **design references created in HTML** — high-fidelity prototypes showing intended look, copy, and behaviour. **Do not ship the HTML directly.** The task is to recreate these designs in your target codebase (React, Next.js, or whatever framework the project uses) using its established patterns and libraries, lifting the exact colours, typography, spacing and interaction details documented here.

## Fidelity

**High-fidelity.** The prototypes use the final colour palette, type scale, spacing system and interactions. Recreate pixel-accurately, adapting only what the target framework requires structurally.

---

## Design Tokens

### Colours

| Token | Hex | Usage |
|---|---|---|
| `--paper` | `#FBFAF8` | App/page background |
| `--cream` | `#F5F3EF` | Alternate section background |
| `--sand` | `#ECE9E3` | Hover surfaces, subtle fills |
| `--linen` | `#E0DCD4` | Dividers, chip borders |
| `--taupe-200` | `#CFC9BF` | |
| `--taupe-300` | `#B3ACA0` | |
| `--taupe-400` | `#948C7E` | Faint text |
| `--taupe-500` | `#6F685C` | Muted text |
| `--taupe-600` | `#4E483F` | |
| `--espresso` | `#322E28` | Body text |
| `--ink` | `#1E1B17` | Heading / near-black |
| `--clay-50` | `#F2EEEB` | Accent soft bg |
| `--clay-200` | `#D8C7BE` | |
| `--clay-400` | `#B5957F` | |
| `--clay-500` | `#9B7A66` | **Primary CTA / accent** |
| `--clay-600` | `#836556` | CTA hover |
| `--clay-700` | `#654E43` | CTA pressed |
| `--sage-100` | `#E8EAE2` | |
| `--sage-300` | `#BCC0AE` | |
| `--sage-500` | `#76795F` | Secondary |
| `--surface-dark` | `#26221C` | Nav/footer dark bg |
| `--surface-dark-2` | `#322D26` | |
| `--success-500` | `#5E7B52` | |
| `--warning-500` | `#C08A2D` | |
| `--danger-500` | `#A8473A` | |

### Semantic aliases

| Token | Points to |
|---|---|
| `--bg-app` | `--paper` |
| `--bg-subtle` | `--cream` |
| `--text-strong` | `--ink` |
| `--text-body` | `--espresso` |
| `--text-muted` | `--taupe-500` |
| `--accent` | `--clay-500` |
| `--accent-hover` | `--clay-600` |
| `--border-subtle` | `--linen` |
| `--border-default` | `--taupe-200` |

### Typography

| Token | Value | Notes |
|---|---|---|
| `--font-logo` | `"Cinzel"` | Latin wordmark (Trajan sub) |
| `--font-display` | `"Frank Ruhl Libre"` | Hebrew+Latin editorial serif |
| `--font-body` | `"Assistant"` | Hebrew+Latin sans, all UI |
| `--font-num` | `"Heebo"` | Numerals, supporting |
| `--fs-display` | `4.5rem / 72px` | Hero |
| `--fs-h1` | `3rem / 48px` | |
| `--fs-h2` | `2.25rem / 36px` | |
| `--fs-h3` | `1.625rem / 26px` | |
| `--fs-h4` | `1.25rem / 20px` | |
| `--fs-base` | `1rem / 16px` | Body |
| `--fs-sm` | `0.875rem / 14px` | |
| `--fs-xs` | `0.75rem / 12px` | |
| `--lh-tight` | `1.08` | Headings |
| `--lh-normal` | `1.5` | Body |
| `--ls-wider` | `0.14em` | Overlines, caps |

### Spacing (4px base)

| Token | Value |
|---|---|
| `--space-1` | `4px` |
| `--space-2` | `8px` |
| `--space-3` | `12px` |
| `--space-4` | `16px` |
| `--space-5` | `24px` |
| `--space-6` | `32px` |
| `--space-8` | `48px` |
| `--space-10` | `80px` |
| `--space-12` | `112px` (section rhythm) |
| `--gutter` | `clamp(1rem, 4vw, 3rem)` |
| `--container-xl` | `1320px` |
| `--container-lg` | `1140px` |

### Borders & Elevation

| Token | Value |
|---|---|
| `--radius-sm` | `4px` |
| `--radius-md` | `8px` |
| `--radius-lg` | `12px` |
| `--radius-xl` | `20px` |
| `--radius-pill` | `9999px` |
| `--shadow-sm` | `0 1px 3px rgba(30,27,23,.07)` |
| `--shadow-md` | `0 4px 12px rgba(30,27,23,.09)` |
| `--shadow-lg` | `0 8px 28px rgba(30,27,23,.13)` |

---

## Screens / Views

### 1. Marketing Landing Page (`ui_kits/landing/index.html`)

**Purpose:** Conversion-focused B2B lead-gen for trade buyers (stores + decorators). Single scroll. Hebrew default, RTL.

**Layout (1320px max-width, `clamp(1rem,4vw,3rem)` horizontal gutter):**

#### Sticky Header
- Height: ~74px (10px top+bottom padding on content row)
- Background: `#FBFAF8` (paper), bottom border `#E0DCD4`
- Logo: stacked PNG lockup, height 54px — left (RTL: right)
- Right (RTL: left): lang toggle pill + primary CTA button

#### Hero Section
- `min-height: 600px`, background image (curtained bedroom), dark overlay  
  `linear-gradient(90deg, rgba(38,34,28,.82) 0%, rgba(38,34,28,.55) 50%, rgba(38,34,28,.18) 100%)`
- 2-col grid: `1.25fr 380px`, gap `48px`, `align-items: center`
- **Left col (text):**
  - Eyebrow: 12px, weight 700, `letter-spacing: .16em`, uppercase, colour `#D8C7BE`
  - H1: `clamp(40px,5vw,68px)`, Frank Ruhl Libre, colour `#FBFAF8`, `line-height: 1.05`
  - Body: 19px, `line-height: 1.6`, colour `rgba(250,246,239,.9)`, `max-width: 480px`
  - Checklist: 16px, gap 11px, icon `ph-fill ph-check-circle` 22px colour `#D8C7BE`
- **Right col (lead form card):**
  - Background: `#FBFAF8`, border-radius 12px, padding 28px
  - Box-shadow: `0 8px 28px rgba(30,27,23,.13)`, border `1px solid #E0DCD4`
  - Max-width: 380px
  - Form title: Frank Ruhl Libre 24px, body 14px muted
  - Fields: Input (full width), gap 12px between fields
  - Checkbox + submit button (full width, primary, size lg)

#### Trust Strip
- Background: `#FBFAF8`, border-bottom `1px solid #E0DCD4`
- Centered flex: label text 13px muted + brand name pills in Cinzel 17px, `letter-spacing: .12em`, colour `#948C7E`

#### Benefits (4-up)
- Max-width 1320px, centred, padding top+bottom `112px`
- H2 centred: `clamp(28px,3.4vw,40px)`, Frank Ruhl Libre
- Grid: `repeat(4, 1fr)`, gap 22px
- Each card: `#FBFAF8`, border `1px solid #E0DCD4`, radius 12px, padding 26px
  - Icon badge: 48×48px, radius 8px, bg `#F2EEEB`, icon 26px colour `#9B7A66`
  - Title: Frank Ruhl Libre 20px strong
  - Body: 15px muted, `line-height: 1.55`

#### Product Showcase (4-up)
- Background: `#F5F3EF`, max-width 1320px
- Grid: `repeat(4,1fr)`, gap 20px
- Uses `ProductCard` component (see Components)

#### Testimonial
- Max-width 880px, centred, `padding: 112px gutter`, `text-align: center`
- Quote icon: `ph-fill ph-quotes` 40px, colour `#D8C7BE`
- Blockquote: Frank Ruhl Libre `clamp(24px,2.8vw,34px)`, `line-height: 1.4`, strong colour
- Attribution: 16px bold + 14px muted below

#### Dark CTA Band
- Background: `#26221C`, colour `#FBFAF8`
- Centred column, padding `80px gutter`
- H2: `clamp(28px,3.6vw,46px)`, max-width 680px
- Body: 18px, `line-height: 1.6`, colour `rgba(250,246,239,.82)`
- Flex row: Primary button + ghost link

#### Footer (dark)
- Background: `#1E1B17`
- Grid: `1.4fr 1fr 1fr 1fr`, gap 32px
- Logo: height 72px, `filter: invert(1) brightness(1.7)` for white version
- Column heads: 13px, weight 700, `letter-spacing: .1em`, uppercase, colour `#FBFAF8`
- Links: 14px, colour `rgba(250,246,239,.75)`
- Copyright bar: border-top `rgba(250,246,239,.12)`, 13px, colour `rgba(250,246,239,.5)`

---

### 2. Marketing Homepage (`ui_kits/homepage/index.html`)

Full storefront: sticky header with cart, hero banner, category grid (3-col), featured products (4-col), trade CTA band, footer. Same tokens as landing.

### 3. Trade Portal (`ui_kits/trade-portal/index.html`)

B2B dealer area: login screen → authenticated dashboard with sidebar nav, product catalog with filters, order panel.

---

## Components

All components live in `components/` and are exported on `window.DecoritDesignSystem_d86daa`.

### Button
```jsx
<Button variant="primary" size="lg">פתיחת חשבון</Button>
<Button variant="secondary" size="md">ביטול</Button>
<Button variant="ghost" size="sm">עוד</Button>
```
- **primary**: bg `#9B7A66`, text white, hover `#836556`, radius pill, font-weight 600
- **secondary**: border `#9B7A66`, text `#9B7A66`, bg transparent, hover bg `#F2EEEB`
- **ghost**: no border, text `#322E28`, hover bg `#ECE9E3`
- **sizes**: sm (h32, px12, 14px) / md (h40, px16, 15px) / lg (h56, px24, 16px)

### Input
```jsx
<Input placeholder="שם מלא" />
<Input placeholder="חיפוש..." type="search" />
```
- Height 44px, border `1px solid #CFC9BF`, radius 8px, padding `0 14px`
- Focus: border `#B5957F`, ring `2px solid #B5957F`

### ProductCard
```jsx
<ProductCard
  image="https://images.unsplash.com/..."
  category="וילונות"
  name="וילון פשתן מילאנו"
  price={89}
  unit="למ׳"
  badge={{ label: "חדש", tone: "accent" }}
/>
```
- White card, radius 12px, shadow-sm
- Image: 16:10 aspect, `object-fit: cover`, scale on hover
- Category: 11px uppercase muted, name: Frank Ruhl Libre 17px, price: 18px bold + unit 13px muted
- Badge (optional): pill, tones: accent/warning/danger/success

### Badge / Tag
```jsx
<Badge tone="accent">חדש</Badge>
<Badge tone="warning">מבצע</Badge>
<Tag>קטגוריה</Tag>
```

### Checkbox
```jsx
<Checkbox label="אני מאשר/ת קבלת מחירון" />
```

---

## Interactions & Behaviour

- **Language toggle**: `document.documentElement.lang` + `dir` switch; all copy swaps via state
- **Cart toast**: fixed bottom, pill shape, dark bg, `opacity` transition 0.25s, auto-dismiss 1.6s
- **Hover on category tiles**: `transform: scale(1.05)` on inner `<img>`, transition `0.4s ease-out`
- **Form submit**: `preventDefault`, show toast "תודה! נחזור אליכם בקרוב"
- **Sticky header**: `position: sticky; top: 0; z-index: 20`

---

## Assets

| Asset | Path | Notes |
|---|---|---|
| Logo (black) | `assets/logo/decorit-logo-1024.png` | 1024×1023px PNG, transparent bg |
| Logo (small) | `assets/logo/decorit-logo.png` | Same, smaller file |

**On dark surfaces:** apply `filter: invert(1) brightness(1.7)` to render white. A proper white SVG version would be cleaner — request from brand owner.

**Iconography:** Phosphor Icons CDN (`@phosphor-icons/web@2.1.1`). Usage: `<i className="ph ph-tag" />` (regular), `<i className="ph-fill ph-check-circle" />` (filled).

---

## Files in this Package

| File | Description |
|---|---|
| `README.md` | This document |
| `showcase.html` | Visual design-system showcase (open in browser) |
| `styles.css` ref | Root stylesheet (relative: `../../styles.css` from handoff folder) |
| `ui_kits/landing/` | Trade landing page (lead-gen) |
| `ui_kits/homepage/` | Marketing storefront homepage |
| `ui_kits/trade-portal/` | B2B dealer portal |

**Full source** lives in the Decorit Design System project. GitHub input repo: https://github.com/elad-ux/decorit_desing (currently minimal — may be expanded).

---

## Localisation Notes

- **RTL-first**: `html { direction: rtl; }` is the base. Flip to `dir="ltr"` on subtrees or the whole document for English.
- Use CSS logical properties (`inset-inline-start`, `margin-inline-end`, etc.) everywhere — never `left`/`right` for layout.
- Hebrew display font: Frank Ruhl Libre. Latin wordmark: Cinzel (Trajan substitute).
- Number formatting: Hebrew uses `₪` prefix, e.g. `₪249`.

---

## Checklist for Developer

- [ ] Load Google Fonts: Cinzel (400–700), Frank Ruhl Libre (400–900), Assistant (300–700), Heebo (400–700)
- [ ] Set `<html dir="rtl" lang="he">` as default; toggle dynamically on lang switch
- [ ] Apply CSS custom properties from `tokens/` to `:root`
- [ ] Use logical CSS properties throughout
- [ ] Phosphor Icons loaded from CDN or bundled
- [ ] Logo PNG in `/public/` or equivalent; invert filter for dark surfaces
- [ ] Replace all Unsplash placeholder images with real Decorit product/interior photography
- [ ] Wire up real form backend for lead capture
- [ ] Add real inventory / pricing data to product grid
