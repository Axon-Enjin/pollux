# Pitch Deck & Demo Script (PITCH)

**Project:** Pollux
**Date:** 2026-08-15
**Version:** 0.1
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled with demo)
**IDEA:** [idea-pollux.md](idea-pollux.md)
**PRD:** [prd-pollux.md](prd-pollux.md)
**Proposal input:** [research-pollux-unesco-proposal-2026.md](research-pollux-unesco-proposal-2026.md)

---

## 1. Narrative Spine

**Hook (first 10 seconds):** A fake evacuation map is in the barangay chat. It looks official. Mia is 19. She is SK information officer. She has a phone and a Page. She does not have Meltwater.

**Problem (15 seconds):** UNESCO MIL asks people to think, check, and share fairly. That work happens at 2 a.m. in a flood, not in a quiz. Fluent AI text makes rumors look like government voice. Two-thirds of creators do not systematically fact-check before they share. SK already has the mandate. They cannot launch a gate without a vendor in the room. Youth outside Manila rarely get to build the tools they are asked to use.

**Solution (20 seconds):** Pollux is an aide SK councils launch themselves. Clone a flood template. Fill our routes. Publish. Pause. Then share as SK-official, or refuse if it is not in the pack. Seekers Guild is the community that stewards the open-source project. Guild is not on her Page. She does not need to join to go live.

**Proof (demo tease):** Phone: create org, clone, fill three fields, publish, commit share, refuse a rumor. Paper card with QR if 3G dies.

**Differentiation (10 seconds):** We are not a fact-check model. We are not a game. We are not a Guild app wearing SK clothes. Official speech stays a human commit.

**Ask / close:** Showcase this as Pollux plus Seekers Guild. Then let SK desks launch without us.

---

## 2. Slide / Scene Outline

| # | Scene | On screen | Speaker says (bullet script) | Duration |
|---|-------|-----------|------------------------------|----------|
| 1 | Fake map | Chat screenshot of a fluent fake route | Mia is SK. The map is fake. It still spreads. | 15s |
| 2 | MIL, not a quiz | UNESCO MIL six goals as six gates | MIL is what she does when she posts, not a lesson she finished in June. | 20s |
| 3 | Three roles | SK / Pollux / Guild diagram | They launch. We aide. Guild stewards. Facts stay SK. | 20s |
| 4 | Demo | Live phone or recording | Clone. Fill. Publish. Commit. Refuse. Card. | 70s |
| 5 | Close | Jury sentence | Equal billing. Human commit. Provinces can contribute. | 25s |

**Total time:** 150 seconds (leave 30s slack under 3:00)

---

## 3. Live Demo Script

**Pre-flight (before judges enter):** Signed in as Mia. Empty org or reset clone. Flood template ready with three blank fields. Paper card printed. Recording fallback on the same phone. No Guild logo on the pack screen.

**Demo path (happy path only):**

1. Open Pollux on phone. Show org create. Name it after a barangay, not Seekers Guild.
2. Clone flood template. Fill pickup point, hotline, who approved.
3. Publish. Show version stamp. Show a draft stays hidden.
4. Commit share: read publisher, date, version. Confirm. Copy official link. Then refuse a rumor not in the pack.

**Fallback if live fails:** Recorded screen capture of the same four steps plus the printed QR card held to camera.

**Do not demo:** Inoculation game, settings, login errors, LLM coach, Meltwater-style dashboards, Guild membership wall.

---

## 4. Judging Criteria Map

*UNESCO Youth Hackathon 2026: theme, clarity, innovation, feasibility, impact/inclusion.*

| Official criterion | Where we address it | Evidence |
|--------------------|---------------------|----------|
| Theme: Play Your Part, youth designing the future of MIL | Hook + MIL gates | SK officer as change agent; Guild as provincial contributors |
| Clarity | Three-role diagram + jury sentence | One product, one community, SK owns speech |
| Innovation | Commit share vs fact-check LLM | Canon pack + human pause; AI may draft later, cannot publish |
| Feasibility | Demo + paper card | Phone loop; Apache-2.0; templates; no paid messaging |
| Impact / inclusion | Provinces + cheap phone + 3G card | Launch-without-us; contribution rungs; 18+ demo persona while CLR blocks minor public launch |

---

## 5. Production Readiness Gate (pre-demo)

*Confirm before demo day. Full checklist: AGENTS.md Production Readiness Gate.*

| Check | Status | Notes |
|-------|--------|-------|
| Security reviewed | Fail | App not scaffolded; confinement specified in RFC-001 |
| CLR (if user data) | Fail | Consent/PIA still blocker for public under-18 launch; demo uses Mia 19 |
| AIA (if AI/ML component) | N/A | No model on critical path; flag off |
| Context hygiene (if AI product) | N/A | No live agent |
| QAD Must-Have paths | Fail | QAD still describes old game; rewrite before code |
| OPS wired | Fail | No production deploy |
| Rollback (PRD §9) | Pass (docs) | Named; nothing to revert yet |
| BUILD stack pinned | Pass (docs) | Next.js / Supabase / Cloudflare in BUILD; verify before code |
| DSD §8 gate (if UI) | N/A | Concept frames only |

Contest video may use paper card + recorded walkthrough. Do not claim production-ready.

---

## 6. Anticipated Q&A

| Likely question | Short answer |
|-----------------|--------------|
| Is this a game? | No. Optional drill later. v1 is the SK desk. |
| Are you fact-checking the internet? | No. If it is not in the published pack, it is not SK-official. |
| Why Seekers Guild? | Community and contribution, especially outside Manila. Not the publisher. |
| Can SK launch without you? | That is the test. If they need a workshop, we failed. |
| What about AI? | It may draft inside the pack later. A human still publishes and shares. |
| Under-18 learners? | CLR consent is still a public-launch blocker. Demo is an adult SK officer. |

---

## 7. Submit this edition

Deadline: **16 Aug 2026 23:59 Paris** (about 17 Aug 05:59 Philippine time).

1. Fill team block in [research-pollux-unesco-proposal-2026.md](research-pollux-unesco-proposal-2026.md).
2. Export that file to PDF.
3. Record this script in one take, max 3:00. English or local with English subs.
4. Upload proposal + video on the UNESCO portal. This repo cannot submit for you.
5. If the team cannot tell the SK-launch story in three minutes, skip the portal and keep building the desk.

---

## Self-Check

- [x] Hook does not start with "Today we will…"
- [x] IDEA one-liner is quoted or clearly restated in Hook / Solution
- [x] Named user or their pain appears in Hook or Problem beat
- [x] Every judging criterion has a mapped beat
- [x] Production Readiness Gate (§5) passed or blockers documented
- [x] Demo script is rehearse-able in under 3:00
- [ ] Rehearsal done once (time the hook; speak it aloud or record)
- [x] Fallback exists for live demo failure
- [x] AGENTS hard bans applied; VOICE polish pass before lock
- [x] Next suggested doc: WRAP (after event) or keep GTM
