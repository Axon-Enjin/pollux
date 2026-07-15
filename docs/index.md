# Documentation Index: Pollux

**Project slug:** `pollux`
**Maintained by:** Pollux founding team
**Last updated:** 2026-07-15
**Built on FMD:** v1.19.0

> The manifest. Read this first to learn what exists, each doc's version and status, and whether anything is stale.

---

## 1. Document Suite

| Document | File | Version | Status | Last Updated | Last Reconciled |
|----------|------|---------|--------|--------------|-----------------|
| IDEA · Idea Brief | [idea-pollux.md](idea-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| VALIDATION · Validation Brief | [val-pollux.md](val-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| SCRUTINY · Scrutiny Gate | [scrutiny-pollux.md](scrutiny-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| VOICE · House Style | - | - | N/A (hard bans always-on; polish on lock) | - | - |
| PITCH · Pitch & Demo | - | - | N/A (optional; skip unless fundraising) | - | - |
| WRAP · Next Steps | - | - | N/A (after suite lock) | - | - |
| BRD · Business Requirements | [brd-pollux.md](brd-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| UES · Unit Economics Sheet | [ues-pollux.md](ues-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| LOG · Build Session Log | [log-pollux.md](log-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| PRD · Product Requirements | [prd-pollux.md](prd-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| DSD · Design System | [dsd-pollux.md](dsd-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| SDD · System Design | [sdd-pollux.md](sdd-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| QAD · QA & Test Plan | [qad-pollux.md](qad-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| SAD · Subagents | [sad-pollux.md](sad-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| BUILD · Build Guide | [build-pollux.md](build-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| CLR · Compliance & Legal | [clr-pollux.md](clr-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| AIA · AI Assurance Dossier | [aia-pollux.md](aia-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| GTM · Go-To-Market | [gtm-pollux.md](gtm-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |
| OPS · Ops & Observability | [ops-pollux.md](ops-pollux.md) | 0.1 | Draft | 2026-07-15 | N/A |

**Materialized at project root (not in `docs/`):** `README.md`, `BRAND.md`, `DESIGN.md`, `AGENTS.md` (from BUILD). Optional: `MODEL_CARD.md` (from AIA §1).

### RFCs (one per major feature)

| RFC ID | File | Feature | Status | Last Updated |
|--------|------|---------|--------|--------------|
| pollux-rfc-001 | [rfc-pollux-channel-packs.md](rfc-pollux-channel-packs.md) | Channel adapter + content-pack confinement | Draft | 2026-07-15 |

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
- [x] **Validator green:** `python D:\PROJECTS\FMD\scripts\check.py D:\PROJECTS\pollux\docs\ --scale full`

---

## 5. Notes

Hybrid C product. Bootstrap burn doctrine in IDEA/UES. Research sources in repo root are inputs only, not specs.

**Decision register (2026-07-15):** Telegram first (G-4); LLM post-MVP (G-5); commercial host Cloudflare (G-3); provisional pricing B2G $4k first paid / seats $12 list; audience includes under-18 (CLR consent still blocker for public launch). Still open/stale: named pilot (G-1), pack approval chain (G-6).
