# Idea Brief (IDEA)

**Project:** Pollux
**Date:** 2026-08-16
**Version:** 0.5
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled with reality)
**Event / context:** Real SK/LGU product. Seekers Guild is a partner community that stewards it. UNESCO Global Youth Hackathon 2026 is the first showcase venue, not the reason the product exists.
**Research input:** [research-pollux-agent-era-mil.md](research-pollux-agent-era-mil.md) (2026-08-13); UNESCO MIL programme (2026-08-15)

---

## 1. The Spark

**Production intent:** Real product from day one. Ship a deployable PWA with auth, tests, observability, and rollback. Demo proves an SK officer can run this week's outreach or bootcamp from the kit, and students still have a URL after. No throwaway mock. No contest-only game.

**One-line pitch:** Pollux is the open campaign kit an SK officer runs herself: modules, a program guide, and a site students return to after.

**UVP:** For SK and LGU youth officers who need an outreach or bootcamp this week and do not know where to start, Pollux is the open campaign kit: teachable modules, a run-of-show, logistics, and a site students can keep using. Unlike a blank Facebook event or a paid vendor workshop. Materials stay free.

**Tagline:** They run the session. We pack the bag.

**Problem:** Saturday outreach is on the calendar. Mia has a Page and a mandate, and a blank morning: no agenda, no handouts, no link students keep after the tarps come down. A Facebook event is an empty room. A paid vendor workshop prices out the desks that need it this week. Youth outside Manila rarely get to run the session themselves. Fluent rumors and official-pack tools still matter later. They are not this week's blocker.

**Insight (why us, why now):** UNESCO MIL is not a quiz and not a reason this product exists. It is critical thinking, source-checking, safe use, ethical share, and public talk that is fair ([Media and Information Literacy](https://www.unesco.org/en/media-information-literacy)). Those goals belong in a session an SK officer can run herself this Saturday, with modules, a 3Ds run-of-show, print, and a student URL. Seekers Guild partners with youth desks, especially outside the big cities. Guild is not the SK Page and does not publish barangay facts. We do not build a fact-check LLM, a companion, or a web-surfing agent. An inoculation game is not the product. Official pack desk (clone, publish, human commit share) is a later tool, not the headline.

---

## 2. Who It's For

**Primary user (named, specific):** Mia, 19, Sangguniang Kabataan information officer in a flood-prone barangay. She has a phone, a Facebook Page, and no paid tools.

**Their moment of pain:** Saturday outreach. No agenda, no handouts, no after-link. Students will show up. She does not know where to start.

**Success in their words:** "I ran the session from the kit. Students still have the URL."

**Secondary user:** A seeker outside a major hub. They file feedback, a template gap, a code fix, or an SK introduction through Seekers Guild. They do not publish that barangay's facts. Success: "I helped from my province. I did not need to sit in Manila."

---

## 3. Scope & Cut Line

**Three roles (do not collapse):**

| Role | Owns | Does not own |
|------|------|----------------|
| SK / LGU youth desk | Session, Page, official speech | Pollux brand on their Page |
| Pollux | Open campaign kit: modules, run-of-show, print, student site | Barangay hotlines and routes; SK Page identity |
| Seekers Guild | Partner community, partnerships, OSS stewardship | Official SK speech; barangay facts; required for a Saturday run |

**Launch-without-us test:** If an SK officer cannot finish Saturday from the six modules, 3Ds run-of-show, print packet, and student reader URL, without a Guild workshop or a paid vendor, the product failed. Official pack desk (create org, clone, publish, commit share) is later. It does not block the kit.

**In scope for this sprint:**

| # | Capability | Demo-critical? |
|---|------------|----------------|
| 1 | DIY campaign kit (PRD-F15): six modules, 3Ds run-of-show, print packet, student reader access (content home: `docs/outreach-kit/`). Not a scored inoculation game. Kit text is not SK-official crisis canon. | Yes |
| 2 | Student site they can keep using after the session (published-only reader; no open-web RAG) | Yes |
| 3 | Auth; roles: reader / leader / admin; identity from session | Yes |
| 4 | OSS contribution path: feedback + kit/template PRs; SK facts stay SK-owned | No (Should-Have in product; Must-Have in narrative) |
| 5 | Official pack desk: draft, publish, version pin, archive; cloneable templates; human commit share | No (later / side; not the one thing) |
| 6 | Helper draft that can only cite published items | No (Should-Have; later) |
| 7 | Optional Telegram adapter for pack share, user-initiated | No |
| 8 | Optional short inoculation drill | No (Could-Have; not the brand) |

**Explicitly out of scope (v0):** SMS broadcast; WhatsApp cold templates at our cost; zero-rated Meta as a product promise; Meltwater or paid social listening; algorithmic credibility graph / TrustOps API; open-ended LLM crisis Q&A; general web-surfing agent; AI companion as primary path; racing AI volume with a fact-check model; Guild required to run a session; Guild logo as the SK Page identity; intercepting Facebook forward; mixing seminar-kit text into SK-official crisis canon; shipping the official pack desk as the product instead of the DIY campaign kit; public camp for under-18 (CLR still blocks; demo is 18+).

**If we only ship one thing:** DIY campaign kit: existing six modules + 3Ds run-of-show + print + student reader access. Official pack desk is later / side. A blank Facebook event or a paid vendor workshop is not a substitute.

**UNESCO MIL as product behavior (not a curriculum):**

| MIL goal | Product behavior |
|----------|------------------|
| Think critically | Pause-before-share module in the Saturday run |
| Spot fake news | Not-in-pack-not-official: allowlist, not a fact-check model |
| Know the source | Access-the-pack: publisher, date, version |
| Use media well | Print + PWA; minimize youth PII; CLR blocks public camp for under-18; demo 18+ |
| Share ethically | Ethical share or refuse; kit never mints SK-official speech |
| Build a better society | SK officer runs the session herself; Guild partners beyond NCR; materials stay free |

**Licenses (when code and templates exist):** Apache-2.0 for code. CC-BY-4.0 for empty template shells and kit materials meant for reuse. SK-published facts are not in the public repo unless that SK contributes a sanitized template.

---

## 4. Success & Judging Criteria

**How we win (metrics or rubric):** Startup readiness, not a contest score. An SK officer runs a session from the kit. Students still have the URL. Monthly burn stays under about $20 until a paid pilot. Production Readiness Gate items are either done or explicitly owned. UNESCO showcase tells the campaign-kit story. It does not replace a paid pilot and is not why the product exists.

| Criterion | How we hit it |
|-----------|---------------|
| North star | Session run from the kit; students still have the reader URL |
| Principal stance | Kit is not SK-official crisis canon; later desk (if shipped) still requires a human commit |
| Self-launch | Launch-without-us test passes on print + cheap phone |
| Open community | Seekers outside major hubs can contribute without being the publisher |
| Feasibility on bootstrap budget | Free-tier stack; materials stay free; no paid messaging |
| Ethical channel stance | Low-bandwidth PWA; zero-rated Meta is a non-goal; CLR covers consent, youth data, under-18 camp block |
| Path to revenue | OSS self-serve is the community rung; paid DFY / hosted LGU install later (UES/GTM) |

**Demo script (30-90 seconds):** Open Pollux as Mia, 18+ demo. Show the six modules. Walk the 3Ds run-of-show. Hold the print packet. Open the student URL they keep after. Name Seekers Guild as partner, not as the Page, not as publisher of barangay facts. Official pack desk is a later tool; do not make "only her tap makes it SK-official" the pitch.

**UNESCO jury sentence:** Pollux is the open campaign kit SK councils run themselves. Seekers Guild partners with youth desks, especially outside the big cities. Modules, program guide, and student access stay free.

---

## 5. Concept Visuals

*Lo-fi references generated before build. Link files; do not describe what you haven't generated.*

**Visual direction (one sentence):** Peer-led, calm, high-intent mobile screens. SK-owned session, not Guild-branded chrome, no crisis-red panic UI.

**Tooling used:** GenerateImage (concept frames). Impeccable shape deferred to DSD lock.

| Screen / section | Asset path | Notes |
|------------------|------------|-------|
| Leader pack / launch | [docs/assets/concept/pollux-leader.png](assets/concept/pollux-leader.png) | Later-tool desk frames; not the campaign-kit headline |
| Legacy lesson frame | [docs/assets/concept/pollux-lesson.png](assets/concept/pollux-lesson.png) | Kept as Could-Have drill reference; not v1 brand |

**Team decision:** Approve calm peer-led direction in DSD §0. Reject competition trophy aesthetics and dark-mode glow defaults. Reject Guild sigil on SK official share screens. Kit screens still need a concept pass.

---

## 6. Open Questions

| Question | Owner | Status | Resolve by |
|----------|-------|--------|------------|
| First pilot LGU or SK federation for a live pack | Founders | Stale (open) | Before GTM lock |
| Telegram vs Messenger for first bot adapter | Eng | **Resolved: Telegram first** | Done (2026-07-15) |
| Whether optional LLM coaching ships in v1 or waits | Product | **Resolved: post-MVP; flag off** | Done (2026-07-15) |
| Product spine | Product | **Resolved: DIY campaign kit first; official pack desk later / side** | Done (2026-08-16) |
| Seekers Guild role | Product | **Resolved: partner community; not SK Page; not publisher of barangay facts; not required to run Saturday** | Done (2026-08-16) |
| Pack approval chain (G-6) when packs are civic canon | Product | Stale (open); later-tool under principal thesis | Before public desk pilot |
| Commit-share proof (in-app event vs Page post) | Product | Open (later tool) | Before PRD lock on desk share |
| First camp venue for the outreach / seminar kit | Founders | Open | Before first camp |
| Under-18 public camp | CLR | **Resolved: blocked; demo 18+** | Done (standing CLR) |

---

## Self-Check

- [x] Production intent stated in §1 (real product, not throwaway demo)
- [x] One-line pitch is specific to this project (not generic)
- [x] Cut line is explicit; minimum demo is named
- [x] Success criteria mapped (startup, not contest)
- [x] Concept visuals linked once assets exist
- [x] AGENTS hard bans applied (no em-dashes)
- [x] Next suggested doc: PRD reconcile to kit-first spine, then SDD/QAD
