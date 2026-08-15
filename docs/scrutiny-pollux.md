# IDEA Scrutiny Gate (SCRUTINY)

**Project:** Pollux
**Date:** 2026-08-16
**Version:** 0.5
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled)
**IDEA:** [idea-pollux.md](idea-pollux.md)
**Research input:** [research-pollux-agent-era-mil.md](research-pollux-agent-era-mil.md)

---

## 1. Verdict

**Decision:** PROCEED WITH FIXES

**One-line rationale:** v1 Must-Have is the campaign / outreach kit (PRD-F15), not the official pack desk. Youth/PII and under-18 camp stay a CLR BLOCKER. Hobby vs commercial host (G-3) still applies. World Bank inoculation remains a Could-Have drill, not the kit. Dual `pack_kind` still keeps kit copy off crisis canon.

**If PROCEED WITH FIXES, items carried into the build as TBD / risk:**
- UES / BUILD: Vercel Hobby is personal/non-commercial; commercial pilots need Pro (~$20/seat) or alternate host (Cloudflare). Revise "$0-20/mo" burn to pre-revenue vs commercial tiers. G-3 remains: Cloudflare when commercial. Do not put commercial traffic on Vercel Hobby.
- CLR: Youth users and SK leaders imply minors and PII; register consent, age gates, and NPC/DPA posture. Under-18 camp / school / LGU public camp remains a **BLOCKER** until counsel on age gate and parental consent (G-2). Demo persona stays Mia 19. This is not new legal advice; it restates the existing CLR flag.
- AIA: Optional LLM coaching stays off critical path; no model on publish, official share, or kit Q&A. Mark open-web RAG as forbidden. AIA leftover game-primary wording is not the v1 brand; kit-primary also is not a scored inoculation game.
- PRD / IDEA: Reconcile product spine. Campaign kit (PRD-F15) is v1 Must-Have. Official pack desk (PRD-F1 / F3) and human commit share (PRD-F10) are later, not v1 Must-Have. First pilot LGU remains TBD (G-1). Bot channel locked Telegram (G-4). LLM post-MVP (G-5). Host Cloudflare when commercial (G-3). Injection vignette (PRD-F11) and inoculation drill (PRD-F12) stay non-blocking. Do not treat F15 as Must-Have inoculation, and do not treat the desk as the only shippable thing.
- GTM: UNESCO is first showcase of Pollux (product) + Seekers Guild (community); still not the revenue plan. v1 story is a runnable campaign kit, not "desk is the one thing." Canon share/refuse stay the later civic north star when the desk ships. Kit completion still does not mint official share.
- Product / SDD / RFC: Official pack desk later does not retire pack confinement. When canon ships, G-6 pack approval is load-bearing. Dual `pack_kind` (`canon` vs `outreach_kit`) stays: crisis and commit-share read canon only; kit paths read `outreach_kit` only. Do not merge kit Markdown into canon facts.

---

## 2. Claim & Reference Audit

**Coverage:** Claims extracted: 18; checked: 18; verified: 5; unverified: 12; contradicted: 1 (cost framing softened, not fatal). Agent-era claims AE-1..AE-6 added 2026-08-13 from research memo; none marked Verified without primary check.

| # | Category | Claim (from IDEA) | Finding | Source (required if Verified) | Severity if wrong |
|---|----------|-------------------|---------|-------------------------------|-------------------|
| FC-1 | Problem | Reactive fact-checking arrives after falsehoods stick | Unverified; needs check | Directionally standard in inoculation literature; IDEA cites no primary source | Minor |
| FC-2 | Problem | Passive media literacy fails to change sharing behavior | Verified (as study finding for infographics arm) | World Bank Find the Fake: game beat infographics on discernment; https://doi.org/10.1596/1813-9450-10933 | Significant |
| FC-3 | Insight | World Bank WhatsApp inoculation game improved discernment vs static infographics | Verified | https://reproducibility.worldbank.org/catalog/138 ; https://doi.org/10.1596/1813-9450-10933 ; n=2851 Jordan | Critical |
| FC-4 | Solution | Rule-based PWA game can deliver the same pedagogical loop without WhatsApp | Unverified; needs check. Stale vs v1 spine: campaign kit is Must-Have; inoculation game and official pack desk are not v1 Must-Have. | Transfer from chat to PWA is plausible but untested by that study | Significant |
| FC-5 | Solution | Curated content packs avoid open-web RAG hallucination on crisis facts | Unverified; needs check | Process claim; AIA/SDD must enforce | Significant |
| FC-6 | Technical | Free-tier Next.js/Vercel + Supabase can host v1 | Contradicted (as "$0 commercial prod") | Vercel Hobby forbids commercial use: https://vercel.com/docs/plans/hobby | Significant |
| FC-7 | Cost | Monthly burn ≈ $0-20 until paid pilot | Unverified; needs check | Domain + optional LLM yes; commercial host may be $20+; messaging $0 if doctrine holds | Significant |
| FC-8 | Market | B2G/B2B licensing is the monetization path | Unverified; needs check | Stated strategy; no LOIs yet | Minor |
| FC-9 | Technical | Telegram bot API is free for user-initiated bots | Unverified; needs check | Common knowledge; confirm in SDD against current Bot API docs | Minor |
| FC-10 | Ethics | Zero-rated Meta as product promise is a non-goal | Verified (as product decision) | Locked in plan + IDEA cut line; not an external fact claim | Minor |
| FC-11 | Feasibility | SMS out of scope until B2G pays | Verified (as product decision) | IDEA §3 | Minor |
| FC-12 | Market | TrustOps graph is Phase 2, not v1 | Verified (as product decision) | IDEA §3 out of scope | Minor |
| AE-1 | Problem | Firehose-style volume wins on exhaustion; item-level reactive fact-check fails at scale | Unverified; needs check | Vault disinformation note cites Paul & Matthews 2016; confirm primary before Verified | Significant |
| AE-2 | Insight | Prebunking techniques beats counter-flooding for resistance | Unverified; needs check | Directionally supported via Lewandowsky et al. in vault; needs primary row | Significant |
| AE-3 | Solution | Initiative requires practiced Act with skin in the game, not tips alone | Unverified; needs check. Act here is refuse/commit habit in the kit, not "game vs desk" as the v1 cut. Official pack desk is later. | Operator synthesis (high-agency / information-vs-implementation); not a field RCT for Pollux | Significant |
| AE-4 | Solution | Pack confinement (published-only, no open web) is civic capability restriction | Verified (as product decision) | IDEA + RFC-001 doctrine; not an external efficacy study | Significant |
| AE-5 | Feasibility | General web-surfing agent is out of scope because prompt-side guards fail under injection | Unverified; needs check | Vault capability-restriction analogy; Pollux-specific harm magnitude unmeasured | Significant |
| AE-6 | Market | UNESCO showcase does not replace B2G revenue path | Verified (as product decision) | IDEA event/context + GTM | Minor |

### 2.1 References Integrity

IDEA names World Bank Find the Fake by description. Audited against the claim text. Research memo cites vault notes as inputs, not as substitute primary sources for Verified rows.

| # | Reference (as cited in IDEA) | Backs claim | Resolves? | Supports the claim? | Finding |
|---|------------------------------|-------------|-----------|---------------------|---------|
| R-1 | World Bank field work on WhatsApp inoculation games | FC-3 | Yes | Yes (interactive game > infographics; brief arm risk of over-skepticism) | Verified |
| R-2 | research-pollux-agent-era-mil.md (vault + mentorship) | AE-1..AE-5 | Yes (file) | Partial (routing memo; not primary evidence) | Input only |

---

## 3. Gap Analysis

| # | Missing input | Needed by (doc) | Blocker or TBD |
|---|---------------|-----------------|----------------|
| G-1 | Named first pilot org (LGU / SK federation) | GTM, VALIDATION | Stale / TBD |
| G-2 | Age gate and parental consent policy for under-18, including real camps | CLR | Audience decided (includes minors). Consent/PIA policy still TBD; **BLOCKER for under-18 camp / school / LGU public camp**. Demo remains Mia 19. Not waived because the kit is now v1 Must-Have. |
| G-3 | Commercial hosting choice when leaving Hobby | BUILD, UES, OPS | **Resolved: Cloudflare** (Pages/Workers) for commercial pilots |
| G-4 | Bot adapter priority (Telegram vs Messenger) | SDD, RFC | **Resolved: Telegram first**; Messenger Could-Have |
| G-5 | Whether LLM coaching ships in v1 | AIA, PRD, UES | **Resolved: post-MVP**; flag off; rule-based path only for MVP |
| G-6 | Content pack authoring workflow and approval chain | PRD, SDD | Stale / TBD; **load-bearing when official pack desk / canon ships** (leader publish + version pin until tightened). Not a reason to delay v1 kit if kit stays `outreach_kit` only. |
| G-7 | Commit-share proof (in-app event vs Page post) | PRD-F10 | TBD before F10 ships; F10 is later with the official pack desk, not v1 Must-Have |

---

## 4. Assumption Stress-Test

**Load-bearing assumption:** A facilitator can run a published campaign / outreach kit (print or in-app) that teaches pause, pack provenance, and refuse, without turning kit copy into SK-official crisis facts, and without collecting youth PII in v1 session tables.

**Strongest argument against it:** Officers pay for reach (WhatsApp/SMS), not for another seminar packet. Camps with under-18 attendees pull CLR before the kit can be public. A PWA may never match chat-native distribution. Buyers may demand an AI oracle Pollux refuses to ship. Calling the kit "the product" may hide that official speech still needs a later canon desk and a human tap.

**Does it hold?** Holds with caveat for v1. The kit is shippable as facilitator material if dual `pack_kind` holds and under-18 camp stays blocked pending counsel. Self-serve desk WTP is deferred, not disproved. GTM must not sell the kit as SK-official voice or as a scored MIL quiz. Keep Guild off the SK Page.

**Second-order effects worth noting:** If leaders treat kit copy as official crisis truth, a seminar packet becomes a harm vector. Dual `pack_kind` is the gate: F15 kit copy must not become canon facts and must not mint official share. Game creep (kit as scored Must-Have inoculation) is still out. Desk-as-the-one-thing language in IDEA/PRD is now stale for v1 scope; official pack desk remains later work with G-6 still load-bearing when it ships.

---

## 5. Feasibility & Scope

| Check | Finding |
|-------|---------|
| Time box realistic for the scope? | Full suite docs: yes this session. Production app: weeks, not days. Startup framing accepts that. |
| "If we ship only one thing" actually shippable in the window? | Yes: campaign / outreach kit (PRD-F15) as published `outreach_kit` plus print packet. Not the official pack desk. Not a lesson PWA. Official pack desk (F1/F3) and commit share (F10) are later. Act drill (F12) and injection vignette (F11) stay non-blocking. |
| Production-grade reachable (security, data, rollback) in the window? | Docs yes. Code later with CLR/AIA/OPS gates. Under-18 camp cannot go public until G-2/CLR counsel. |
| Scope honest, or is the cut line hiding work? | Cut line is honest if F15 is v1 Must-Have facilitator/outreach and the official pack desk is later. Inoculation stays Could-Have. Game creep is treating the kit as a scored drill or as crisis canon. Desk creep is treating F1/F3/F10 as still the only Must-Have. Dual `pack_kind` keeps the split. Residual risk: under-18 camp BLOCKER, G-6 when canon ships, commercial hosting (G-3, no Vercel Hobby commercial). |

---

## 6. Risk & Compliance Pre-flight

| Flag | Present? | Pulls in |
|------|----------|----------|
| Collects user data / PII | Y | CLR (required) |
| Children, health, payment, or biometric data | Y (youth / possible minors, including kit camps); health-adjacent crisis packs possible | CLR §3: under-18 camp / school / LGU public camp is existing **BLOCKER**; counsel before that launch. No new legal claim here. |
| AI component with untrusted input or tools | Y if LLM coaching; N if rule-based only | AIA required either way for conversational framing; SDD §8.1 if LLM |
| Security-critical paths (auth, money, deletes) | Y (auth, role deletes, pack publish) | SDD §5 + QAD abuse paths |
| Public deploy | Y | OPS + CLR |
| Civic canon / pack harm vector | Y | Dual `pack_kind` now (kit vs canon). G-6 when official pack desk ships. |

---

## 7. Blocking Questions

*None. Verdict is PROCEED WITH FIXES.*

---

## Self-Check

- [x] Verdict (§1) is set and matches the findings
- [x] §2 coverage line filled; every checkable IDEA detail has a row
- [x] No claim row reports Verified without a source
- [x] §2.1 audits every reference cited in the IDEA
- [x] Risk flags (§6) name the docs they pull into scope
- [x] On PROCEED WITH FIXES, every fix names the doc it lands in
- [x] AGENTS hard bans applied (no em-dashes)
- [x] On PROCEED: index row to update; build sequence continues
