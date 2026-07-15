# Validation Brief (VALIDATION)

**Project:** Pollux
**Date:** 2026-07-15
**Version:** 0.1
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A
**IDEA:** [idea-pollux.md](idea-pollux.md)

---

## 1. Problem Evidence

**Claim:** Passive tips and late fact-checks fail where active inoculation games succeed, and grassroots leaders cannot afford enterprise listening or paid blast messaging.

**Evidence we have:**

| Source | What it shows |
|--------|---------------|
| World Bank Find the Fake (Jordan, WhatsApp chatbot game) | Interactive game improved misinformation discernment vs infographics; brief game-only arm risked over-skepticism. https://doi.org/10.1596/1813-9450-10933 |
| Scrutiny FC-3 | Claim audited; study resolves and supports pedagogy thesis |

**Evidence we don't have (and accept for this sprint):** PWA transfer of WhatsApp study effects; LOIs from LGUs; willingness-to-pay for B2B seats in PH.

---

## 2. Competitor / Substitute Scan

| Substitute | How users cope today | Our wedge |
|------------|----------------------|-----------|
| Static MIL PDFs / DepEd modules | Workshops, then forgotten | Active lesson with score and true/false calibration |
| Meltwater / enterprise listening | SK cannot afford | Keyword watch lite + curated packs |
| Bad News / Go Viral style games | Global English web games | Local packs + leader workflow for barangay context |
| SMS / WhatsApp template blasts | LGU pays carriers | Explicit non-goal until buyer funds |

**Why we still build:** Pedagogy is evidenced. Distribution and ops can start on free-tier web without paid messaging.

---

## 3. Feasibility in Timebox

**Available time:** Startup Full docs this session; product MVP weeks (not hours).

**Must ship for demo:** Rule-based inoculation lesson on PWA with one true-news vignette per technique; one published content pack; leader share link.

| Workstream | Estimate | Risk |
|------------|----------|------|
| Lesson rule engine + UI | 1-2 weeks | Content quality |
| Packs + admin lite | 1 week | Approval workflow ambiguity |
| Auth + roles | 3-5 days | Supabase free pause |
| Telegram adapter | Optional later | Channel TBD |

**Biggest technical unknown:** Whether LGU buyers accept a PWA without WhatsApp reach.

**Mitigation:** Pilot with one SK federation; sell measurable completion + discernment quiz, not blast reach.

---

## 4. Kill Criteria

| Kill signal | Status (Go / Pivot / Stop) |
|-------------|----------------------------|
| Cannot ship rule-based lesson without LLM spend | Go (architecture forbids it) |
| First pilot refuses curated packs / demands open AI Q&A on crisis | Pivot (hold line or stop LGU path) |
| Commercial host cost exceeds contribution before first paid seat (UES-D1) | Stop paid growth; stay prototype on Hobby |

**Decision:** Go; pedagogy and bootstrap doctrine hold. Distribution and pricing remain TBDs in GTM/UES.

---

## 5. Concept Visual Reactions

| Asset (from IDEA) | Reaction | Change requested |
|-------------------|----------|------------------|
| pollux-lesson.png | Calm, readable; teal OK | Keep; avoid confetti |
| pollux-leader.png | Pack list clear | Keep; no Meltwater-style dashboards |

**Visual go/no-go:** Go for peer-led calm direction.

---

## Self-Check

- [x] At least one piece of real evidence cited
- [x] Kill criteria are concrete
- [x] Feasibility table fits startup framing
- [x] No em-dashes
- [x] Next suggested doc: BRD / UES / PRD
