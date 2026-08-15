# Contributing to Pollux

Pollux is the open campaign kit an SK officer runs herself. Seekers Guild is the community that keeps this repo. You do not need to join the Guild to contribute. You can help modules, empty templates, and facilitation notes. You cannot publish another barangay's official facts from here.

## Who speaks as whom

- **SK / LGU** owns pack facts, the Facebook Page, and official speech.
- **Pollux** is this campaign kit: modules, a program guide, the return site, and empty templates.
- **Seekers Guild** partners and mentors contributors, especially seekers outside major hubs. Guild does not speak for an SK Page.

If Guild membership were required to run the kit, we failed. Do not add that gate.

## Licenses

- Code: [Apache-2.0](LICENSE)
- Empty template shells (flood / election / notices field lists): CC-BY-4.0 when those files exist
- Outreach kit empty shells (PRD-F15: modules, agendas, activities, facilitation notes, handouts, sources with no live SK facts): CC-BY-4.0, same rule as the empty flood/election shells
- Live SK hotlines, routes, and names: stay with that SK. Do not paste them into a PR "to make the demo look real." That includes `docs/outreach-kit/` Markdown.

## Rungs (lowest first)

1. **Feedback.** Open an issue: what broke on a cheap phone, what the barangay session needed, what the program guide left unclear.
2. **Modules and facilitation notes.** PRs under `docs/outreach-kit/` (modules, print, facilitator notes). Keep them empty of live hotlines, routes, and SK officer names. Kit copy is facilitator material. Maintainers will not merge it as crisis facts or into a canon pack.
3. **Empty templates.** File a template gap (fields, not secrets): "flood packs need river names and pickup points."
4. **Partnership.** Introduce an SK or LGU youth desk. You are a connector, not their publisher.
5. **Product development.** The site students return to after: docs, accessibility, PWA, tests, translations. Prefer work that does not require being in Manila.
6. **Stewardship.** Maintainers review kit vs canon confinement (`pack_kind`: `canon` vs `outreach_kit`). Shared leadership does not mean anyone can mint another barangay's official facts.

## What we will not merge

- Live SK hotlines, routes, or names in kit Markdown or templates
- Kit text treated as SK-official crisis canon (do not copy F15 copy into canon `fact|route|contact` items)
- Open-web RAG or a fact-check model on the crisis path
- A companion or web-surfing agent
- Auto-publish or auto official-share
- Guild branding as the SK Page identity
- A scored lesson that blocks running the kit or publishing a pack

## How to send work

Issues and pull requests against this repository. Keep PRs small. Name the `PRD-F#` you touch. Validate docs with `python D:/PROJECTS/FMD/scripts/check.py D:/PROJECTS/pollux/docs --scale full` when you edit `docs/`.
