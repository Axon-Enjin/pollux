---
title: Access the pack
type: concept
domain: outreach-kit
tags: [outreach-kit, mil, unesco]
related:
  - "[[pause-before-share]]"
  - "[[not-in-pack-not-official]]"
confidence: high for "every official item names publisher/date/version"; medium for mapping that product rule onto UNESCO programme wording beyond "check sources / know the source"
source_tier: mixed
created: 2026-08-16
---

# Access the pack

> Official information is usable when you can name the publisher, the date, and the version. Access is finding that labeled pack, not trusting fluent text that arrived first.

## Definition

**Access the pack** is the first outreach-kit module. Participants learn where SK-official facts live: a published content pack whose items carry provenance (who published, when, which version, and why the item is in the pack).

In Pollux this is the UNESCO MIL goal **know the source**, made concrete. It is also AACRA **Access**: using media to receive messages and knowing where to find information, including noticing that algorithms and chat forwards are not a catalog.

Access is not "search the web until something looks official." Crisis and MIL facts on the desk come only from a published **canon** pack (`status = published`, `pack_kind = canon`) at a pinned version. This seminar module is itself from a published **outreach_kit**. Kit copy is facilitator material. It is not SK-official crisis canon.

## Why It Works

Fluent rumors win because they arrive first and look like government voice. Provenance is slower and less shareable, which is why it has to be taught as a habit, not hoped for.

Naming publisher, date, and version does three jobs:

1. **Findability.** Participants know the desk exists (PWA, paper card, or a share that pins version). They stop treating the group chat as the archive.
2. **Comparability.** A screenshot with no version cannot beat pack version 2 published this morning.
3. **Refusal setup.** Once people can see the label, the next modules can ask "is this in the pack?" and "should we share it as official?"

The product does not race AI volume with a fact-check model. Access works because the allowlist is small and labeled. Fluency is not evidence.

## Evidence & Origins

UNESCO's Media and Information Literacy programme frames MIL as critical thinking, checking sources, using media safely, sharing ethically, and fairer public talk. Pollux maps **know the source** to publisher, date, version, and why the item is in the pack ([idea-pollux.md](../../idea-pollux.md) UNESCO MIL table; [research-pollux-unesco-proposal-2026.md](../../research-pollux-unesco-proposal-2026.md)).

That mapping is a product behavior, not a claim that UNESCO wrote Pollux's schema. Confidence is **high** that every official item must name publisher, date, and version. Confidence is **medium** if a facilitator stretches UNESCO programme language into extra competencies this module does not own.

Pack confinement makes provenance executable: publish stamps `version`, `published_at`, and `published_by`; share links pin `pack_id` + `pack_version`; items may carry `source_label` (and optional `source_url` that is not fetched at answer time). Draft and in_review stay quarantine: invisible to learners and to public share tokens ([rfc-pollux-channel-packs.md](../../rfc-pollux-channel-packs.md)).

Mentorship 1 July 2026 (Lizette Ferris, DW Akademie): AACRA **Access** is using media technology to receive messages and knowing where to find information. In AI-shaped chats, access also means noticing automated filtering. Andre (Access hero) is the story cue: reliable information beyond the algorithm, not "the model told me."

## Worked Example (barangay flood pack)

**Setting:** Youth camp or barangay hall. Facilitator has a published `outreach_kit` session. Nearby, the SK desk has (or pretends to have) a published **canon** flood pack, e.g. slug `barangay-flood-routes`, version 2, `published_at` shown on the pack detail screen. Kit and canon are two allowlists. Do not mix them.

**Activity (about 10 minutes, not a scored game):**

1. Show the pack header: org or SK as publisher, date, version. Ask: "If this were official, what three labels must you see?"
2. Open one pack item (a route or FAQ). Read `source_label` aloud. Ask why it is in the pack (local mandate, not because it trended).
3. Contrast with a **quarantine / not canon** anecdote:

> **Quarantine / not canon.** A chat forward shows a colorful "evacuation map" with no publisher, no date, and no version. Someone says an AI chatbot confirmed the arrows. Do not treat this map as SK-official. Do not invent evacuation sites, contacts, or crisis numbers from the anecdote. The point is the missing labels, not geography.

4. Participants practice: "I can access official flood facts at [pack title], version N, published [date]." If 3G dies, the print packet still shows those labels. The print QR is not a second government identity.

No real hotlines. No LLM-generated "facts" in the example. Completing this beat does not make anyone media-literate for the next typhoon. It only installs the find-the-label move.

## When It Breaks

- **Labels missing or fake.** A Page post or screenshot claims to be SK-official but has no pack version. Access has nowhere to land.
- **Draft treated as live.** Facilitators demo an unpublished pack. Learners learn the wrong catalog.
- **Kit leaked into crisis.** Someone answers "where do we go?" from this module's handout. Kit items cannot satisfy crisis `GetPackItem`.
- **Version drift.** A later edit is described as "the same pack" without bumping version. Share tokens that pin an old version then disagree with the screen.
- **Algorithm as catalog.** "It was on top of my feed" replaces publisher/date/version.
- **LLM restatement.** A helper paraphrases pack text without citing item and version. That is not access; it is fluency again.
- **Session overclaim.** A 45-minute barangay format (`barangay_45m`) is a facilitation slot. It does not fix MIL.

## Hidden Assumptions

- Someone actually published a canon pack with honest `published_by`, `published_at`, and `source_label`. Empty templates are not sources.
- Participants can read the three labels (literacy, contrast, language). If not, the facilitator must speak them, not skip them.
- Publisher means the SK or LGU desk that owns the pack, not Seekers Guild and not UNESCO.
- "Date" means publish time of this version, not the rumor timestamp in the chat.
- Access assumes a known place (PWA, paper card, pinned share). It assumes the firehose is not the library.
- AACRA Access includes "where to find information." It does not require Pollux to teach general web search or AI-tool literacy in this module.

## Application

Facilitator checklist for this module:

- Open only a published `outreach_kit` for notes and activities.
- Point at a published **canon** pack (or a clearly labeled demo) to show publisher, date, version on every official item.
- Ask the three-label question before any share discussion ([[pause-before-share]]).
- Keep the fake-map story in **quarantine / not canon**. Route "is this official?" to [[not-in-pack-not-official]].
- On paper: print pack title, version, date. No improvised contact lists.
- Record `kit_module_opened` if a session is running. Do not mint `canon_share` from the kit.
- Close the beat: "Access is the labeled pack. Next we pause before we treat anything as official."

## Ethical Caution

This module teaches finding labeled official text. It does not authorize facilitators to recite crisis procedures, invent contacts, or promote hotlines as pack facts. If a participant is in distress, stop the exercise and follow the host organization's existing human process. Do not ask an LLM. Do not scrape the web.

Kit text must never be presented as SK-official. Dual allowlists exist so seminar copy cannot become government voice. Do not sell the session. Do not claim UNESCO certification. Do not claim a short outreach slot produces MIL competence.

## Related

- [[pause-before-share]] (think critically: who made this, why, is it in the pack)
- [[not-in-pack-not-official]] (spot falsehoods without a fact-check model)

## Sources

- [Primary] UNESCO, Media and Information Literacy programme page, https://www.unesco.org/en/media-information-literacy. Verified as the programme URL already cited in-repo (`idea-pollux.md`, `research-pollux-unesco-proposal-2026.md`). Used here for the public MIL frame (critical thinking, source-checking, safe use, ethical share, fairer public talk), not as a schema spec. Pollux's "publisher, date, version" line is the product mapping of "know the source," stated with medium confidence as UNESCO wording.
- [Expert] `docs/idea-pollux.md` UNESCO MIL table (know the source → publisher, date, version, why the item is in the pack) and `docs/rfc-pollux-channel-packs.md` plus `docs/sdd-pollux.md` pack provenance (`version`, `published_at`, `published_by`, `source_label`, version-pinned shares, dual allowlists, draft quarantine). Verified in-repo on 2026-08-16.
- [Input] `docs/mentorship-july-1.md` Lizette Ferris / DW Akademie AACRA **Access** (1 July 2026): receive messages and know where to find information; AI-shaped access notices filtering. Supporting color from `docs/research-pollux-agent-era-mil.md` (Lizette: AACRA wheel). Mentorship notes, not DW publication text.
- [Input] `docs/research-pollux-unesco-proposal-2026.md` and `docs/prd-pollux.md` US-10 (PRD-F15 module name `access-the-pack`). Proposal/product input; not a UNESCO award.
