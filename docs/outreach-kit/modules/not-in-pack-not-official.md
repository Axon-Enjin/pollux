---
title: Not in the pack, not official
type: concept
domain: outreach-kit
tags: [outreach-kit, mil, aacra, unesco, canon, quarantine]
aliases:
  - "allowlist not oracle"
  - "spot fake news as product"
  - "published pack is live canon"
related:
  - "[[access-the-pack]]"
  - "[[ethical-share-or-refuse]]"
  - "[[act-launch-the-desk]]"
confidence: medium
source_tier: mixed
created: 2026-08-16
---

# Not in the pack, not official

> If it is not in the published canon pack, it is not SK-official. Spotting falsehood is an allowlist, not a fact-check LLM.

## Definition

**Not in the pack, not official** is Pollux's product form of UNESCO "spot fake news" and AACRA **Reflect**. You do not ask a model whether a rumor is true. You ask whether the claim sits on the **canon allowlist**: `pack_kind = 'canon'` and `status = 'published'`, at a pinned version, with item kinds `fact|route|contact|faq|media`. [1][2]

Two published buckets exist. They are not one truth pile. [2]

| Allowlist | What it is | Counts as SK-official crisis fact? |
|-----------|------------|-------------------------------------|
| **Canon** (`pack_kind = 'canon'`, published) | Live civic pack the desk filled and published | Yes, after a human commit share |
| **Outreach kit** (`pack_kind = 'outreach_kit'`, published) | Facilitator modules, agendas, handouts | No. Kit text is not crisis canon |
| **Draft / in_review** | Work in progress | **Quarantine / not canon.** Invisible to learners and share tokens |

**Oracle** here means a system that answers "is this true?" from fluency, the open web, or an LLM. Pollux refuses that job. **Allowlist** means absence of tools: crisis reads hit published canon SQL, or they refuse. [2][3]

Reflect, in the DW Akademie AACRA wheel, is critical self-examination of sources used and of the impact a post can have. [5] In Pollux that self-check is operational: "Would I stamp this as SK-official? Is it in the published pack?"

## Why It Works

Item-level reactive fact-check cannot race volume. Fluency is cheap. Official voice should not be. [3]

The allowlist works as **capability restriction**, not as a smarter chatbot:

1. **Pasteability is earned by provenance.** Published pack items are live canon. Drafts, rumors, and kit copy stay quarantine until a human publish (and, for official voice, a human commit). [2][3]
2. **Gates beat advice.** A prompt that says "do not invent facts" lives inside the thing being restrained. SQL and service filters do not. [2][3]
3. **Reflect stays human.** The officer still decides impact (who sees this, what happens if we are wrong). The product only answers membership: in the published canon pack, or not.

This is a **product decision** (AE-4: pack confinement as civic restriction). It is not an external efficacy study proving that allowlists stop disinformation in the wild. Treat causal "this module defeats the firehose" as **Unverified** (AE-1 still needs a SCRUTINY primary-source row). Confidence on those causal claims stays **medium**. [3]

## Evidence & Origins

UNESCO MIL names "spot fake news" as a programme goal. Pollux maps that goal to product behavior, not to a quiz: if it is not in the published pack, it is not official; no fact-check model. [1][4]

RFC-001 makes the map executable. Crisis UI and bot fact replies resolve only to published **canon**. Kit catalog/run/print resolve only to published **outreach_kit**. Kit items cannot satisfy `GetPackItem`. Kit sessions cannot mint `canon_share`. Draft and in_review remain quarantine. Hard ban: open-web RAG and LLM generation of crisis facts. [2]

The agent-era memo states the same split as doctrine: published pack = live canon; draft = quarantine; no open-web or LLM crisis answers; enforce in SQL and service, not in a system prompt. It also records AE-1 (item-level fact-check fails at scale) as not Verified until SCRUTINY checks primary sources, and AE-4 as Verified **as a decision**, not as measured field effect. [3]

DW Akademie AACRA **Reflect** is the session pillar: examine sources and impact before communication. This module is that pillar as a gate, not as a journal prompt alone. [5]

## Worked Example

Youth camp, flood barangay. A volunteer holds up a phone: a fluent **fake evacuation map** in the group chat. Arrows look official. It has been forwarded twelve times.

Facilitator (not a truth oracle): "Hindi natin tatanungin ang AI kung totoo ito. Titingnan natin ang published canon pack."

Steps:

1. Open the SK canon pack (published, version pinned). Search evacuation / mapa / evacuation center. See [[access-the-pack]] for publisher, date, version.
2. The fake map is **not** an item in that pack. Label it **quarantine / not canon**. It is not SK-official, even if it looks government-made.
3. Do **not** run it through a fact-check LLM. Do **not** paste kit handout text as if it were the evacuation map.
4. If the real map **is** in the published pack, the officer walks [[ethical-share-or-refuse]] and may commit-share the official item. If the pack has no map because nobody filled and published one, refuse the rumor **and** do not invent a substitute. Empty pack is not a truth machine. See Hidden Assumptions and [[act-launch-the-desk]].

Participant takeaway: "Wala sa published pack = hindi official. Quarantine / not canon hangga't wala sa live canon."

## When It Breaks

- **Empty or unpublished pack.** Allowlist of nothing is silence, not truth. Officers may feel pressure to "just confirm" from memory or ChatGPT. That is the oracle path. Refuse, then fill and publish.
- **Wrong allowlist.** A published `outreach_kit` module about maps is still **not** the crisis map. Treating kit copy as SK-official launders facilitator text into government voice. [2]
- **Draft mistaken for live.** In_review items feel almost done. They stay **quarantine / not canon** until publish. [2][3]
- **Over-skepticism.** "Not official" is not "proven false." The fake map might accidentally match reality. Pollux still will not stamp it SK-official. Teach that distinction so the session does not become "everything is fake." [3]
- **45-minute camp honesty.** One Reflect drill does not drain the firehose. AE-1 remains Unverified as a causal product claim. Do not sell the module as a disinformation vaccine. [3]
- **Stale publish.** An old published version can be wrong about tonight's water. Version pin is honesty about *which* official text you shared, not a guarantee the river stayed put. Update via a new published version, not by improvising off-pack.

## Hidden Assumptions

1. **Someone actually filled and published the canon pack.** The rule "not in pack, not official" only protects the public if live canon exists. An empty published shell, or a pack that never left draft, is not a truth machine. Launch is a separate Act ([[act-launch-the-desk]]), not a side effect of this module.
2. **Publishers are accountable humans.** Allowlist membership is not omniscience. A published lie is still a published lie. Pack approval chain (Scrutiny G-6) stays open in product docs; this note does not close it.
3. **Learners can reach the pack** (PWA, print card, or a leader holding the phone). If the pack is unpublished to "keep it safe," Reflect has no object.
4. **Official** here means SK/LGU voice via Pollux commit share, not every true fact in the universe.

## Application

**Facilitator**

- Put the published canon pack on the table (phone or print). Name pack_kind: this is **canon**, not the seminar kit.
- Cue: "Spot fake news dito ay allowlist, hindi oracle. Walang fact-check LLM."
- Run one rumor (fake map or similar). Chorus: "Nasa published pack ba? Hindi? Quarantine / not canon. Huwag i-share as SK-official."
- If someone asks the model, stop the demo. Show refuse. Do not score the rumor as a game (that is PRD-F12, not this kit).
- Close with who can publish and who can commit-share. Point to [[ethical-share-or-refuse]] and, if the pack is empty, [[act-launch-the-desk]].

**Participant**

- Before resharing anything that looks like SK: open the pack, check membership, check version.
- Taglish check: "Official ba talaga, o fluent lang?" Fluent + repeated is weak evidence. [3]
- If it is missing: do not invent; do not ask AI to "verify"; label **quarantine / not canon**; tell the officer.
- If it is present: still pause on impact (Reflect), then share or refuse as a human.

## Ethical Caution

Refusing a rumor is not the same as proving it false. Do not mock people who forwarded the fake map; volume and repetition are the environment, not a moral IQ test. [3]

Do not use this module to hide bad news. Adverse true updates belong in a **new published canon version**, not in a private chat while the old pack stays live.

Kit sessions must not mint official share. Facilitators must not paste outreach-kit lines into the Page as crisis facts. [2]

Youth PII and under-18 public launch stay under CLR. This note does not authorize scraping chats to "catch fakes."

## Related

- [[access-the-pack]]: know publisher, date, version before you treat an item as source
- [[ethical-share-or-refuse]]: human commit; refuse-forward is first-class
- [[act-launch-the-desk]]: clone, fill, publish so the allowlist is not empty

## Sources

1. **[Derived / Internal]** Pollux IDEA. *UNESCO MIL as product behavior; "Spot fake news" maps to published pack only, no fact-check model; fake-map success line.* [docs/idea-pollux.md](../../idea-pollux.md). *Verified 2026-08-16: file in repo; Draft. Product lock for this module's one-liner. Not a field evaluation of allowlists.*
2. **[Derived / Internal]** Pollux RFC-001. *Dual allowlist (`canon` vs `outreach_kit`); published-only reads; draft = quarantine; kit cannot satisfy crisis GetPackItem or mint canon_share; no RAG/LLM crisis facts.* [docs/rfc-pollux-channel-packs.md](../../rfc-pollux-channel-packs.md). *Verified 2026-08-16: file in repo; Draft. Canonical confinement rules this note teaches.*
3. **[Derived / Internal]** Research memo, Agent-era MIL. *Published pack = live canon; draft = quarantine; no LLM oracle; AE-1 Unverified until SCRUTINY primary check; AE-4 Verified as decision, not efficacy study.* [docs/research-pollux-agent-era-mil.md](../../research-pollux-agent-era-mil.md). *Verified 2026-08-16: file in repo; Input, not Locked. Causal product claims kept at medium confidence per AE table.*
4. **[Primary / Programme]** UNESCO, *Media and Information Literacy* (programme page already cited in IDEA). https://www.unesco.org/en/media-information-literacy. *Cited in docs/idea-pollux.md (research input 2026-08-15). Use for MIL goal names (including spotting falsehoods / source-checking). Do not stretch programme copy into a claim that UNESCO endorsed Pollux's allowlist design.*
5. **[Derived / Mentorship]** DW Akademie AACRA wheel via Pollux notes. *Reflect: examine sources used and impact of communication; AACRA in AI-shaped contexts.* [docs/mentorship-july-1.md](../../mentorship-july-1.md). *Verified 2026-08-16: file in repo. Session pedagogy; not a Pollux efficacy trial.*
