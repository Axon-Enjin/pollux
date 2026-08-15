# Pitch Deck & Demo Script (PITCH)

**Project:** Pollux
**Date:** 2026-08-16
**Version:** 0.5
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled with demo)
**IDEA:** [idea-pollux.md](idea-pollux.md)
**PRD:** [prd-pollux.md](prd-pollux.md)
**Proposal input:** [research-pollux-unesco-proposal-2026.md](research-pollux-unesco-proposal-2026.md)

---

## 1. Narrative Spine

**Hook (first 10 seconds):** SK wants a barangay outreach this Saturday. Mia is 19. She is SK information officer. She has a phone and a Page. No agenda. No handouts. No way for students to keep learning after.

**Problem (15 seconds):** UNESCO MIL asks people to think, check, and share fairly. That work is the hour she has to run this Saturday. Fluent AI text makes rumors look like government voice. Two-thirds of creators do not systematically fact-check before they share. SK already has the mandate. They cannot buy a vendor workshop every week. Youth outside Manila rarely get the same kit.

**Solution (20 seconds):** Pollux is the open campaign kit an SK officer runs herself: modules, a program guide, and a site students return to after. Pre-made modules they can teach. A run-of-show and a logistics list they can tailor. A site students can open after the session. Seekers Guild partners with SK and LGU on the same materials, including outside Manila. Nothing valuable is paywalled. They run the session. We pack the bag.

**Proof (demo tease):** Primary: print packet plus facilitator run-of-show. Open the kit. Clock one module (pause before share). Show the student URL. Name Guild as partner. F3 tap and clone-fill-publish stay off camera.

**Differentiation (10 seconds):** UNESCO format is an open toolkit plus community intervention. Modules, program guide, and student access stay free. Guild is a partner. Guild does not speak for her Page.

**Ask / close:** Pollux is the open campaign kit SK councils run themselves. Seekers Guild partners with youth desks, especially outside the big cities. Modules, program guide, and student access stay free. Showcase both. Then let SK officers run Saturday without us.

---

## 2. Slide / Scene Outline

UNESCO video asks: tell the story (scenes 1-2), explain the solution (scenes 3-4), highlight originality and impact (scene 5, seeded in Proof).

| # | Scene | On screen | Speaker says (bullet script) | Duration |
|---|-------|-----------|------------------------------|----------|
| 1 | Story: the problem | Mia, phone, empty outreach | Saturday is outreach. No agenda. No handouts. | 15s |
| 2 | Story: why it matters | UNESCO MIL as session behavior | MIL is the hour she runs this Saturday. | 20s |
| 3 | Solution: what and who | Packet + run-of-show on table | Modules, program guide, student site. They run the session. We pack the bag. | 20s |
| 4 | Solution: how | Hands on packet and run-of-show | Open kit. Run one module. Student URL. Guild partners. | 70s |
| 5 | Originality and impact | Jury sentence | Kit they run themselves. Guild partners. Materials stay free. | 25s |

**Total time:** 150 seconds (leave 30s slack under 3:00)

---

## 3. Live Demo Script

**Pre-flight (before judges enter):** Print packet on the table. Facilitator run-of-show printed (3Ds / 45-minute agenda). Student URL or kit reader page ready on the phone if you show it. Mia 19. Synthetic session only. No Guild logo as SK Page. Do not stage an F3 tap.

**Demo path (happy path only):**

1. Hold the blank Saturday: no agenda, no handouts, nowhere for students after.
2. Open the print packet. Show the run-of-show. Name six modules. Forty-five minutes or half day.
3. Run one module from the page: pause before share. Hands stay down. Check the source. If it is not in the pack, it is not official. Label the hour as practice.
4. Show the student URL. They can open the site after the session.
5. Name Seekers Guild as partner on the same materials, especially outside Manila. Nothing valuable is paywalled.

**Fallback if live fails:** Hold the print packet and the run-of-show to camera. Recorded walk of opening the packet, clocking one module, and showing the student URL. Do not fall back to an F3 tap.

**Do not demo:** F3 tap, clone-fill-publish, inoculation game, scored lesson UI, settings, login errors, LLM coach, Meltwater-style dashboards, Guild membership wall, kit text as SK-official crisis canon.

Word-for-word UNESCO cut: §8. Table props: [print/README.md](outreach-kit/print/README.md) (packet pages; F3 card is not this cut). Subtitles: [pitch/unesco-3min.srt](pitch/unesco-3min.srt).

---

## 4. Judging Criteria Map

*UNESCO Youth Hackathon 2026 official jury criteria. Every row has a spoken beat or table prop.*

| Official criterion | Where we address it | Evidence |
|--------------------|---------------------|----------|
| Consistency with the Theme | Hook + MIL hour + kit demo | Strong alignment with Play Your Part and MIL principles: an SK officer runs Saturday outreach herself; think, check, and share fairly are the hour she teaches from the kit |
| Clarity of Presentation | Kit objects + one-take §8 + jury sentence | One kit on the table, one partner community, one close. Print packet and run-of-show on camera. Spoken cut is 279 words. |
| Innovation & Creativity | Run-of-show plus student return URL | A session they can run this week. After-link so MIL continues after dismissal. 3Ds: document, demonstrate, duplicate. |
| Feasibility & Sustainability | Print packet + run-of-show + reuse | Paper path this Saturday. Apache-2.0 / CC-BY when they exist. Officers reuse the same kit next week. No paid vendor in the room. |
| Impact & Inclusion | Provinces + free materials + cheap phone | Same kit outside Manila. Materials stay free. Demo uses Mia 19. CLR still blocks public under-18 camp. |

---

## 5. Production Readiness Gate (pre-demo)

*Confirm before demo day. Full checklist: AGENTS.md Production Readiness Gate.*

| Check | Status | Notes |
|-------|--------|-------|
| Security reviewed | Fail | App not scaffolded; confinement specified in RFC-001 |
| CLR (if user data) | Fail | Consent/PIA still blocker for public under-18 camp; demo uses Mia 19 |
| AIA (if AI/ML component) | N/A | No model on critical path; flag off |
| Context hygiene (if AI product) | N/A | No live agent |
| QAD Must-Have paths | Fail | QAD still catching up to campaign kit; rewrite before code |
| OPS wired | Fail | No production deploy |
| Rollback (PRD §9) | Pass (docs) | Named; nothing to revert yet |
| BUILD stack pinned | Pass (docs) | Next.js / Supabase / Cloudflare in BUILD; verify before code |
| DSD §8 gate (if UI) | N/A | Concept frames only |

Contest video uses the print packet and run-of-show. Do not claim production-ready. Do not claim an F3 tap as the product.

---

## 6. Anticipated Q&A

| Likely question | Short answer |
|-----------------|--------------|
| Is this a game? | UNESCO format is an open toolkit. v1 is the campaign kit an SK officer runs herself. An optional drill can come later. |
| Is the camp kit official? | Facilitator notes and a paper packet. The hour is practice. |
| Are you fact-checking the internet? | The session teaches pause and refuse. Official SK facts come from a published pack. |
| Why Seekers Guild? | Partner channel, especially outside Manila. Same materials. Guild does not speak for her Page. |
| Can SK run Saturday without you? | That is the test. A vendor in the room means we failed. |
| What about the official pack desk? | v1 is modules, program guide, and student access. Official-pack tap is a later side tool. |
| What about AI? | A human still runs the session. A model may draft inside a pack later. |
| Under-18 learners? | CLR consent is still a public-camp blocker. Demo is an adult SK officer. |

---

## 7. Submit this edition

Deadline: **16 Aug 2026 23:59 Paris** (about 17 Aug 05:59 Philippine time).

1. Team roster of six is filled in [research-pollux-unesco-proposal-2026.md](research-pollux-unesco-proposal-2026.md) § Team (every row is Team member). Re-export PDF if that table moved.
2. Proposal HTML/PDF: [pitch/unesco-proposal.html](pitch/unesco-proposal.html) and [pitch/unesco-proposal.pdf](pitch/unesco-proposal.pdf) (regenerate if you edit the input).
3. Record §8 in one take, max 3:00. Burn [pitch/unesco-3min.srt](pitch/unesco-3min.srt). English or local with English subs.
4. Upload proposal + video on the [UNESCO Youth Hackathon 2026](https://www.unesco.org/en/articles/unesco-youth-hackathon-2026) portal. This repo cannot log in for you.
5. If the team cannot tell the Saturday kit story in three minutes, skip the portal and keep packing the kit.

---

## 8. UNESCO spoken script and shot list (150s)

Target **2:30**. Hard cap **3:00**. About 130 words per minute. Do not add slides. Speak this text.

UNESCO video asks in this cut: story (Hook + Problem), solution (Solution + Proof), originality and impact (Close, with Guild partner and free materials named in Proof).

**Pre-flight:** quiet room; print packet + run-of-show on the table; student URL ready on the phone if you show it; no Guild logo as SK Page; no lesson/game UI; no F3 tap; Mia 19; synthetic session only.

Spoken word count: **279 words**. At 130 wpm that is about 129 seconds of speech. Leave the remaining time in Proof for hands on the packet.

### Shot list

| Time | Camera | On screen / in hand | On-screen words (few) |
|------|--------|---------------------|------------------------|
| 0:00-0:15 | Face | Empty Saturday: phone, no packet yet | Saturday |
| 0:15-0:35 | Face | Still of the blank table, dim | (none) |
| 0:35-0:55 | Face | Hands set packet and run-of-show | They run the session. |
| 0:55-2:05 | Hands | Open packet; clock pause-before-share; show student URL | Open kit / Pause / Student URL |
| 2:05-2:30 | Face | Packet + run-of-show still; no Guild crest | (none; jury sentence is spoken) |

Cuts only on these five beats if you cannot do one take.

### Spoken text

**Story: the problem (0:00-0:15)**

SK wants a barangay outreach this Saturday. Mia is nineteen, SK information officer. She has a phone and a Page. No agenda. No handouts. Nowhere for students to go after.

**Story: why it matters (0:15-0:35)**

Media and information literacy happens in the hour she has to run this Saturday, not in a quiz she finished in June. Fluent AI makes rumors look official. SK already has the mandate. They have no agenda, no handouts, and no vendor in the room.

**Solution: what and who (0:35-0:55)**

Pollux is the open campaign kit an SK officer runs herself: modules, a program guide, and a site students return to after. Pre-made modules they can teach. A run-of-show and a logistics list they can tailor. They run the session. We pack the bag.

**Solution: how (0:55-2:05)**

Watch the kit. This print packet is what we demo. This page is the run-of-show. Mia opens both herself. She does not wait for a vendor. Six modules. Forty-five minutes on a covered court, or a half day if they have the hall.

Document. Demonstrate. Duplicate. She writes the checklist. She shows pause before share once. Then the room copies from the handout. A fluent rumor hits. Hands stay down until they check the source. If it is not in the pack, it is not official. Practice, not crisis canon.

Students leave with a URL. They can open the site after the session. Seekers Guild partners with SK and LGU on the same materials, including outside Manila. Nothing valuable is paywalled.

**Originality and impact (2:05-2:30)**

Pollux is the open campaign kit SK councils run themselves. Seekers Guild partners with youth desks, especially outside the big cities. Modules, program guide, and student access stay free. Showcase both. Then let SK officers run Saturday without us.

### Claim audit (say only this)

Allowed: docs and kit notes exist; v1 is the campaign kit; print packet and run-of-show are the demo; kit is facilitator notes, not crisis canon; demo persona is 18+; CLR still blocks public under-18 camp; Apache-2.0 / CC-BY templates when they exist; materials stay free.

Forbidden: production-ready; we fact-check the internet; kit completion launches an official pack; Guild publishes SK facts; we race rumor volume with a model; F3 tap as the product.

Rehearsal checklist: [pitch/unesco-rehearsal.md](pitch/unesco-rehearsal.md). Teleprompter: [pitch/unesco-teleprompter.html](pitch/unesco-teleprompter.html).

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
