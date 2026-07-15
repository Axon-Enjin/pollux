# IDEA Scrutiny Gate (SCRUTINY)

**Project:** Pollux
**Date:** 2026-07-15
**Version:** 0.1
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled)
**IDEA:** [idea-pollux.md](idea-pollux.md)

---

## 1. Verdict

**Decision:** PROCEED WITH FIXES

**One-line rationale:** The wedge is coherent and the World Bank inoculation claim checks out, but bootstrap cost language must reflect Vercel Hobby non-commercial limits and youth/PII compliance before lock.

**If PROCEED WITH FIXES, items carried into the build as TBD / risk:**
- UES / BUILD: Vercel Hobby is personal/non-commercial; commercial pilots need Pro (~$20/seat) or alternate host (Cloudflare). Revise "$0-20/mo" burn to pre-revenue vs commercial tiers.
- CLR: Youth users and SK leaders imply minors and PII; register consent, age gates, and NPC/DPA posture.
- AIA: Optional LLM coaching stays off critical path; rule-based game is primary. Mark open-web RAG as forbidden.
- PRD: First pilot LGU and bot channel (Telegram vs Messenger) remain TBD.
- GTM: UNESCO remains optional distribution, not a revenue plan.

---

## 2. Claim & Reference Audit

**Coverage:** Claims extracted: 12; checked: 12; verified: 4; unverified: 7; contradicted: 1 (cost framing softened, not fatal).

| # | Category | Claim (from IDEA) | Finding | Source (required if Verified) | Severity if wrong |
|---|----------|-------------------|---------|-------------------------------|-------------------|
| FC-1 | Problem | Reactive fact-checking arrives after falsehoods stick | Unverified; needs check | Directionally standard in inoculation literature; IDEA cites no primary source | Minor |
| FC-2 | Problem | Passive media literacy fails to change sharing behavior | Verified (as study finding for infographics arm) | World Bank Find the Fake: game beat infographics on discernment; https://doi.org/10.1596/1813-9450-10933 | Significant |
| FC-3 | Insight | World Bank WhatsApp inoculation game improved discernment vs static infographics | Verified | https://reproducibility.worldbank.org/catalog/138 ; https://doi.org/10.1596/1813-9450-10933 ; n=2851 Jordan | Critical |
| FC-4 | Solution | Rule-based PWA game can deliver the same pedagogical loop without WhatsApp | Unverified; needs check | Transfer from chat to PWA is plausible but untested by that study | Significant |
| FC-5 | Solution | Curated content packs avoid open-web RAG hallucination on crisis facts | Unverified; needs check | Process claim; AIA/SDD must enforce | Significant |
| FC-6 | Technical | Free-tier Next.js/Vercel + Supabase can host v1 | Contradicted (as "$0 commercial prod") | Vercel Hobby forbids commercial use: https://vercel.com/docs/plans/hobby | Significant |
| FC-7 | Cost | Monthly burn ≈ $0-20 until paid pilot | Unverified; needs check | Domain + optional LLM yes; commercial host may be $20+; messaging $0 if doctrine holds | Significant |
| FC-8 | Market | B2G/B2B licensing is the monetization path | Unverified; needs check | Stated strategy; no LOIs yet | Minor |
| FC-9 | Technical | Telegram bot API is free for user-initiated bots | Unverified; needs check | Common knowledge; confirm in SDD against current Bot API docs | Minor |
| FC-10 | Ethics | Zero-rated Meta as product promise is a non-goal | Verified (as product decision) | Locked in plan + IDEA cut line; not an external fact claim | Minor |
| FC-11 | Feasibility | SMS out of scope until B2G pays | Verified (as product decision) | IDEA §3 | Minor |
| FC-12 | Market | TrustOps graph is Phase 2, not v1 | Verified (as product decision) | IDEA §3 out of scope | Minor |

### 2.1 References Integrity

IDEA names World Bank Find the Fake by description without a URL. Audited against the claim text.

| # | Reference (as cited in IDEA) | Backs claim | Resolves? | Supports the claim? | Finding |
|---|------------------------------|-------------|-----------|---------------------|---------|
| R-1 | World Bank field work on WhatsApp inoculation games | FC-3 | Yes | Yes (interactive game > infographics; brief arm risk of over-skepticism) | Verified |

---

## 3. Gap Analysis

| # | Missing input | Needed by (doc) | Blocker or TBD |
|---|---------------|-----------------|----------------|
| G-1 | Named first pilot org (LGU / SK federation) | GTM, VALIDATION | TBD |
| G-2 | Age gate and parental consent policy for under-18 | CLR | TBD (not Blocker for docs; Blocker for public launch) |
| G-3 | Commercial hosting choice when leaving Hobby | BUILD, UES, OPS | TBD |
| G-4 | Bot adapter priority (Telegram vs Messenger) | SDD, RFC | TBD |
| G-5 | Whether LLM coaching ships in v1 | AIA, PRD, UES | TBD |
| G-6 | Content pack authoring workflow and approval chain | PRD, SDD | TBD |

---

## 4. Assumption Stress-Test

**Load-bearing assumption:** Active, gamified broad-spectrum inoculation on a low-cost PWA will improve discernment enough that LGUs and enterprises will pay for licenses, without needing paid messaging or a credibility graph on day one.

**Strongest argument against it:** Buyers pay for reach (WhatsApp/SMS) and threat intel dashboards, not for another lesson app. A PWA may never match chat-native distribution, so CAC stays high and pilots stall.

**Does it hold?** Holds with caveat. Pedagogy evidence is real. Distribution and willingness-to-pay are unproven. GTM must sell measurable workforce/civic resilience, not "another MIL quiz."

**Second-order effects worth noting:** If leaders treat Pollux packs as official crisis truth without governance, a bad pack becomes a harm vector. CLR and content approval are load-bearing.

---

## 5. Feasibility & Scope

| Check | Finding |
|-------|---------|
| Time box realistic for the scope? | Full suite docs: yes this session. Production app: weeks, not days. Startup framing accepts that. |
| "If we ship only one thing" actually shippable in the window? | Yes: rule-based lesson PWA is a bounded build. |
| Production-grade reachable (security, data, rollback) in the window? | Docs yes. Code later with CLR/AIA/OPS gates. |
| Scope honest, or is the cut line hiding work? | Cut line is honest. Risk is underestimating content-pack ops and commercial hosting. |

---

## 6. Risk & Compliance Pre-flight

| Flag | Present? | Pulls in |
|------|----------|----------|
| Collects user data / PII | Y | CLR (required) |
| Children, health, payment, or biometric data | Y (youth / possible minors); health-adjacent crisis packs possible | CLR §3 escalation + counsel before school/LGU launch |
| AI component with untrusted input or tools | Y if LLM coaching; N if rule-based only | AIA required either way for conversational framing; SDD §8.1 if LLM |
| Security-critical paths (auth, money, deletes) | Y (auth, role deletes, pack publish) | SDD §5 + QAD abuse paths |
| Public deploy | Y | OPS + CLR |

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
