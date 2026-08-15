# Contributing to Pollux

Pollux is an aide SK and LGU youth desks launch themselves. Seekers Guild is the community that stewards this repo. You do not need to join the Guild to contribute. You cannot publish another barangay's official facts from here.

## Who speaks as whom

- **SK / LGU** owns pack facts, the Facebook Page, and official speech.
- **Pollux** is this product: templates, version pin, human commit before official share.
- **Seekers Guild** recruits and mentors contributors, especially seekers outside major hubs.

If Guild membership were required to launch an SK pack, we failed. Do not add that gate.

## Licenses

- Code: [Apache-2.0](LICENSE)
- Empty template shells (flood / election / notices field lists): CC-BY-4.0 when those files exist
- Live SK hotlines, routes, and names: stay with that SK. Do not paste them into a PR "to make the demo look real."

## Rungs (lowest first)

1. **Feedback.** Open an issue: what broke on a cheap phone, what the barangay actually needed, what the pause before share should ask.
2. **Local knowledge as templates.** File a template gap (fields, not secrets): "flood packs need river names and pickup points."
3. **Partnership.** Introduce an SK or LGU youth desk. You are a connector, not their publisher.
4. **Product development.** Docs, accessibility, PWA, tests, translations. Prefer work that does not require being in Manila.
5. **Stewardship.** Maintainers review publish-path security and pack confinement. Shared leadership does not mean anyone can bypass the human-commit gate.

## What we will not merge

- Open-web RAG or a fact-check model on the crisis path
- A companion or web-surfing agent
- Auto-publish or auto official-share
- Guild branding as the SK Page identity
- A game as a blocker to launch a pack

## How to send work

Issues and pull requests against this repository. Keep PRs small. Name the `PRD-F#` you touch. Validate docs with `python D:/PROJECTS/FMD/scripts/check.py D:/PROJECTS/pollux/docs --scale full` when you edit `docs/`.
