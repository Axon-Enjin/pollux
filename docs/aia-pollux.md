# AI Assurance Dossier (AIA)

**Project:** Pollux
**Date:** 2026-07-15
**Version:** 0.1
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled with code)
**PRD:** [prd-pollux.md](prd-pollux.md)
**SDD:** [sdd-pollux.md](sdd-pollux.md)
**QAD:** [qad-pollux.md](qad-pollux.md)
**CLR:** [clr-pollux.md](clr-pollux.md)

---

> ⚠️ **Governance and assurance-readiness awareness only; NOT an audit and NOT a certification.** This dossier assembles documentation for assessment. It does **not** certify ISO/IEC 42001, does **not** discharge EU AI Act duties, and does **not** replace a qualified independent AI auditor or licensed attorney. FMD produces the auditable record; a competent assessor performs the audit. Items flagged **"counsel/assessor needed"** must be escalated before launch.

---

## 0. Trigger and Scope

| Field | Value |
|-------|-------|
| AI component | Optional post-lesson LLM coaching (**post-MVP**; off by default). Primary product path is **rule-based** inoculation (no model on critical path). |
| Realizing feature ID(s) | PRD-F1 (rule engine; non-AI). Optional coaching is PRD-F7 when flag on after MVP. |
| System boundary | In: optional coach over lesson metadata after score. Out: pack authorship, auth, watch lists, crisis facts (curated packs only). **Open-web RAG for crisis is forbidden.** |
| Autonomy level | Coaching text for user reading only; no tools; no pack publish; no admin actions |
| Provisional risk classification (awareness) | Not framed as high-risk automated decisioning on rights; pedagogical aid. Confirm with counsel before school/LGU scale. |

**Why an AIA here:** Even with a rule-based primary path, optional generative coaching plus crisis-adjacent product context needs a documented risk register before any model flag is enabled for real users. **MVP ships with coaching disabled** (Scrutiny G-5, 2026-07-15).

**Self-check:**

- [x] AI component bounded; rule-based primary stated
- [x] Provisional risk classification is awareness, not a legal conclusion

---

## 1. Model / System Card

*Optional public materialization: `MODEL_CARD.md` at repo root may be generated from this section when coaching ships. Do not hand-edit the root copy as source of truth. Defer until flag-on launch.*

### 1.1 Intended use

| Field | Value |
|-------|-------|
| Intended use | After the rule engine scores a vignette, optionally explain the named manipulation technique in plain language |
| Intended users / affected parties | Learners (operators). Leaders/admins are not decided by the model. Crisis-affected communities must not treat coach output as official instructions. |
| Out-of-scope / prohibited uses | Crisis fact generation; evacuation orders; open-web RAG; automated pack publish; medical/legal advice; grading people for employment or benefits |
| Human-in-the-loop points | User opts into coaching; can ignore or hide it. Pack facts remain human-published (F3). |

### 1.2 Model(s) and data

| Model / stage | Identifier + version | Role | Source of data it sees |
|---------------|----------------------|------|------------------------|
| Optional coach | TBD at enable time (pin exact version in CR) | Explain technique labels | Lesson metadata + user question; **not** live web; **not** other users' data |
| Rule engine (non-ML) | App-owned scorer | Primary game logic | Curated vignette bank |

- **Training / tuning data:** Provider base model if coaching enabled; no Pollux fine-tune in v1.
- **Run-time input:** Technique ids, vignette ids, short user question. Labeled untrusted. No tool APIs.
- **Output contract:** Plain text coaching bound to known technique taxonomy; reject if model invents pack facts or URLs not in allowlist (allowlist empty for crisis).
- **Provider data terms:** TBD when vendor chosen; reconcile with CLR §1 before enable.

### 1.3 Limitations and performance caveats

- Coach may over-generalize technique explanations; it is not a source of news.
- Quality irrelevant if flag off; product must fully work without it.
- **Known failure modes:** Prompt injection asking for fake LGU orders; hallucinated routes; cross-user leakage if mis-wired context.
- **Fallback behavior:** On model error, hide coach and keep rule-based score. Never block lesson completion on model failure.

**Self-check:**

- [x] Intended use AND prohibited uses stated
- [x] Model version TBD explicitly until enable
- [x] Provider terms deferred with CLR reconcile note

---

## 2. NIST AI RMF Risk Register

*Lean register. GenAI categories aligned to NIST AI RMF GenAI Profile (NIST-AI-600-1) awareness as of 2026-07-15; verify again before lock.*

| Risk ID | Risk | RMF function | GenAI category (if applicable) | Severity | Likelihood | Mitigation / control | Eval (QAD ref) | Owner | Status |
|---------|------|--------------|--------------------------------|----------|------------|----------------------|----------------|-------|--------|
| AIA-R1 | Prompt injection steers coach into fake crisis orders | Map / Measure | Information security | High | Med | No tools; crisis answers refused; packs only (F2) | QAD AI-04, AI-02 | Eng | Mitigated (design) |
| AIA-R2 | Confabulation of crisis facts / routes | Measure / Manage | Information integrity | High | Med | Open-web RAG forbidden; coach cannot write packs | QAD AI-02, AB-07 | Eng | Mitigated (design) |
| AIA-R3 | Optional coach treated as required path | Govern / Map | Human-AI configuration | Med | Med | Flag off by default; lesson works offline of model | QAD AI-03, H-01 | Product | Mitigated (design) |
| AIA-R4 | Cross-user or draft-pack leakage into prompt | Map / Manage | Data privacy | High | Low | Context scoped to requesting user + public lesson metadata | QAD AI-06, AB-02 | Eng | Open (needs SDD) |
| AIA-R5 | Cost / abuse bomb on coaching API | Measure / Manage | Information security | Med | Med | Rate limit + daily cap; kill switch | QAD AB-style + OPS | Eng | Open (needs impl) |

> **Govern:** Pollux founding team reviews this register each release and when the coaching flag flips; changes go through a Change Record.

**Self-check:**

- [x] Lean set of risks with owners and statuses
- [x] Each row ties to QAD evals where possible
- [x] GenAI column filled with dated awareness note

---

## 3. SMACTR Self-Audit Checklist

| Stage | What it produces here | Done? | Evidence link |
|-------|-----------------------|-------|---------------|
| **Scoping** | Intended use, prohibited use, risk class | Yes | §0, §1.1 |
| **Mapping** | Boundary: rule engine primary; packs non-AI; no open-web RAG | Partial | Awaiting SDD §8 |
| **Artifact collection** | This card + register + CLR links | Yes | §1, §2, CLR |
| **Testing** | Red-team evals defined | Partial | QAD AI-01..AI-07 (not yet executed) |
| **Reflection** | Residual risk + escalation | Yes | §4 |

**Residual-risk statement:** With coaching off, residual AI risk is near zero; the product is a rule-based lesson plus curated packs. With coaching on, residual risk of misleading explanatory text remains. Acceptable for private pilots only if refusals hold and packs stay authoritative. Not acceptable as "official crisis advice."

**Go / no-go:** No-go for enabling coaching in production until SDD §8 exists, QAD AI evals run green, and CLR youth counsel path is started for school/LGU audiences.

---

## 4. Cross-links and Escalation

| Dimension | Lives in | This AIA relies on |
|-----------|----------|--------------------|
| AI architecture and threat surface | SDD §8 / §8.1 (pending) | To be linked when SDD lands |
| Red-team and abuse evals | QAD | [qad-pollux.md](qad-pollux.md) AI + AB-06/AB-07 |
| Data, sub-processors, legal | CLR | [clr-pollux.md](clr-pollux.md) |
| Prompt-injection / RAG posture | FMD Context Hygiene | Engine AGENTS.md; no open-web RAG |

### Escalation flags

| Flag | Present? | Why it escalates |
|------|----------|------------------|
| Output affects rights, access, credit, employment, or benefits | No | Pedagogical coaching only |
| Automated decision with legal/significant effect, no human review | No | |
| Health, safety, biometric, or sensitive inference | Possible | Crisis-adjacent UX; coach must not give safety-critical instructions |
| General-purpose model placed on market / systemic-risk scale | No | API consumer only |
| Training or run-time data with unresolved provenance | Yes if coaching on before vendor terms reviewed | Reconcile with CLR §5 |
| Deployment in market whose AI rules not mapped | Partial | PH NPC / NAIS awareness started; counsel confirm |

**If any flag is Yes:** Pause enabling coaching for that audience; obtain counsel/assessor review. Packs and rule-based game may still proceed under CLR constraints.

---

## 5. Regulatory Awareness (PH-first, then global)

*Awareness only; NOT legal advice. Specs verified at awareness level 2026-07-15; re-check before lock.*

| Regime | Applies? | What it asks of an AI system (awareness) | Our note / action |
|--------|----------|------------------------------------------|-------------------|
| **PH: NPC Advisory 2024-04** | Yes (awareness) | Privacy principles across AI lifecycle | Align processing records; counsel before public AI feature |
| **PH: NAIS-PH** ethics pillar | Yes (awareness) | Fairness, accountability, transparency, human oversight | HITL + flag-off default |
| **NIST AI RMF + GenAI Profile** | Yes (voluntary) | Govern/Map/Measure/Manage | §2 register |
| **ISO/IEC 42001** | No (not seeking cert now) | AI management system | Awareness only |
| **EU AI Act** | If EU users | Risk-tiered duties | Provisional not Annex III high-risk; counsel if EU school deploy |

---

## Self-Check

- [x] AIA exists because optional AI may ship; rule-based primary documented
- [x] §1 states use and limits; MODEL_CARD optional/deferred noted
- [x] §2 lean NIST-style register with QAD ties
- [x] §3 SMACTR points at real artifacts; testing partial until code
- [x] §4 escalations named; banner set
- [x] §5 PH-first regimes noted with dated awareness
- [x] Disclaimer discipline held; no em-dashes
