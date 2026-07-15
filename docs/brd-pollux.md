# Business Requirements Document (BRD)

**Project:** Pollux
**Date:** 2026-07-15
**Version:** 0.1
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A

---

## 1. Executive Summary

Pollux sells cognitive resilience training and curated civic information packs to governments, NGOs, and enterprises. Learners practice spotting manipulation techniques in a short game. Local leaders publish official crisis and MIL packs without buying enterprise listening or SMS blasts. Phase 2 adds a TrustOps credibility API once revenue or grant capital exists.

---

## 2. The Problem & Opportunity

**The Problem:**
Disinformation spreads in chat before corrections arrive. Passive literacy materials do not change sharing behavior. Youth officers like barangay SK information leads face rumor spikes with no budget for Meltwater or carrier messaging.

**The Opportunity:**
Active inoculation has field evidence. Institutions already buy training and disaster-communication tools. A low-cost PWA can prove completion and discernment gains, then expand into licensed seats and later TrustOps APIs.

**Target Customer / User:**
Buyer: LGU / SK federation DRRM or youth development office, and enterprise L&D / trust-and-safety. End user: Mia-type youth leaders and peers on mobile web.

---

## 3. Business Model

Value is created by measurable inoculation lessons plus governed content packs. Delivered via web PWA (Telegram optional). Captured as B2G project fees and B2B annual seats. Unit economics live in [ues-pollux.md](ues-pollux.md).

**Unit (named):** One licensed learner seat-year (B2B) or one funded municipal deployment project (B2G)

**Capture mechanism:** Invoice / grant drawdown; no D2C subscription for v1

---

## 4. Business Model Canvas

| Block | Content |
|-------|---------|
| **Customer Segments** | LGUs/SK federations; NGO MIL programs; enterprise L&D / disinformation security |
| **Value Propositions** | Active inoculation with completion metrics; curated crisis packs; bootstrap-friendly ops |
| **Channels** | Direct B2G outreach; NGO partners; optional UNESCO visibility |
| **Customer Relationships** | Pilot success managers; pack approval with local owners |
| **Revenue Streams** | Project fees (B2G); per-seat licenses (B2B); Phase 2 API (later) |
| **Key Resources** | Lesson content; pack governance; product codebase |
| **Key Activities** | Ship lesson; localize packs; run pilots; measure discernment |
| **Key Partners** | Pilot LGU TBD; NGOs; optional telco later (not v1) |
| **Cost Structure** | Founder time; commercial hosting when monetizing; optional LLM; no paid messaging until funded |

**UES handoff:** Segments → UES-D8; Revenue → UES-E1; Cost → UES-E2 / UES-F#.

---

## 5. Impact Variables (Pareto / Power Law)

**Candidates considered:** pilot conversion, pack adoption, lesson completion, paid CAC, WhatsApp reach, TrustOps API attach

| ID | Impact variable | Why it dominates | Falsifier | Rank |
|----|-----------------|------------------|-----------|------|
| BRD-V1 | Paid pilot conversion (B2G/B2B) | Without a paying buyer, burn doctrine collapses | 90 days, zero LOI or paid pilot after outreach | 1 |
| BRD-V2 | Lesson completion rate | Proves product works for buyers | Completion under 40% in pilot cohort | 2 |
| BRD-V3 | Pack publish latency | Leaders abandon if packs cannot ship fast | Median publish over 7 days with trained admin | 3 |

**Concentration rule:** First 90 days: all experiment budget on BRD-V1 and BRD-V2 only.

---

## 6. Capital Philosophy Gate

| # | Principle | Research question (one-line answer) | Status | UES link |
|---|-----------|-------------------------------------|--------|----------|
| 1 | DO NOT LOSE MONEY | Do not buy messaging or paid ads that turn unit economics red | Pass | UES-D1 |
| 2 | ASSET ALLOCATION | Capital goes to product + one pilot channel; experiments capped | Pass | UES-D2 |
| 3 | Asymmetrical RISK-REWARD | Cap pilot content cost; upside is multi-LGU license | Pass | UES-D3 |
| 4 | 1 in 5 out | Experiment cost ≤ expected contribution / 5 | Pass | UES-D4 |
| 5 | Margins run the business | Growth spend from contribution after first paid pilot | Pass | UES-D5 |
| 6 | Operating Cashflow | Track OCF from seats/projects, not vanity signups | Pass | UES-D6 |
| 7 | Capital Gains | Raise only if §6 UES triggers; bootstrap default | Pass | UES-D7 |
| 8 | User Centric, Tailored | Primary: PH youth leaders / SK; kill vanity global dashboard | Pass | UES-D8 |

---

## 7. Strategic Alignment

Build a default-alive digital-trust company. v1 proves pedagogy and municipal ops. Phase 2 TrustOps monetizes credibility data once packs and seats exist. UNESCO is optional credibility, not the plan.

---

## 8. Scope

**In Scope:**
- Inoculation PWA + SK admin lite
- B2G/B2B licensing narrative
- Bootstrap cost doctrine

**Out of Scope:**
- SMS / paid WhatsApp templates at our cost
- Zero-rated Meta as a product promise
- Meltwater-class listening
- TrustOps graph / MTF billing in v1

---

## 9. Success Metrics

| ID | Metric | Baseline | Target | Timeline |
|----|--------|----------|--------|----------|
| BRD-M1 | Paying pilots | 0 | 1 paid or signed LOI | 90 days post-MVP |
| BRD-M2 | Lesson completion (pilot) | n/a | ≥60% start→finish | First pilot |
| BRD-M3 | Monthly burn (pre-revenue) | n/a | ≤ hosting doctrine in UES | Ongoing |

---

## 10. Stakeholders & Owners

| Role | Person | Responsibility |
|------|--------|----------------|
| Sponsor / Decision Maker | Founders | Funding and kill calls |
| Business Owner | Founders | Pilot sales and packs |
| Product / Tech Lead | Founders | Build and ops |

---

## Self-Check

- [x] §1 readable without tech jargon
- [x] Unit named; numbers deferred to UES
- [x] BMC core blocks filled
- [x] BRD-V# with falsifiers
- [x] Out of scope explicit
- [x] No CAC/LTV tables in this BRD
