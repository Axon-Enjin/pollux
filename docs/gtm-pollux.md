# Go-To-Market (GTM) Strategy

**Project:** Pollux
**Date:** 2026-08-16
**Version:** 0.5
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A (not yet reconciled with code)
**PRD:** [prd-pollux.md](prd-pollux.md)
**UES:** [ues-pollux.md](ues-pollux.md)
**Research input:** [research-pollux-agent-era-mil.md](research-pollux-agent-era-mil.md)
**Outreach kit (PRD-F15):** [outreach-kit/README.md](outreach-kit/README.md)

---

## 1. Product Summary (GTM View)

**One-liner:** Pollux is the open campaign kit an SK officer runs herself: modules, a program guide, and a site students return to after.

**UVP:** For SK and LGU youth officers who need an outreach or bootcamp this week and do not know where to start, Pollux is the open campaign kit: teachable modules, a run-of-show, logistics, and a site students can keep using. Unlike a blank Facebook event or a paid vendor workshop. Materials stay free.

**Who it's for:** SK officers and LGU youth officers who must run outreach and have no program. Seekers Guild is a partner channel (facilitation, intros, contribution), not the buyer and not the Page brand.

**Category:** Civic tech / SK campaign operations / MIL open toolkit (UNESCO narrative). Not a fact-check vendor. Not a paid workshop shop.

---

## 2. Target Audience

**Primary ICP (Ideal Customer Profile):**
- *Who:* SK officer (or LGU youth officer) who must run outreach or a bootcamp this week and has no program
- *Where they hang out:* SK federation chats, barangay halls, LGU youth desks, campus orgs, Saturday outreach
- *What they already believe:* They are supposed to "do MIL" or youth outreach. A blank Facebook event is not a program. A Manila vendor workshop is late and priced for someone else.
- *What will make them try this:* A printable packet plus a run-of-show they can run Saturday without a founder in the room. Students can open the same modules after, with no paywall.

**Secondary audience:**
- *Who:* Seekers Guild members and provincial seekers
- *Why secondary:* Partner channel. They co-facilitate, introduce SK desks outside the big cities, and contribute kit fixes. They do not own the SK Page. Guild membership is not required to run a session.

**Channel audience (PRD-F15):**
- *Who:* Facilitator at barangay outreach, youth camp, or SK federation (leader, or a trained Guild partner with kit access). Participants are learners.
- *Why a channel, not the ICP:* The officer still owns the session. Guild helps run it when invited. Kit text is not SK-official crisis canon.

**Tertiary audience:**
- *Who:* LGU or city desk that wants hosted install later (DFY B2G)
- *Why tertiary:* Paid path after the open kit works. Not v1 revenue. Does not paywall the open materials.

**TBD (Scrutiny G-1):** First named SK council that will run a Saturday session. First federation venue. Resolve before claiming a live campaign.

**Unit hierarchy (services ladder):** See §3. Do not require Guild membership to run DIY. Do not quote vendor workshop seats as the v1 metric.

---

## 3. Pricing Model and Services Ladder

**Model:** Open campaign kit is free. Paid is DFY hosted later, not a kit paywall. Honor UES-D1. Do not sell the kit as a fact-check product.

| Rung | Name | Price | What's included | Gate / note |
|------|------|-------|-----------------|-------------|
| 1 | DIY campaign kit | $0 | Teachable modules, run-of-show, logistics notes, print packet, site students keep using | UNESCO Must-Have. Materials stay free. |
| 2 | DWY runner | $0 when on | In-app facilitator cockpit + participant view (`ENABLE_OUTREACH_KIT`) | Later flag. Default off until PRD-F15 ships. Does not block DIY print. |
| 3 | Guild partnership | $0 | Co-facilitation, SK intros, provincial contribution, trained runners | Partner channel. Not Page brand. Not required to run DIY. |
| 4 | Official pack desk | Later / side | SK publishes local official facts; human commit before official share | Side path, not the campaign-kit headline. |
| 5 | DFY B2G | Later (UES-E1 band when quoted) | Hosted install + training for an LGU or SK office | First paid ACV later. No paywall on open materials. |

**Pricing rationale:** UNESCO "open toolkit" is rung 1, not a SKU. Closing the repo is not a revenue plan. Free DIY does not require an LOI. Paid DFY names a conversion path at kickoff without locking modules behind a fee.

**Payment processor:** Invoice / grant first; Stripe later.

**Commercial host:** Cloudflare Pages/Workers before first paid invoice (Scrutiny G-3).

---

## 4. Positioning & Messaging

**Tagline:** They run the session. We pack the bag.

**Primary message:** She has to run outreach this week. Pollux packs modules, a program guide, logistics, and a site students return to after. She runs it. A blank event page is not a curriculum. A paid vendor is not the only option. Seekers Guild partners with youth desks, especially outside the big cities.

**Jury + UNESCO showcase:** Pollux is the open campaign kit SK councils run themselves. Seekers Guild partners with youth desks, especially outside the big cities. Modules, program guide, and student access stay free.

**Three examples (tell these, in this order):**

1. **Barangay 45 minutes, SK San Roque, Saturday.** Mia prints the packet Friday. Saturday she runs the modules with a run-of-show. No vendor. No founder. Students leave with a URL they can open again.
2. **Federation half-day + Guild facilitator.** A city SK federation books a half-day. A Seekers Guild partner co-facilitates. The federation still owns the session. Guild is not on their Page.
3. **Student opens modules after, no paywall.** A learner who missed a station, or wants to show a sibling, opens the same modules on the site. No account wall for the open kit. No "pay to finish."

**Proof points:**
- UNESCO MIL as a session she can run, not a MOOC she cannot staff ([MIL programme](https://www.unesco.org/en/media-information-literacy))
- Open toolkit: sequenced modules + run-of-show + print if 3G dies (PRD-F15; Must-Have for the UNESCO toolkit story)
- Students keep using the site after the Saturday clock
- Launch-without-us: an SK officer runs DIY without Guild membership
- Bootstrap burn doctrine: no paid messaging until a buyer funds it
- Guild partnership is facilitation and intros, not barangay voice

**Objection handling:**

| Objection | Response |
|-----------|----------|
| "We already posted a Facebook event." | An event is a time slot. The kit is the program: modules, run-of-show, logistics, and a site after. |
| "We will hire a workshop vendor." | You can. Materials here stay free. DIY is for the Saturday she cannot wait or cannot pay. |
| "Is this a Seekers Guild app?" | Guild is a partner channel. SK runs the session. Guild is not the Page brand. DIY does not require joining. |
| "Another MIL quiz." | The product is a campaign kit she runs. Scoring a game is not the headline. |
| "So you sell a fact-check kit?" | No. Rung 1 is free. Paid is hosted DFY later. Open modules are not the paywall. |
| "Did they finish the module?" | Useful for a facilitator note. Success is a session that ran and a site students still open. |

---

## 5. Launch Channels & Tactics

**Owned channels:**

| Channel | Audience Size | Planned Action |
|---------|--------------|----------------|
| Founder network / SK contacts | TBD | Book 3 "can you run Saturday?" conversations |
| Product landing + README | Public | DIY kit CTA; no vendor pitch |
| GitHub (Apache-2.0) | Public | Issues + module / packet PRs |
| DIY print packet | SK / barangay facilitators | Ship printable packet as rung 1 |

**Community / earned channels:**

| Channel | Tactic | Timing |
|---------|--------|--------|
| Barangay outreach | Example 1: 45-minute Saturday with print | After packet is usable |
| SK federations | Example 2: half-day; optional Guild facilitator | After first barangay run |
| Student site | Example 3: modules stay open after the session | With DIY packet |
| Seekers Guild | Partner channel: intros, co-facilitate, provincial desks | Ongoing; not a publish gate; not Page brand |
| UNESCO Youth Hackathon | First showcase of the open campaign kit + Guild partnership | 16 Aug 2026 23:59 Paris deadline for this edition |
| NGO MIL partners | Co-run sessions, not a fact-check retainer | After first DIY run |

**Content assets needed before launch:**

- [ ] Demo: officer runs a 45-minute barangay session from the packet (not a rumor-tap headline)
- [ ] Landing page: UVP + tagline + three examples; kit free
- [ ] README that stands alone as DIY start
- [ ] UNESCO proposal + 3-min pitch ([pitch-pollux.md](pitch-pollux.md)); jury sentence as in §4
- [ ] DIY print packet (facilitator one-pager, learner handout, consent stub) from [outreach-kit/print](outreach-kit/print)
- [ ] Camp / outreach run-of-show ([outreach-kit/facilitator/3ds-run-of-show.md](outreach-kit/facilitator/3ds-run-of-show.md))

---

## 6. Launch Phases

| Phase | Criteria to Enter | Target Date | Goal |
|-------|------------------|-------------|------|
| **Alpha** | DIY packet + run-of-show usable without founder | TBD | 1 SK officer runs a Saturday session (Example 1) |
| **Beta** | Alpha feedback; no P0 in packet or site access | TBD | 1 federation or camp half-day; optional Guild facilitator (Example 2) |
| **Public Launch** | CLR cleared for youth data; OSS repo public; open modules reachable after session | TBD | Students open modules after with no paywall (Example 3); second self-serve SK |
| **Post-launch** | Two DIY runs live | TBD | First DFY hosted conversation (rung 5); still no kit paywall |

F15 (`ENABLE_OUTREACH_KIT`) may stay off through Alpha. Public UNESCO-toolkit claims require the open kit (print counts). DIY print does not wait on the DWY flag.

---

## 7. Success Metrics (30-day post-launch)

| ID | Metric | Target | How to Measure |
|----|--------|--------|----------------|
| Session | SK-run DIY outreach using the packet | ≥1 (Example 1) | Facilitator note / date |
| Channel | Federation or camp with optional Guild partner | ≥0 required; ≥1 if claiming partnership story (Example 2) | Facilitator note |
| After | Learner opens modules after the session | ≥1 if claiming open site (Example 3) | `kit_module_opened` if flag on; else facilitator URL check |
| BRD-M1 | Paying DFY / LOIs | 1 (later, rung 5) | CRM / signed note |
| BRD-M3 | Product burn | Within UES hosting doctrine | Invoice / Cloudflare bill |
| Contribute | Issues or packet PRs from outside NCR | ≥1 | GitHub |

Do not use lesson-seat revenue or kit paywall conversion as a v1 metric. Do not make a rumor-tap count the campaign-kit headline.

---

## Self-Check

- [x] ICP is the SK officer who must run outreach and has no program
- [x] UVP, one-liner, tagline, and UNESCO jury sentence match the open campaign kit
- [x] Services ladder: DIY (UNESCO Must-Have), DWY later flag, Guild partnership, official pack desk later/side, DFY B2G later with no paywall on open materials
- [x] Three examples: barangay 45m Saturday; federation half-day + Guild facilitator; student opens modules after
- [x] Seekers Guild is partner channel, not Page brand
- [x] OSS kit $0; paid is DFY hosted later
- [x] No fake-map tap as headline
- [x] UNESCO is first showcase, not the revenue plan
