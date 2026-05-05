---
version: 1.0
name: Verdant
description: A design system for environmental and geospatial analytics platforms. The canvas opens on deep forest ink (`#0e1a12`) — the rare case of a dark-first editorial system. Warm parchment (`#f2ede4`) carries display text with a field-notebook lightness. The single brand voltage is **Signal Green** (`#3ecf72`) — the NDVI-chart green — reserved for CTAs, data highlights, and the wordmark. A signature spectral index palette (deep red, amber, lime, teal, blue) maps vegetation and water index value ranges across maps and charts. Cards use thin moss-tinted borders, no heavy shadows. Canela for display, DM Mono on every data/map surface.

colors:
  primary: "#3ecf72"
  primary-active: "#2ab05c"
  primary-muted: "#1a6637"

  ink: "#f2ede4"
  ink-strong: "#ffffff"
  body: "#b8c4b0"
  body-strong: "#d4ddd0"
  muted: "#7a9070"
  muted-soft: "#506050"

  hairline: "#1e2e20"
  hairline-soft: "#192518"
  hairline-strong: "#2c4030"

  canvas: "#0e1a12"
  canvas-soft: "#111f15"
  canvas-raised: "#162219"

  surface-card: "#142018"
  surface-strong: "#1e2e20"
  surface-overlay: "#0a1209"

  on-primary: "#0a1a0e"

  # Spectral index scale — NDVI / vegetation health visualization only
  index-dead: "#8b1a1a"          # < 0.1  bare / dead
  index-sparse: "#c97d2b"        # 0.1–0.2  sparse
  index-stressed: "#d4c043"      # 0.2–0.4  stressed / dry
  index-moderate: "#7dbd4a"      # 0.4–0.6  moderate
  index-healthy: "#3ecf72"       # 0.6–0.8  healthy
  index-dense: "#1a8f5a"         # 0.8–1.0  dense canopy
  index-water: "#2b7ec9"         # < 0     open water

  semantic-error: "#e0404a"
  semantic-warning: "#d4934a"
  semantic-success: "#3ecf72"
  semantic-info: "#4a9fd4"

typography:
  display-mega:
    fontFamily: "'Canela', 'Georgia', 'Times New Roman', serif"
    fontSize: 72px
    fontWeight: 300
    lineHeight: 1.05
    letterSpacing: -1.8px

  display-lg:
    fontFamily: "'Canela', serif"
    fontSize: 44px
    fontWeight: 300
    lineHeight: 1.12
    letterSpacing: -0.88px

  display-md:
    fontFamily: "'Canela', serif"
    fontSize: 30px
    fontWeight: 300
    lineHeight: 1.2
    letterSpacing: -0.45px

  display-sm:
    fontFamily: "'Canela', serif"
    fontSize: 22px
    fontWeight: 300
    lineHeight: 1.3
    letterSpacing: -0.22px

  title-md:
    fontFamily: "'DM Sans', system-ui, sans-serif"
    fontSize: 15px
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: 0

  title-sm:
    fontFamily: "'DM Sans', sans-serif"
    fontSize: 13px
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: 0.02px

  body-md:
    fontFamily: "'DM Sans', sans-serif"
    fontSize: 15px
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: 0

  body-sm:
    fontFamily: "'DM Sans', sans-serif"
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: 0

  caption:
    fontFamily: "'DM Sans', sans-serif"
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 0

  label-uppercase:
    fontFamily: "'DM Sans', sans-serif"
    fontSize: 10px
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: 1.2px
    textTransform: uppercase

  code:
    fontFamily: "'DM Mono', 'Fira Code', monospace"
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: 0

  data:
    fontFamily: "'DM Mono', monospace"
    fontSize: 13px
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: -0.2px

  button:
    fontFamily: "'DM Sans', sans-serif"
    fontSize: 13px
    fontWeight: 500
    lineHeight: 1.0
    letterSpacing: 0.1px

  nav-link:
    fontFamily: "'DM Sans', sans-serif"
    fontSize: 13px
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: 0

rounded:
  none: 0px
  xs: 2px
  sm: 4px
  md: 6px
  lg: 10px
  xl: 14px
  pill: 9999px
  full: 9999px

spacing:
  xxs: 4px
  xs: 8px
  sm: 12px
  base: 16px
  md: 20px
  lg: 24px
  xl: 32px
  xxl: 48px
  section: 80px
  section-lg: 120px

components:
  top-nav:
    backgroundColor: "{colors.canvas}"
    borderBottom: "1px solid {colors.hairline}"
    textColor: "{colors.body}"
    typography: "{typography.nav-link}"
    height: 60px

  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button}"
    rounded: "{rounded.sm}"
    padding: 9px 18px
    height: 38px

  button-primary-active:
    backgroundColor: "{colors.primary-active}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.sm}"

  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    border: "1px solid {colors.hairline-strong}"
    typography: "{typography.button}"
    rounded: "{rounded.sm}"
    padding: 8px 17px
    height: 38px

  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.muted}"
    typography: "{typography.button}"

  hero-band:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.display-mega}"
    padding: "120px 80px"

  map-card:
    backgroundColor: "{colors.surface-card}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.lg}"
    padding: 0

  data-pane:
    backgroundColor: "{colors.canvas-soft}"
    textColor: "{colors.body}"
    typography: "{typography.code}"
    rounded: "{rounded.md}"
    padding: 16px
    border: "1px solid {colors.hairline-soft}"

  feature-card:
    backgroundColor: "{colors.surface-card}"
    textColor: "{colors.ink}"
    border: "1px solid {colors.hairline}"
    typography: "{typography.title-md}"
    rounded: "{rounded.lg}"
    padding: 24px

  stat-card:
    backgroundColor: "{colors.surface-card}"
    textColor: "{colors.ink}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.lg}"
    padding: 20px

  # Spectral index legend chips — map/chart use only
  index-chip-dead:
    backgroundColor: "{colors.index-dead}"
    textColor: "#fff"
    rounded: "{rounded.xs}"
    padding: "3px 8px"

  index-chip-sparse:
    backgroundColor: "{colors.index-sparse}"
    textColor: "#fff"
    rounded: "{rounded.xs}"
    padding: "3px 8px"

  index-chip-stressed:
    backgroundColor: "{colors.index-stressed}"
    textColor: "#0e1a12"
    rounded: "{rounded.xs}"
    padding: "3px 8px"

  index-chip-moderate:
    backgroundColor: "{colors.index-moderate}"
    textColor: "#0e1a12"
    rounded: "{rounded.xs}"
    padding: "3px 8px"

  index-chip-healthy:
    backgroundColor: "{colors.index-healthy}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.xs}"
    padding: "3px 8px"

  index-chip-dense:
    backgroundColor: "{colors.index-dense}"
    textColor: "#fff"
    rounded: "{rounded.xs}"
    padding: "3px 8px"

  index-chip-water:
    backgroundColor: "{colors.index-water}"
    textColor: "#fff"
    rounded: "{rounded.xs}"
    padding: "3px 8px"

  code-block:
    backgroundColor: "{colors.surface-overlay}"
    textColor: "{colors.body-strong}"
    typography: "{typography.code}"
    rounded: "{rounded.md}"
    padding: 20px
    border: "1px solid {colors.hairline}"

  badge-pill:
    backgroundColor: "{colors.surface-strong}"
    textColor: "{colors.muted}"
    typography: "{typography.label-uppercase}"
    rounded: "{rounded.pill}"
    padding: "3px 10px"

  cta-band:
    backgroundColor: "{colors.canvas-raised}"
    textColor: "{colors.ink}"
    border: "1px solid {colors.hairline}"
    typography: "{typography.display-md}"
    padding: "96px 80px"

  footer:
    backgroundColor: "{colors.canvas}"
    borderTop: "1px solid {colors.hairline-soft}"
    textColor: "{colors.muted}"
    typography: "{typography.body-sm}"
    padding: "64px 48px"
---

## Overview

Verdant is a dark-first editorial system for environmental and geospatial analytics products. The page floor is deep forest ink (`{colors.canvas}` — #0e1a12), warm parchment (`{colors.ink}` — #f2ede4) carries long-form reading, and a single accent, **Signal Green** (`{colors.primary}` — #3ecf72), provides the system's only brand voltage.

Canela drives the display layer at weight 300, DM Sans handles interface chrome, and DM Mono owns all numeric, geospatial, and code-facing surfaces. The strongest signature is the spectral index chip palette, a seven-stop NDVI/data-only colour ramp reserved for legends, charts, and tabular analytics.

> Use Verdant when the product should feel editorial, scientific, and terrain-aware rather than generic SaaS-dark.

### At a Glance

| Aspect | Decision | Notes |
|---|---|---|
| Product category | Environmental and geospatial analytics | Built for maps, dashboards, metrics, and editorial storytelling |
| Visual mood | Dark-first editorial | Forest ink canvas, parchment text, restrained contrast |
| Brand accent | `{colors.primary}` / #3ecf72 | Only for CTAs, wordmark, and live data highlights |
| Display type | Canela at 300 | Never bolded; used to create scientific publishing tone |
| UI type | DM Sans | Interface chrome, labels, controls |
| Data type | DM Mono | Coordinates, index values, timestamps, tables, code |
| Surface treatment | Hairline-only depth | No drop shadows; contrast is driven by surface shifts and borders |
| Rhythm | 80px standard sections, 120px hero bands | Generous spacing prevents dark-surface fatigue |

### Signature Characteristics

| Trait | Implementation |
|---|---|
| Forest canvas | Deep green-undertoned near-black, not neutral charcoal |
| Single-voltage CTA system | Signal Green is scarce and intentional |
| Editorial display layer | Canela 300 with negative tracking on dark surfaces |
| Data-native UI layer | DM Mono applied to every metric and coordinate surface |
| NDVI identity | Seven dedicated spectral tokens for vegetation and water mapping |
| Depth model | Thin moss-tinted borders, no shadow stack |

---

## Colors

### Core Palette

| Group | Token | Value | Primary Use |
|---|---|---|---|
| Brand | `{colors.primary}` | #3ecf72 | Primary CTAs, wordmark, live data highlights |
| Brand | `{colors.primary-active}` | #2ab05c | Pressed and active CTA state |
| Brand | `{colors.primary-muted}` | #1a6637 | Subtle accent fills on dark surfaces |
| Surface | `{colors.canvas}` | #0e1a12 | Forest-ink page floor |
| Surface | `{colors.canvas-soft}` | #111f15 | Inset panes and softened dark interiors |
| Surface | `{colors.canvas-raised}` | #162219 | Elevated bands and alternating sections |
| Surface | `{colors.surface-card}` | #142018 | Card surfaces over the main canvas |
| Surface | `{colors.surface-strong}` | #1e2e20 | Badge fills and stronger containers |
| Surface | `{colors.surface-overlay}` | #0a1209 | Deep inset layers such as code blocks |
| Hairline | `{colors.hairline}` | #1e2e20 | Standard 1px card and panel borders |
| Hairline | `{colors.hairline-soft}` | #192518 | Quiet separators and footer dividers |
| Hairline | `{colors.hairline-strong}` | #2c4030 | Stronger panel edges and button outlines |
| Text | `{colors.ink}` | #f2ede4 | Headings and long-form display text |
| Text | `{colors.ink-strong}` | #ffffff | High-emphasis states and active nav |
| Text | `{colors.body}` | #b8c4b0 | Default running copy |
| Text | `{colors.body-strong}` | #d4ddd0 | Strong secondary text |
| Text | `{colors.muted}` | #7a9070 | Labels, captions, low-emphasis copy |
| Text | `{colors.muted-soft}` | #506050 | Disabled or receding UI states |
| Text | `{colors.on-primary}` | #0a1a0e | Text placed on Signal Green |

### Spectral Index Scale (map / chart use only)

| Token | Value | NDVI Range | Meaning |
|---|---|---|---|
| `{colors.index-dead}` | #8b1a1a | < 0.1 | Bare / dead vegetation |
| `{colors.index-sparse}` | #c97d2b | 0.1–0.2 | Sparse cover |
| `{colors.index-stressed}` | #d4c043 | 0.2–0.4 | Stressed / dry |
| `{colors.index-moderate}` | #7dbd4a | 0.4–0.6 | Moderate health |
| `{colors.index-healthy}` | #3ecf72 | 0.6–0.8 | Healthy vegetation |
| `{colors.index-dense}` | #1a8f5a | 0.8–1.0 | Dense canopy |
| `{colors.index-water}` | #2b7ec9 | < 0 | Open water |

### Semantic

| Token | Value | Usage Note |
|---|---|---|
| `{colors.semantic-error}` | #e0404a | Error messaging and destructive status |
| `{colors.semantic-warning}` | #d4934a | Warning states |
| `{colors.semantic-success}` | #3ecf72 | Success state; intentionally shares Signal Green |
| `{colors.semantic-info}` | #4a9fd4 | Informational state |

---

## Typography

### Font Families

| Layer | Primary Family | Fallback | Weight Range | Intended Use |
|---|---|---|---|---|
| Display | Canela | `Georgia`, `Times New Roman`, serif | 300 only | Hero headlines, section titles, editorial display |
| UI / Body | DM Sans | `system-ui`, sans-serif | 400 / 500 / 600 | Body copy, controls, navigation, labels |
| Data / Code | DM Mono | `Fira Code`, monospace | 400 / 500 | Coordinates, metrics, timestamps, code blocks |

### Hierarchy

| Token | Size | Weight | Line Height | Letter Spacing | Family | Use |
|---|---|---|---|---|---|---|
| `{typography.display-mega}` | 72px | 300 | 1.05 | -1.8px | Canela | Homepage hero h1 |
| `{typography.display-lg}` | 44px | 300 | 1.12 | -0.88px | Canela | Section headlines |
| `{typography.display-md}` | 30px | 300 | 1.20 | -0.45px | Canela | Feature section titles |
| `{typography.display-sm}` | 22px | 300 | 1.30 | -0.22px | Canela | Card group headings |
| `{typography.title-md}` | 15px | 500 | 1.4 | 0 | DM Sans | Component titles |
| `{typography.title-sm}` | 13px | 600 | 1.4 | 0.02px | DM Sans | List labels, metadata keys |
| `{typography.body-md}` | 15px | 400 | 1.6 | 0 | DM Sans | Default body copy |
| `{typography.body-sm}` | 13px | 400 | 1.55 | 0 | DM Sans | Footer, captions |
| `{typography.caption}` | 12px | 400 | 1.4 | 0 | DM Sans | Secondary labels |
| `{typography.label-uppercase}` | 10px | 600 | 1.4 | 1.2px | DM Sans | Section tags, chip labels |
| `{typography.code}` | 12px | 400 | 1.6 | 0 | DM Mono | Code blocks |
| `{typography.data}` | 13px | 500 | 1.4 | -0.2px | DM Mono | Index values, coordinates, stats |
| `{typography.button}` | 13px | 500 | 1.0 | 0.1px | DM Sans | CTA labels |
| `{typography.nav-link}` | 13px | 500 | 1.4 | 0 | DM Sans | Navigation |

### Principles

| Principle | Rule | Why It Exists |
|---|---|---|
| Display restraint | Canela stays at weight 300 only | Preserves precision and editorial authority on dark surfaces |
| Numeric consistency | All numbers and coordinates use DM Mono | Prevents visual drift in tables, legends, and dashboards |
| Tracking discipline | Negative tracking is limited to display sizes | Keeps large serif headings compact without harming body readability |
| Warm headline contrast | Use `{colors.ink}` rather than pure white for display | Maintains natural warmth and avoids harsh high-contrast glare |

---

## Layout

### Spacing System

Base unit: 4px.

| Token | Value | Typical Use |
|---|---|---|
| `{spacing.xxs}` | 4px | Fine internal spacing |
| `{spacing.xs}` | 8px | Tight gaps and micro-layout |
| `{spacing.sm}` | 12px | Compact UI spacing |
| `{spacing.base}` | 16px | Base body rhythm |
| `{spacing.md}` | 20px | Dense card interiors |
| `{spacing.lg}` | 24px | Standard card padding |
| `{spacing.xl}` | 32px | Larger component separation |
| `{spacing.xxl}` | 48px | Block spacing |
| `{spacing.section}` | 80px | Standard section spacing |
| `{spacing.section-lg}` | 120px | Hero and full-width band spacing |

### Layout Rules

| Area | Structure | Notes |
|---|---|---|
| Content container | 1200px max width | Wide margins keep the dark surface breathable |
| Hero | Single-column lead with full-width artefact below | Map or product mockup anchors the story |
| Feature grid | 3-up on desktop | Collapses responsively for tablet and mobile |
| Dashboard preview | 60 / 40 split | Map on the left, data panel on the right |
| Footer | 4-column link grid | Maintains editorial rather than app-shell feel |
| Card interiors | 16px to 24px | Denser than light-mode systems by design |

### Whitespace Philosophy

Dark surfaces tolerate more density inside components, so internal spacing stays tighter than in light UI systems. The compensation happens at the macro level: section spacing remains generous at 80px to 120px to prevent fatigue during extended reading.

---

## Elevation & Depth

The system uses **hairline-only depth**. No drop shadows — they disappear on dark backgrounds. Cards emerge from the canvas via the slight `{colors.surface-card}` / `{colors.canvas}` contrast and a 1px moss-tinted hairline border.

| Level | Treatment | Use |
|---|---|---|
| Canvas | `{colors.canvas}` #0e1a12 | Page floor |
| Raised band | `{colors.canvas-raised}` #162219 | CTA sections, alternating feature rows |
| Card | `{colors.surface-card}` #142018 | Content cards |
| Inset pane | `{colors.canvas-soft}` #111f15 | Data panels inside cards |
| Deep inset | `{colors.surface-overlay}` #0a1209 | Code blocks, terminal views |

### Decorative Depth

| Device | Treatment |
|---|---|
| Map card border | `{colors.hairline}` creates a topographic-line effect |
| Spectral chips | Chromatic depth comes from the data palette, not extra elevation |
| Hero artefact | Imagery carries the visual weight; borders stay thin and shadowless |

---

## Shapes

### Border Radius Scale

| Token | Value | Use |
|---|---|---|
| `{rounded.none}` | 0px | Map edges, full-bleed panels |
| `{rounded.xs}` | 2px | Index chips, tiny badges |
| `{rounded.sm}` | 4px | CTA buttons, inputs |
| `{rounded.md}` | 6px | Form elements, inline tags |
| `{rounded.lg}` | 10px | Cards, data panes |
| `{rounded.xl}` | 14px | Modal dialogs, floating panels |
| `{rounded.pill}` | 9999px | Navigation pills, legend badges |

---

## Components

### Core Components

| Component | Role | Key Specs |
|---|---|---|
| `top-nav` | Global navigation | `{colors.canvas}` background, 1px `{colors.hairline}` bottom border, 60px height, Signal Green wordmark |
| `button-primary` | Primary CTA | `{colors.primary}` fill, `{colors.on-primary}` text, `{rounded.sm}`, 9px x 18px padding, 38px height |
| `button-primary-active` | Active primary CTA | Swaps to `{colors.primary-active}` |
| `button-secondary` | Outline CTA | Transparent fill, `{colors.ink}` text, 1px `{colors.hairline-strong}` border |
| `button-ghost` | Inline or tertiary action | Transparent fill, `{colors.muted}` text |
| `map-card` | Hero or preview artefact container | `{colors.surface-card}` background, `{rounded.lg}`, 1px `{colors.hairline}`, edge-to-edge imagery |
| `data-pane` | Inset metric or code panel | `{colors.canvas-soft}` background, `{typography.code}`, `{rounded.md}`, 16px padding |
| `feature-card` | General content card | `{colors.surface-card}`, 1px `{colors.hairline}`, `{rounded.lg}`, 24px padding |
| `stat-card` | Metric display card | `{colors.surface-card}`, 1px `{colors.hairline}`, `{rounded.lg}`, 20px padding, DM Mono value |

### Spectral Index Chips (map / chart use only)

Seven chips correspond to the seven index tokens. They appear exclusively in legends, chart scales, and data-table value columns. All use `{typography.label-uppercase}` and `{rounded.xs}`.

| Chip | Background | Text Color | Data Meaning |
|---|---|---|---|
| `index-chip-dead` | `{colors.index-dead}` / #8b1a1a | #fff | Bare or dead vegetation |
| `index-chip-sparse` | `{colors.index-sparse}` / #c97d2b | #fff | Sparse cover |
| `index-chip-stressed` | `{colors.index-stressed}` / #d4c043 | #0e1a12 | Stressed or dry vegetation |
| `index-chip-moderate` | `{colors.index-moderate}` / #7dbd4a | #0e1a12 | Moderate vegetation health |
| `index-chip-healthy` | `{colors.index-healthy}` / #3ecf72 | `{colors.on-primary}` | Healthy vegetation |
| `index-chip-dense` | `{colors.index-dense}` / #1a8f5a | #fff | Dense canopy |
| `index-chip-water` | `{colors.index-water}` / #2b7ec9 | #fff | Open water |

### Support Components

| Component | Role | Key Specs |
|---|---|---|
| `code-block` | Code or terminal presentation | `{colors.surface-overlay}` background, `{colors.body-strong}` text, `{typography.code}`, 20px padding |
| `badge-pill` | Quiet status or taxonomy marker | `{colors.surface-strong}` background, `{colors.muted}` text, `{rounded.pill}`, 3px x 10px padding |
| `cta-band` | Section-level conversion block | `{colors.canvas-raised}` background, 1px `{colors.hairline}` border, `{typography.display-md}`, 96px vertical padding |
| `footer` | Global footer | `{colors.canvas}` background, 1px `{colors.hairline-soft}` top border, 4-column link grid, 64px x 48px padding |

---

## Do's and Don'ts

| Do | Don't |
|---|---|
| Use `{colors.primary}` only for primary CTAs, the wordmark, and live data highlights | Introduce a second brand action colour |
| Keep Canela at weight 300 | Use Canela at 400 or heavier |
| Use `{colors.ink}` for display text | Switch headline text to pure white by default |
| Use DM Mono for NDVI values, coordinates, timestamps, and area figures | Use DM Sans for numeric data surfaces |
| Reserve spectral index colours for legends, charts, and tables | Reuse NDVI ramp colours for generic UI states |
| Create depth with surface contrast and hairlines | Add drop shadows to force elevation |
| Treat Signal Green as scarce voltage | Spread Signal Green across secondary UI elements |

---

## Responsive Behaviour

### Breakpoints

| Name | Width | Key Changes |
|---|---|---|
| Mobile | < 640px | Hero 72px → 32px Canela; map card single-pane; feature grid 1-up; nav hamburger. |
| Tablet | 640–1024px | Hero 48px; 60/40 map+data pane compresses; feature grid 2-up. |
| Desktop | 1024–1280px | Full hero 72px; split map+data layout; feature grid 3-up. |
| Wide | > 1280px | Content caps at 1200px; generous outer margins. |

### Collapsing Strategy

| Element | Mobile / Tablet Behavior |
|---|---|
| Top navigation | Switches to hamburger below 768px |
| Map plus data pane | Stacks vertically on tablet; simplifies to map-first presentation on mobile |
| Feature grid | 3-up to 2-up to 1-up |
| Stat cards | 4-up to 2-up, staying scannable on mobile |

---

## Known Gaps

| Gap | Status / Recommendation |
|---|---|
| Canela licensing | Use Cormorant Garamond at 300 or Lora at 400 as open-source substitutes |
| DM Sans / DM Mono sourcing | Available through Google Fonts |
| Map tile rendering and satellite compositing | Outside the scope of this design-system definition |
| NDVI ramp implementation logic | Application-layer concern, not a system token concern |
| Light mode | Not defined in v1.0 |
| Motion system | Animation timings for map load, chips, and data panes are intentionally out of scope |