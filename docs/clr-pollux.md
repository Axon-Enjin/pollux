# Compliance & Legal Readiness Register (CLR)

**Project:** Pollux
**Date:** 2026-08-16
**Version:** 0.2
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled with code)
**PRD:** [prd-pollux.md](prd-pollux.md)
**SDD:** [sdd-pollux.md](sdd-pollux.md)

---

> ⚠️ **Structural and regulatory awareness only; NOT legal advice.** This register maps the data Pollux handles and surfaces obligations. It does not draft a Privacy Policy or Terms of Use and does not replace a licensed attorney. Items flagged **"counsel needed"** must be reviewed by a lawyer qualified in the relevant jurisdiction before launch. **Escalate to counsel before any school or LGU public launch.**

---

## 0. Target Markets (drives the rest of this document)

| Region | In scope? | Notes |
|--------|-----------|-------|
| European Union / UK (GDPR / UK GDPR) | Yes | Public PWA, no geo-block; treat as reachable |
| California, USA (CCPA / CPRA) | Yes | Same public reach |
| Philippines (Data Privacy Act 2012, RA 10173) | Yes | Primary market; SK / LGU pilots; NPC awareness required |
| Other | No | Revisit if expansion markets named |

**Geo-blocking:** None planned. A public web app reaches everyone declared above.

---

## 1. Data Inventory / Record of Processing

| Activity | Purpose | Data categories | Data subjects | Recipients / sub-processors | Cross-border transfer | Retention | Legal basis |
|----------|---------|-----------------|---------------|-----------------------------|-----------------------|-----------|-------------|
| Authentication (F4) | Account access, roles | email, OAuth ids, session tokens | learners, leaders, admins | Supabase Auth | US/EU region per project (SCCs as applicable) | until account deletion | contract / consent TBD counsel |
| Lesson progress (F1) | Score, badges, completion | user id, lesson id, scores, badge flags | learners | Supabase DB | same as project region | until account deletion or 24 months inactive TBD | contract |
| Content packs (F2/F3) | Publish / view curated crisis facts | pack text, version, attribution, org id | leaders (authors); learners (readers) | Supabase DB + Storage | same | versions retained per org policy; default 24 months after unpublish TBD | contract / public-interest TBD counsel |
| Keyword watch lite (F3) | Leader keyword list (no paid listening) | keywords, org id | leaders | Supabase DB | same | until deleted by leader | contract |
| Messaging / Telegram (F5) | User-initiated game loop | Telegram user id, chat id, lesson progress | bot users | Telegram Bot API; Supabase | Telegram infra + project DB | until unlink / account deletion | consent (user-initiated) |
| Optional LLM coaching | Explain techniques after score | prompt context from lesson metadata; no pack invent | learners who opt in | Model provider TBD | provider region | provider retention per DPA; minimize | consent; off by default |
| Product analytics | Funnel / completion metrics | pseudonymous events | users | TBD (PostHog or Vercel Analytics) | per vendor | 12 months | consent / legitimate interest TBD |
| Crash logs | Reliability | stack traces, hashed user id | users | Vercel / Sentry TBD | per vendor | 30-90 days | legitimate interest |
| Outreach / seminar kit (PRD-F15) | Facilitation at camps and org sessions; print packets | kit session metadata: org, pack version, format, started_by officer. No student names in v1 session table. Print packets carry no PII; consent checklist is a stub pointing to counsel, not a legal form | officers / leaders who start sessions; under-18 may attend real camps (product demo remains Mia 19) | Supabase DB; print is offline | same as project region | until org deletion or session retention TBD | contract / school-camp lawful basis TBD counsel |

**Sensitivity flags:**

| Data type | Collected? | Notes |
|-----------|-----------|-------|
| Basic PII (name, email) | Yes | email at auth; display name optional |
| Special-category / sensitive | Possible | crisis packs may be health-adjacent (flood, disease); content is curated facts, not clinical records. Flag for counsel. |
| Children's data (under 16 EU / under 13 COPPA) | Yes (audience decided) | Product serves **all ages including under-18**, including kit/outreach camps (PRD-F15). Age gate + parental consent + school rules still **TBD with counsel**. **BLOCKER** for public school/LGU camp launch (same under-18 blocker, now covering F15). Minimize participant PII; do not collect student names in v1 session table. Fixtures are synthetic only; no real minor accounts. |
| Precise location | No | Not collected in v1 |
| Photos / camera / microphone | No | |
| Device IDs / advertising IDs | No | No ad network in v1 |
| Analytics / telemetry | Yes | pseudonymous preferred |
| Crash logs | Yes | scrub PII |
| Payment / card data | No | licensing offline / invoice for B2G; no card vault in app |

**Messaging consent:** Telegram (and any future Messenger/WhatsApp) is **user-initiated only**. No cold blast, no SMS until a buyer funds it. Document opt-in timestamp for bot link. WhatsApp template campaigns remain out of scope at our cost.

**Self-check:**

| Item | Done? | Evidence link | Counsel needed? |
|------|-------|---------------|-----------------|
| Every processing activity has a retention period | Partial | this table; several TBD | Yes |
| Every sub-processor is named and has a DPA in place | Partial | Supabase; Telegram; model provider TBD | Yes |
| Inventory is dated and treated as a living document | Yes | header date 2026-08-16 | No |

---

## 2. Multi-Jurisdiction Obligations Matrix

| Dimension | EU / UK GDPR | California CCPA / CPRA | Philippines DPA 2012 |
|-----------|--------------|------------------------|----------------------|
| **Consent / legal basis** | Opt-in; one of 6 lawful bases; special-category restricted | Opt-out of sale/share + limit sensitive PI | Consent or other lawful criteria; sensitive PI needs explicit consent |
| **Data subject rights** | Access, rectify, erase, port, object, restrict | Know, delete, correct, opt-out, limit SPI | Access, correct, erase/block, object, portability, damages |
| **Breach notification** | Authority ≤72h; subjects if high risk | Without unreasonable delay; CA AG if >500 residents | NPC **and** subjects ≤72h from knowledge if real risk of serious harm |
| **DPO / representative** | DPO if large-scale/special; EU/UK rep if no establishment | Contact method required | **Mandatory DPO** + PIA + Privacy Management Program (awareness) |
| **Cross-border transfer** | Adequacy / SCCs / BCRs | Contractual flow-down | Controller accountable; comparable protection |
| **Our status / action** | No EU entity; EU rep **TBD counsel**; SCCs with US vendors when signed | Privacy contact + no sale of data; opt-out link if analytics share | **NPC awareness**; DPO designation TBD; PIA before school/LGU launch; **counsel** |

**Watch list:** CCPA clarifying regs (2026-01-01); NPC AI/privacy advisories; youth age-assurance practice. Pilot org still TBD (Scrutiny G-1).

**Self-check:**

| Item | Done? | Evidence link | Counsel needed? |
|------|-------|---------------|-----------------|
| Consent model implemented for each in-scope region | No | not built | Yes |
| A working data-subject-request path exists (access/delete) | No | planned with F4 settings | Yes |
| Breach response runbook exists with tightest timeline | Partial | OPS §4 draft; 72h PH/EU | Yes |
| DPO / representative designated where required | No | PH DPO TBD; EU rep TBD | Yes |

---

## 3. Escalation Flags; Counsel Required

| Flag | Present? | Why it escalates |
|------|----------|------------------|
| Children's data | **Yes (audience locked; policy TBD)** | Under-18 learners are in scope, including real camps and outreach kit sessions (PRD-F15). Age gate, parental consent, and school rules need counsel before public school/LGU camp launch. Demo persona remains Mia 19; fixtures stay synthetic (no real youth PII). |
| Health / medical data | Possible | Crisis packs may include health-adjacent guidance; not a clinical product, but counsel on framing |
| Payments / card data | No | |
| Biometric data | No | |
| Large-scale / systematic monitoring or profiling | No for v1 | Keyword watch is leader-owned lists, not Meltwater-scale monitoring |
| Automated decisions with legal/significant effect | No | Game scores are pedagogical; packs are curated publications |
| Sale / share / cross-context behavioral advertising | No | Explicit non-goal |
| Operating in a market with no local entity | Yes | PH-first team may lack EU establishment → representative trigger |

**DPIA required?** Likely **Yes** before school/LGU-scale processing of youth data. Out of scope for this register; counsel + applicable DPIA process.

**Critical escalations (do not soft-launch these surfaces without counsel):**
1. Minors / youth age gate and parental consent (school, LGU public camp, or under-18 marketing). Counsel required before school/LGU camp (PRD-F15).
2. LGU or school-branded pack as "official" crisis truth (governance + liability).
3. PH DPO / NPC registration posture for a live public service.
4. Any paid messaging channel (WhatsApp/SMS) if later funded.

---

## 4. Terms of Use / EULA Readiness

| Clause | Present? | Evidence link | Counsel needed? |
|--------|----------|---------------|-----------------|
| License grant + scope | TBD | | |
| Acceptable use / prohibited conduct | TBD | | |
| Limitation of liability + warranty disclaimer | TBD | | Yes |
| Governing law + jurisdiction | TBD | | Yes |
| Dispute resolution | TBD | | Yes |
| Termination + suspension rights | TBD | | |
| User-generated content license (leader pack items) | TBD | | Yes |
| Modification / notice mechanism | TBD | | |
| Payment / refund terms | TBD | B2G invoice offline | Yes |
| Age eligibility | TBD | must align with §3 minors decision | Yes |
| Privacy Policy incorporated by reference | TBD | | Yes |

*Presence-checking only. Lawyer drafts before public launch.*

---

## 5. IP Infringement & Protection Readiness

| Item | Status | Evidence link | Counsel needed? |
|------|--------|---------------|-----------------|
| Product/brand name trademark knockout ("Pollux") | Not done | | Yes |
| Open-source license compliance; SBOM | Not yet | generate at first ship | |
| Copyleft scan | Not yet | | |
| Third-party assets licensed (fonts, images) | TBD at DSD lock | | |
| AI training-data provenance + output ownership | TBD if coaching ships | | Yes |
| DMCA / takedown process | TBD | | |
| Written IP assignment from founders/contractors | TBD | | Yes |

---

## 6. App Store / Platform Compliance

N/A for v1. Web PWA + optional Telegram bot only. No Apple App Store or Google Play submission. Revisit if a native shell ships.

Telegram Bot API: comply with Telegram terms; user-initiated messages only; store consent to bot link.

---

## Self-Check

- [x] Section 0 declares every market; geo-blocking reality is honest
- [x] Section 1 has processing rows with retention (some TBD flagged)
- [x] Section 2 actions filled for PH / EU / CA
- [x] Every Section 3 "Yes" has counsel action; banner set
- [x] Section 4 ToU presence checked (drafting left to counsel)
- [x] Section 5 IP items flagged
- [x] Section 6 N/A with reason
- [x] This document maps obligations and escalates; it does not give legal advice
- [x] AGENTS hard bans applied (no em-dashes)
