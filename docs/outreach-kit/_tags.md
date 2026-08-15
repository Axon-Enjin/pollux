---
title: Outreach kit controlled tags
type: taxonomy
domain: outreach-kit
tags:
  - outreach-kit
aliases:
  - F15 tags
  - kit taxonomy
related:
  - README
  - _STACK
confidence: high
source_tier: T0
created: 2026-08-16
---

# Outreach kit controlled tags

> Tiny vocabulary. Domain tag first. Do not mint tags freely.

Every note in `docs/outreach-kit/` must put `outreach-kit` first in `tags`. Add further tags only from the closed list below. If a sibling module wants a new tag, change this file first; do not invent a tag in the note.

Anatomy: [[README]]. Sequence: [[_STACK]].

## Closed list

| Tag | Meaning in this vault | Typical on |
|-----|----------------------|------------|
| `outreach-kit` | Domain. Required first tag. PRD-F15 authoring home. | Every note |
| `mil` | Media and information literacy pedagogy (UNESCO goals as Pollux reads them). | Concept modules, stack |
| `aacra` | Access / Analyze / Create / Reflect / Act mapping. | [[_STACK]], concept modules |
| `unesco` | Alignment to the in-repo UNESCO MIL programme citation. Not a claim of UNESCO endorsement. | Stack, concept notes that cite T1 |
| `facilitator` | Facilitator-only material or cues. | [[3ds-run-of-show]], [[facilitator-one-pager]], notes with `facilitation_note` |
| `print` | Print packet copy. | [[facilitator-one-pager]], [[learner-handout]], [[consent-checklist]] |
| `canon` | Contrast with SK live canon (`pack_kind = canon`) or "this kit is not canon." | Notes that teach pack vs rumor |
| `quarantine` | Draft, unpublished, or worked-example rumor. Label rumors quarantine / not canon. | Worked examples, ethical caution |
| `principal` | Human remains principal for publish and official share. | [[ethical-share-or-refuse]], [[act-launch-the-desk]], [[ai-does-not-know]] |

## Assignment cheat sheet

| Slug | Tags (after `outreach-kit`) |
|------|-----------------------------|
| [[access-the-pack]] | `mil`, `aacra`, `canon` |
| [[pause-before-share]] | `mil`, `aacra` |
| [[not-in-pack-not-official]] | `mil`, `aacra`, `canon`, `quarantine` |
| [[ai-does-not-know]] | `mil`, `aacra`, `principal` |
| [[ethical-share-or-refuse]] | `mil`, `aacra`, `principal`, `canon` |
| [[act-launch-the-desk]] | `mil`, `aacra`, `principal` |
| [[3ds-run-of-show]] | `facilitator` |
| [[facilitator-one-pager]] | `facilitator`, `print` |
| [[learner-handout]] | `print`, `mil` |
| [[consent-checklist]] | `print`, `facilitator` |
| This file | (domain only) |
| [[README]], [[_STACK]] | as needed from the closed list; still first tag `outreach-kit` |

Do not add: `game`, `f12`, `sk-page`, `guild`, `crisis`, `telegram`, `coach`, `lesson`, `score`. Those ideas belong in conflation prose ([[README]]), not as tags.

`unesco` is optional on concept notes. Use it when the note cites the T1 programme page. Do not use it as a prestige stamp.

## Front matter reminder

```yaml
tags:
  - outreach-kit
  - mil
```

Wrong: putting `mil` first. Wrong: `outreach_kit` (underscore is the **database** `pack_kind`, not a tag). Wrong: `#quarantine` in the body as a substitute for the YAML tag plus an explicit "quarantine / not canon" sentence on rumor text.

## Related

- [[README]]
- [[_STACK]]

## Sources

1. [T0] Worker lock: keep vocabulary tiny; domain tag first; listed tags only. Verification: this file is the list.
2. [T0] PRD-F15 / RFC dual allowlist language (`canon` vs `outreach_kit`). Verification: `docs/prd-pollux.md`, `docs/rfc-pollux-channel-packs.md`.
3. [T1] UNESCO MIL programme page already cited in Pollux (for the `unesco` and `mil` tags). https://www.unesco.org/en/media-information-literacy
4. [T2] AACRA naming. Verification: `docs/mentorship-july-1.md`.
