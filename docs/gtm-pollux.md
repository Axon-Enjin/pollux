# Go-To-Market (GTM) Strategy

**Project:** Pollux
**Date:** 2026-08-15
**Version:** 0.3
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A
**PRD:** [prd-pollux.md](prd-pollux.md)
**UES:** [ues-pollux.md](ues-pollux.md)
**Research input:** [research-pollux-agent-era-mil.md](research-pollux-agent-era-mil.md)

---

## 1. Product Summary (GTM View)

**What it does (one sentence):** Pollux is an open-source aide SK and LGU youth desks launch themselves: a local official pack plus a human commit before anything counts as SK-official.

**Who it's for:** SK officers and LGU youth / DRRM desks. Seekers Guild is the contributor and partnership channel, not the buyer.

**Core value proposition:** Official information they can launch without a vendor in the room. You cannot hire a firehose-checker. You can give Mia a canon desk.

**Category:** Civic tech / SK operations / MIL infrastructure

---

## 2. Target Audience

**Primary ICP (Ideal Customer Profile):**
- *Who:* SK information officer or LGU youth development / DRRM lead who already runs a barangay info Page
- *Where they hang out:* LGU meetings, SK federations, barangay chats, Facebook Pages (as users, not our paid channel)
- *What they already believe:* Rumors during storms and elections hurt their community; they lack tools they can run themselves
- *What will make them try this:* A phone demo: clone a flood template, publish, copy an official link, refuse a rumor not in the pack

**Secondary audience:**
- *Who:* Seekers Guild members and provincial seekers
- *Why secondary:* They contribute templates, issues, and SK introductions. They are not the publisher of SK facts.

**Tertiary audience:**
- *Who:* Enterprise L&D / trust-and-safety buyers
- *Why tertiary:* Longer sales cycle; not v1.

**TBD (Scrutiny G-1):** First named pilot org (stale / open).

**Unit hierarchy:** OSS self-serve is free. B2G project fee (DFY install / hosted) is the first paid ACV. Do not require Guild membership to launch. Do not quote lesson seats as the v1 metric.

---

## 3. Pricing Model

**Model:** Free OSS self-serve for SK launch. Paid B2G DFY / hosted later. B2B seats are not the v1 story.

| Tier | Price | What's Included | Limit / Gate |
|------|-------|-----------------|-------------|
| OSS self-serve | $0 | Canon desk, templates, commit share, paper card | SK owns facts; they host or use community instance |
| Community / Guild contribute | $0 | Issues, template PRs, partnership intros | Cannot publish another SK's facts |
| B2G project (first paid DFY) | **$4,000 USD** (UES-E1) | Install + 1 localized pack + admin training + report | Scoped barangays / one SK or LGU office |
| B2G project (city / multi-barangay) | $8,000–12,000 | More packs + facilitator days | Still inside UES $2k–15k band |
| Hosted LGU (later) | TBD | Cloudflare-hosted org so they do not self-host | After OSS loop works |

**Pricing rationale:** Trace to UES-E1/E3 for paid DFY. Closing the repo is not a revenue plan. Honor UES-D1. Free self-serve does not require an LOI. Paid DFY names a conversion path at kickoff.

**Payment processor:** Invoice / grant first; Stripe later

**Commercial host:** Cloudflare Pages/Workers before first paid invoice (Scrutiny G-3).

---

## 4. Positioning & Messaging

**Tagline:** They launch. We aide. Official only if a human commits.

**Primary message:** SK already has the mandate. Pollux is the gate: a pack they publish, a pause before official share, a paper card for 3G. Seekers Guild is how youth outside Manila help build it.

**UNESCO showcase sentence:** Pollux is an open-source aide SK councils launch themselves. Seekers Guild is the youth community that stewards it, especially seekers outside major hubs. Only a human SK officer can share a pack as official.

**Proof points:**
- UNESCO MIL goals as product behavior, not a MOOC ([MIL programme](https://www.unesco.org/en/media-information-literacy))
- Pack confinement as civic gate: no open-web crisis oracle
- Launch-without-us test on a phone
- Bootstrap burn doctrine: no paid messaging until a buyer funds it
- Peer-led UX for youth leaders, not a surveillance dashboard

**Objection handling:**

| Objection | Response |
|-----------|----------|
| "Just use WhatsApp blasts" | Blasts cost money and do not stop a fake map from looking official. We make official speech a human commit. |
| "Is this Free Facebook?" | No. We ship a low-bandwidth PWA. Zero-rated Meta is not our product. |
| "Another MIL quiz" | We dropped the game as the product. The product is the SK desk. |
| "Why not an AI that fact-checks everything?" | Volume wins that race. We refuse fluency as proof and keep crisis answers in published packs. |
| "Why not a surfing agent?" | Prompt-side guards fail under injection. We keep the officer as principal. |
| "Is this a Seekers Guild app?" | Guild stewards the repo. SK owns the Page and the facts. Launch does not require joining. |

---

## 5. Launch Channels & Tactics

**Owned channels:**

| Channel | Audience Size | Planned Action |
|---------|--------------|----------------|
| Founder network / SK contacts | TBD | Book 3 pilot conversations |
| Product landing + README | Public | Self-launch CTA |
| GitHub (Apache-2.0) | Public | Issues + template PRs |

**Community / earned channels:**

| Channel | Tactic | Timing |
|---------|--------|--------|
| Seekers Guild | Contribution rungs; provincial seekers; SK intros | Ongoing; not a publish gate |
| SK federations / LGU youth desks | Self-launch kit | After MVP |
| UNESCO Youth Hackathon | **First showcase venue** of the SK+Guild story; not a revenue plan | 16 Aug 2026 23:59 Paris deadline for this edition |
| NGO MIL partners | Co-branded pilot | After MVP |

**Content assets needed before launch:**

- [ ] Demo video (60-90 sec): clone, publish, commit share
- [ ] Landing page with CTA
- [ ] One flood template (empty local fields)
- [ ] README that stands alone
- [ ] UNESCO proposal + 3-min pitch ([pitch-pollux.md](pitch-pollux.md))

---

## 6. Launch Phases

| Phase | Criteria to Enter | Target Date | Goal |
|-------|------------------|-------------|------|
| **Alpha** | PRD Must-Haves coded; QAD happy path for F1–F4, F10 | TBD | 1 SK org live pack |
| **Beta** | Alpha feedback; no P0; CLR counsel flags tracked | TBD | 1 LGU/SK pack used in a rumor or weather window |
| **Public Launch** | CLR cleared for youth data; OSS repo public; UES-F4 Cloudflare if paid | TBD | First paid DFY or second self-serve SK |
| **Post-launch** | Paid or second SK live | TBD | Provincial template contributions |

---

## 7. Success Metrics (30-day post-launch)

| ID | Metric | Target | How to Measure |
|----|--------|--------|----------------|
| BRD-M1 | Paying DFY / LOIs | 1 (later) | CRM / signed note |
| North star | Canon shares + refuses in an incident window | ≥1 org with both event types | `canon_share`, `canon_refuse` |
| Launch | Self-serve orgs that finish checklist | ≥1 without founder in the room | `launch_checklist_completed` |
| BRD-M3 | Product burn | Within UES hosting doctrine | Invoice / Cloudflare bill |
| Contribute | Issues or template PRs from outside NCR | ≥1 | GitHub |

BRD-M2 lesson completion is retired as north star until BRD is rewritten.

---

## Self-Check

- [x] ICP specific enough to name real people
- [x] Pricing traces to UES for paid DFY; OSS is free
- [x] UNESCO is first showcase, not the revenue plan
- [x] Phase gates binary where possible
