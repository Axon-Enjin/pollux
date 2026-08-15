# Idea Brief (IDEA)

**Project:** Pollux
**Date:** 2026-08-15
**Version:** 0.3
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled with reality)
**Event / context:** Real SK/LGU product. Seekers Guild is the open community that stewards it. UNESCO Global Youth Hackathon 2026 is the first showcase venue, not the reason the product exists.
**Research input:** [research-pollux-agent-era-mil.md](research-pollux-agent-era-mil.md) (2026-08-13); UNESCO MIL programme (2026-08-15)

---

## 1. The Spark

**Production intent:** Real product from day one. Ship a deployable PWA with auth, tests, observability, and rollback. Demo proves an SK officer can launch a local pack herself and share it as official. No throwaway mock. No contest-only game.

**One-line pitch:** Pollux is an open-source aide Sangguniang Kabataan and LGU youth desks launch themselves: they publish a local official-information pack, and only a human officer can share it as SK-official.

**Problem:** Fluent rumors in barangay chats become de facto government voice because SK officers have a Page and a mandate but no gate. Reactive fact-checking arrives after falsehoods stick and cannot race AI-scale volume. Paid blast tools price out the desks that need them. Passive MIL lectures do not change what an officer posts at 2 a.m. during a flood. Youth outside Manila rarely get to shape the tools they are asked to use.

**Insight (why us, why now):** UNESCO MIL is not a quiz. It is critical thinking, source-checking, safe use, ethical share, and public talk that is fair ([Media and Information Literacy](https://www.unesco.org/en/media-information-literacy)). Those goals belong in the SK officer's hand at the moment she posts, not in a lesson she finishes once. The solvable layer is keeping the human as principal: published packs as live canon, a human commit before official share, and crisis limits enforced outside any model. SK already has the public role. Pollux makes that role executable. Seekers Guild makes the aide open so seekers in the provinces can contribute without moving to a major hub. We do not build a fact-check LLM, a companion, or a web-surfing agent. An inoculation game is not the product.

---

## 2. Who It's For

**Primary user (named, specific):** Mia, 19, Sangguniang Kabataan information officer in a flood-prone barangay. She has a phone, a Facebook Page, and no paid tools.

**Their moment of pain:** A fake evacuation map spreads in the barangay chat. The post is fluent and repeated. She needs something she can launch herself and post as SK-official. A workshop next month does not help tonight.

**Success in their words:** "I launched our pack myself. When the fake map hit, I posted the official version. Nothing else counts as SK-official."

**Secondary user:** A seeker outside a major hub. They file feedback, a template gap, a code fix, or an SK introduction through Seekers Guild. They do not publish that barangay's facts. Success: "I helped from my province. I did not need to sit in Manila."

---

## 3. Scope & Cut Line

**Three roles (do not collapse):**

| Role | Owns | Does not own |
|------|------|----------------|
| SK / LGU youth desk | Pack facts, Page, official speech | Pollux brand on their Page |
| Pollux | Gate, templates, version pin, commit share | Barangay hotlines and routes |
| Seekers Guild | Contributor community, partnerships, OSS stewardship | Official SK speech; required for launch |

**Launch-without-us test:** If an SK officer cannot finish create org, clone template, fill local fields, publish, copy link or print card, post from her Page, without a Guild workshop, the product failed.

**In scope for this sprint:**

| # | Capability | Demo-critical? |
|---|------------|----------------|
| 1 | Canon desk: draft, publish, version pin, archive; cloneable templates (flood, election rumor, official notices) | Yes |
| 2 | Published-only pack read (SQL + service gate; no open-web RAG) | Yes |
| 3 | SK self-launch: org space, launch checklist, paper card with QR | Yes |
| 4 | Human commit share: official link or refuse; records `canon_share` / `canon_refuse` | Yes |
| 5 | Auth; roles: reader / leader / admin; identity from session | Yes |
| 6 | OSS contribution path: feedback + template PRs; SK facts stay SK-owned | No (Should-Have in product; Must-Have in narrative) |
| 7 | Helper draft that can only cite published items | No (Should-Have) |
| 8 | Optional Telegram adapter for pack share, user-initiated | No |
| 9 | Optional short inoculation drill | No (Could-Have; not the brand) |

**Explicitly out of scope (v0):** SMS broadcast; WhatsApp cold templates at our cost; zero-rated Meta as a product promise; Meltwater or paid social listening; algorithmic credibility graph / TrustOps API; open-ended LLM crisis Q&A; general web-surfing agent; AI companion as primary path; racing AI volume with a fact-check model; Guild required to publish; Guild logo as the SK Page identity; intercepting Facebook forward.

**If we only ship one thing:** Canon desk plus cloneable templates plus human commit share, on a phone, that an SK officer can launch without us.

**UNESCO MIL as product behavior (not a curriculum):**

| MIL goal | Product behavior |
|----------|------------------|
| Think critically | Pause before official share: who made this, why, is it in the pack |
| Spot fake news | If it is not in the published pack, it is not official. No fact-check model |
| Know the source | Publisher, date, version, why the item is in the pack |
| Use media well | PWA, no scrape, minimize youth PII; CLR still blocks public launch for under-18 |
| Share ethically | Human commit; refuse-forward is first-class; no auto-post |
| Build a better society | SK mandate made executable; Guild extends contribution beyond NCR |

**Licenses (when code and templates exist):** Apache-2.0 for code. CC-BY-4.0 for empty template shells. SK-published facts are not in the public repo unless that SK contributes a sanitized template.

---

## 4. Success & Judging Criteria

**How we win (metrics or rubric):** Startup readiness, not a contest score. An SK officer publishes a pack she filled. She records a canon share or refuse in an incident window. Monthly burn stays under about $20 until a paid pilot. Production Readiness Gate items are either done or explicitly owned. UNESCO showcase proves the SK-launch story. It does not replace a paid pilot.

| Criterion | How we hit it |
|-----------|---------------|
| North star | `canon_share` and `canon_refuse` during a live incident window, by SK org |
| Principal stance | Pack confinement enforced as gate; official share is human-only |
| Self-launch | Launch-without-us test passes on a cheap phone |
| Open community | Seekers outside major hubs can contribute without being the publisher |
| Feasibility on bootstrap budget | Free-tier stack; no paid messaging |
| Ethical channel stance | Low-bandwidth PWA; zero-rated Meta is a non-goal; CLR covers consent and youth data |
| Path to revenue | OSS self-serve is the community rung; paid DFY / hosted LGU install later (UES/GTM) |

**Demo script (30-90 seconds):** Open Pollux on phone as Mia. Create org. Clone flood template. Fill three local fields. Publish. Hit commit share. Copy official link. Show refuse path for a rumor not in the pack. Show paper card QR. Name Seekers Guild as the community, not as the Page.

**UNESCO jury sentence:** Pollux is an open-source aide SK councils launch themselves. Seekers Guild is the youth community that stewards it, especially seekers outside major hubs. Only a human SK officer can share a pack as official, so fluent rumors do not become government voice.

---

## 5. Concept Visuals

*Lo-fi references generated before build. Link files; do not describe what you haven't generated.*

**Visual direction (one sentence):** Peer-led, calm, high-intent mobile screens. SK-owned, not Guild-branded chrome, no crisis-red panic UI.

**Tooling used:** GenerateImage (concept frames). Impeccable shape deferred to DSD lock.

| Screen / section | Asset path | Notes |
|------------------|------------|-------|
| Leader pack / launch | [docs/assets/concept/pollux-leader.png](assets/concept/pollux-leader.png) | Pack list + share; no dashboard clutter |
| Legacy lesson frame | [docs/assets/concept/pollux-lesson.png](assets/concept/pollux-lesson.png) | Kept as Could-Have drill reference; not v1 brand |

**Team decision:** Approve calm peer-led direction in DSD §0. Reject competition trophy aesthetics and dark-mode glow defaults. Reject Guild sigil on SK official share screens.

---

## 6. Open Questions

| Question | Owner | Status | Resolve by |
|----------|-------|--------|------------|
| First pilot LGU or SK federation for a live pack | Founders | Stale (open) | Before GTM lock |
| Telegram vs Messenger for first bot adapter | Eng | **Resolved: Telegram first** | Done (2026-07-15) |
| Whether optional LLM coaching ships in v1 or waits | Product | **Resolved: post-MVP; flag off** | Done (2026-07-15) |
| Product spine | Product | **Resolved: SK self-launch aide, not a game** | Done (2026-08-15) |
| Seekers Guild role | Product | **Resolved: community medium; equal UNESCO billing; not required to launch** | Done (2026-08-15) |
| Pack approval chain (G-6) when packs are civic canon | Product | Stale (open); load-bearing under principal thesis | Before public pilot |
| Commit-share proof (in-app event vs Page post) | Product | Open | Before PRD lock on PRD-F10 |

---

## Self-Check

- [x] Production intent stated in §1 (real product, not throwaway demo)
- [x] One-line pitch is specific to this project (not generic)
- [x] Cut line is explicit; minimum demo is named
- [x] Success criteria mapped (startup, not contest)
- [x] Concept visuals linked once assets exist
- [x] AGENTS hard bans applied (no em-dashes)
- [x] Next suggested doc: PRD v0.3 (this pass), then SDD/QAD reconcile
