# Pollux

[![Status: Draft](https://img.shields.io/badge/Status-Draft-yellow)](docs/index.md)
[![Stack: Next.js](https://img.shields.io/badge/Stack-Next.js%20%2B%20Supabase-black)](docs/idea-pollux.md)
[![Docs: FMD](https://img.shields.io/badge/Docs-FMD%20v1.19.0-333)](docs/index.md)

Pollux teaches youth to spot manipulation techniques through a short gamified lesson, and gives local youth leaders a lightweight way to publish verified crisis facts without paying for messaging or enterprise listening tools.

Built with the [Foundational Matrix Documents (FMD)](https://github.com/delatorrecj/fmd) workflow (v1.19.0).

## Quick start

```bash
# App scaffold lands with BUILD. Until then, docs-only:
cd docs
# Validate FMD suite when the local engine is available:
python D:/PROJECTS/FMD/scripts/check.py .
```

**Requirements:** Node 20+ and pnpm when the Next.js app exists. Python 3.11+ for `check.py`.

## What it does

- Rule-based inoculation game on a mobile-first PWA (score + badges)
- Curated, versioned crisis/MIL content packs (no open-web RAG)
- SK / youth-leader admin lite: publish packs, keyword watch, share links
- Auth with learner / leader / admin roles
- Optional Telegram bot for the same game loop (user-initiated)

## Documentation

| Doc | Purpose |
|-----|---------|
| [IDEA](docs/idea-pollux.md) | Spark, cut line, concept visuals |
| [SCRUTINY](docs/scrutiny-pollux.md) | Gate verdict and carry-in fixes |
| [QAD](docs/qad-pollux.md) | Test plan |
| [CLR](docs/clr-pollux.md) | Compliance register (not legal advice) |
| [AIA](docs/aia-pollux.md) | AI assurance (rule-based primary) |
| [OPS](docs/ops-pollux.md) | Runbook, SLOs, rollback |
| [Index](docs/index.md) | Full doc manifest |

**Bootstrap doctrine:** no paid messaging until a buyer funds it; free-tier host for pre-revenue; commercial pilots need Vercel Pro or Cloudflare Pages. See OPS and IDEA.

**Living design files:** `BRAND.md` / `DESIGN.md` when DSD materializes.

## Demo

Open the PWA (when deployed) → finish Spot the Trick → as leader, open a flood pack and copy a share link. Burn note: $0 messaging. Full script lives in IDEA §4.

## Team

Pollux founding team · startup build · UNESCO Youth Hackathon optional distribution only

## License

TBD; add `LICENSE` before public release.

---

*README materialized from FMD README_Template.md · 2026-07-15*
