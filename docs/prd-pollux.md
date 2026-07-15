# Product Requirements Document (PRD)

**Project:** Pollux
**Date:** 2026-07-15
**Version:** 0.1
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A
**BRD:** [brd-pollux.md](brd-pollux.md)
**IDEA:** [idea-pollux.md](idea-pollux.md)

---

## 1. Product Purpose & Value Proposition

Pollux helps youth learn to recognize manipulation techniques through a short, rule-based game, and helps local youth leaders publish curated crisis and MIL packs. Buyers get completion and discernment metrics without paying for SMS blasts or enterprise listening in v1.

---

## 2. Target Personas

**Primary Persona; Mia, SK information officer**
- *Who they are:* 19, Sangguniang Kabataan information officer in a flood-prone barangay.
- *Their core frustration:* Fake maps and rumors in group chats; no budget for tools.
- *What success looks like:* Finishes a 10-minute lesson; posts an official pack link her LGU already approved.

**Secondary Persona; enterprise L&D buyer**
- *Who they are:* Trust-and-safety or L&D lead needing measurable resilience training.
- *Their core frustration:* Passive compliance videos nobody remembers.

---

## 3. Core Features & Priorities

| ID | Feature | Description | Priority |
|----|---------|-------------|----------|
| PRD-F1 | Inoculation lesson (PWA) | Rule-based vignettes for emotion appeal, false expert, digital manipulation; true vs false items; score + badges | Must-Have |
| PRD-F2 | Curated content packs | Versioned, admin-published packs; crisis/MIL facts; no open-web RAG | Must-Have |
| PRD-F3 | SK admin lite | Publish pack items; keyword watch list; copy share links | Must-Have |
| PRD-F4 | Auth and roles | Learner / leader / admin; server-side authorization | Must-Have |
| PRD-F5 | Telegram bot adapter | Same lesson loop via user-initiated Telegram | Should-Have |
| PRD-F6 | Messenger Page bot | Optional Page messaging adapter | Could-Have |
| PRD-F7 | LLM coaching | Optional coaching behind flag; default off | Could-Have |
| PRD-F8 | TrustOps credibility graph | Phase 2 platform | Won't-Have (v1) |
| PRD-F9 | SMS / paid WhatsApp templates / zero-rated Meta / Meltwater | Explicit non-goals | Won't-Have (v1) |

---

## 4. User Stories & Acceptance Criteria

**US-01; Play a lesson** *(PRD-F1)*
> As Mia, I want to complete a short game that teaches manipulation tricks so I can spot them in chats.

Acceptance Criteria:
- Given a signed-in learner, when they start Spot the Trick, then they see vignettes one at a time with at least two choices.
- Given a response, when submitted, then they get immediate feedback and a running score.
- Given the lesson includes true-news vignettes, when completed, then a badge is awarded and `lesson_completed` is recorded.

**US-02; Read a pack** *(PRD-F2)*
> As Mia, I want to open the official flood pack so I share verified routes, not rumors.

Acceptance Criteria:
- Given a published pack, when a learner opens it, then only published items appear.
- Given a draft pack, when a learner requests it, then it is denied.

**US-03; Publish and share** *(PRD-F3)*
> As a leader, I want to publish pack items and copy a share link.

Acceptance Criteria:
- Given a leader role, when they publish an item, then version increments and learners can see it.
- Given a watch keyword list, when they save keywords, then the list persists for their org.
- Given a pack, when they copy share link, then the URL opens the pack for learners.

**US-04; Authz** *(PRD-F4)*
> As Mia, I want only leaders to publish packs.

Acceptance Criteria:
- Given a learner token, when they call publish, then the server returns 403.
- Given unauthenticated access to admin routes, when requested, then 401.

**US-05; Telegram lesson** *(PRD-F5, Should-Have)*
> As Mia, I want to play the lesson in Telegram if I prefer chat.

Acceptance Criteria:
- Given user starts the bot, when they play, then scoring matches web lesson rules.
- Given no user message, when the system would cold-push, then it does not (user-initiated only).

---

## 5. App Flow & UX Intent

**Design reference:** [dsd-pollux.md](dsd-pollux.md)

### 5.1 Screen Inventory

| Screen | Purpose | Entry points | States |
|--------|---------|--------------|--------|
| Landing | Explain + CTA | public URL | static |
| Sign in | Auth | landing, gated routes | loading / error / success |
| Lesson home | Start / resume lesson | post-login | empty / in-progress / complete |
| Vignette | One trick, choices | lesson | answering / feedback |
| Pack list | Browse published packs | nav | empty / loading / success |
| Pack detail | Items + share | pack list | success |
| Admin packs | Create / publish | leader nav | draft / published / error |
| Watch list | Keywords | leader nav | empty / saved |

### 5.6 Events (instrumentation)

| Event | When | Feeds |
|-------|------|-------|
| `lesson_started` | User starts lesson | BRD-M2 |
| `lesson_completed` | User finishes lesson | BRD-M2, GTM |
| `pack_published` | Leader publishes | BRD-V3 |
| `share_link_copied` | Leader copies link | GTM |

---

## 6. Non-Functional Requirements

| Area | Requirement |
|------|-------------|
| Performance | Vignette interaction < 200ms local; pack pages usable on 3G |
| Security | Authz on every mutate; secrets in env; input validation at boundary |
| Privacy | Youth/PII per CLR; minimize data |
| Offline | Cache current lesson assets where feasible (PWA) |
| Cost | No paid messaging in product paths |

---

## 7. AI / ML Components

Rule-based lesson engine is primary (not generative). Optional LLM coaching (PRD-F7) is flagged off by default. Crisis answers must come only from published packs. See [aia-pollux.md](aia-pollux.md).

---

## 8. Dependencies & Assumptions

- Supabase Auth + Postgres available
- Commercial hosting upgraded before monetized public launch (UES-F4)
- First pilot org TBD (GTM)

---

## 9. Rollback

**Single-source rollback:** Revert Vercel/Cloudflare deployment to previous production deployment; database migrations must be backward-compatible or have a documented down migration. Feature flags disable PRD-F7 LLM and PRD-F5 bot without redeploy when possible.

---

## 10. Open Questions

| Question | Owner | Resolve by |
|----------|-------|------------|
| Telegram vs Messenger first | Eng | SDD lock |
| Age gate for under-18 | CLR | Public launch |
| Exact B2B seat price | Biz | First paid pilot |

---

## Self-Check

- [x] Stable PRD-F# IDs
- [x] Cut line matches IDEA
- [x] Rollback named
- [x] Events for BRD-M2
- [x] No em-dashes
