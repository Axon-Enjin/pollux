# AI Assurance Dossier (AIA)

**Project:** Pollux
**Date:** 2026-08-16
**Version:** 0.2
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** 2026-08-16 (PRD 0.4 spine + F15 kits; not reconciled with code)
**PRD:** [prd-pollux.md](prd-pollux.md)
**SDD:** [sdd-pollux.md](sdd-pollux.md)
**QAD:** [qad-pollux.md](qad-pollux.md)
**CLR:** [clr-pollux.md](clr-pollux.md)

---

> ⚠️ **Governance and assurance-readiness awareness only; NOT an audit and NOT a certification.** This dossier assembles documentation for assessment. It does **not** certify ISO/IEC 42001, does **not** discharge EU AI Act duties, and does **not** replace a qualified independent AI auditor or licensed attorney. FMD produces the auditable record; a competent assessor performs the audit. Items flagged **"counsel/assessor needed"** must be escalated before launch.

---

## 0. Trigger and Scope

> **Reconciliation (2026-08-16):** v0.2 of this AIA treated the inoculation game as the primary product path. PRD 0.4 spine is the SK/LGU self-launch aide (canon desk, published packs, human commit share). PRD-F15 is the outreach/seminar kit layer: human-authored Markdown published as `outreach_kit` packs, plus a printable packet and in-app session runner. F15 is not the inoculation game. PRD-F12 remains Could-Have. Remaining game-primary wording below is leftover F7/F12 coaching context, not the v1 brand.

| Field | Value |
|-------|-------|
| AI component | Optional post-lesson LLM coaching (**post-MVP**; off by default). **No model on kit authoring, kit module facts, or live session Q&A.** Product critical path is non-AI. |
| Realizing feature ID(s) | Optional coaching is PRD-F7 when flag on after MVP. PRD-F15 kits are non-AI. PRD-F12 drill is Could-Have (non-ML scorer if shipped). Stale v0.2 mapping of PRD-F1 to the rule engine is retired; PRD-F1 is canon desk. |
| System boundary | In: optional coach over lesson metadata after score (F7 only, flag off). Out: pack authorship, **kit module facts**, **camp session Q&A**, auth, watch lists, crisis facts (curated published packs only). **Open-web RAG for crisis or session Q&A is forbidden.** |
| Autonomy level | Coaching text for user reading only; no tools; no pack or kit publish; no official share; no admin actions. Human remains principal for publish and official share. |
| Provisional risk classification (awareness) | Not framed as high-risk automated decisioning on rights; pedagogical aid if F7 ever enables. Confirm with counsel before school/LGU scale. |

**Why an AIA here:** Even with a non-AI primary path (aide + F15 kits), optional generative coaching plus crisis-adjacent product context needs a documented risk register before any model flag is enabled for real users. **MVP ships with coaching disabled** (Scrutiny G-5, 2026-07-15). F15 does not introduce a model.

**Self-check:**

- [x] AI component bounded; non-AI primary (aide + F15 kits) stated; F12 not primary
- [x] Provisional risk classification is awareness, not a legal conclusion

---

## 1. Model / System Card

*Optional public materialization: `MODEL_CARD.md` at repo root may be generated from this section when coaching ships. Do not hand-edit the root copy as source of truth. Defer until flag-on launch.*

### 1.1 Intended use

| Field | Value |
|-------|-------|
| Intended use | After the rule engine scores a vignette (PRD-F12 only, if shipped), optionally explain the named manipulation technique in plain language |
| Intended users / affected parties | Learners (operators) if F12/F7 ship. Leaders/admins are not decided by the model. Crisis-affected communities must not treat coach output as official instructions. Camp facilitators use F15 kits, not the coach, for session facts. |
| Out-of-scope / prohibited uses | Crisis fact generation; evacuation orders; open-web RAG; automated pack or kit publish; **LLM generation of kit module facts**; **live session answers from RAG/LLM**; medical/legal advice; grading people for employment or benefits |
| Human-in-the-loop points | User opts into coaching; can ignore or hide it. Pack and kit facts remain human-authored and human-published (F3, F15). Human is principal for publish and official share (F10). |

### 1.2 Model(s) and data

| Model / stage | Identifier + version | Role | Source of data it sees |
|---------------|----------------------|------|------------------------|
| Optional coach | TBD at enable time (pin exact version in CR) | Explain technique labels (F7; flag off) | Lesson metadata + user question; **not** live web; **not** kit modules; **not** other users' data |
| Rule engine (non-ML) | App-owned scorer | Optional F12 drill only (Could-Have); not the v1 brand | Curated vignette bank |
| F15 kit runner (non-AI) | App-owned pack read | Session runner + printable packet from published `outreach_kit` | Human-authored Markdown items in a published pack only |

- **Training / tuning data:** Provider base model if coaching enabled; no Pollux fine-tune in v1. **No model trains on or authors kit content.**
- **Run-time input:** Technique ids, vignette ids, short user question. Labeled untrusted. No tool APIs. Session Q&A must not send questions to an LLM or open-web RAG.
- **Output contract:** Plain text coaching bound to known technique taxonomy; reject if model invents pack facts, kit facts, or URLs not in allowlist (allowlist empty for crisis and for kit Q&A).
- **Provider data terms:** TBD when vendor chosen; reconcile with CLR §1 before enable.

### 1.3 Limitations and performance caveats

- Coach may over-generalize technique explanations; it is not a source of news or kit canon.
- Quality irrelevant if flag off; product (including F15 kits) must fully work without a model.
- **Known failure modes:** Prompt injection asking for fake LGU orders; hallucinated routes; kit Q&A answered from the web; cross-user leakage if mis-wired context.
- **Fallback behavior:** On model error, hide coach and keep non-AI paths (published packs, F15 session from pack items, optional F12 score). Never block kit session or lesson completion on model failure.

**Self-check:**

- [x] Intended use AND prohibited uses stated
- [x] Model version TBD explicitly until enable
- [x] Provider terms deferred with CLR reconcile note
- [x] Kit content human-authored; no model on kit critical path
- [x] Session Q&A cannot call RAG/LLM for facts
- [x] F15 distinguished from F12

---

## 2. NIST AI RMF Risk Register

*Lean register. GenAI categories aligned to NIST AI RMF GenAI Profile (NIST-AI-600-1) awareness as of 2026-07-15; verify again before lock.*

| Risk ID | Risk | RMF function | GenAI category (if applicable) | Severity | Likelihood | Mitigation / control | Eval (QAD ref) | Owner | Status |
|---------|------|--------------|--------------------------------|----------|------------|----------------------|----------------|-------|--------|
| AIA-R1 | Prompt injection steers coach into fake crisis orders | Map / Measure | Information security | High | Med | No tools; crisis answers refused; packs only (F2) | QAD AI-04, AI-02 | Eng | Mitigated (design) |
| AIA-R2 | Confabulation of crisis facts / routes | Measure / Manage | Information integrity | High | Med | Open-web RAG forbidden; coach cannot write packs | QAD AI-02, AB-07 | Eng | Mitigated (design) |
| AIA-R3 | Optional coach treated as required path | Govern / Map | Human-AI configuration | Med | Med | Flag off by default; aide, kits, and optional drill work without a model | QAD AI-03, H-01 | Product | Mitigated (design) |
| AIA-R4 | Cross-user or draft-pack leakage into prompt | Map / Manage | Data privacy | High | Low | Context scoped to requesting user + public lesson metadata | QAD AI-06, AB-02 | Eng | Open (needs SDD) |
| AIA-R5 | Cost / abuse bomb on coaching API | Measure / Manage | Information security | Med | Med | Rate limit + daily cap; kill switch | QAD AB-style + OPS | Eng | Open (needs impl) |
| AIA-R6 | LLM authors kit modules or answers camp session Q&A | Measure / Manage | Information integrity | High | Med | F15 content is human-authored Markdown published as `outreach_kit`; session facts from published pack only; F7 must not answer kit Q&A from the web | QAD AI-02, AB-07 | Eng | Mitigated (design) |
| AIA-R7 | Open-web RAG during a camp session | Map / Manage | Information integrity | High | Low | No RAG on session path; runner reads published pack items only | QAD AB-07 | Eng | Mitigated (design) |

> **Govern:** Pollux founding team reviews this register each release and when the coaching flag flips; changes go through a Change Record.

**Self-check:**

- [x] Lean set of risks with owners and statuses
- [x] Each row ties to QAD evals where possible
- [x] GenAI column filled with dated awareness note
- [x] F15 kit and session Q&A controls explicit

---

## 3. SMACTR Self-Audit Checklist

| Stage | What it produces here | Done? | Evidence link |
|-------|-----------------------|-------|---------------|
| **Scoping** | Intended use, prohibited use, risk class | Yes | §0, §1.1 |
| **Mapping** | Boundary: non-AI aide + F15 kits; F12 Could-Have; packs/kits non-AI; no open-web RAG on crisis or session Q&A | Partial | Awaiting SDD §8 |
| **Artifact collection** | This card + register + CLR links | Yes | §1, §2, CLR |
| **Testing** | Red-team evals defined | Partial | QAD AI-01..AI-07 (not yet executed) |
| **Reflection** | Residual risk + escalation | Yes | §4 |

**Residual-risk statement:** With coaching off, residual AI risk is near zero; the product is an SK aide plus curated packs and human-authored F15 kits. With coaching on, residual risk of misleading explanatory text remains. Acceptable for private pilots only if refusals hold and packs stay authoritative. Not acceptable as "official crisis advice" or as live kit Q&A.

**Go / no-go:** No-go for enabling coaching in production until SDD §8 exists, QAD AI evals run green, and CLR youth counsel path is started for school/LGU audiences. F15 kits may ship with coaching off.

---

## 4. Cross-links and Escalation

| Dimension | Lives in | This AIA relies on |
|-----------|----------|--------------------|
| AI architecture and threat surface | SDD §8 / §8.1 (pending) | To be linked when SDD lands |
| Red-team and abuse evals | QAD | [qad-pollux.md](qad-pollux.md) AI + AB-06/AB-07 |
| Data, sub-processors, legal | CLR | [clr-pollux.md](clr-pollux.md) |
| Prompt-injection / RAG posture | FMD Context Hygiene | Engine AGENTS.md; no open-web RAG (crisis, kits, or session Q&A) |

### Escalation flags

| Flag | Present? | Why it escalates |
|------|----------|------------------|
| Output affects rights, access, credit, employment, or benefits | No | Pedagogical coaching only; kits are not automated decisions |
| Automated decision with legal/significant effect, no human review | No | Human remains principal for publish and official share |
| Health, safety, biometric, or sensitive inference | Possible | Crisis-adjacent UX; coach must not give safety-critical instructions; kit Q&A must not invent crisis facts |
| General-purpose model placed on market / systemic-risk scale | No | API consumer only |
| Training or run-time data with unresolved provenance | Yes if coaching on before vendor terms reviewed | Reconcile with CLR §5 |
| Deployment in market whose AI rules not mapped | Partial | PH NPC / NAIS awareness started; counsel confirm |

**If any flag is Yes:** Pause enabling coaching for that audience; obtain counsel/assessor review. Published packs, F15 kits, and optional F12 drill may still proceed under CLR constraints. Human remains principal for publish and official share.

---

## 5. Regulatory Awareness (PH-first, then global)

*Awareness only; NOT legal advice. Specs verified at awareness level 2026-07-15; re-check before lock.*

| Regime | Applies? | What it asks of an AI system (awareness) | Our note / action |
|--------|----------|------------------------------------------|-------------------|
| **PH: NPC Advisory 2024-04** | Yes (awareness) | Privacy principles across AI lifecycle | Align processing records; counsel before public AI feature |
| **PH: NAIS-PH** ethics pillar | Yes (awareness) | Fairness, accountability, transparency, human oversight | HITL + flag-off default; human principal on publish/share |
| **NIST AI RMF + GenAI Profile** | Yes (voluntary) | Govern/Map/Measure/Manage | §2 register |
| **ISO/IEC 42001** | No (not seeking cert now) | AI management system | Awareness only |
| **EU AI Act** | If EU users | Risk-tiered duties | Provisional not Annex III high-risk; counsel if EU school deploy |

---

## Self-Check

- [x] AIA exists because optional AI may ship; non-AI primary (PRD 0.4 aide + F15) documented; F12 Could-Have
- [x] Kit content human-authored Markdown as `outreach_kit`; no model on kit critical path
- [x] Session Q&A cannot call RAG/LLM for facts; F7 must not answer crisis or kit Q&A from the web
- [x] §1 states use and limits; MODEL_CARD optional/deferred noted
- [x] §2 lean NIST-style register with QAD ties (incl. AIA-R6, AIA-R7)
- [x] §3 SMACTR points at real artifacts; testing partial until code
- [x] §4 escalations named; banner set; human principal for publish and official share
- [x] §5 PH-first regimes noted with dated awareness
- [x] Disclaimer discipline held; no em-dashes
