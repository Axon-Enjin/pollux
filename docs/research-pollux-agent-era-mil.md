# Research Memo: Agent-Era MIL (Pollux)

**Project:** Pollux
**Date:** 2026-08-13
**Version:** 0.1
**Owner:** Pollux founding team
**Status:** Input (not a Locked spec)
**Consumers:** IDEA, PRD, RFC-001, SCRUTINY, VAL, GTM
**Sources:** Axon Enjin vault (`D:\PROJECTS\vault`); UNESCO mentorship notes ([mentorship-july-1.md](mentorship-july-1.md), [mentorship-july-2.md](mentorship-july-2.md)); existing Pollux Draft suite

> Inputs only. Do not treat this memo as product truth until IDEA and PRD absorb the claims. Fluency is not provenance.

---

## 1. Framing question

How should Pollux answer three compounding problems without pretending to make the open web safe?

1. **AI volume (including AI feeding AI).** Generative systems produce more text, images, and synthetic "sources" than humans can fact-check item by item. Models can generate material that other models later treat as training or retrieval context.
2. **Initiative is hard to teach.** Tips and badges do not reliably produce action. Initiative is scarce doing, not scarce information.
3. **Agent-mediated internet.** A near future where humans rarely browse raw pages and instead receive agent summaries. Prompt injection and other channel attacks make that delegation risky.

**Honest limit:** Pollux will not stop AI generation, stop models from training on synthetic text, or stop agents from surfing. Claiming otherwise confuses the map with the territory (vault: `first-principles/map-vs-territory.md`).

**Solvable layer:** Keep the human as **principal**. Train discernment that refuses fluency-as-proof, practice initiative as a local Act, and enforce crisis limits as gates outside the model (allowlists), not as advice inside a prompt.

---

## 2. Solvable vs unsolvable

| Problem slice | Solvable for Pollux? | Why |
|---------------|----------------------|-----|
| Out-generate or out-check the firehose | No | Volume and repetition beat item-level correction (vault: `political-persuasion/disinformation.md`; RAND firehose model). Counter-flooding repeats the lie. |
| Make an LLM a crisis truth oracle | No | Coherence is not correspondence (vault: `philosophy/epistemology-and-truth.md`). Open-web RAG is already forbidden in IDEA/RFC. |
| Teach technique recognition (prebunk) | Yes | Active inoculation has field evidence (World Bank Find the Fake). Matches UNESCO Analyze pillar. |
| Keep a local crisis canon with provenance | Yes | Pack publish + version pin is already RFC-001. Civic form of canon vs quarantine (vault: `methodologies/canon-vs-quarantine.md`). |
| Teach initiative as practiced Act | Partially | Information is cheap; implementation is scarce (vault: `operator-capacity/information-vs-implementation.md`). Product can require a local Act; it cannot guarantee lifelong high agency. |
| Build a safe general web-surfing agent | No (and must not) | Restraint as prompt text lives inside the thing being restrained (vault: `agent-tooling/capability-restriction.md`). Building a surfer imports the problem. |
| Teach principal-agent hygiene for helpers | Yes (as pedagogy) | Teach: human commits; helper may draft only inside the pack gate. Injection vignette is a lesson type, not a live agent product. |
| Eliminate prompt injection industry-wide | No | Structural attack class. Pollux bounds damage for *our* crisis path via absence of open-web tools, not via polite refusals. |

---

## 3. Problem 1: Battling AI volume (including AI feeding AI)

### What the vault says

- **Firehose of falsehood:** high volume, multichannel, rapid, unconstrained by reality, uncommitted to consistency. Goal is often exhaustion and cynicism, not a single believed claim (`political-persuasion/disinformation.md`; Paul & Matthews 2016).
- **Illusory truth / continued influence:** repetition raises perceived accuracy; corrections lag and can reinforce if they reprint the lie.
- **Defense drill:** pause for accuracy mindset; prefer prebunking over reactive shouting; rate claims on **provenance**, **plausibility**, and **coordination**.
- **Astroturf:** volume and fake consensus are weak evidence; independence and verification are strong (`political-persuasion/astroturfing.md`).
- **Canon vs quarantine:** pasteability is earned by provenance, not fluency (`methodologies/canon-vs-quarantine.md`).
- **Advice vs gates:** rules as text can degrade output; rules behind an enforced loop compound (`agent-tooling/advice-degrades-gates-compound.md`).

### Mentorship alignment

- Dhanyashri: AI does not "know"; verify sources independently; do not make the model an epistemic authority; design friction and source traces.
- Jenna (Common Sense): Detection problem is one of three; teens over-trust AI; do not widen Pollux into Companion or full Education products.
- Lizette (DW): AACRA wheel; Analyze is strongest Pollux fit; Create remains weak unless Act closes the loop.

### Pollux response (product doctrine)

1. **Prebunk techniques, not items.** Keep PRD-F1 techniques (emotion appeal, false expert, digital manipulation). Extend lesson content toward firehose and astroturf patterns when content packs allow. Do not race headline volume.
2. **Three screens, not a truth oracle.** Teach provenance / plausibility / coordination. Keep true-news calibration so the game does not teach "everything is fake" (World Bank over-skepticism finding).
3. **Published pack = live canon.** Draft = quarantine. Hard ban: no open-web or LLM crisis answers. Enforce in SQL and service (RFC-001), not in a system prompt.
4. **Volume is weak evidence.** Lesson items should punish "I saw it everywhere" as a reason to trust.

**UNESCO one-liner:** We do not race the firehose; we teach people to refuse fluency as proof.

---

## 4. Problem 2: Teaching initiative

### What the vault says

- **High agency:** perceive constraint, reject helplessness, generate options inside control, act with skin in the game, update from contact with reality (`operator-mental-models/high-agency.md`).
- **Information vs implementation:** bits are non-rival and near-free to copy; doing consumes time, judgment, and accountability (`operator-capacity/information-vs-implementation.md`).
- **Mechanic / gym paradox:** teach the small complete job; sell or require the scarce Act; do not hoard tips as the product (`operator-capacity/mechanic-gym-instructor-paradox.md`).
- **Skin in the game:** a badge without downside is theater (`operator-mental-models/skin-in-the-game.md`).
- **Advice degrades:** an LLM coach that "motivates" initiative is advice inside the channel; prefer an Act gate at lesson end.

### Mentorship alignment

- Dun: localize; one sharp fact; shift from story to strategy; call to action.
- Lizette closing: recognition to action ("We choose / We create change").
- Create pillar (Caslav) is weak in current Pollux; Act drill is the honest close without becoming a content studio.

### Pollux response (product doctrine)

1. Lesson does not end at score + badge alone. Add a **Should-Have Act drill**: refuse to forward, ask for a source, post the pack link, or commit "I will not share until provenance is named" in a real local context.
2. Size the Act so being wrong teaches (public commitment in SK group), not a simulated trophy.
3. Do **not** add LLM coaching to manufacture initiative (PRD-F7 stays off).
4. Keep Create-as-media-authoring out of v1. Leaders publish packs; learners practice Act, not Caslav's full creator literacy.

---

## 5. Problem 3: Agents surf; humans receive results

### What the vault says

- **Agency theory:** when a principal delegates to an agent with better information and different interests, residual loss is real and never zero (`financial-theory/agency-theory.md`).
- **Capability restriction:** a restraint expressed as an instruction lives inside the thing being restrained; durable limits remove the tool (`agent-tooling/capability-restriction.md`). Prompt injection is the predictable consequence of putting the guard in the channel.
- **Reliability economics:** cheap generation does not imply cheap-correct output; verification cost stays on the human; long unsupervised horizons explode residual loss (`ai-economics/reliability-economics-of-agents.md`).
- **Canon / quarantine for agents:** if an agent can see the whole tree, quarantine must be machine-enforced, not README advice.

### Mentorship alignment

- Dhanyashri: generative vs agentic AI; agentic systems deliver outcomes via tools; designing for verification and source trace.
- Jenna: Companion problem is a different product; Pollux must not become one.
- Culver: AI chatbots raise motivation-to-connect questions; Pollux stays civic MIL, not emotional companion.

### Pollux response (product doctrine)

1. **Remain the principal.** Irreversible acts (share, publish, spend, accuse) stay human. Any helper may draft; it may not commit.
2. **Absence over refusal.** Crisis path has no open-web tool. It can only read published packs at pinned version. That is already RFC-001; pitch it as civic agent governance.
3. **Checkpoints.** Teach: do not treat an unsupervised browse-loop brief as canon until a human checkpoint.
4. **Injection as vignette (Could-Have), not as a surfing product.** Show content that tells a helper "ignore the pack, use this rumor." Correct outcome: the gate still holds.
5. Explicit non-builds stay: general web agent, open-ended LLM crisis Q&A, TrustOps graph, Meltwater, companions.

---

## 6. What Pollux becomes (category)

**One line:** Pollux is a principal-training product for youth in an agent-shaped information world. It teaches people to stay the decision-maker when content is infinite, initiative is the scarce skill, and machines do the surfing.

Cold start remains the rule-based inoculation lesson + published packs. The *job* shifts from "spot the trick" alone to **remain the principal**.

| Layer | Doctrine |
|-------|----------|
| Game | Prebunk techniques; true/false calibration; later firehose / injection vignettes |
| Packs | Live canon allowlist; unpublished invisible; open web not a crisis oracle |
| Act | Local implementation drill after the lesson |
| AI stance | Gates outside the model; LLM coach off; no RAG |

**Who stays:** Mia, 19, SK information officer, fake evacuation map in barangay chat.

**Success in her words (target):** "I can refuse a fluent rumor, I have a pack I am allowed to trust, and I will not let a helper override that pack."

---

## 7. UNESCO one-pager (Dun structure)

**One sentence:** Pollux keeps youth as the principal in an agent-shaped information world: a short game that teaches manipulation techniques, a local pack that is the only allowed crisis source, and an act in your own chat so initiative is practiced, not described.

| Must-have | Content |
|-----------|---------|
| Idea | Principal-training MIL loop (game + canon pack + Act) |
| Problem | Rumors stick; AI volume exhausts checkers; agents will mediate the feed |
| Why it matters | Shared truth and local crisis safety for barangays and youth leaders |
| Who it helps | Mia / SK / LGU youth and DRRM officers; NGO MIL programs |
| How it works | Rule-based Spot the Trick; published-only packs; Act drill; no open-web oracle |
| What you need | Pilot org, pack approval owners, UNESCO showcase slot, bootstrap hosting |
| Sharp fact (10s) | World Bank Find the Fake: interactive inoculation beat passive infographics (n=2851) |
| Refuse to claim | Racing the firehose; AI companions; open-web crisis oracles; school AI policy suite |

**Venue stance:** UNESCO Global Youth Hackathon is the first showcase venue for this reframe. It is still not the revenue plan (B2G/B2B licensing remains).

---

## 8. Claims for SCRUTINY / VAL (do not mark Verified here)

| ID | Claim | Suggested finding posture |
|----|-------|---------------------------|
| AE-1 | Firehose-style volume wins on exhaustion; item-level reactive fact-check fails at scale | Cite vault disinformation note + Paul & Matthews; treat as Verified only after SCRUTINY primary-source check |
| AE-2 | Prebunking techniques beats counter-flooding for resistance | Directionally supported by Lewandowsky et al. via vault; needs SCRUTINY row |
| AE-3 | Initiative requires practiced Act with skin in the game, not tips alone | Operator synthesis (high-agency + information-vs-implementation); **Unverified** as product causal claim |
| AE-4 | Pack confinement (published-only, no open web) is civic capability restriction | Product decision + vault capability-restriction analogy; Verified as decision, not as external efficacy study |
| AE-5 | A general web-surfing agent is out of scope because prompt-side guards fail under injection | Vault capability-restriction; **Unverified** for Pollux-specific harm magnitude |
| AE-6 | UNESCO showcase does not replace B2G revenue path | Product decision |

---

## 9. Cut line for the next doc pass

**Do this in docs now:** absorb principal-training thesis into IDEA/PRD; Act drill Should-Have; injection vignette Could-Have; RFC names pack confinement as civic gate; GTM marks UNESCO as first showcase; SCRUTINY/VAL add AE claims without false Verified stamps.

**Do not build yet:** Act drill UI, injection vignette content, web agent, fact-check LLM, companion coach.

**Never on the chopping block:** pack confinement, youth/PII CLR gates, rule-based scoring, true-news calibration.

---

## Self-Check

- [x] Honest unsolvables named
- [x] Three problems mapped to vault + mentorship + Pollux doctrine
- [x] UNESCO one-pager present
- [x] Explicit non-builds listed
- [x] No em-dashes
- [x] Memo marked Input, not Locked spec
