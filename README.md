# Pollux

[![Status: Draft](https://img.shields.io/badge/Status-Draft-yellow)](docs/index.md)
[![Stack: Next.js](https://img.shields.io/badge/Stack-Next.js%20%2B%20Supabase-black)](docs/idea-pollux.md)
[![Docs: FMD](https://img.shields.io/badge/Docs-FMD%20v1.19.0-333)](docs/index.md)

Pollux is the open campaign kit an SK officer runs herself: modules, a program guide, and a site students return to after.

Seekers Guild partners. Guild does not speak for an SK Page. Materials are open source. There is no paywall.

Built with the [Foundational Matrix Documents (FMD)](https://github.com/delatorrecj/fmd) workflow (v1.19.0).

## Quick start

Campaign materials live in [`docs/outreach-kit/`](docs/outreach-kit/00-INDEX.md) (modules, facilitator notes, print packet).

```bash
# App scaffold lands with BUILD. Until then, docs-only:
cd docs
# Validate FMD suite when the local engine is available:
python D:/PROJECTS/FMD/scripts/check.py .
```

**Requirements:** Node 20+ and pnpm when the Next.js app exists. Python 3.11+ for `check.py`.

## What it does

- She runs the modules herself: camp or barangay sessions from a published kit
- A program guide (facilitator notes, run of show, print packet) so a second officer can run the same session
- A site students return to after the session
- Official crisis facts stay on that SK's published pack, not in kit Markdown
- Open contribution: modules, empty templates, facilitation notes ([CONTRIBUTING.md](CONTRIBUTING.md))
- Guild partners on the kit. Guild is not the brand on her Page

Code: Apache-2.0. Empty templates and kit shells: CC-BY-4.0. SK-published facts stay with that SK.

## Documentation

| Doc | Purpose |
|-----|---------|
| [Outreach kit](docs/outreach-kit/00-INDEX.md) | Modules, program guide, print packet |
| [IDEA](docs/idea-pollux.md) | Spark, cut line, concept visuals |
| [SCRUTINY](docs/scrutiny-pollux.md) | Gate verdict and carry-in fixes |
| [QAD](docs/qad-pollux.md) | Test plan |
| [CLR](docs/clr-pollux.md) | Compliance register (not legal advice) |
| [AIA](docs/aia-pollux.md) | AI assurance (no model on kit or crisis facts) |
| [OPS](docs/ops-pollux.md) | Runbook, SLOs, rollback |
| [Index](docs/index.md) | Full doc manifest |

**Bootstrap doctrine:** no paid messaging until a buyer funds it; free-tier host for pre-revenue; commercial pilots use Cloudflare Pages/Workers. See OPS and IDEA.

**Living design files:** `BRAND.md` / `DESIGN.md` when DSD materializes.

## Demo

Open the [kit index](docs/outreach-kit/00-INDEX.md). Run a module from the program guide or print packet. After the session, students return to the site. Showcase script lives in [docs/pitch-pollux.md](docs/pitch-pollux.md).

## Team

Pollux founding team. Seekers Guild is the community around this repo. UNESCO Youth Hackathon 2026 is a showcase.

## License

[Apache-2.0](LICENSE). See [CONTRIBUTING.md](CONTRIBUTING.md).

---

*README materialized from FMD README_Template.md · 2026-07-15*
