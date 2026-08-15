---
title: Pollux campaign kit (product home)
type: spine
domain: outreach-kit
tags:
  - outreach-kit
  - mil
  - facilitator
aliases:
  - PRD-F15 kit README
  - outreach-kit anatomy
  - DIY campaign kit
related:
  - _STACK
  - _tags
  - access-the-pack
  - pause-before-share
  - not-in-pack-not-official
  - ai-does-not-know
  - ethical-share-or-refuse
  - act-launch-the-desk
  - 3ds-run-of-show
  - facilitator-one-pager
  - learner-handout
  - consent-checklist
confidence: high
source_tier: T0
created: 2026-08-16
---

# Pollux campaign kit (product home)

> Pollux is the open campaign kit an SK officer runs herself: modules, a program guide, and a site students return to after. Not crisis canon. Not a scored game.

This folder is the **v1 product home**: a DIY campaign kit (PRD-F15). An officer prints the packet, runs the 3Ds session, and points youth at the published kit site afterward. Desk / F3 is an optional later walk. It is not why this kit exists.

Product lock for dual allowlist, kit APIs, and camp rules still lives in the PRD, SDD, RFC, and CLR. Notes here are human-authored modules and print copy. They are not Sangguniang Kabataan official crisis facts. They do not score anyone.

Entry is [[00-INDEX]], this README, [[_STACK]], and [[_tags]]. Wikilink by slug.

## Scope

| In | Out |
|----|-----|
| DIY campaign kit: six modules, 3Ds program guide, print packet, site youth return to | Scored inoculation drill (PRD-F12) |
| Facilitator notes, participant-safe copy, 3G print | Crisis facts, routes, contacts, FAQ from `pack_kind = canon` |
| Published `outreach_kit` item kinds only | Minting `canon_share` from a kit path |
| Optional later walk into F3 desk or F10 refuse | Treating F3 self-launch as the reason this kit exists |
| Stage-0 honesty: a 45-minute session does not solve disinformation | Companion, fact-check LLM, open-web RAG, Guild-as-SK-Page |

**v1 product.** Completing the kit never gates a canon publish. Module 6 never requires a desk in the hall.

## Vault anatomy

Every note in this folder uses YAML front matter, then a body. Required keys:

| Key | Rule |
|-----|------|
| `title` | Human title. English spec language. |
| `type` | One of: `spine`, `stack`, `taxonomy`, `concept`, `instrument`, `print`. |
| `domain` | Always `outreach-kit`. |
| `tags` | First tag is `outreach-kit`. Then only tags listed in [[_tags]]. Do not mint tags freely. |
| `aliases` | Optional search names. |
| `related` | Slugs, not paths. Same as wikilinks. |
| `confidence` | `high` (product lock), `medium` (pedagogy mapping), `low` (illustrative only). |
| `source_tier` | `T0` product lock, `T1` UNESCO programme page already cited in this repo, `T2` Pollux research or mentorship input, `T3` worked example (quarantine rumor). |
| `created` | ISO date. Kit authoring batch uses `2026-08-16`. |

**Source URL rule:** numbered Sources may include a URL only if it already appears in Pollux docs or is the UNESCO Media and Information Literacy programme page already cited in-repo. Do not fetch or invent new web citations here.

**Prose rule:** English spec language. No em-dashes. Taglish is allowed only in Application facilitator/participant cues.

### Note types

| `type` | Who writes it | Body |
|--------|---------------|------|
| `spine` | This README | Product home, anatomy, conflation table, conventions. |
| `stack` | [[_STACK]] | Sequence table and print list. |
| `taxonomy` | [[_tags]] | Closed tag list. |
| `concept` | The six AACRA sequence modules | **Must** follow the concept body order below. Do not rewrite modules from this spine unless a dedicated pass says so. |
| `instrument` | [[3ds-run-of-show]] | Facilitator timing and agenda (Document / Demonstrate / Duplicate). Not a participant lesson. Not scored. |
| `print` | [[facilitator-one-pager]], [[learner-handout]], [[consent-checklist]] | Print-ready packet copy. No PII. Consent is a counsel stub, not a legal form (CLR). |

### Concept note body order

Sibling `concept` modules must use this order so the pack assembler can stay dumb:

1. `# Title` plus a one-sentence essence as a blockquote
2. `## Definition`
3. `## Why It Works`
4. `## Evidence & Origins` (inline `[n]` matching Sources)
5. `## Worked Example` (camp or barangay. Label rumor text **quarantine / not canon**)
6. `## When It Breaks`
7. `## Hidden Assumptions`
8. `## Application` (facilitator + participant. Taglish cues OK **here only**)
9. `## Ethical Caution`
10. `## Related` (wikilinks to slugs)
11. `## Sources` (numbered, tiered, verification note; URL only per the source URL rule)

Do not skip a heading. If a section has nothing honest to say, write one Stage-0 sentence (for example, that a 45-minute block does not close the firehose).

### Wikilinks

Use slugs in `[[double brackets]]`:

- Sequence: [[access-the-pack]] [[pause-before-share]] [[not-in-pack-not-official]] [[ai-does-not-know]] [[ethical-share-or-refuse]] [[act-launch-the-desk]]
- Instrument: [[3ds-run-of-show]]
- Print: [[facilitator-one-pager]] [[learner-handout]] [[consent-checklist]]
- Spine: [[_STACK]] [[_tags]]

## Sequence (AACRA x UNESCO MIL)

Canonical order and UNESCO mapping live in [[_STACK]]. Summary:

| Order | Slug | AACRA | UNESCO MIL (product reading) |
|-------|------|-------|------------------------------|
| 1 | [[access-the-pack]] | Access | Know the source |
| 2 | [[pause-before-share]] | Analyze | Think critically |
| 3 | [[not-in-pack-not-official]] | Reflect | Spot falsehoods without a fact-check model |
| 4 | [[ai-does-not-know]] | Create-adjacent (agent-era; no companion) | Use media well; fluency is not provenance |
| 5 | [[ethical-share-or-refuse]] | Act | Share ethically |
| 6 | [[act-launch-the-desk]] | Act | Optional later desk walk; **never a launch gate** |

Facilitator instrument (not a participant lesson): [[3ds-run-of-show]] (3Ds).

Print packet: [[facilitator-one-pager]], [[learner-handout]], [[consent-checklist]].

## What not to conflate

| Thing | What it is | What it is not |
|-------|------------|----------------|
| **This kit (v1 product)** | DIY campaign kit an SK officer runs herself. Modules + 3Ds program guide + site students return to. Published as `pack_kind = outreach_kit` | Pedagogy bolted onto a desk. Not F3. Not F12. Not SK-official crisis facts. |
| **PRD-F3 self-launch kit** | Org checklist (create, clone, fill, publish, post, print) plus a **paper card** (URL + QR) for an SK **canon** pack | The v1 product. Optional later walk from module 6. Not MIL session copy. |
| **PRD-F12 inoculation drill** | Optional scored game. Could-Have. Rule engine + `attempts` | The brand. Do not reuse `lessons` / scores / badges for kits. |
| **`pack_kind = canon`** | Crisis facts, routes, contacts, FAQ. Commit-share (`canon_share` / `canon_refuse`) | Kit modules. Kit print. Kit session events. Dual allowlist: crisis SQL must not read kit rows. |
| **`pack_kind = outreach_kit`** | Facilitator material. Optional `kit_sessions`. Print packet if 3G dies | Never mints `canon_share`. RFC dual allowlist keeps canon and kit apart. |
| **Canon vs kit text** | Published canon is live SK voice after a human commit | Kit text stays pedagogy. Fluency in a handout does not make a rumor official. |
| **Canon vs quarantine** | Published, version-pinned, human-approved | Draft / in_review, and any **worked-example rumor** labeled quarantine in concept notes |
| **Seekers Guild** | OSS community that stewards contribution | Not the SK Page brand. Not the barangay voice. Not required to run the kit. |
| **Principal** | Human officer for publish and official share | Model, helper draft, Guild, or kit runner |

Kit events (`kit_session_started`, `kit_module_opened`, `kit_packet_printed`) do not replace north-star `canon_share` / `canon_refuse`.

## Product surfaces (do not author as extra notes)

The officer runs the kit herself: print packet first, then the published kit URL as the site students return to. In-app facilitator cockpit / session runner is a later convenience behind `ENABLE_OUTREACH_KIT` (default off). Flag off is 404, not a silent mix-in of canon facts. Readers see participant-safe items only (no `facilitation_note`).

## CLR under-18 blocker

Product audience includes under-18 camp attendees. Public school or LGU camp launch stays **BLOCKER** until counsel clears age gate, parental consent, and school/LGU rules. Print has no PII. Consent checklist is a stub, not a legal form. v1 session table does not collect student names. Demo persona remains Mia, 19. See [clr-pollux.md](../clr-pollux.md).

## Stage-0 honesty

This kit trains a local habit: know the pack, pause, refuse unofficial fluent text, keep the human as principal. It does not out-check the firehose, certify a camp as "MIL complete," or authorize anyone to speak as SK. A 45-minute block does not solve disinformation. Launching a desk is optional later, not the session's pass/fail.

## Related

- [[_STACK]]
- [[_tags]]
- Product: [prd-pollux.md](../prd-pollux.md) (US-10, US-11), [sdd-pollux.md](../sdd-pollux.md) §3 and §4, [rfc-pollux-channel-packs.md](../rfc-pollux-channel-packs.md), [clr-pollux.md](../clr-pollux.md)

## Sources

1. [T0] Pollux PRD v0.4, PRD-F15, US-10, US-11, screen inventory. Verification: in-repo `docs/prd-pollux.md`. No extra URL.
2. [T0] Pollux SDD dual `pack_kind` and kit APIs. Verification: in-repo `docs/sdd-pollux.md`.
3. [T0] RFC-001 dual allowlist; kit cannot mint share. Verification: in-repo `docs/rfc-pollux-channel-packs.md`.
4. [T1] UNESCO Media and Information Literacy programme page (already cited in IDEA, PRD, GTM, UNESCO proposal). Verification: same URL as existing Pollux citations. https://www.unesco.org/en/media-information-literacy
5. [T2] AACRA labels from UNESCO mentorship notes. Verification: in-repo `docs/mentorship-july-1.md`. Pedagogy mapping to six slugs is medium confidence.
6. [T0] CLR: print has no PII; consent checklist is a counsel stub; under-18 school/LGU camp is BLOCKER. Verification: in-repo `docs/clr-pollux.md`.
