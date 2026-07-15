> Materialized file. Edit the docs source and re-run materialize.

# Design:

> Visual language, materialized from DSD §2-§8.

## 2. Brand Primitives

### 2.1 Colors

| Token | Value | Usage |
|-------|-------|-------|
| `--color-paper` | `#F7F3EA` | App background |
| `--color-ink` | `#1C1A17` | Body text |
| `--color-teal` | `#0F6B5C` | Primary actions, links |
| `--color-teal-soft` | `#D8EDE8` | Selected / badge wash |
| `--color-danger` | `#9B2C2C` | Errors only (not crisis chrome) |
| `--color-border` | `#DDD4C4` | Hairlines |

### 2.2 Typography

| Role | Font | Notes |
|------|------|-------|
| Display | Fraunces or similar warm serif | Headings; expressive, not Inter |
| Body | Source Serif 4 or Literata | Readable on phone |
| UI / labels | IBM Plex Sans | Buttons, forms |

### 2.3 Spacing & radius

| Token | Value |
|-------|-------|
| `--space-1` | 4px |
| `--space-2` | 8px |
| `--space-3` | 16px |
| `--space-4` | 24px |
| `--radius` | 8px (not pill-full for primary chrome) |

### 2.4 Imagery

Local, documentary, daylight. No stock "hacker in hoodie." Prefer empty states with simple line icons over illustrations that shout EdTech.

---
## 3. Components (v1)

| Component | Rules |
|-----------|-------|
| Primary button | Teal fill, ink label on soft; min 44px height |
| Vignette card | Full-bleed text block; not nested card-in-card |
| Choice buttons | Equal weight until selected; then teal-soft |
| Badge | Small, quiet; no confetti |
| Pack list row | Title + status + share; no KPI strip |

---
## 4-7. Deferred

Patterns, motion, full a11y matrix, and taste dials: fill before lock. Minimum a11y now: color contrast ≥ WCAG AA for ink on paper; focus rings visible; tap targets ≥ 44px.

---
## 8. Impeccable Gate

**Status:** Not run. Before public launch: no open P0/P1; every audit dimension ≥ 3.

---
