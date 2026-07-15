# Operations & Observability Runbook (OPS)

**Project:** Pollux
**Date:** 2026-07-15
**Version:** 0.1
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled with prod)
**SDD:** [sdd-pollux.md](sdd-pollux.md)

> Bootstrap stack: Next.js on Vercel Hobby (non-commercial prototypes only) or Cloudflare Pages; Supabase free; Telegram after MVP. Commercial pilots use **Cloudflare** (see section 5). Rollback: prefer [prd-pollux.md](prd-pollux.md) section 9 when present; else this runbook.

---

## 1. SLOs & SLIs

*Free-tier honest targets. Not enterprise 99.99.*

| SLI (what you measure) | SLO (target) | Measured by | Breach action |
|------------------------|--------------|-------------|---------------|
| Availability (PWA) | 99.0% / mo (best-effort on free tier) | UptimeRobot or Better Stack free check, 5-min | Investigate; announce if >30 min down |
| API / SSR p95 (non-AI) | <800ms on Hobby cold-start tolerant | Vercel Analytics | Note cold starts; tune if warm p95 >500ms sustained |
| Error rate (5xx) | <2% of requests / 15 min | Vercel logs | Trip the one alert (§3) |
| Lesson complete success | >95% of started lessons that reach final vignette submit | App event `lesson_complete` | Fix scoring / session bugs before demo |
| Coaching cost (if enabled) | <2× baseline per day | Provider usage | Kill switch `ENABLE_LLM_COACHING=false` |

---

## 2. Observability; Logs, Metrics, Traces

| Pillar | Tool | What's captured | Retention |
|--------|------|-----------------|-----------|
| Logs | Vercel / host logs + structured JSON | `request_id`, route, status; no raw emails or pack PII | ~1-7 days on free tier (export if needed) |
| Metrics | Vercel Analytics + app events | SLIs; `lesson_complete`, `pack_publish` | per vendor free retention |
| Traces | Optional later (Langfuse) if coaching on | model, tokens, cost per coach call | 30 days when enabled |

**Dashboards:** One health view (uptime + error rate). Funnel board when PostHog or equivalent lands. No dashboard sprawl on free tier.

**Correlation ID:** `request_id` from edge/middleware through API routes into logs.

**No-PII-in-logs rule:** Never log raw email, magic links, Telegram tokens, or full pack bodies. Hash user ids. Reconcile with CLR §1.

---

## 3. Alerting & On-Call

**One actionable alert for v1** (alert hygiene over coverage theater):

| Alert | Condition | Severity | Who / how notified |
|-------|-----------|----------|--------------------|
| Error spike / downtime | Uptime check fail ×2 **or** 5xx rate >2% for 15 min | P1 | Founder phone/SMS via uptime provider webhook |

Deferred until traffic justifies: separate coaching cost alert, Telegram bot health, Supabase disk.

**On-call model:** Solo best-effort founders; no formal rotation until paid pilot.
**Alert hygiene:** If this alert nags without action, fix the threshold. Do not add a second alert until the first is trusted.

---

## 4. Incident Response

**Severity ladder:** QAD P0-P3.

**When an incident fires:**
1. **Acknowledge**; claim in team chat.
2. **Assess**; blast radius (auth down vs one pack).
3. **Mitigate first;** roll back deploy, flip kill switches, or pause feature. Diagnose after users are safe.
4. **Communicate;** short status to pilot contacts if user-facing.
5. **Resolve & verify;** error rate and uptime healthy.
6. **Postmortem;** any P0/P1 → `docs/pm-pollux-NNN.md` within 48h.

**Rollback trigger & mechanism:**
- Trigger: P0 on main lesson/auth, or sustained SLO breach after a deploy.
- Mechanism: Redeploy previous Vercel/Cloudflare deployment (instant rollback). DB migrations must be backward-compatible; no expand-contract break without a forward fix ready.
- Until PRD §9 exists, this section is the rollback source of truth.

**Kill switches / feature flags:**
- `ENABLE_LLM_COACHING` (default false)
- `ENABLE_TELEGRAM_BOT` (default false until staging proven)
- Pack publish can be restricted to admin-only via role flag without redeploy if coded as config

---

## 5. Routine Operations

- **Secret rotation:** Supabase service role, Vercel env, Telegram bot token; rotate on leak and quarterly.
- **Dependency / security updates:** Dependabot or equivalent weekly; security patches within 7 days when app exists.
- **Backup restore drill:** Use Supabase PITR/export on free tier as available; run one restore to a scratch project before first public pilot.
- **Cost review:** Monthly. Pre-revenue burn targets free tiers. Messaging $0 until a buyer funds it.
- **Cert / domain expiry:** Auto-renew on host; calendar backstop.

### Supabase free-tier pause keepalive

Supabase free projects can **pause after inactivity**. Before demos and weekly during quiet periods, hit a cheap authenticated health route or scheduled edge ping so the project stays awake. Document the ping URL in the team vault. If paused mid-incident, unpause in dashboard first, then diagnose.

### Commercial hosting upgrade path

| Phase | Host | Notes |
|-------|------|-------|
| Pre-revenue / non-commercial prototype | Vercel Hobby **or** Cloudflare Pages + Supabase free | Hobby forbids commercial use ([Vercel Hobby](https://vercel.com/docs/plans/hobby)) |
| Commercial pilot / paid B2G | **Cloudflare Pages + Workers** (locked G-3) | Vercel Pro (~$20) alternate; update UES burn |
| Scale later | Pro + paid Supabase as needed | Still no paid messaging until funded |

Scrutiny FC-6/FC-7: do not claim "$0 commercial production" on Hobby.

---

## Self-Check

- [x] Every SLO has a measurement source appropriate to free tier
- [x] Logs carry correlation ID policy and no-PII rule
- [x] Exactly one primary actionable alert defined
- [x] §4 names rollback and kill switches
- [x] Supabase pause keepalive noted
- [x] Commercial hosting upgrade path stated
- [x] P0/P1 Postmortem SLA set
- [x] AGENTS hard bans applied (no em-dashes)
