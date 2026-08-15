# Product Requirements Document (PRD)

**Project:** Pollux
**Date:** 2026-08-16
**Version:** 0.5
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A
**BRD:** [brd-pollux.md](brd-pollux.md)
**IDEA:** [idea-pollux.md](idea-pollux.md)
**Research input:** [research-pollux-agent-era-mil.md](research-pollux-agent-era-mil.md)

---

## 1. Product Purpose & Value Proposition

Pollux is the open campaign kit an SK officer runs herself: modules, a program guide, and a site students return to after.

She runs a sequenced MIL session at a youth camp or barangay outreach from a published `outreach_kit`. The DIY kit is free and Must-Have (existing six modules plus run-of-show, print packet, return site). The DWY in-app runner is later. Seekers Guild is partnership and contribution, especially from outside major hubs; Guild is not required to run a session and is not the brand on her Page. The official pack desk (clone, publish, commit share) is later. Paid DFY install is later.

The kit is not SK-official crisis canon. Dual allowlist holds: `pack_kind` is `canon` (default, later desk) or `outreach_kit` (v1 product). Crisis facts and commit-share use canon only; kit paths use `outreach_kit` only. Module activities and short checks are allowed. A scored inoculation drill is not the north star. Optional LLM coaching stays off by default. UNESCO MIL goals (think critically, spot falsehoods, know the source, use media well, share ethically, build a fairer public) are gates and fields in the session.

---

## 2. Target Personas

**Primary Persona; Mia, SK information officer**
- *Who they are:* 19, Sangguniang Kabataan information officer in a flood-prone barangay.
- *Their core frustration:* Fake maps and fluent rumors in group chats; no budget; she cannot wait for a workshop.
- *What success looks like:* She ran the campaign kit herself. The packet printed. Students returned to the site after. Official pack publish is later.

**Secondary Persona; seeker outside a major hub**
- *Who they are:* Student or young professional in a province. Guildmate or Guildmate-in-the-making.
- *Their core frustration:* Tools and events sit in Manila. They have local knowledge and no merge path.
- *What success looks like:* They filed a template gap, a bug, or an SK introduction without publishing that barangay's facts.

**Tertiary Persona; LGU youth / DRRM buyer (paid later)**
- *Who they are:* Youth development or DRRM lead who already runs info pages.
- *Their core frustration:* Rumors during storms; no tool they can hand to SK without a vendor in the room.
- *What success looks like:* SK officers run the free DIY kit without a vendor in the room. Optional paid DFY install later. Pack desk later.

**Facilitator (not a fourth role)**
- *Who they are:* Leader at a youth camp or barangay outreach (or a trained seeker with leader-equivalent kit access). Reader is the participant.
- *Their core frustration:* Session dies when 3G dies; they need a sequenced MIL kit that is not the inoculation drill and not SK crisis facts.
- *What success looks like:* They run the published `outreach_kit` from the DIY packet (Must-Have) and the return site. DWY in-app runner later. Optional walk into F3 launch or F10 refuse is later, never a v1 blocker. The kit never mints SK-official crisis canon.

---

## 3. Core Features & Priorities

| ID | Feature | Description | Priority |
|----|---------|-------------|----------|
| PRD-F15 | Campaign kit | Product. Open kit an SK officer runs herself: program guide, print packet, site students return to. V1 content is the existing six modules plus run-of-show (do not invent a 20-module catalog). DIY free Must-Have. DWY in-app runner later. Not F3 (canon paper card). Not F12 (scored inoculation drill). Not SK-official crisis facts; Guild is not the barangay voice. Dual allowlist: `pack_kind` is `canon` (default, later desk) or `outreach_kit` (v1). Crisis and commit-share use canon only; kit paths use `outreach_kit` only. Kit item kinds: module, agenda, activity, facilitation_note, handout, source. Optional `kit_sessions`. Short in-module checks OK; not north star scoring. Flag `ENABLE_OUTREACH_KIT` gates the later DWY runner; DIY packet and return site ship without that flag. | Must-Have |
| PRD-F2 | Published pack read | Versioned packs; published = live, draft invisible; no open-web RAG. v1 serves `outreach_kit`. Canon crisis facts stay on `canon` only (later desk). Kit paths never serve canon crisis items. | Must-Have |
| PRD-F4 | Auth and roles | reader / leader / admin; server-side authorization; ignore client `role`. Reader is participant. | Must-Have |
| PRD-F13 | Contribution ladder | Public feedback; CC-BY template PRs; GitHub issues; SK facts stay SK-owned. Apache-2.0 code. Guild partnership, not a publish gate. | Should-Have |
| PRD-F14 | Helper draft (pack-bound) | Draft text may cite published items only; SK still publishes. Pack desk later. | Should-Have |
| PRD-F5 | Telegram adapter | User-initiated kit or pack share / read, not a game loop | Should-Have |
| PRD-F1 | Canon desk + templates | Later pack desk. Org space; clone flood / election / notices templates; empty local fields; draft, publish, version pin, archive | Could-Have |
| PRD-F3 | SK self-launch kit | Later pack desk. Launch checklist (create, clone, fill, publish, post, print); paper card with pack URL and QR | Could-Have |
| PRD-F10 | Human commit share | Later pack desk. Official share only after commit: provenance, pack match, human click. Copy official link or refuse. Records `canon_share` / `canon_refuse`. Kit paths must not mint these. | Could-Have |
| PRD-F6 | Messenger Page bot | Optional Page messaging adapter | Could-Have |
| PRD-F7 | LLM coaching | Optional coaching behind flag; default off; never crisis facts | Could-Have |
| PRD-F11 | Injection / agent-principal vignette | Rule-based authored content; gate holds; no live web agent | Could-Have |
| PRD-F12 | Inoculation drill | Former v0.2 Must-Have game. Optional short drill. Not the brand. Not the F15 north star. Module activities/short checks live on F15, not here. | Could-Have |
| PRD-F8 | TrustOps credibility graph | Phase 2 platform | Won't-Have (v1) |
| PRD-F9 | SMS / paid WhatsApp templates / zero-rated Meta / Meltwater / general web-surfing agent / fact-check LLM racing volume / Guild-required publish / mixing kit text into SK-official crisis canon | Explicit non-goals | Won't-Have (v1) |

**ID note:** PRD-F1 previously meant the inoculation lesson, then the canon desk (Must-Have). v0.5 product is PRD-F15. F1/F3/F10 are Could-Have / later pack desk. SDD, QAD, BUILD, AIA may still describe desk-first until reconciled. Build against this PRD, not those stale rows.

**Services (cut line):** DIY campaign kit free Must-Have. DWY runner later. Guild partnership (F13). Pack desk (F1/F3/F10) later. DFY paid install later.

---

## 4. User Stories & Acceptance Criteria

**Priority retarget (v0.5):** US-10 and US-11 are Must-Have (PRD-F15 campaign kit). US-02 and US-04 stay Must-Have for published-kit read and roles. US-01, US-03, and US-05 are Could-Have / later with the pack desk (PRD-F1, F3, F10); their acceptance is not a v1 blocker. US-09 stays Could-Have (F12 scored drill). Module short checks may live in F15 activities; they are not F12.

**US-01; Launch a pack** *(PRD-F1, PRD-F3, Could-Have / later)*
> As Mia, I want to clone a flood template and fill our routes so I can go live without a vendor.

Acceptance Criteria:
- Given a signed-in leader, when they create an org, then they get an org space that is not Guild-branded as the program name.
- Given a template pack, when they clone it, then local fields are empty and they must fill them before publish.
- Given incomplete required fields, when they try to publish, then publish is denied.
- Given they complete the launch checklist, when done, then they can print or save a one-page card with URL and QR.

**US-02; Read a pack** *(PRD-F2)*
> As a student or SK officer, I want to open the published campaign kit (and later a canon pack) so I see only published items, not drafts or rumors from the open web.

Acceptance Criteria:
- Given a published pack, when a reader opens it, then only published items appear, each with publisher, date, and version. v1 is `outreach_kit` on the return site.
- Given a draft pack, when a reader requests it, then it is denied.
- Given any crisis fact path, when resolved, then the source is a published `canon` pack version, never open-web RAG, an LLM, or an `outreach_kit` item.

**US-03; Publish** *(PRD-F1, Could-Have / later)*
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

**US-05; Official share or refuse** *(PRD-F10, Could-Have / later)*
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
> As a facilitator, I want an optional short drill that is not required to run the campaign kit.

Acceptance Criteria:
- Given v1, when Mia runs the kit, then she is not blocked on a lesson completion. Completing the kit does not require F1/F3/F10.
- Given the drill is enabled later, when played, then scoring is rule-based and does not author pack facts.

**US-10; Facilitate an outreach session** *(PRD-F15, Must-Have)*
> As a facilitator (a leader, or a trained seeker with leader-equivalent kit access), I want to run a sequenced MIL session from a published outreach kit so camp and barangay outreach can teach MIL without treating the kit as SK-official crisis facts.

Acceptance Criteria:
- Given v1 DIY, when a leader runs the kit, then they can use the six named modules plus run-of-show and print the packet without the in-app runner: `access-the-pack`, `pause-before-share`, `not-in-pack-not-official`, `ai-does-not-know`, `ethical-share-or-refuse`, and `act-launch-the-desk` (names only in this PRD; full facilitation notes are authored in the pack, not here). Do not add a 20-module catalog in v1.
- Given `ENABLE_OUTREACH_KIT` is on (DWY later) and a published pack with `pack_kind` `outreach_kit`, when a leader opens the facilitator cockpit, then they can run those same sequenced modules in-app.
- Given kit item kinds module, agenda, activity, facilitation_note, handout, and source, when the cockpit or packet loads, then only `outreach_kit` items appear. Canon crisis facts do not appear on kit paths.
- Given 3G fails, when they print the packet, then they can continue from paper. The print QR points at the kit return site. It may reuse an F3 paper card only if a canon pack exists later. It never creates a second official government identity.
- Given they start a `kit_session` (print-led or later in-app), when the session begins or a module opens, then `kit_session_started` and `kit_module_opened` may be recorded. `kit_packet_printed` and `kit_return_opened` are north star. Those events do not mint `canon_share` / `canon_refuse`.
- Given a reader token, when they request facilitator start or print of facilitator notes, then the server returns 403. Reader is participant. Do not invent a fourth role.
- Given pack launch (F1/F3, later), when a leader publishes, then the kit never blocks launch and launch never blocks the kit.
- Given the last modules, when offered, then an optional walk into F3 launch or F10 refuse is allowed later. The kit itself is not a scored inoculation game. Short in-module checks are allowed.

**US-11; Participate in an outreach session** *(PRD-F15, Must-Have)*
> As a reader (participant at a youth camp or barangay outreach), I want a participant view of the current module so I can follow along without facilitator notes or SK crisis canon from a kit path.

Acceptance Criteria:
- Given an optional `kit_session` in progress (print-led or later in-app), when a reader opens participant view or the return site, then they see participant-safe kit items (module, activity, handout as authored for participants), not `facilitation_note`, and not canon crisis facts.
- Given any kit path, when resolved, then the pack is `pack_kind` `outreach_kit`. Crisis facts and commit-share remain canon-only (later desk).
- Given the session ends, when they finish, then they are not scored as in F12. Opening the return site may record `kit_return_opened`. Optional next step may be F3 launch or F10 refuse later. The kit does not mint an official share token.

---

## 5. App Flow & UX Intent

**Design reference:** [dsd-pollux.md](dsd-pollux.md)

### 5.1 Screen Inventory

| Screen | Purpose | Entry points | States |
|--------|---------|--------------|--------|
| Landing | Explain campaign kit + return site; Guild contribute | public URL | static |
| Sign in | Auth | landing, gated routes | loading / error / success |
| Org home | Launch checklist | post-login leader | empty / in-progress / live |
| Template pick | Clone flood / election / notices | org home | empty / success |
| Pack editor | Fill local fields | clone | draft / invalid / ready |
| Pack detail | Items + provenance + share | pack list, QR | success |
| Commit share | Pause then official or refuse | pack detail | choosing / shared / refused |
| Paper card | Print/save QR | checklist done | static |
| Admin packs | Create / publish / archive | leader nav | draft / published / error |
| Contribute | Link to issues / templates | landing | static |
| Kit catalog | List published `outreach_kit` packs | leader nav, kit URL, return site | empty / listed |
| Facilitator cockpit | Agenda, notes, start session, print (DWY later) | catalog | ready / session live / print / flag off |
| Session runner | Advance sequenced modules (DWY later) | cockpit | module / complete / flag off |
| Participant view | Follow current module or return site; no facilitator notes | session join, QR, return URL | waiting / module / done |
| Print packet | DIY paper if 3G dies; QR to kit return site. Reuse F3 card only if a canon pack exists later (never a second official government identity) | catalog, cockpit | static |

### 5.6 Events (instrumentation)

North star is a **session run**: kit started, packet printed, student return. Not `canon_share`.

| Event | When | Feeds |
|-------|------|-------|
| `kit_session_started` | Facilitator starts a kit session (print-led or later in-app) | North star, GTM |
| `kit_packet_printed` | Print packet requested or downloaded | North star, GTM |
| `kit_return_opened` | Student opens the return site after (or during) the session | North star, GTM |
| `kit_module_opened` | Module opened in the session runner or return site | GTM |
| `org_created` | Leader creates org | GTM (later desk) |
| `pack_cloned` | Template cloned | GTM (later desk) |
| `pack_published` | Leader publishes | GTM (later desk) |
| `launch_checklist_completed` | Checklist done | GTM (later desk) |
| `canon_share` | Official share confirmed | GTM when F10 ships; not v1 north star |
| `canon_refuse` | Refuse official share | GTM when F10 ships; not v1 north star |
| `share_link_copied` | Leader copies official URL | GTM when F10 ships |

Legacy events `lesson_started` / `lesson_completed` / `act_completed` apply only if PRD-F12 ships. They are not v1 north star. Kit events do not mint `canon_share` / `canon_refuse`. BRD-M2 (lesson completion) is stale until BRD is rewritten. North star is `kit_session_started` / `kit_packet_printed` / `kit_return_opened`.

---

## 6. Non-Functional Requirements

| Area | Requirement |
|------|-------------|
| Performance | Kit pages and print packet usable on 3G; return site is a short read, not a quiz; scored drill is not the 3G fallback |
| Security | Authz on every mutate; secrets in env; input validation at boundary; pack confinement in SQL + service; kit paths cannot serve `canon` crisis items |
| Privacy | Youth/PII per CLR; minimize data |
| Offline | DIY print packet is the 3G fallback for `outreach_kit`; cache published kit on the return site when possible; paper card for canon packs is later (F3) |
| Cost | No paid messaging in product paths |
| Agent governance | Crisis path has no open-web tool; irreversible commit stays human when F10 ships; kit never mints official share |
| Open source | Apache-2.0 code; CC-BY-4.0 empty templates; SK facts stay SK-owned |

---

## 7. AI / ML Components

No model on the critical path. Optional LLM coaching (PRD-F7) is flagged off by default. Helper draft (PRD-F14) may only cite published pack items; it cannot publish. Crisis answers must come only from published packs (`pack_kind` `canon`) when the later desk ships. Campaign kit (PRD-F15) is authored `outreach_kit` content, not an LLM curriculum and not crisis canon. Injection vignettes (PRD-F11) are authored content, not live agents. See [aia-pollux.md](aia-pollux.md) and [rfc-pollux-channel-packs.md](rfc-pollux-channel-packs.md). AIA still describes the old game-primary or desk-primary path until reconciled.

---

## 8. Dependencies & Assumptions

- Supabase Auth + Postgres available
- Commercial hosting upgraded before monetized public launch (UES-F4)
- First pilot org still open / stale (GTM G-1)
- PRD-F7 LLM coaching deferred past MVP; flag remains off
- Learner/resident audience may include under-18; CLR age gate + parental consent still required before public school/LGU launch
- Pack approval chain (G-6) remains load-bearing when canon packs ship; v1 kit copy is not civic crisis canon
- Seekers Guild can recruit contributors; it cannot be a session or publish gate
- SDD/QAD/BUILD may still describe desk-first Must-Haves; treat those rows as stale until patched
- Dual allowlist is load-bearing in v1: kit is never crisis canon

---

## 9. Rollback

**Single-source rollback:** Revert Cloudflare (commercial) or prior prototype host deployment to the previous production deployment; database migrations must be backward-compatible or have a documented down migration. Feature flags disable PRD-F7 LLM, PRD-F5 bot, PRD-F12 drill, PRD-F11 vignettes, PRD-F14 helper draft, and the later DWY runner (`ENABLE_OUTREACH_KIT`) without redeploy when possible. DIY packet and return site are Must-Have; do not treat turning the runner flag off as deleting the product. PRD-F10 commit share is Could-Have / later; do not ship a kit path that mints official shares.

---

## 10. Open Questions

| Question | Owner | Status | Resolve by |
|----------|-------|--------|------------|
| Telegram vs Messenger first | Eng | **Resolved: Telegram** (PRD-F5 when shipped; not MVP-blocking) | Done (2026-07-15) |
| Age audience + gate for under-18 | CLR | Audience includes minors; consent/PIA policy still **Blocker for public launch** | Public launch |
| Exact B2B / B2G price | Biz | **Resolved provisional:** seats $12/yr list; first paid B2G project $4,000 (see GTM/UES). OSS self-serve is free. | Renegotiate at first paid DFY |
| Pack authoring approval chain | Product | Stale (open); ship leader publish + version pin; tighten before public pilot | Before SDD lock on G-6 |
| Commit-share proof of official post | Product | Open (in-app event vs Page post); F10 is later | Before PRD-F10 lock |
| Product spine | Product | **Resolved: campaign kit first; pack desk later; Guild is community** | Done (2026-08-16) |

---

## Self-Check

- [x] Stable PRD-F# IDs (F1 meaning changed; F15 is v1 product; noted)
- [x] Cut line matches campaign-kit pivot (IDEA may still be catching up)
- [x] Rollback named
- [x] Events for north star (session run, not canon_share)
- [x] No em-dashes
