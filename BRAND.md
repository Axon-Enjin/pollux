> Materialized file. Edit the docs source and re-run materialize.

# Brand:

> Verbal identity, materialized from the DSD (sections 0, 0.5, 1, 2, 8, 9). Subsections 2.2-2.4 and 8.4 ride along when present in those sections.

## 0. Brand Stance

### The Three Rules

| Rule | How Pollux satisfies it |
|---|---|
| **Make it relatable** | Barangay chat energy: a phone in a typhoon queue, not a Davos trust dashboard. Warm paper, civic peer tone. |
| **Make it human** | Peer-led copy ("spot the trick with us"), paced text, no mascot guilt. |
| **Make them part of the branding** | Leaders publish *their* official packs; learners see local routes and keywords, not generic stock crisis photos. |

### Mode

**Selected mode:** `Both`; Brand Mode for landing; Product Mode for lesson and admin.

### Aesthetic Provenance

| Question | Answer |
|---|---|
| **Specific cultural / aesthetic reference** | Philippine barangay hall bulletin board + quiet study desk: paper notices, ballpoint underlines, teal stamp ink. Not Silicon Valley Trust & Safety chrome. |
| **One sentence that would never appear in AI slop here** | "Finish the trick. Share the pack your kapitbahay can trust." |
| **The archetypical user** | Mia, 19, SK information officer (PRD §2). |
| **The slop default for this category** | Purple MIL SaaS, dark-mode glow shields, trophy hackathon badges, confetti for correct answers. |
| **How users appear in the brand** | Local pack titles and leader-published items; optional first-name in lesson progress only. |

### Anti-References

| Anti-reference | Why it's forbidden here |
|---|---|
| Purple-on-white AI SaaS | Category default; fails Three Rules |
| Dark cyber glow "threat intel" | Signals surveillance, not peer civic care |
| Duolingo confetti streaks | Turns literacy into dopamine debt |

---
## 0.5 Concept Visuals (from IDEA)

**IDEA link:** [idea-pollux.md](idea-pollux.md) §5

| Screen / section | Asset path | Approved in IDEA? | DSD notes |
|------------------|------------|-------------------|-----------|
| Learner lesson | [assets/concept/pollux-lesson.png](assets/concept/pollux-lesson.png) | Yes | Warm paper, teal accents, choice buttons |
| Leader pack | [assets/concept/pollux-leader.png](assets/concept/pollux-leader.png) | Yes | List + share; no heavy dashboard |

**Impeccable init:** Deferred (TBD). Run `/impeccable init` before locking DSD. ui-ux-pro-max token generation TBD.

---
## 1. Design Philosophy & Vision

**Core aesthetic:** Warm paper, deep teal ink, paced mobile screens, one task at a time.

**Emotional intent:** Steady civic confidence. Not panic. Not gamified guilt.

**What this system explicitly avoids:**
- Purple/indigo gradients and Inter-as-only-font.
- Confetti, streak shame, trophy walls.
- Enterprise listening dashboard density in v1 admin.

---
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
## 8. Impeccable Gate

**Status:** Not run. Before public launch: no open P0/P1; every audit dimension ≥ 3.

---
## 9. Governance

DSD is source of truth. Materialize `BRAND.md` and `DESIGN.md` via FMD templates after lock. Do not hand-edit materialized files as source.

---
