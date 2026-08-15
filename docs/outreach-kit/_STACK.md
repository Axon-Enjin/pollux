---
title: Outreach kit sequence stack
type: stack
domain: outreach-kit
tags:
  - outreach-kit
  - mil
  - aacra
  - unesco
  - facilitator
  - print
aliases:
  - F15 sequence
  - AACRA stack
related:
  - README
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

# Outreach kit sequence stack

> Six concept modules in fixed order, plus one facilitator instrument and three print artifacts. AACRA x UNESCO MIL mapping is pedagogical, not a second product.

Run this stack as authored. Do not reorder to "make Create stronger." Do not insert F12 scoring between modules. Do not treat module 6 as a launch gate.

Anatomy and conflation rules: [[README]]. Closed tags: [[_tags]].

## Participant sequence

| Order | Slug | `type` | AACRA | UNESCO MIL (Pollux reading) | Pack item kinds (typical) | Launch / share |
|-------|------|--------|-------|-----------------------------|---------------------------|----------------|
| 1 | [[access-the-pack]] | concept | Access | Know the source | module, activity, handout | None |
| 2 | [[pause-before-share]] | concept | Analyze | Think critically | module, activity | None |
| 3 | [[not-in-pack-not-official]] | concept | Reflect | Spot falsehoods without a fact-check model | module, activity, facilitation_note | May preview F10 refuse; does not mint `canon_refuse` |
| 4 | [[ai-does-not-know]] | concept | Create-adjacent (agent-era) | Use media well; fluency is not knowledge | module, activity | No companion. No live agent. |
| 5 | [[ethical-share-or-refuse]] | concept | Act | Share ethically | module, activity | Optional walk into F10 on a **canon** pack later; kit path never mints `canon_share` |
| 6 | [[act-launch-the-desk]] | concept | Act | Local desk as fairer public talk | module, activity, handout | Optional walk into F3 clone, fill, publish. **Never a launch gate.** Kit completion does not block F1/F3. |

UNESCO programme goals cited in Pollux (think critically, spot falsehoods, know the source, use media well, share ethically, fairer public talk) are **gates and fields in the SK flow**, not a MOOC syllabus. This stack is the camp-shaped reading of those goals. It is not SK crisis canon.

**Create-adjacent (row 4):** AACRA Create is not "ship a content studio." Here it means agent-era restraint: do not treat a model as an author of official facts; do not build a companion. Participants may draft only inside pack bounds in later product (PRD-F14). The kit itself does not call a model.

## Facilitator instrument

| Slug | `type` | Role |
|------|--------|------|
| [[3ds-run-of-show]] | instrument | Timed agenda for the facilitator only. Not a participant lesson. Not F12. Not F3 checklist. |

Readers must not receive `facilitation_note` or this instrument in participant view.

## Print packet

Print is the 3G fallback for a published `outreach_kit`. QR may point at the kit URL, or reuse the F3 paper card for a **canon** pack. Print never creates a second official government identity. Print never mixes canon `fact` / `route` / `contact` / `faq` / `media` into kit pages.

| Slug | `type` | Audience | Notes |
|------|--------|----------|-------|
| [[facilitator-one-pager]] | print | Facilitator | Agenda cues, quarantine labels, "not canon" banner. |
| [[learner-handout]] | print | Participant | No facilitator secrets. No crisis hotlines invented in the kit. |
| [[consent-checklist]] | print | Facilitator / org | Stub pointing to counsel. Not a legal form. No student names. No PII on the packet (CLR). |

Pack item kind `handout` and `source` may carry print copy. Kind `agenda` may mirror [[3ds-run-of-show]] once published.

## What this stack is not

- Not PRD-F3 (org checklist + paper card for SK canon).
- Not PRD-F12 (optional scored inoculation drill).
- Not a score, badge, `attempts` row, or `max_score`.
- Not a permit to speak as SK or as Seekers Guild on the SK Page.
- Not a 45-minute solution to disinformation.

## Suggested timing (illustrative, not a promise)

Total about 45 minutes if the facilitator keeps discussion short. Honesty: this clock is for camp logistics, not efficacy.

| Block | Slug | Minutes (illustrative) |
|-------|------|------------------------|
| Open | [[3ds-run-of-show]] cues | 3 |
| 1 | [[access-the-pack]] | 7 |
| 2 | [[pause-before-share]] | 7 |
| 3 | [[not-in-pack-not-official]] | 8 |
| 4 | [[ai-does-not-know]] | 7 |
| 5 | [[ethical-share-or-refuse]] | 7 |
| 6 | [[act-launch-the-desk]] | 6 |

If time dies, cut discussion, not the quarantine label on rumor examples.

## Related

- [[README]]
- [[_tags]]
- [[access-the-pack]]
- [[pause-before-share]]
- [[not-in-pack-not-official]]
- [[ai-does-not-know]]
- [[ethical-share-or-refuse]]
- [[act-launch-the-desk]]
- [[3ds-run-of-show]]
- [[facilitator-one-pager]]
- [[learner-handout]]
- [[consent-checklist]]

## Sources

1. [T0] PRD-F15 module names (names only in PRD; notes authored here). Verification: `docs/prd-pollux.md` US-10. No extra URL.
2. [T0] Kit never blocks launch; optional walk into F3 or F10; kit does not mint official share. Verification: same PRD US-10, US-11.
3. [T0] Dual allowlist and print packet. Verification: `docs/sdd-pollux.md`, `docs/rfc-pollux-channel-packs.md`.
4. [T1] UNESCO MIL programme page already cited in Pollux. https://www.unesco.org/en/media-information-literacy
5. [T2] AACRA wheel (Access, Analyze, Create, Reflect, Act) in mentorship notes. Verification: `docs/mentorship-july-1.md`. Mapping of Create to [[ai-does-not-know]] is medium confidence, product-constrained.
6. [T0] Consent stub and no PII on print. Verification: `docs/clr-pollux.md`.
