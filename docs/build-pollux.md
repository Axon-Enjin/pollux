# Project Build Guide

**Project:** Pollux
**Date:** 2026-08-16
**Version:** 0.2
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled with code)

> **STALE vs PRD 0.5 (2026-08-16):** v1 Must-Have is the campaign kit (PRD-F15): modules, run-of-show, print, student return. Canon desk (F1/F3) and commit share (F10) are later. Dual `pack_kind` allowlists in this RFC still apply. Do not implement desk-first golden paths as the product. Reconcile this file before code.

**PRD:** [prd-pollux.md](prd-pollux.md)
**SDD:** [sdd-pollux.md](sdd-pollux.md)
**SAD:** N/A (no SAD yet; main agent builds inline)

> Spec → code bridge. Canonical file. Materialize to root `AGENTS.md` later (parent owns materialization). Edit here; do not hand-edit root copies as source of truth.

---

## 1. How to Build From These Docs

The documentation suite is the source of truth. Read in this order before writing code:

1. [`docs/index.md`](index.md). What exists, status, staleness.
2. [IDEA](idea-pollux.md) + [SCRUTINY](scrutiny-pollux.md). Product lock and carried fixes.
3. [PRD](prd-pollux.md). Features and acceptance. F1 is the canon desk. F12 is the optional inoculation drill (Could-Have; former F1 meaning is stale-labeled). F15 is the outreach kit.
4. [SDD](sdd-pollux.md). Schema, APIs, security, optional AI. Dual `pack_kind` (`canon` vs `outreach_kit`).
5. [RFC channel-packs](rfc-pollux-channel-packs.md). Adapter interface, pack confinement, dual allowlists. For F15 also [docs/outreach-kit/_STACK.md](outreach-kit/_STACK.md).
6. [DSD](dsd-pollux.md). Visual rules when present.
7. [QAD](qad-pollux.md). Tests before calling a feature done.
8. [CLR](clr-pollux.md) / [AIA](aia-pollux.md). Before public launch or enabling LLM coach.
9. [OPS](ops-pollux.md). Before production pilot.
10. This guide. Stack conventions, golden paths, guardrails.

**Only build against `Locked` docs.** These eng docs are `Draft`. Flag that before large implementation. If reality diverges from a Locked doc later, write a Change Record (`docs/cr-*.md`). Do not silently code around it.

### Traceability map; "to build X, read Y"

| To implement… | Read | Then verify against |
|---------------|------|---------------------|
| Canon desk (PRD-F1) | PRD feature + SDD §3/§4 pack APIs + RFC publish | Org space; clone templates; empty local fields; unpublished invisible |
| Content packs (PRD-F2) | SDD §3 packs + [RFC](rfc-pollux-channel-packs.md) confinement | Unpublished invisible; `pack_kind = canon` on crisis paths; no RAG |
| SK self-launch kit (PRD-F3) | SDD §4 leader APIs + RFC publish workflow | Role checks; share pin version; not F15 |
| Auth roles (PRD-F4) | SDD §5 | RLS + server role check; ignore client `role` |
| Telegram adapter (PRD-F5) | RFC `ChannelAdapter` + webhook contract | Secret header; flag default off |
| Outreach / seminar kit (PRD-F15) | PRD + SDD + [RFC](rfc-pollux-channel-packs.md) + [docs/outreach-kit/_STACK.md](outreach-kit/_STACK.md) | Published `outreach_kit` only; `ENABLE_OUTREACH_KIT` default off (404); kit never blocks F1/F3 launch; not F3, not F12, not canon facts |
| Optional inoculation drill (PRD-F12, Could-Have; stale-labeled former F1) | PRD feature + SDD §3 (`lessons`, `vignettes`, `attempts`) + rule engine notes | QAD happy/sad/abuse for scoring if it ships; not the v1 brand |
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
| Hosting | Cloudflare Pages/Workers (commercial); Vercel Hobby optional for non-commercial proto | Cloudflare locked G-3 | 2026-07-15 | https://developers.cloudflare.com/pages/ |
| DB / Auth | Supabase Postgres + Auth | current JS client + `@supabase/ssr` | 2026-07-15 | https://supabase.com/docs |
| ORM | Drizzle | current | 2026-07-15 | https://orm.drizzle.team |
| Validation | Zod | current | 2026-07-15 | https://zod.dev |
| Bot (optional) | Telegram Bot API | webhook + secret token | 2026-07-15 | https://core.telegram.org/bots/api |
| LLM coach (optional, post-MVP) | Provider TBD; flag off | pin exact model id before enable | 2026-07-15 | provider docs at enable time |

*Re-verify before coding. A sample two majors stale is worse than none.*

### Deprecations & convention changes; DO NOT use the stale form

| ❌ Stale / deprecated | ✅ Current convention | Since (version/date) | Source |
|----------------------|----------------------|----------------------|--------|
| `middleware.ts` as default network boundary | `proxy.ts` exporting `proxy` (Next.js 16+) | Next.js 16.0 | https://nextjs.org/docs/app/api-reference/file-conventions/proxy |
| Supabase `auth-helpers` | `@supabase/ssr` for cookie session on server | 2024+ | https://supabase.com/docs |
| Client-passed `user_id` / `role` | Derive identity from session; enforce RLS + server role check | always | SDD §5 |
| Open-web RAG or LLM for crisis facts | Published pack items only (`pack_kind = canon`) | product lock | RFC pack confinement |
| Inoculation game as PRD-F1 / v1 primary | F1 = canon desk; F12 = optional drill (Could-Have, stale-labeled) | PRD 2026-08 | PRD ID note |
| Pack / kit read without `pack_kind` | `getPublishedPack` filters `canon`; `getPublishedKit` filters `outreach_kit` + `ENABLE_OUTREACH_KIT` | RFC dual allowlists | RFC + SDD §3 |
| Vercel Hobby for commercial pilots | Cloudflare Pages/Workers before paid use (Vercel Pro alternate) | Scrutiny FC-6 / G-3 | https://developers.cloudflare.com/pages/ |
| Pages Router defaults / `getServerSideProps` patterns | App Router server components, route handlers, server actions | App Router | https://nextjs.org/docs/app |

**Fast-moving deps that require live verification before coding:** Next.js (proxy vs middleware, cache APIs), React 19, `@supabase/ssr`, Drizzle kit migrate commands, Telegram Bot API webhook fields.

**Self-anneal:** when drift is found, add a row here. If behavior changed under a Locked doc, also file a Change Record.

---

## 4. Golden-Path Patterns

> Minimal shapes for this repo. Confirm against §3 pins before copying. Update the sample date when APIs move.

### Rule-engine lesson score (PRD-F12 Could-Have; stale-labeled former primary)  ·  *verified 2026-07-15 against SDD §3*

Do not treat this as the v1 golden path. Keep the shape if F12 ships. Do not call it from kit or canon-desk routes.

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

### Published-only pack read  ·  *verified 2026-08-16 against RFC confinement*

```ts
// lib/packs/read.ts
export async function getPublishedPack(db: Db, slug: string) {
  const pack = await db.query.contentPacks.findFirst({
    where: (p, { and, eq }) =>
      and(eq(p.slug, slug), eq(p.status, 'published'), eq(p.packKind, 'canon')),
    with: { items: true },
  });
  if (!pack) return null;
  return pack;
}
```

*Why this shape:* Status and `pack_kind` filters in the query. Crisis and commit-share never see `outreach_kit`. Service does not "also allow draft for debugging" on learner paths.

### Published-only kit read (PRD-F15)  ·  *verified 2026-08-16 against RFC dual allowlists*

```ts
// lib/kits/read.ts
export async function getPublishedKit(db: Db, slug: string) {
  if (process.env.ENABLE_OUTREACH_KIT !== 'true') {
    return null;
  }
  const pack = await db.query.contentPacks.findFirst({
    where: (p, { and, eq }) =>
      and(
        eq(p.slug, slug),
        eq(p.status, 'published'),
        eq(p.packKind, 'outreach_kit'),
      ),
    with: { items: true },
  });
  if (!pack) return null;
  return pack;
}
```

*Why this shape:* Same published-only gate as `getPublishedPack`, plus `pack_kind = outreach_kit`. Flag default off. Kit routes 404 when the flag is not `true`. Do not reuse `scoreAttempt` or `attempts`. Kit completion never blocks F1/F3 launch.

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
`app/` routes · `components/` UI · `lib/lessons` rule engine (F12 Could-Have only) · `lib/packs` canon confinement · `lib/kits` outreach-kit confinement · `lib/channels` adapters · `lib/auth` session helpers · `db/` Drizzle schema + migrations · `docs/` FMD suite · `docs/outreach-kit/` F15 authoring home (`_STACK.md` is the sequence)

**Naming:** `PRD-F#` in PR descriptions. Tables snake_case. TypeScript camelCase in app code. Zod schemas colocated with handlers or in `lib/*/schema.ts`.

**Always:**
- Validate external input at the boundary with Zod.
- Enforce role checks on the server. Rely on RLS as backstop, not sole gate.
- Keep F12 lesson scoring deterministic and unit-tested if that Could-Have ships.
- Serve crisis facts only from published packs with `pack_kind = canon`.
- Serve kit catalog / get / session / print only from published packs with `pack_kind = outreach_kit`. Gate those routes with `ENABLE_OUTREACH_KIT` (default off; not `true` means 404).

**Never:**
- Commit secrets. Use env vars.
- Use deprecated APIs from §3 because they "look right" from memory.
- Call an LLM for crisis Q&A or pack authoring auto-publish.
- Deploy commercial traffic on Vercel Hobby.
- Trust client `user_id`, `role`, or vignette ground-truth fields.
- Treat the inoculation game as the v1 brand or primary path (PRD-F12 is Could-Have; stale-labeled former F1).
- Mix `outreach_kit` items into crisis Q&A or commit-share. Mix canon `fact`/`route`/`contact`/`faq`/`media` into kit paths.
- Turn `ENABLE_OUTREACH_KIT` on by default. Call `scoreAttempt` or write `attempts` from kit routes. Let kit completion block F1/F3 launch.

**Tests:** Every Must-Have ships with QAD happy + sad + abuse coverage once QAD exists. Until then, unit-test `getPublishedPack` (canon) and `getPublishedKit` (`outreach_kit` + flag off). Keep `scoreAttempt` tests only if F12 is in scope. Run `pnpm test` (or the repo script once scaffolded) before claiming done.

### Restraint / YAGNI (ponytail)

Before adding code, libraries, or abstractions, stop at the first rung that holds:

1. Does this need to exist? → if no, skip it
2. Already in this codebase? → reuse it
3. Stdlib does it? → use it
4. Native platform feature? → use it
5. Installed dependency? → use it
6. One line? → one line
7. Only then: the minimum that works

**Never on the chopping block:** input validation, error handling, security checks, accessibility, pack confinement (canon vs `outreach_kit`), or anything QAD/CLR requires.

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
