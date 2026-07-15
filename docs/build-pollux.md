# Project Build Guide

**Project:** Pollux
**Date:** 2026-07-15
**Version:** 0.1
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled with code)
**PRD:** [prd-pollux.md](prd-pollux.md) (provisional feature IDs until PRD lands)
**SDD:** [sdd-pollux.md](sdd-pollux.md)
**SAD:** N/A (no SAD yet; main agent builds inline)

> Spec → code bridge. Canonical file. Materialize to root `AGENTS.md` later (parent owns materialization). Edit here; do not hand-edit root copies as source of truth.

---

## 1. How to Build From These Docs

The documentation suite is the source of truth. Read in this order before writing code:

1. [`docs/index.md`](index.md). What exists, status, staleness.
2. [IDEA](idea-pollux.md) + [SCRUTINY](scrutiny-pollux.md). Product lock and carried fixes.
3. [PRD](prd-pollux.md). Features and acceptance (use provisional PRD-F1…F5 until written).
4. [SDD](sdd-pollux.md). Schema, APIs, security, optional AI.
5. [RFC channel-packs](rfc-pollux-channel-packs.md). Adapter interface and pack confinement.
6. [DSD](dsd-pollux.md). Visual rules when present.
7. [QAD](qad-pollux.md). Tests before calling a feature done.
8. [CLR](clr-pollux.md) / [AIA](aia-pollux.md). Before public launch or enabling LLM coach.
9. [OPS](ops-pollux.md). Before production pilot.
10. This guide. Stack conventions, golden paths, guardrails.

**Only build against `Locked` docs.** These eng docs are `Draft`. Flag that before large implementation. If reality diverges from a Locked doc later, write a Change Record (`docs/cr-*.md`). Do not silently code around it.

### Traceability map; "to build X, read Y"

| To implement… | Read | Then verify against |
|---------------|------|---------------------|
| Inoculation game (PRD-F1) | PRD feature + SDD §3 (`lessons`, `vignettes`, `attempts`) + rule engine notes | QAD happy/sad/abuse for scoring |
| Content packs (PRD-F2) | SDD §3 packs + [RFC](rfc-pollux-channel-packs.md) confinement | Unpublished invisible; no RAG |
| Admin lite (PRD-F3) | SDD §4 leader APIs + RFC publish workflow | Role checks; share pin version |
| Auth roles (PRD-F4) | SDD §5 | RLS + server role check; ignore client `role` |
| Telegram adapter (PRD-F5) | RFC `ChannelAdapter` + webhook contract | Secret header; flag default off |
| Optional LLM coach | SDD §8 / §8.1 | Flag off; never crisis answers |

---

## 2. Subagents

No SAD yet. Main agent implements inline. If specialist agents are added later, define them in `docs/sad-pollux.md` and materialize per platform.

---

## 3. Stack Currency & Deprecations

> Do **not** trust training memory for fast-moving frameworks. Verify against the authoritative source for the pinned version before writing framework code. If you cannot verify, say so. Do not emit a plausible-but-stale API.

### Pinned stack

| Layer | Technology | Pinned version | Convention verified (date) | Authoritative source |
|-------|------------|----------------|-----------------------------|----------------------|
| Language | TypeScript | 5.x | 2026-07-15 | https://www.typescriptlang.org/docs/ |
| Framework | Next.js App Router | 16.x | 2026-07-15 | https://nextjs.org/docs |
| UI | React | 19.x | 2026-07-15 | https://react.dev |
| Hosting | Vercel | Hobby (non-commercial prototype only); Pro or Cloudflare for commercial | 2026-07-15 | https://vercel.com/docs/plans/hobby |
| DB / Auth | Supabase Postgres + Auth | current JS client + `@supabase/ssr` | 2026-07-15 | https://supabase.com/docs |
| ORM | Drizzle | current | 2026-07-15 | https://orm.drizzle.team |
| Validation | Zod | current | 2026-07-15 | https://zod.dev |
| Bot (optional) | Telegram Bot API | webhook + secret token | 2026-07-15 | https://core.telegram.org/bots/api |
| LLM coach (optional) | Provider TBD; flag off | pin exact model id before enable | 2026-07-15 | provider docs at enable time |

*Re-verify before coding. A sample two majors stale is worse than none.*

### Deprecations & convention changes; DO NOT use the stale form

| ❌ Stale / deprecated | ✅ Current convention | Since (version/date) | Source |
|----------------------|----------------------|----------------------|--------|
| `middleware.ts` as default network boundary | `proxy.ts` exporting `proxy` (Next.js 16+) | Next.js 16.0 | https://nextjs.org/docs/app/api-reference/file-conventions/proxy |
| Supabase `auth-helpers` | `@supabase/ssr` for cookie session on server | 2024+ | https://supabase.com/docs |
| Client-passed `user_id` / `role` | Derive identity from session; enforce RLS + server role check | always | SDD §5 |
| Open-web RAG or LLM for crisis facts | Published pack items only | product lock | RFC pack confinement |
| Vercel Hobby for commercial pilots | Vercel Pro or Cloudflare before paid use | Scrutiny FC-6 | https://vercel.com/docs/plans/hobby |
| Pages Router defaults / `getServerSideProps` patterns | App Router server components, route handlers, server actions | App Router | https://nextjs.org/docs/app |

**Fast-moving deps that require live verification before coding:** Next.js (proxy vs middleware, cache APIs), React 19, `@supabase/ssr`, Drizzle kit migrate commands, Telegram Bot API webhook fields.

**Self-anneal:** when drift is found, add a row here. If behavior changed under a Locked doc, also file a Change Record.

---

## 4. Golden-Path Patterns

> Minimal shapes for this repo. Confirm against §3 pins before copying. Update the sample date when APIs move.

### Rule-engine lesson score  ·  *verified 2026-07-15 against SDD §3*

```ts
// lib/lessons/score.ts
import { z } from 'zod';

const AnswerSchema = z.object({
  vignetteId: z.string().uuid(),
  choseManipulative: z.boolean(),
});

export function scoreAttempt(
  vignettes: { id: string; isManipulative: boolean }[],
  rawAnswers: unknown,
) {
  const answers = z.array(AnswerSchema).parse(rawAnswers);
  const byId = new Map(vignettes.map((v) => [v.id, v]));
  let score = 0;
  const detail = answers.map((a) => {
    const v = byId.get(a.vignetteId);
    if (!v) throw new Error('unknown_vignette');
    const correct = a.choseManipulative === v.isManipulative;
    if (correct) score += 1;
    return { vignetteId: a.vignetteId, correct };
  });
  return { score, maxScore: vignettes.length, detail };
}
```

*Why this shape:* Scoring is pure. No LLM. Zod at the boundary. Ground truth never trusted from the client.

### Published-only pack read  ·  *verified 2026-07-15 against RFC confinement*

```ts
// lib/packs/read.ts
export async function getPublishedPack(db: Db, slug: string) {
  const pack = await db.query.contentPacks.findFirst({
    where: (p, { and, eq }) => and(eq(p.slug, slug), eq(p.status, 'published')),
    with: { items: true },
  });
  if (!pack) return null;
  return pack;
}
```

*Why this shape:* Status filter in the query. Service does not "also allow draft for debugging" on learner paths.

### Session identity + role check  ·  *verified 2026-07-15 against @supabase/ssr pattern*

```ts
// lib/auth/session.ts
export async function requireRole(allowed: Array<'learner' | 'leader' | 'admin'>) {
  const user = await getSessionUser(); // from cookies via @supabase/ssr; never from body
  if (!user) throw new AuthError(401);
  if (!allowed.includes(user.role)) throw new AuthError(403);
  return user;
}
```

*Why this shape:* Identity and role come from the server session. Body fields named `role` are ignored.

### Telegram webhook gate  ·  *verified 2026-07-15 against Bot API secret token*

```ts
// app/api/channels/telegram/webhook/route.ts
export async function POST(req: Request) {
  if (process.env.ENABLE_TELEGRAM_ADAPTER !== 'true') {
    return new Response('disabled', { status: 404 });
  }
  const secret = req.headers.get('x-telegram-bot-api-secret-token');
  if (secret !== process.env.TELEGRAM_WEBHOOK_SECRET) {
    return new Response('unauthorized', { status: 401 });
  }
  const update = TelegramUpdateSchema.parse(await req.json());
  // dedupe update.update_id → adapter.parseInbound → core → render
  return new Response('ok', { status: 200 });
}
```

*Why this shape:* Flag default off. Secret checked before parse. Core services stay channel-agnostic.

---

## 5. Conventions & Guardrails

**Repo layout (target):**
`app/` routes · `components/` UI · `lib/lessons` rule engine · `lib/packs` confinement · `lib/channels` adapters · `lib/auth` session helpers · `db/` Drizzle schema + migrations · `docs/` FMD suite

**Naming:** `PRD-F#` in PR descriptions. Tables snake_case. TypeScript camelCase in app code. Zod schemas colocated with handlers or in `lib/*/schema.ts`.

**Always:**
- Validate external input at the boundary with Zod.
- Enforce role checks on the server. Rely on RLS as backstop, not sole gate.
- Keep lesson scoring deterministic and unit-tested.
- Serve crisis facts only from published packs.

**Never:**
- Commit secrets. Use env vars.
- Use deprecated APIs from §3 because they "look right" from memory.
- Call an LLM for crisis Q&A or pack authoring auto-publish.
- Deploy commercial traffic on Vercel Hobby.
- Trust client `user_id`, `role`, or vignette ground-truth fields.

**Tests:** Every Must-Have ships with QAD happy + sad + abuse coverage once QAD exists. Until then, unit-test `scoreAttempt` and published-only pack reads. Run `pnpm test` (or the repo script once scaffolded) before claiming done.

### Restraint / YAGNI (ponytail)

Before adding code, libraries, or abstractions, stop at the first rung that holds:

1. Does this need to exist? → if no, skip it
2. Already in this codebase? → reuse it
3. Stdlib does it? → use it
4. Native platform feature? → use it
5. Installed dependency? → use it
6. One line? → one line
7. Only then: the minimum that works

**Never on the chopping block:** input validation, error handling, security checks, accessibility, pack confinement, or anything QAD/CLR requires.

**v1 explicit non-builds:** Meltwater, SMS blast, WhatsApp cold templates, TrustOps graph, Redis, job queue, Messenger adapter (until F5 Telegram works).

## 5.1 Brownfield Change Workflow

Greenfield now. When PRD/SDD lock and code is live, prefer the Change Workflow over re-running "Build the FMD":

1. `python D:/PROJECTS/FMD/scripts/change.py init` once per repo (when adopting)
2. `explore change` before proposing on unfamiliar areas
3. `propose change {{slug}}` → validate → review → `apply change` → `verify change` → `archive change`
4. Honor delta specs; merge lands in `docs/specs/`
5. Locked PRD/SDD drift → CR in the same pass as archive

**Definition of Done (one task):**
- [ ] Implements the referenced `PRD-F#` / `US-##` acceptance criteria
- [ ] Approach checked against current docs for security/data/a11y; source cited when non-obvious
- [ ] Restraint ladder applied (§5)
- [ ] Framework conventions verified against §3
- [ ] Tests pass for the touched path
- [ ] No new secrets committed; input validated at boundaries
- [ ] Touched a Locked doc's assumptions? → Change Record logged

**Definition of Done (build / release):** Production Readiness Gate in FMD `AGENTS.md` must pass before calling the build shipped, demo-ready, or done. Commercial host choice must be resolved before paid pilots.

---

## 6. Materialization

| Target | File | Notes |
|--------|------|-------|
| Canonical | `docs/build-pollux.md` | edit here |
| All agents | `AGENTS.md` (project root) | materialize later; parent may run this |
| Claude Code | `CLAUDE.md` | pointer to `AGENTS.md` + Claude-only notes |
| Cursor | `.cursor/rules/build.mdc` | pointer (`alwaysApply: true`) |
| Gemini CLI | `GEMINI.md` | pointer |

Re-materialize whenever this guide changes. Treat root copies as build artifacts, not sources of truth. This repo currently has an FMD **pointer** `AGENTS.md`; replacing it with the materialized BUILD content is a deliberate parent step, not done in this fill.
