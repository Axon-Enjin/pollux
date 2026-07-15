# Idea Brief (IDEA)

**Project:** Pollux
**Date:** 2026-07-15
**Version:** 0.1
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled with reality)
**Event / context:** Startup build. Bootstrap digital-trust company. UNESCO Youth Hackathon is optional distribution, not the product goal.

---

## 1. The Spark

**Production intent:** Real product from day one. Ship a deployable PWA with auth, tests, observability, and rollback. Demo proves the inoculation loop. No throwaway mock.

**One-line pitch:** Pollux teaches youth to spot manipulation techniques through a short gamified lesson, and gives local youth leaders a lightweight way to watch and share verified crisis facts without paying for messaging or enterprise listening tools.

**Problem:** Reactive fact-checking arrives after falsehoods stick. Passive media literacy fails to change sharing behavior. Low-income communities often meet rumor and crisis info only through chat apps, while paid tools (SMS blasts, Meltwater, WhatsApp template campaigns) price out the grassroots operators who need them most.

**Insight (why us, why now):** Active, interactive prebunking beats passive tips. World Bank field work on WhatsApp inoculation games showed interactive play improved discernment where static infographics did not. We can deliver that loop on a free-tier web PWA first, keep the game rule-based, and sell B2G/B2B licenses later. Credibility-graph TrustOps is the Phase 2 platform, not the cold start.

---

## 2. Who It's For

**Primary user (named, specific):** Mia, 19, Sangguniang Kabataan information officer in a flood-prone barangay. She gets group-chat rumors during typhoon season and has no paid tools, only a phone and a Facebook Page.

**Their moment of pain:** A fake evacuation map spreads in the barangay chat. She cannot tell who to trust, and she has no budget for SMS or Meltwater.

**Success in their words:** "I finished a ten-minute game that taught me the tricks, and I can post the official flood routes from a pack our LGU already approved."

---

## 3. Scope & Cut Line

**In scope for this sprint:**

| # | Capability | Demo-critical? |
|---|------------|----------------|
| 1 | Rule-based inoculation game on mobile web PWA (emotion appeal, false expert, digital manipulation; true vs false vignettes; score + badges) | Yes |
| 2 | Curated crisis/MIL content pack viewer (admin-published, versioned, no open-web RAG) | Yes |
| 3 | SK / youth-leader admin lite: publish pack items, simple keyword watch list, share links (no paid listening) | Yes |
| 4 | Auth (email/magic link or OAuth), roles: learner / leader / admin | Yes |
| 5 | Optional Telegram bot adapter for the same game loop (user-initiated) | No |

**Explicitly out of scope (v0):** SMS broadcast; WhatsApp cold templates at our cost; zero-rated Meta as a product promise; Meltwater or paid social listening; algorithmic credibility graph / TrustOps API; MTF ad-tech billing; open-ended LLM crisis Q&A.

**If we only ship one thing:** The comprehensive inoculation game on PWA with score feedback and at least one true-news calibration vignette per technique.

---

## 4. Success & Judging Criteria

**How we win (metrics or rubric):** Startup readiness, not a contest score. Learners complete a full lesson. Leaders can publish a pack. Monthly burn stays under about $20 until a paid pilot. Production Readiness Gate items are either done or explicitly owned.

| Criterion | How we hit it |
|-----------|---------------|
| Cognitive effect (product north star) | Lesson design mirrors proven active inoculation pattern; QAD measures completion and post-lesson discernment quiz |
| Feasibility on bootstrap budget | Free-tier stack; no paid messaging; rule-based game core |
| Ethical channel stance | Low-bandwidth PWA; zero-rated Meta is a non-goal; CLR covers consent and youth data |
| Path to revenue | B2G/B2B licensing documented in UES/GTM; Phase 2 TrustOps documented, not built |

**Demo script (30-90 seconds):** Open Pollux on phone. Start "Spot the Trick" lesson. Mark a vignette as manipulative, see why, get a badge. Switch to leader view, open the barangay flood pack, copy a share link. Show burn dashboard or README cost note: $0 messaging.

---

## 5. Concept Visuals

*Lo-fi references generated before build. Link files; do not describe what you haven't generated.*

**Visual direction (one sentence):** Peer-led, calm, high-intent mobile screens. No purple SaaS chrome, no crisis-red panic UI.

**Tooling used:** GenerateImage (concept frames). Impeccable shape deferred to DSD lock.

| Screen / section | Asset path | Notes |
|------------------|------------|-------|
| Learner lesson (vignette + choices) | [docs/assets/concept/pollux-lesson.png](assets/concept/pollux-lesson.png) | Teal on warm paper; choice buttons |
| Leader pack / watch lite | [docs/assets/concept/pollux-leader.png](assets/concept/pollux-leader.png) | Pack list + share; no dashboard clutter |

**Team decision:** Approve calm peer-led direction in DSD §0. Reject competition trophy aesthetics and dark-mode glow defaults.

---

## 6. Open Questions

| Question | Owner | Status | Resolve by |
|----------|-------|--------|------------|
| First pilot LGU or SK federation for content pack | Founders | Stale (open) | Before GTM lock |
| Telegram vs Messenger for first bot adapter | Eng | **Resolved: Telegram first** | Done (2026-07-15) |
| Whether optional LLM coaching ships in v1 or waits | Product | **Resolved: post-MVP; flag off** | Done (2026-07-15) |

---

## Self-Check

- [x] Production intent stated in §1 (real product, not throwaway demo)
- [x] One-line pitch is specific to this project (not generic)
- [x] Cut line is explicit; minimum demo is named
- [x] Success criteria mapped (startup, not contest)
- [x] Concept visuals linked once assets exist
- [x] AGENTS hard bans applied (no em-dashes)
- [x] Next suggested doc: SCRUTINY (Build the FMD gate), then VALIDATION
