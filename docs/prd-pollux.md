# Product Requirements Document (PRD)

**Project:** Pollux
**Date:** 2026-08-15
**Version:** 0.3
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A
**BRD:** [brd-pollux.md](brd-pollux.md)
**IDEA:** [idea-pollux.md](idea-pollux.md)
**Research input:** [research-pollux-agent-era-mil.md](research-pollux-agent-era-mil.md)

---

## 1. Product Purpose & Value Proposition

Pollux is an open-source aide SK and LGU youth desks launch themselves. They fill a local official-information pack from a template, publish it, and only a human officer can share it as SK-official. Seekers Guild stewards contribution (feedback, templates, code, partnerships), especially from outside major hubs. Guild is not required to launch and is not the brand on the SK Page.

Pollux does not race AI volume with a fact-check model, does not ship a web-surfing agent, and keeps optional LLM coaching off by default. An inoculation game is Could-Have, not the v1 brand. UNESCO MIL goals (think critically, spot falsehoods, know the source, use media well, share ethically, build a fairer public) are gates and fields in the SK flow, not a lesson list.

---

## 2. Target Personas

**Primary Persona; Mia, SK information officer**
- *Who they are:* 19, Sangguniang Kabataan information officer in a flood-prone barangay.
- *Their core frustration:* Fake maps and fluent rumors in group chats; no budget; she cannot wait for a workshop.
- *What success looks like:* She launched the pack herself. She posted the official version. Nothing else counts as SK-official.

**Secondary Persona; seeker outside a major hub**
- *Who they are:* Student or young professional in a province. Guildmate or Guildmate-in-the-making.
- *Their core frustration:* Tools and events sit in Manila. They have local knowledge and no merge path.
- *What success looks like:* They filed a template gap, a bug, or an SK introduction without publishing that barangay's facts.

**Tertiary Persona; LGU youth / DRRM buyer (paid later)**
- *Who they are:* Youth development or DRRM lead who already runs info pages.
- *Their core frustration:* Rumors during storms; no tool they can hand to SK without a vendor in the room.
- *What success looks like:* SK desks self-serve. Optional paid DFY install later.

---

## 3. Core Features & Priorities

| ID | Feature | Description | Priority |
|----|---------|-------------|----------|
| PRD-F1 | Canon desk + templates | Org space; clone flood / election / notices templates; empty local fields; draft, publish, version pin, archive | Must-Have |
| PRD-F2 | Published pack read | Versioned packs; crisis/MIL facts; no open-web RAG; published = live canon; draft invisible | Must-Have |
| PRD-F3 | SK self-launch kit | Launch checklist (create, clone, fill, publish, post, print); paper card with pack URL and QR | Must-Have |
| PRD-F4 | Auth and roles | reader / leader / admin; server-side authorization; ignore client `role` | Must-Have |
| PRD-F10 | Human commit share | Official share only after commit: provenance, pack match, human click. Copy official link or refuse. Records `canon_share` / `canon_refuse` | Must-Have |
| PRD-F13 | Contribution ladder | Public feedback; CC-BY template PRs; GitHub issues; SK facts stay SK-owned. Apache-2.0 code | Should-Have |
| PRD-F14 | Helper draft (pack-bound) | Draft text may cite published items only; SK still publishes | Should-Have |
| PRD-F5 | Telegram adapter | User-initiated pack share / read, not a game loop | Should-Have |
| PRD-F6 | Messenger Page bot | Optional Page messaging adapter | Could-Have |
| PRD-F7 | LLM coaching | Optional coaching behind flag; default off; never crisis facts | Could-Have |
| PRD-F11 | Injection / agent-principal vignette | Rule-based authored content; gate holds; no live web agent | Could-Have |
| PRD-F12 | Inoculation drill | Former v0.2 Must-Have game. Optional short drill. Not the brand | Could-Have |
| PRD-F8 | TrustOps credibility graph | Phase 2 platform | Won't-Have (v1) |
| PRD-F9 | SMS / paid WhatsApp templates / zero-rated Meta / Meltwater / general web-surfing agent / fact-check LLM racing volume / Guild-required publish | Explicit non-goals | Won't-Have (v1) |

**ID note:** PRD-F1 previously meant the inoculation lesson. SDD, QAD, BUILD, AIA still describe that meaning until reconciled. Build against this PRD, not those stale rows.

---

## 4. User Stories & Acceptance Criteria

**US-01; Launch a pack** *(PRD-F1, PRD-F3)*
> As Mia, I want to clone a flood template and fill our routes so I can go live without a vendor.

Acceptance Criteria:
- Given a signed-in leader, when they create an org, then they get an org space that is not Guild-branded as the program name.
- Given a template pack, when they clone it, then local fields are empty and they must fill them before publish.
- Given incomplete required fields, when they try to publish, then publish is denied.
- Given they complete the launch checklist, when done, then they can print or save a one-page card with URL and QR.

**US-02; Read a pack** *(PRD-F2)*
> As a resident or SK officer, I want to open the official flood pack so I share verified routes, not rumors.

Acceptance Criteria:
- Given a published pack, when a reader opens it, then only published items appear, each with publisher, date, and version.
- Given a draft pack, when a reader requests it, then it is denied.
- Given any crisis fact path, when resolved, then the source is a published pack version, never open-web RAG or an LLM.

**US-03; Publish** *(PRD-F1)*
> As a leader, I want to publish pack items so the barangay sees only what I approved.

Acceptance Criteria:
- Given a leader role, when they publish, then version increments and readers can see it.
- Given a learner or reader token, when they call publish, then the server returns 403.
- Given publish, when executed, then no automated agent may flip `status` to `published`.

**US-04; Authz** *(PRD-F4)*
> As Mia, I want only leaders to publish packs.

Acceptance Criteria:
- Given a reader token, when they call publish, then the server returns 403.
- Given unauthenticated access to admin routes, when requested, then 401.
- Given a body field named `role`, when sent, then the server ignores it.

**US-05; Official share or refuse** *(PRD-F10)*
> As Mia, I want to commit before something counts as SK-official so fluent rumors do not become our voice.

Acceptance Criteria:
- Given a published pack, when she chooses official share, then she sees a pause: who published, version, why it is in the pack.
- Given she confirms, when submitted, then `canon_share` is recorded and she can copy the official URL.
- Given a rumor not in the pack, when she chooses refuse, then `canon_refuse` is recorded and the product does not mint an official share token.
- Given commit share, when offered, then it does not call an LLM coach.

**US-06; Contribute without publishing SK facts** *(PRD-F13)*
> As a seeker outside Manila, I want to file a template gap or an issue so I can help without speaking as SK.

Acceptance Criteria:
- Given the public repo, when they open CONTRIBUTING, then rungs are listed: feedback, templates, partnership, code, stewardship.
- Given a template PR, when merged, then it contains empty local fields, not live hotlines.
- Given SK-published facts, when the default export runs, then those facts are not copied into the public repo.

**US-07; Telegram pack** *(PRD-F5, Should-Have)*
> As Mia, I want to open the published pack in Telegram if I prefer chat.

Acceptance Criteria:
- Given user starts the bot, when they request the pack, then only published items return.
- Given no user message, when the system would cold-push, then it does not (user-initiated only).

**US-08; Injection vignette** *(PRD-F11, Could-Have)*
> As Mia, I want to see a helper told to ignore the pack so I learn that the gate must hold.

Acceptance Criteria:
- Given the vignette is present, when she answers, then correct feedback states the pack allowlist still applies.
- Given the vignette path, when executed, then no live web agent or open-web fetch runs.

**US-09; Optional drill** *(PRD-F12, Could-Have)*
> As a facilitator, I want an optional short drill that is not required to launch a pack.

Acceptance Criteria:
- Given v1, when Mia launches, then she is not blocked on a lesson completion.
- Given the drill is enabled later, when played, then scoring is rule-based and does not author pack facts.

---

## 5. App Flow & UX Intent

**Design reference:** [dsd-pollux.md](dsd-pollux.md)

### 5.1 Screen Inventory

| Screen | Purpose | Entry points | States |
|--------|---------|--------------|--------|
| Landing | Explain SK self-launch + Guild contribute | public URL | static |
| Sign in | Auth | landing, gated routes | loading / error / success |
| Org home | Launch checklist | post-login leader | empty / in-progress / live |
| Template pick | Clone flood / election / notices | org home | empty / success |
| Pack editor | Fill local fields | clone | draft / invalid / ready |
| Pack detail | Items + provenance + share | pack list, QR | success |
| Commit share | Pause then official or refuse | pack detail | choosing / shared / refused |
| Paper card | Print/save QR | checklist done | static |
| Admin packs | Create / publish / archive | leader nav | draft / published / error |
| Contribute | Link to issues / templates | landing | static |

### 5.6 Events (instrumentation)

| Event | When | Feeds |
|-------|------|-------|
| `org_created` | Leader creates org | GTM |
| `pack_cloned` | Template cloned | GTM |
| `pack_published` | Leader publishes | BRD-V3, GTM |
| `launch_checklist_completed` | Checklist done | GTM |
| `canon_share` | Official share confirmed | North star, GTM |
| `canon_refuse` | Refuse official share | North star, GTM |
| `share_link_copied` | Leader copies official URL | GTM |

Legacy events `lesson_started` / `lesson_completed` / `act_completed` apply only if PRD-F12 ships. They are not v1 north star. BRD-M2 (lesson completion) is stale until BRD is rewritten; GTM uses canon events.

---

## 6. Non-Functional Requirements

| Area | Requirement |
|------|-------------|
| Performance | Pack pages usable on 3G; commit share is a short pause, not a quiz |
| Security | Authz on every mutate; secrets in env; input validation at boundary; pack confinement in SQL + service |
| Privacy | Youth/PII per CLR; minimize data |
| Offline | Cache published pack + paper card fallback for 3G |
| Cost | No paid messaging in product paths |
| Agent governance | Crisis path has no open-web tool; irreversible commit stays human |
| Open source | Apache-2.0 code; CC-BY-4.0 empty templates; SK facts stay SK-owned |

---

## 7. AI / ML Components

No model on the critical path. Optional LLM coaching (PRD-F7) is flagged off by default. Helper draft (PRD-F14) may only cite published pack items; it cannot publish. Crisis answers must come only from published packs. Injection vignettes (PRD-F11) are authored content, not live agents. See [aia-pollux.md](aia-pollux.md) and [rfc-pollux-channel-packs.md](rfc-pollux-channel-packs.md). AIA still describes the old game-primary path until reconciled.

---

## 8. Dependencies & Assumptions

- Supabase Auth + Postgres available
- Commercial hosting upgraded before monetized public launch (UES-F4)
- First pilot org still open / stale (GTM G-1)
- PRD-F7 LLM coaching deferred past MVP; flag remains off
- Learner/resident audience may include under-18; CLR age gate + parental consent still required before public school/LGU launch
- Pack approval chain (G-6) remains load-bearing because packs are civic canon
- Seekers Guild can recruit contributors; it cannot be a publish gate
- SDD/QAD/BUILD still describe PRD-F1 as a game; treat those rows as stale until patched

---

## 9. Rollback

**Single-source rollback:** Revert Cloudflare (commercial) or prior prototype host deployment to the previous production deployment; database migrations must be backward-compatible or have a documented down migration. Feature flags disable PRD-F7 LLM, PRD-F5 bot, PRD-F12 drill, PRD-F11 vignettes, and PRD-F14 helper draft without redeploy when possible. PRD-F10 commit share is Must-Have; do not ship a path that mints official shares without it.

---

## 10. Open Questions

| Question | Owner | Status | Resolve by |
|----------|-------|--------|------------|
| Telegram vs Messenger first | Eng | **Resolved: Telegram** (PRD-F5 when shipped; not MVP-blocking) | Done (2026-07-15) |
| Age audience + gate for under-18 | CLR | Audience includes minors; consent/PIA policy still **Blocker for public launch** | Public launch |
| Exact B2B / B2G price | Biz | **Resolved provisional:** seats $12/yr list; first paid B2G project $4,000 (see GTM/UES). OSS self-serve is free. | Renegotiate at first paid DFY |
| Pack authoring approval chain | Product | Stale (open); ship leader publish + version pin; tighten before public pilot | Before SDD lock on G-6 |
| Commit-share proof of official post | Product | Open (in-app event vs Page post) | Before PRD-F10 lock |
| Product spine | Product | **Resolved: SK aide, not game; Guild is community** | Done (2026-08-15) |

---

## Self-Check

- [x] Stable PRD-F# IDs (F1 meaning changed; noted)
- [x] Cut line matches IDEA
- [x] Rollback named
- [x] Events for north star
- [x] No em-dashes
