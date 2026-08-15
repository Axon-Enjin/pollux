# Documentation Index: Pollux

**Project slug:** `pollux`
**Maintained by:** Pollux founding team
**Last updated:** 2026-08-15
**Built on FMD:** v1.19.0

> The manifest. Read this first to learn what exists, each doc's version and status, and whether anything is stale.

---

## 1. Document Suite

| Document | File | Version | Status | Last Updated | Last Reconciled |
|----------|------|---------|--------|--------------|-----------------|
| IDEA · Idea Brief | [idea-pollux.md](idea-pollux.md) | 0.3 | Draft | 2026-08-15 | N/A |
| VALIDATION · Validation Brief | [val-pollux.md](val-pollux.md) | 0.3 | Draft | 2026-08-15 | N/A |
| SCRUTINY · Scrutiny Gate | [scrutiny-pollux.md](scrutiny-pollux.md) | 0.3 | Draft | 2026-08-15 | N/A |
| VOICE · House Style | - | - | N/A (hard bans always-on; polish on lock) | - | - |
| PITCH · Pitch & Demo | [pitch-pollux.md](pitch-pollux.md) | 0.1 | Draft | 2026-08-15 | N/A |
| WRAP · Next Steps | - | - | N/A (after suite lock) | - | - |
| BRD · Business Requirements | [brd-pollux.md](brd-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A (stale vs IDEA 0.3) |
| UES · Unit Economics Sheet | [ues-pollux.md](ues-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| LOG · Build Session Log | [log-pollux.md](log-pollux.md) | 0.1 | Draft | 2026-08-15 | N/A |
| PRD · Product Requirements | [prd-pollux.md](prd-pollux.md) | 0.3 | Draft | 2026-08-15 | N/A |
| DSD · Design System | [dsd-pollux.md](dsd-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| SDD · System Design | [sdd-pollux.md](sdd-pollux.md) | 0.1 | Draft | 2026-08-15 | N/A (F10 added; lesson APIs still listed) |
| QAD · QA & Test Plan | [qad-pollux.md](qad-pollux.md) | 0.1 | Draft | 2026-08-15 | N/A (happy path remapped to SK launch + F10) |
| SAD · Subagents | [sad-pollux.md](sad-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| BUILD · Build Guide | [build-pollux.md](build-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A (stale: inoculation golden path) |
| CLR · Compliance & Legal | [clr-pollux.md](clr-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| AIA · AI Assurance Dossier | [aia-pollux.md](aia-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A (stale: game-primary wording) |
| GTM · Go-To-Market | [gtm-pollux.md](gtm-pollux.md) | 0.3 | Draft | 2026-08-15 | N/A |
| OPS · Ops & Observability | [ops-pollux.md](ops-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| RESEARCH · Agent-era MIL | [research-pollux-agent-era-mil.md](research-pollux-agent-era-mil.md) | 0.1 | Input | 2026-08-13 | N/A |
| RESEARCH · UNESCO proposal 2026 | [research-pollux-unesco-proposal-2026.md](research-pollux-unesco-proposal-2026.md) | 0.1 | Input | 2026-08-15 | N/A |
| INPUT · Mentorship 1 July | [mentorship-july-1.md](mentorship-july-1.md) | 0.1 | Input | 2026-07-01 | N/A |
| INPUT · Mentorship 2 July | [mentorship-july-2.md](mentorship-july-2.md) | 0.1 | Input | 2026-07-02 | N/A |

**Materialized at project root (not in `docs/`):** `README.md`, `BRAND.md`, `DESIGN.md`, `AGENTS.md` (from BUILD), `LICENSE`, `CONTRIBUTING.md`. Optional: `MODEL_CARD.md` (from AIA §1).

### RFCs (one per major feature)

| RFC ID | File | Feature | Status | Last Updated |
|--------|------|---------|--------|--------------|
| pollux-rfc-001 | [rfc-pollux-channel-packs.md](rfc-pollux-channel-packs.md) | Channel adapter + content-pack confinement (civic gate) | Draft | 2026-08-15 |

---

## 2. Change Log

| CR ID | Date | Summary | Trigger doc | Docs touched | File |
|-------|------|---------|-------------|--------------|------|
| - | - | None yet | - | - | - |

---

## 3. Incident Log (Postmortems)

| PM ID | Incident date | Severity | Summary | Action items closed? | File |
|-------|---------------|----------|---------|----------------------|------|
| - | - | - | None yet | - | - |

---

## 4. Health Check

- [ ] Every Locked doc's **Last Reconciled** date is newer than the last code change to its area.
- [ ] No doc has been in `Draft` longer than expected without movement.
- [x] Feature IDs (`PRD-F#`) present in PRD for downstream cite.
- [x] UES present with `UES-E#` / `UES-D#`.
- [ ] **Production Readiness Gate** before code ship.
- [x] **Validator green:** `python D:\PROJECTS\FMD\scripts\check.py D:\PROJECTS\pollux\docs\ --scale full` (2026-08-15; 0 fail / 2 warn: G34 R-1 cite; SDD Request shapes)

---

## 5. Notes

Hybrid C product. Bootstrap burn doctrine in IDEA/UES. Research sources in repo root and `docs/research-*` / mentorship notes are inputs only, not specs until IDEA/PRD absorb them.

**Decision register (2026-07-15):** Telegram first (G-4); LLM post-MVP (G-5); commercial host Cloudflare (G-3); provisional pricing B2G $4k first paid / seats $12 list; audience includes under-18 (CLR consent still blocker for public launch). Still open/stale: named pilot (G-1), pack approval chain (G-6).

**Decision register addendum (2026-08-13):** Principal-training thesis absorbed into IDEA/PRD from [research-pollux-agent-era-mil.md](research-pollux-agent-era-mil.md). Pack confinement named as civic capability-restriction gate (RFC-001). UNESCO = first showcase venue, not revenue plan. Explicit non-builds: web-surfing agent, fact-check LLM racing volume, companion as primary path. G-6 remains load-bearing under civic-canon framing.

**Decision register addendum (2026-08-15):** Product spine is SK/LGU self-launch aide, not a game. PRD-F1 = canon desk + templates. PRD-F10 = human commit share (Must-Have). PRD-F12 = optional inoculation drill (Could-Have). Seekers Guild = open community medium (feedback, code, templates, partnerships); equal UNESCO billing; not required to launch; not the SK Page brand. OSS: Apache-2.0 code, CC-BY empty templates, SK facts stay SK-owned. SDD/QAD/BUILD/AIA/BRD still describe the old game-primary path until reconciled. Do not build against those stale F1 rows.
