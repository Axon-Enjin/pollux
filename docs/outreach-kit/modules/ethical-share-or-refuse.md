---
title: Ethical share or refuse
type: concept
domain: outreach-kit
tags: [outreach-kit, mil, aacra, unesco, principal]
aliases:
  - "human commit share"
  - "canon_share or canon_refuse"
  - "refuse-forward is first-class"
related:
  - "[[pause-before-share]]"
  - "[[not-in-pack-not-official]]"
  - "[[act-launch-the-desk]]"
confidence: high for product rules (human commit, events, kit cannot mint); medium for UNESCO programme wording beyond "share ethically"
source_tier: mixed
created: 2026-08-16
---

# Ethical share or refuse

> Official voice is a human choice: confirm a published canon item and mint a share, or refuse a rumor and mint nothing. UNESCO "share ethically" is that commit, not a like, not a kit badge.

## Definition

**Ethical share or refuse** is the outreach-kit module for AACRA **Act** and UNESCO **share ethically**. In Pollux it is PRD-F10: only an authenticated leader, after a pause that names provenance, pack match, and a human click, may treat something as SK-official. [1][2]

Two first-class outcomes exist. They are the north star, not kit telemetry. [1]

| Choice | What the product records | What it mints |
|--------|--------------------------|---------------|
| Confirm official | `canon_share` | Official URL / share token, version-pinned to a published **canon** pack |
| Refuse | `canon_refuse` | Nothing. No token. The rumor does not become government voice |

Refuse is not a failed share. It is the ethical Act when the item is missing, unpublished, or not the desk's to stamp. Commit share does not call an LLM coach. [1]

**Who may mint.** Only a leader (or admin) with a published canon pack. A camp participant practices the **refuse** muscle and the pause. They do not become the SK Page. A kit session (`StartKitSession` / `PrintKitPacket`) **cannot** mint `canon_share`. `MintShareLink` and commit share reject `pack_kind = 'outreach_kit'` with 403. No `share_links` insert. Kit events (`kit_session_started`, `kit_module_opened`) do not replace the north star. [1][3]

This module sits after [[pause-before-share]] and [[not-in-pack-not-official]]. Pause asks who made it and why. Allowlist asks membership. Ethical share asks: will a human officer take responsibility for this as official voice, or refuse?

## Why It Works

Fluent rumors become de facto government voice because forwarding is cheaper than a named commit. UNESCO's programme page reports that two-thirds of digital content creators do not systematically fact-check before sharing online. Pollux does not "fix" that statistic in 45 minutes. It puts a gate where SK speech actually happens. [4]

The gate works because it is **human principal**, not auto-post:

1. **Share ethically is a choice, not a feed.** The officer sees who published, which version, and why the item is in the pack, then confirms or refuses. [1][2]
2. **Refuse-forward is first-class.** Recording `canon_refuse` teaches that not posting is civic action, not cowardice. [2]
3. **Kit cannot launder official voice.** Facilitator packets and camp practice stay on the outreach allowlist. Official URLs stay on canon. [3]
4. **Ethics without "trust nothing."** Culver's mentorship warning: constant "don't trust any source" talk can erode belief that journalism and civic institutions can be trusted at all. This module names **who** may speak as SK, and **when** to refuse, without teaching nihilism. Daily share choices (including a funny disinfo meme) are ethical questions, not only technical ones. [5]

Act, in the DW Akademie AACRA wheel, is informed, ethical media habits after Access, Analyze, Create, and Reflect. Closing frame: we choose, with purpose and care. [6]

## Evidence & Origins

IDEA maps UNESCO "share ethically" to product behavior: human commit; refuse-forward is first-class; no auto-post. Official share is demo-critical. North star is `canon_share` and `canon_refuse` in a live incident window, by SK org. [2]

PRD-F10 / US-05: given a published pack, official share shows a pause (who published, version, why it is in the pack); confirm records `canon_share` and copies the official URL; a rumor not in the pack records `canon_refuse` and does not mint a token; commit share does not call an LLM. US-10/US-11: kit sessions may log module opens; they do not replace those events; the kit does not mint an official share token. [1]

RFC-001 hard bans: kit items cannot satisfy crisis `GetPackItem`; kit session cannot mint official share; publish and official share remain human principal actions; no agent may mint without an authenticated leader/admin session. Alternative rejected: kit session mints the same share token as the canon desk. [3]

UNESCO MIL programme (already cited in IDEA) is the public frame for ethical share and safer use of media. Pollux's schema (events, tokens, dual allowlists) is a product mapping. Confidence is **high** on those product rules. Confidence is **medium** if a facilitator stretches UNESCO copy into extra competencies this module does not own. [2][4]

Sherri Hope Culver (2 July 2026 mentorship): Media Literacy includes **Act** (NAMLE: access, analyze, evaluate, create, and act). Tension to hold: do not train "trust nothing." Tension to hold: ethical awareness is daily digital choice. [5]

## Worked Example

Youth camp, flood barangay. Two artifacts on the table.

**A. Official link (practice as leader-only).** The SK has a published **canon** flood pack, version 2. An item names publisher, date, version (see [[access-the-pack]]). A leader (not the camp cohort as a group) opens commit share. Pause: who published, version, why it is in the pack. She confirms. Product records `canon_share`. She may copy the official URL to post from the **SK Page**. Completing this module is not that click. The kit runner never performs it. [1][3]

**B. Refuse rumor (practice for participants).** A volunteer reads a fluent chat forward: "Evacuation na, follow this map." The map is **quarantine / not canon** (not in the published pack; see [[not-in-pack-not-official]]). Facilitator: "Hindi tayo magmi-mint ng official share mula sa kit. Magpe-practice tayo ng refuse."

Participant script (no SK Page, no Guild stamp):

1. Pause ([[pause-before-share]]). Who made this? Why is it spreading?
2. Check membership. Wala sa published canon pack.
3. **Refuse.** Say it aloud: "Hindi ito SK-official. I will not forward it as government voice."
4. If a session is running, the facilitator may record `kit_module_opened`. That is **not** `canon_refuse`. A real `canon_refuse` happens only when a leader on a **canon** pack chooses refuse in commit share. [1]

Do not invent evacuation sites or hotlines in the anecdote. Do not ask an LLM to "verify then post." If the pack is empty, refuse the rumor and point to [[act-launch-the-desk]]; do not mint a token from the seminar.

## When It Breaks

- **Kit mints or looks like mint.** A facilitator QR, handout, or "share this slide" is treated as SK-official. RFC forbids that path. [3]
- **Participant pressured to post.** Youth are asked to publish from the SK Page "so the session counts." That is not Act. That is using minors as a Page workforce. See Ethical Caution.
- **Guild chrome as government.** Seekers Guild logo, UNESCO badge, or camp hashtag is shown as if it were SK voice. Guild is not the Page brand. [2]
- **Auto-share / agent mint.** A helper or bot posts without the human commit. Abuse path: 403; official share stays human. [1][3]
- **Draft or unpublished pack.** Leader tries `canon_share` on draft. Denied; no token. [1]
- **Trust-nothing close.** Facilitator ends with "never believe anyone." Culver's risk: you erode the fifth estate and the desk you came to make executable. [5]
- **45-minute honesty.** One Act drill does not produce ethical sharers for the next typhoon. Do not sell the slot as MIL competence.
- **Proof gap.** In-app `canon_share` is not yet proof the Page post went out (Scrutiny G-7 / PRD open question). Teach the in-app commit as the product event. Do not claim Meta receipt.

## Hidden Assumptions

1. **A published canon pack exists** if anyone will mint official share. Practice refuse does not require mint. Confirm-share does. Empty allowlist is not a truth machine ([[not-in-pack-not-official]], [[act-launch-the-desk]]).
2. **Leader identity is real.** Role comes from session, not a body field named `role`. Camp "let the youth click" does not mint if they are readers. [1]
3. **Official** means SK/LGU voice via Pollux commit share, not every true sentence on earth, and not Guild or UNESCO speech.
4. **Refuse is available without humiliation.** If refuse is treated as failing the camp, people will share to perform loyalty.
5. **Ethical share is not "trust nothing."** The desk is a source that can be named, versioned, and refused when the rumor is off-pack. [5]
6. **Page post is a separate human act.** Copying the official URL still requires the officer's Page. The product must not auto-post.

## Application

**Facilitator**

- Sequence: pause, then allowlist, then this Act. Do not skip to "share for likes."
- Split roles out loud: "Participants practice refuse. Only a leader with a published **canon** pack can mint official share. This kit session never mints."
- Demo confirm only on a published canon pack (or a clearly labeled demo org). Show the pause fields, then `canon_share` and copy URL. Do not post from a youth phone to the SK Page.
- Demo refuse on a **quarantine / not canon** rumor. If you have leader access, show `canon_refuse` on the canon desk. If you only have the kit, practice the script and say the event is not written.
- Taglish cue: "Share ethically dito ay human commit. Hindi auto-post. Hindi kit badge."
- Close optional walk: if they later act as leader, [[act-launch-the-desk]] then F10. Completing this module is not required to launch. [1]
- Record kit module opens if a session exists. Never treat them as north star.

**Participant**

- Before forwarding anything that looks like SK: pause, check the pack, then share only if you are the officer **and** the item is in the published canon pack **and** you are willing to put your desk's name on it.
- If you are not the officer: refuse-forward. Tell the desk. Do not impersonate SK. Do not paste Guild or camp logos as official.
- Funny meme that is off-pack: still an ethical choice. Refuse is allowed. [5]

## Ethical Caution

Do **not** pressure youth to post from the SK Page so the camp looks successful. Under-18 attendance at real camps is in CLR scope; public school/LGU camp launch remains blocked until counsel on age gate and consent. Minimize participant PII. Do not collect student names in v1 session tables.

Seekers Guild logo, Pollux chrome, and UNESCO mention are **not** government voice. Do not put Guild sigil on official share screens or Page posts as if it were SK.

Do not mock people who forwarded the rumor. Volume is the environment. Refuse the stamp; do not humiliate the neighbor.

Do not use this module to hide bad news. True updates belong in a new published canon version, then a human commit.

Kit text is not crisis canon. Do not recite hotlines from the handout. If someone is in distress, stop the exercise and follow the host organization's human process. No LLM. No scrape.

Do not claim UNESCO certification or that a short outreach slot produces MIL competence. Do not sell the session.

## Related

- [[pause-before-share]] (Analyze: who made this, why, is it in the pack)
- [[not-in-pack-not-official]] (Reflect: allowlist, not a fact-check oracle)
- [[act-launch-the-desk]] (Act: clone, fill, publish so there is something honest to share; never a launch gate)

## Sources

1. **[Derived / Internal]** Pollux PRD. *PRD-F10 human commit share; US-05 official share or refuse (`canon_share` / `canon_refuse`, no token on refuse, no LLM); US-10/US-11 kit events do not replace north star and kit does not mint official share; north star table.* [docs/prd-pollux.md](../../prd-pollux.md). *Verified 2026-08-16: file in repo; Draft. Canonical acceptance for this module.*
2. **[Derived / Internal]** Pollux IDEA. *UNESCO MIL as product behavior: share ethically = human commit, refuse-forward first-class, no auto-post; Guild not the SK Page; launch-without-us not blocked on the kit.* [docs/idea-pollux.md](../../idea-pollux.md). *Verified 2026-08-16: file in repo; Draft. Product lock, not a field trial of ethical-share training.*
3. **[Derived / Internal]** Pollux RFC-001. *Kit cannot mint `canon_share`; MintShareLink / commit share reject `pack_kind = 'outreach_kit'` (403); no share_links from StartKitSession or PrintKitPacket; human principal for publish and official share.* [docs/rfc-pollux-channel-packs.md](../../rfc-pollux-channel-packs.md). *Verified 2026-08-16: file in repo; Draft. Hard bans this module must not violate in facilitation.*
4. **[Primary / Programme]** UNESCO, *Media and Information Literacy* programme page (already cited in IDEA). https://www.unesco.org/en/media-information-literacy. *Cited in docs/idea-pollux.md (research input 2026-08-15). Fetched 2026-08-16: page includes the figure that 2/3 of digital content creators do not systematically fact-check before sharing (UNESCO, 2024). Use for the public MIL frame (ethical share, safer use). Do not stretch into a claim that UNESCO endorsed Pollux's commit-share schema.*
5. **[Input / Mentorship]** Sherri Hope Culver, Temple University / CMIL / Global MIL Alliance, 2 July 2026 session notes. *Ethical awareness as daily digital choice; warning against "don't trust any source" as a fact-check slogan; NAMLE Act as part of media literacy.* [docs/mentorship-july-2.md](../../mentorship-july-2.md). *Verified 2026-08-16: file in repo; Input. Session pedagogy, not a Pollux efficacy study.*
6. **[Input / Mentorship]** DW Akademie AACRA via Pollux notes, 1 July 2026. *Act: informed, ethical media habits; Akosua / Act hero; closing "we choose" with purpose and care.* [docs/mentorship-july-1.md](../../mentorship-july-1.md). *Verified 2026-08-16: file in repo. Session pedagogy.*
