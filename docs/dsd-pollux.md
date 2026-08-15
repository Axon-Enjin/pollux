# Design System Document (DSD)

**System Name:** Pollux Foundation
**Date:** 2026-08-16
**Version:** 0.2
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A
**PRD:** [prd-pollux.md](prd-pollux.md)

---

## 0. Brand Stance

**Tagline:** They run the session. We pack the bag.

**One-liner:** Pollux is the open campaign kit an SK officer runs herself: modules, a program guide, and a site students return to after.

v1 brand is the campaign, the session, and the print. Pack tap is a later desk action, not the product people see first. Lesson-drill phrasing ("spot the trick", "finish the round") belongs only where PRD-F12 is named.

### The Three Rules

| Rule | How Pollux satisfies it |
|---|---|
| **Make it relatable** | Covered-court session energy: a printed packet on a folding table, a phone advancing one module, not a Davos trust dashboard. Warm paper, civic peer tone. |
| **Make it human** | Calm peer-led copy. She runs the session. We pack the bag: modules, a program guide, and a site students return to after. |
| **Make them part of the branding** | Leaders run *their* session and print *their* packet. Neighbors see local modules and routes, not generic stock crisis photos. Seekers Guild is not the barangay voice. |

### Mode

**Selected mode:** `Both`; Brand Mode for landing; Product Mode for campaign session, print packet, kit catalog, and (flag on) the outreach kit. Pack launch and commit share remain Product Mode when those screens ship. They are not the v1 brand metaphor.

### Aesthetic Provenance

| Question | Answer |
|---|---|
| **Specific cultural / aesthetic reference** | Philippine barangay hall bulletin board + quiet study desk: paper notices, ballpoint underlines, teal stamp ink. Not Silicon Valley Trust & Safety chrome. |
| **One sentence that would never appear in AI slop here** | "They run the session. We pack the bag." |
| **The archetypical user** | Mia, 19, SK information officer (PRD §2). Camp facilitator is a second hat, not a different brand. |
| **The slop default for this category** | Purple MIL SaaS, dark-mode glow shields, trophy hackathon badges, confetti for correct answers, Guild crest on government pages. |
| **How users appear in the brand** | Local kit titles, current module, print packet. Optional first-name on session follow-along only. No first-name leaderboards. Participant view shows the current module, not a score. |

### Anti-References

| Anti-reference | Why it's forbidden here |
|---|---|
| Purple-on-white AI SaaS | Category default; fails Three Rules |
| Dark cyber glow "threat intel" | Signals surveillance, not peer civic care |
| Duolingo confetti streaks, trophies, XP | Turns literacy into dopamine debt; F12 drill (if shipped) stays quiet; F15 is never a game |
| Guild sigil on SK-official screens | Seekers Guild is community stewardship, not barangay voice. Pack read, commit share, and F3 paper card must not wear a Guild crest |

---

## 0.5 Concept Visuals (from IDEA)

**IDEA link:** [idea-pollux.md](idea-pollux.md) §5

| Screen / section | Asset path | Approved in IDEA? | DSD notes |
|------------------|------------|-------------------|-----------|
| Leader pack / launch | [assets/concept/pollux-leader.png](assets/concept/pollux-leader.png) | Yes | List + share; no heavy dashboard; v1 primary |
| Legacy lesson frame | [assets/concept/pollux-lesson.png](assets/concept/pollux-lesson.png) | Legacy | Could-Have F12 drill only. Not the v1 brand. Do not reuse choice-button game chrome on F15 |
| F15 kit surfaces | none yet | No | Catalog, cockpit, runner, participant, print: follow §3.1 until frames exist |

**Impeccable init:** Deferred (TBD). Run `/impeccable init` before locking DSD. ui-ux-pro-max token generation TBD.

---

## 1. Design Philosophy & Vision

**Core aesthetic:** Warm paper, deep teal ink, paced mobile screens, one task at a time.

**Emotional intent:** Steady civic confidence. Not panic. Not gamified guilt. Camp sessions feel like a peer briefing in a covered court, not a hackathon stage.

**What this system explicitly avoids:**
- Purple/indigo gradients and Inter-as-only-font.
- Confetti, streak shame, trophy walls, score rings, XP.
- Guild sigil, UNESCO badge, or Pollux logo treated as SK-official identity on pack, share, or paper card.
- Enterprise listening dashboard density in v1 admin.
- Lesson-primary copy ("spot the trick", "finish the round") on pack or kit screens.

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

Local, documentary, daylight. No stock "hacker in hoodie." Prefer empty states with simple line icons over illustrations that shout EdTech. Kit print uses the same paper/ink language as the PWA. Do not switch to contest poster art.

---

## 3. Components (v1)

| Component | Rules |
|-----------|-------|
| Primary button | Teal fill, ink label on soft; min 44px height |
| Vignette card | F12 only if that drill ships. Full-bleed text block; not nested card-in-card. Do not use on F15 |
| Choice buttons | F12 only. Equal weight until selected; then teal-soft. Not on kit participant view |
| Badge | Small, quiet; no confetti. Kit vs canon is a text stamp, not a trophy |
| Pack list row | Title + status + share; no KPI strip |
| Kit kind stamp | Plain label `outreach_kit` or `canon`. Never "official" on kit chrome |
| Quiet banner | One line on kit paths: seminar material, not SK crisis canon |
| Agenda list | Numbered modules; current step underlined; no progress gamification |
| Print page | Browser print, paper background, ink type. No app chrome, no Guild mark |

---

## 3.1 Screens (PRD inventory, F15 added)

Aligns with [prd-pollux.md](prd-pollux.md) §5.1. Product Mode unless noted.

### Identity: F3 paper card vs kit QR

Two printable artifacts. They must not look like twins of government identity.

| Artifact | Owns | Visual rules |
|----------|------|----------------|
| **F3 paper card** | Canon pack identity after SK launch (PRD-F3) | One page. Pack title, publisher, date, version, pack URL, QR to that pack. Looks like a barangay notice. No Guild sigil. No UNESCO mark as publisher. No kit module names |
| **Kit print packet / kit QR** | Seminar fallback if 3G dies (PRD-F15) | Multi-page or one-pager plus handout. Stamp `outreach_kit`. QR may open the kit URL or join the session. Copy must say this is the session, not the official desk. If a published canon pack exists, point at the existing F3 card; do not mint a second official QR from the kit URL |

If there is no published canon pack: print the kit packet only. Do not invent a fake F3 card.

### SK and Guild surfaces (existing)

| Screen | Purpose | Visual notes |
|--------|---------|--------------|
| Landing | SK self-launch + Guild contribute | Brand Mode OK. Guild named as community, not as the Page |
| Sign in | Auth | Quiet form; no trophy |
| Org home | Launch checklist | One task list; complete states without badges |
| Template pick | Clone flood / election / notices | Titles, not game cards |
| Pack editor | Fill local fields | Form density; empty local fields stay empty |
| Pack detail | Items + provenance + share | SK-official. No Guild sigil |
| Commit share | Pause then official or refuse | Calm pause. No countdown gamification. No Guild sigil |
| Paper card | Print/save QR for **canon** pack | See identity table. F3 only |
| Admin packs | Create / publish / archive | List + status; no KPI wall |
| Contribute | Issues / templates | Guild belongs here, not on pack read |

### PRD-F15 outreach kit surfaces

Flag `ENABLE_OUTREACH_KIT`. When off, these routes 404 or hide. Reader never sees facilitator start or print (403).

| Screen | Purpose | States | Visual notes |
|--------|---------|--------|--------------|
| **Kit catalog** | List published `outreach_kit` packs | empty / listed / flag off | Same pack-list row language as admin, plus kind stamp. Empty: one sentence, no illustration contest. Flag off: not a tease of locked trophies |
| **Facilitator cockpit** | Agenda, notes, start session, print | ready / session live / print | Peer briefing desk. Agenda + facilitation notes visible to facilitator only. Start and Print as equal-weight actions. Live state is a quiet "session running" line, not a stage timer. No Guild sigil |
| **Session runner** | Advance sequenced modules | module / complete | One module at a time. Advance / back. Module names from pack (`access-the-pack` … `act-launch-the-desk`). Complete is "session closed", not a diploma. Optional next step to F3 is a text link, never a required gate or score |
| **Participant view** | Follow current module | waiting / module / done | Reader chrome. Module, activity, handout as authored for participants. **No** `facilitation_note`. **No** canon crisis facts from this path. Waiting is "we start when the facilitator is ready", not a lobby with avatars. Done is not scored (not F12) |
| **Print packet** | Paper if 3G dies | static | Browser print. Facilitator one-pager, learner handout, consent checklist as authored. Kit QR labeled seminar. F3 card reused only when a canon pack exists. No second government identity |

Copy register on F15: facilitator notes may be slightly denser; participant and print stay short, bilingual-friendly, same paper/teal. Never "spot the trick", "level up", or "you won."

---

## 4-7. Deferred

Patterns, motion, full a11y matrix, and taste dials: fill before lock. Minimum a11y now: color contrast ≥ WCAG AA for ink on paper; focus rings visible; tap targets ≥ 44px. Print packet must remain readable in black-and-white if the hall printer has no color.

---

## 8. Impeccable Gate

**Status:** Not run. Before public launch: no open P0/P1; every audit dimension ≥ 3.

---

## 9. Governance

DSD is source of truth. Materialize `BRAND.md` and `DESIGN.md` via FMD templates after lock. Do not hand-edit materialized files as source.

---

## Self-Check

- [x] §0 Brand Stance complete
- [x] Concept visuals linked (lesson frame marked legacy)
- [x] Anti-references named (including Guild sigil and trophy UI)
- [x] Tokens drafted
- [x] PRD-F15 screens in §3.1; F3 paper card vs kit QR distinguished
- [x] Lesson-primary copy patched where it would confuse F15
- [x] Impeccable deferred explicitly
