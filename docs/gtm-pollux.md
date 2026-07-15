# Go-To-Market (GTM) Strategy

**Project:** Pollux
**Date:** 2026-07-15
**Version:** 0.1
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A
**PRD:** [prd-pollux.md](prd-pollux.md)
**UES:** [ues-pollux.md](ues-pollux.md)

---

## 1. Product Summary (GTM View)

**What it does (one sentence):** Pollux trains youth to spot manipulation tricks in a short game and helps local leaders publish verified crisis packs without paid blast tools.

**Who it's for:** SK / LGU youth and DRRM officers, NGO MIL programs, and enterprise teams that need measurable resilience training.

**Core value proposition:** Active inoculation you can measure, plus governed packs leaders can trust, at bootstrap cost.

**Category:** Civic tech / enterprise cognitive resilience

---

## 2. Target Audience

**Primary ICP (Ideal Customer Profile):**
- *Who:* SK federation or LGU youth development / DRRM lead who already runs barangay info pages
- *Where they hang out:* LGU meetings, youth councils, NGO workshops, Facebook Pages (as users, not our paid channel)
- *What they already believe:* Rumors during storms and elections hurt their community; they lack tools
- *What will make them try this:* A 10-minute demo lesson + a pack of their own official routes

**Secondary audience:**
- *Who:* Enterprise L&D / trust-and-safety buyers
- *Why secondary:* Longer sales cycle; needs analytics dashboards beyond v1

**TBD (Scrutiny):** First named pilot org.

---

## 3. Pricing Model

**Model:** Paid B2G projects + B2B seats (no D2C freemium for v1 revenue)

| Tier | Price | What's Included | Limit / Gate |
|------|-------|-----------------|-------------|
| Community pilot | $0 (invite) | Lesson + 1 pack | Time-boxed; data shared for learning |
| B2G project | TBD (UES-E1) | Deployment + packs + training | Scoped barangays |
| B2B seats | TBD $8-20/seat-year (UES-E1) | Lesson access + admin | Seat count |

**Pricing rationale:** Trace to UES-E1/E3. Do not underprice below commercial hosting (UES-F4). Honor UES-D1.

**Payment processor:** TBD (invoice / grant first; Stripe later)

---

## 4. Positioning & Messaging

**Tagline:** Spot the trick. Share the verified pack.

**Primary message:** Learn how manipulation works in ten minutes. Publish official facts your barangay can trust, without buying SMS blasts.

**Proof points:**
- World Bank Find the Fake: interactive inoculation beat passive infographics
- Bootstrap burn doctrine: no paid messaging until a buyer funds it
- Peer-led UX for youth leaders, not a surveillance dashboard

**Objection handling:**

| Objection | Response |
|-----------|----------|
| "Just use WhatsApp blasts" | Blasts cost money and do not teach discernment. We teach first; messaging when you fund it. |
| "Is this Free Facebook?" | No. We ship a low-bandwidth PWA. Zero-rated Meta is not our product. |
| "Another MIL quiz" | Active vignettes with true/false calibration; completion and discernment metrics for buyers. |

---

## 5. Launch Channels & Tactics

**Owned channels:**

| Channel | Audience Size | Planned Action |
|---------|--------------|----------------|
| Founder network / SK contacts | TBD | Book 3 pilot conversations |
| Product landing + README | Public | Demo lesson CTA |

**Community / earned channels:**

| Channel | Tactic | Timing |
|---------|--------|--------|
| NGO MIL partners | Co-branded pilot | After MVP |
| UNESCO Youth Hackathon | Optional showcase only | If schedule aligns; not required |
| Local youth summits | Live lesson demo | Post-alpha |

**Content assets needed before launch:**

- [ ] Demo video (60-90 sec)
- [ ] Landing page with CTA
- [ ] One sample barangay flood pack
- [ ] README that stands alone

---

## 6. Launch Phases

| Phase | Criteria to Enter | Target Date | Goal |
|-------|------------------|-------------|------|
| **Alpha** | PRD Must-Haves coded; QAD happy path | TBD | 5-10 learners + 1 leader |
| **Beta** | Alpha feedback; no P0; CLR counsel flags tracked | TBD | 1 LGU/SK pilot pack live |
| **Public Launch** | CLR cleared for youth data; pricing live; UES-F4 commercial host | TBD | First paid pilot (BRD-M1) |
| **Post-launch** | Paid pilot live | TBD | Second LOI; decide TrustOps phase |

---

## 7. Success Metrics (30-day post-launch)

| BRD-M# | Metric | Target | How to Measure |
|--------|--------|--------|----------------|
| BRD-M1 | Paying pilots / LOIs | 1 | CRM / signed note |
| BRD-M2 | Lesson completion | ≥60% | `lesson_completed` / `lesson_started` |
| BRD-M3 | Product burn | Within UES hosting doctrine | Invoice / Vercel bill |

---

## Self-Check

- [x] ICP specific enough to name real people
- [x] Pricing traces to UES
- [x] UNESCO optional, not the plan
- [x] Phase gates binary where possible
