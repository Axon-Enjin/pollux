---
title: Facilitator 3Ds run of show
type: playbook
domain: outreach-kit
tags:
  - outreach-kit
  - facilitator
  - mil
  - unesco
aliases:
  - 3Ds
  - Document Demonstrate Duplicate
  - barangay 45m agenda
  - camp halfday agenda
related:
  - access-the-pack
  - pause-before-share
  - not-in-pack-not-official
  - ai-does-not-know
  - ethical-share-or-refuse
  - act-launch-the-desk
  - facilitator-one-pager
  - learner-handout
  - consent-checklist
  - README
  - _STACK
confidence: high for product gates (pack_kind, flag, CLR, no canon_share); medium for 3Ds as a camp encoding method
source_tier: mixed
created: 2026-08-16
---

# Facilitator 3Ds run of show

> Encode the session so a second officer can run the desk habit from the page: write the checklist, show it once, watch them copy it. If the copy fails, patch the checklist. Do not blame the learner.

This note is a **facilitator instrument** (`facilitation_note` / `agenda` when published). It is not a participant lesson, not PRD-F12, and not SK crisis canon. Readers must not see this file in participant view.

`kit_sessions.format` values: `barangay_45m` (Agenda A), `camp_halfday` (Agenda B).

## What this is not

- Not a scored game. No badges, no `attempts`, no `max_score`.
- Not PRD-F3 (org launch checklist and paper card for a **canon** pack). Module 6 may *point* at F3. Completing this kit never blocks launch.
- Not a permit to speak as SK or as Seekers Guild on the SK Page.
- Not a sales closer, not a pitch script, not a persuasion funnel. Do not import commercial close sequences into a camp.
- Not an RCT. 3Ds here is an **operator encoding pattern**: checklist, demo, observed copy, then artifact patch. It is not evidence that a 45-minute block reduces disinformation.

## CLR gates (read before you book the room)

| Gate | Rule |
|------|------|
| Under-18 camp | **Counsel BLOCKER** for public school / LGU camp launch. Age gate, parental consent, and school rules are TBD with counsel. Do not soft-launch a youth camp on this kit until counsel clears it. |
| Product demo | Demo persona remains **Mia, 19**. Fixtures stay synthetic. No real minor accounts. |
| Names | **Do not collect student names.** v1 `kit_sessions` stores org, pack version, format, `started_by` officer. Print packets carry no PII. |
| Consent paper | [[consent-checklist]] is a stub pointing to counsel. It is not a legal form. |

If the room includes minors and counsel has not cleared the camp, stop. Run Agenda A only with 18+ officers, or do not run.

## Dual allowlist (do not mix)

| Path | `pack_kind` | What you may show | What you must not do |
|------|-------------|-------------------|----------------------|
| This session | `outreach_kit` | module, agenda, activity, facilitation_note (facilitator only), handout, source | Mint `canon_share` or `canon_refuse`. Serve crisis `fact` / `route` / `contact` / `faq` / `media`. |
| Desk / official voice | `canon` | Published crisis items after a human commit | Treat kit fluency as SK-official. |

Kit events (`kit_session_started`, `kit_module_opened`, `kit_packet_printed`) do not replace north-star share events. Optional walk into F10 refuse or F3 launch happens on a **canon** pack, after this kit, as a separate act.

Worked-example rumors stay labeled **quarantine / not canon**.

## Flag off still means paper

`ENABLE_OUTREACH_KIT` defaults **off**. When the flag is not `true`, kit APIs return 404. That does not cancel the session.

| Mode | What you use |
|------|----------------|
| Flag off | This run-of-show plus the print packet ([[facilitator-one-pager]], [[learner-handout]], [[consent-checklist]]). Clock the modules on paper. Fill the cockpit fields on paper. |
| Flag on | Same sequence in the facilitator cockpit / session runner. Print remains the 3G fallback. QR may point at the kit URL, or reuse the F3 paper card for a **canon** pack. Never a second official government identity. |

A reader token must not start or print. Reader is participant.

## Delivery ladder (kit is the free map)

One short ladder. Do not upsell in the room.

| Rung | Name | What it is | Cost in this story |
|------|------|------------|--------------------|
| 1 | **DIY** | Print packet + this checklist. Officer runs the hour without us. | Free map. This kit. |
| 2 | **DWY** | In-app runner when `ENABLE_OUTREACH_KIT` is on. Same modules, sequenced. | Free product path. Flag may still be off. |
| 3 | **DFY** | Later paid B2G / hosted install (org, templates, training). | Later. Not required to finish today. |

The kit is the map, not the invoice. Do not hold Act hostage for a paid install.

## 3Ds pass conditions

Unit of success: **the checklist**, not charisma, not a quiz score, not "they watched me once." If a stranger (second SK officer) cannot hit the session outcome from the page alone, the page is unfinished. That is a facilitator / authoring fault. **Do not blame the learner if the checklist is unfinished.**

| Step | Actor | Artifact | Pass condition | Fail (patch, do not shame) |
|------|-------|----------|----------------|----------------------------|
| **Document** | Facilitator (before doors) | This run-of-show + print packet + pack **version** written at the top | You can run the chosen agenda using only the written steps (no improvising crisis facts) | You needed lore that is not on the page. Add the step. Reprint or write it in the margin. |
| **Demonstrate** | Facilitator | Live walk of one checklist row (usually Access: open pack, name publisher / date / version) | Confusion from the room becomes a checklist edit in the same session | You re-explained verbally and moved on. The next officer still cannot run it. |
| **Duplicate** | Participant copies; you observe | Same checklist in their hands (handout). They pause, check the pack, refuse unofficial fluent text, optionally walk toward launch or refuse on **canon** later | They followed the written steps. If the outcome is wrong while they followed, the checklist is wrong. | They freelanced because a step was vague. Patch the step. Retrain process adherence. Do not grade them as "bad at MIL." |

### Pass / fail for the *session* (not the person)

Check these before you write a cockpit Verdict of "held":

- [ ] Pack kind in use is `outreach_kit` (paper banner: "seminar kit, not SK-official crisis facts").
- [ ] Canon pack version for any optional F3/F10 walk is written as an Evidence ID. Kit version is written too.
- [ ] No student names on the roster, session row, or photos-as-attendance.
- [ ] Rumor examples labeled **quarantine / not canon**.
- [ ] Last block was Act / refuse (Agenda A: last 8 minutes). Kit did not mint `canon_share`.
- [ ] Cockpit four fields filled (paper or app).

If a box is empty, the **checklist** failed. Fix the artifact. Do not mark the learner incomplete.

### How to run the loop in the room

1. **Document (before):** Fill pack slug, `pack_kind = outreach_kit` version, optional canon pack version, format, officer name (starter only). Put the minute table in front of you.
2. **Demonstrate (first module):** Show Access on a real published **canon** pack if one exists, or on a paper card. Speak only provenance fields. Do not invent flood facts from memory.
3. **Duplicate (modules 2 to 6):** Sit on your hands. They use the handout. One correction at a time. Patch the page when several people miss the same step.
4. **Close:** Cockpit fields. Decision bite is one sentence.

UNESCO MIL goals (think critically, spot falsehoods, know the source, use media well, share ethically, fairer public talk) are **product behaviors** in this hour, not a lecture list.

## Agenda A: 45-minute barangay outreach

**Format:** `barangay_45m`. Standing shade, hall, or covered court. Cheap phones, 3G optional. Print first.

Clock is logistics, not efficacy. A 45-minute block does not close the firehose. If time dies, cut discussion. Keep the quarantine label.

| Clock | Min | Slug | Facilitator move (Document on the page) | Duplicate you watch for |
|-------|-----|------|-----------------------------------------|-------------------------|
| 0:00 to 0:06 | 6 | [[access-the-pack]] | Name publisher, date, version on the desk (or paper card). Banner: this seminar is `outreach_kit`. | They can point at provenance, not at the group chat. |
| 0:06 to 0:13 | 7 | [[pause-before-share]] | One fluent rumor. Hands stay down until provenance is checked. | They pause. They do not auto-forward. |
| 0:13 to 0:21 | 8 | [[not-in-pack-not-official]] | Fake map **quarantine / not canon**. If it is not in the published **canon** pack, it is not official. No fact-check model. | They refuse unofficial. They do not ask an LLM. |
| 0:21 to 0:28 | 7 | [[ai-does-not-know]] | Fluent text is not knowledge. Human remains principal. | They do not treat a chatbot as SK. |
| 0:28 to 0:37 | 9 | [[ethical-share-or-refuse]] | Official share is a human commit on **canon**. Refuse is first-class. Kit path does not mint the token. | They can say refuse without shame. |
| 0:37 to 0:45 | **8** | [[act-launch-the-desk]] | **Last 8 minutes: Act / refuse.** Optional point at F3 clone/fill/publish, or F10 refuse on a canon pack. Completing the kit is **not** a launch gate. | They leave with a next step or a written refuse, not a badge. |

Minute 0: ten-second CLR line ("no names on the sheet"). Do not steal Act's eight minutes for a long intro.

## Agenda B: half-day youth camp

**Format:** `camp_halfday`. About four hours including one break. **Counsel BLOCKER** if attendees are under 18 until counsel clears school / LGU camp. If you are demoing product, use Mia 19 and synthetic fixtures.

Same six slugs, more Duplicate reps. Still not a game. Still no student names.

| Clock (example 13:00 start) | Min | Slug | Notes |
|-----------------------------|-----|------|--------|
| 13:00 to 13:15 | 15 | 3Ds Document | Co-facilitator reads this page aloud. Write Evidence IDs. DIY packet on every chair. Confirm flag on/off. If off, stay on paper. |
| 13:15 to 13:50 | 35 | [[access-the-pack]] | Stations: find publisher / date / version. Demonstrate once, then they Duplicate on a second pack page. |
| 13:50 to 14:25 | 35 | [[pause-before-share]] | Two rumors. Trace origin. Primary source or sit down. |
| 14:25 to 15:00 | 35 | [[not-in-pack-not-official]] | Quarantine table: in pack vs not. Fake map. No oracle. |
| 15:00 to 15:15 | 15 | Break | No attendance list of youth names. |
| 15:15 to 15:50 | 35 | [[ai-does-not-know]] | Fluency demo (pre-authored quarantine sample). Do not call a live model for crisis Q&A. |
| 15:50 to 16:20 | 30 | [[ethical-share-or-refuse]] | Pair practice: commit vs refuse language. Token still not minted from the kit. |
| 16:20 to 16:50 | 30 | [[act-launch-the-desk]] | Optional F3 walk for officers who already have org access. Seekers can help templates without publishing that barangay's facts. Not a launch gate. |
| 16:50 to 17:00 | 10 | Cockpit close | Four fields. Decision bite. Thank the room. DIY packet goes home. |

If the camp is 18+ SK officers only, you may lengthen Act. If mixed youth and counsel is uncleared, do not run Agenda B.

## Cockpit fields (session end)

Fill on paper even when the app is 404. This is the meeting output, not a vibe. Adapted from a war-room cockpit: verdicts need evidence IDs so the next officer is not arguing from recollection.

| Field | Write |
|-------|--------|
| **Verdict** | `held` (checklist pass boxes checked) / `held-with-patches` (you edited the page mid-session) / `stopped` (CLR or safety stop) / `incomplete-artifact` (checklist unfinished; **not** "learners failed"). |
| **Evidence IDs** | `outreach_kit` slug + **pack version**. If you pointed at a desk: **canon** pack slug + version. Print edition date if paper-only. No student identifiers. |
| **Open questions** | What the page still does not encode. Example: "refuse script too long for 3G." Empty if none. Do not invent crisis facts to close a question. |
| **Decision bite** | One sentence. Owner = officer `started_by` (or paper signer). Date. Example: "Hold kit as pedagogy; patch Access step 3; do not mint share from this session; next F3 walk Tuesday if counsel ok." |

Do not mark Strong / shipped / UNESCO-complete. Stage-0 honesty: this hour trains a habit. It does not certify MIL.

Optional `kit_session` (flag on): `org_slug`, `pack_id`, `pack_version`, `started_by`, `audience_band`, `format`. Still no student names.

## When it breaks

- Hero demo with no checklist: Duplicate impossible.
- Mixing kit text into a Facebook post as "SK says": allowlist breach. Stay on `canon` + human commit.
- Collecting a yellow pad of youth names "for certificates": CLR fail. Stop.
- Running Agenda B for a school before counsel: BLOCKER. Stop.
- Scoring the room: you built F12 by accident. Tear the scores up.
- Calling DFY a requirement: the kit is the free map.

## Related

- [[access-the-pack]]
- [[pause-before-share]]
- [[not-in-pack-not-official]]
- [[ai-does-not-know]]
- [[ethical-share-or-refuse]]
- [[act-launch-the-desk]]
- [[facilitator-one-pager]]
- [[learner-handout]]
- [[consent-checklist]]
- [[README]]
- [[_STACK]]

## Sources

1. **[Method, not RCT]** Document / Demonstrate / Duplicate as an operator encoding loop: write the exact steps, show them once, watch a second person copy, then patch the *checklist* when copy fails. Cited as a training method for repeatable desk work. Not a trial, not a claim that camps cause civic outcomes. Adapted here for SK / barangay facilitation. Do not treat this as commercial close doctrine.

2. **[T1]** UNESCO Media and Information Literacy programme (think critically, check sources, use media well, share ethically, fairer public talk). Pollux maps those goals to product gates, not a MOOC. Verification: already cited in Pollux IDEA / PRD / UNESCO proposal. https://www.unesco.org/en/media-information-literacy

3. **[T0]** Pollux PRD-F15, US-10, US-11: six module slugs, print fallback, kit does not mint official share, kit never blocks launch. Verification: `docs/prd-pollux.md`.

4. **[T0]** Dual `pack_kind` (`canon` vs `outreach_kit`); `ENABLE_OUTREACH_KIT` default off; `kit_sessions` without student names. Verification: `docs/sdd-pollux.md`, `docs/rfc-pollux-channel-packs.md`.

5. **[T0]** CLR: under-18 camp is counsel BLOCKER; demo Mia 19; no student names; print has no PII; consent stub is not a legal form. Verification: `docs/clr-pollux.md`.

6. **[T2]** AACRA labels (Access, Analyze, Create, Reflect, Act) in mentorship notes. Sequence mapping is pedagogical (see [[_STACK]]). Verification: `docs/mentorship-july-1.md`.
