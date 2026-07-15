# Unit Economics Sheet (UES)

**Project:** Pollux
**Date:** 2026-07-15
**Version:** 0.1
**Owner:** Pollux founding team
**Status:** Draft
**Last reconciled:** N/A
**IDEA:** [idea-pollux.md](idea-pollux.md)
**BRD:** [brd-pollux.md](brd-pollux.md)

---

## 0. Business Model Fit

**The unit:** One B2B learner seat-year, or one B2G municipal deployment project

**Who pays:** LGU / NGO / enterprise buyer (not the learner via D2C)

**Margin thesis:** Growth funded by contribution from seats and projects. No paid messaging or enterprise listening until a buyer funds it.

**BRD BMC handoff:**

| BMC block | Feeds | Value |
|-----------|-------|-------|
| Customer Segments | Cohorts / UES-D8 | LGU/SK, NGO, enterprise L&D |
| Revenue Streams | UES-E1 | Project fees; seat licenses |
| Cost Structure | UES-E2, UES-F# | Hosting, founder time, optional LLM |
| Impact variables | Allocation | BRD-V1 pilot conversion, BRD-V2 completion |

---

## 0.5 Capital Doctrine Register

| ID | Principle | Operational rule | Evidence / metric link | Status |
|----|-----------|------------------|------------------------|--------|
| UES-D1 | DO NOT LOSE MONEY | No paid messaging, Meltwater, or ads that drive Red UES-E7 | UES-E7, §2 | Pass |
| UES-D2 | ASSET ALLOCATION | Ops 60% / proven pilot channel 30% / experiments 10% | Allocation table | Pass |
| UES-D3 | Asymmetrical RISK-REWARD | Cap content-pack experiment loss; upside multi-LGU | Bet register | Pass |
| UES-D4 | 1 in 5 out | Experiment ≤ expected contribution / 5 | §3 | Pass |
| UES-D5 | Margins run the business | Growth spend from contribution after first paid pilot | §3 | Pass |
| UES-D6 | Operating Cashflow | §2 tracks OCF path | §2 | Pass |
| UES-D7 | Capital Gains | Bootstrap default; raise only on §6 triggers | §6 | Pass |
| UES-D8 | User Centric, Tailored | Primary: PH youth leaders / SK buyers | §5 | Pass |

**Bootstrap hosting rule (Scrutiny fix):** Vercel Hobby is non-commercial only (https://vercel.com/docs/plans/hobby). Pre-revenue prototype may use Hobby + Supabase free. Commercial pilots require Vercel Pro (~$20/seat/mo) or Cloudflare Pages. Do not advertise "$0 forever" for a monetized product.

**Asset allocation (UES-D2):**

| Bucket | Capital / time % | Tied to | Cap / notes |
|--------|------------------|---------|-------------|
| Ops | 60% | UES-F# | Keep product alive |
| Proven channels | 30% | BRD-V1 | Direct B2G outreach |
| Experiments | 10% | BRD-V2 | Cap $100/mo cash until paid |
| **Total** | **100%** | | |

**Bet register (UES-D3):**

| Bet | Max loss $ | Upside thesis | Asymmetry | Kill if |
|-----|------------|---------------|-----------|---------|
| First LGU pilot content pack | $200 (founder time + domain) | Multi-barangay license | High | No engagement in 30 days |
| Telegram adapter | $0 cash (time only) | Lower friction for leaders | Medium | Unused after 2 weeks in pilot |

---

## 1. Unit Economics Sheet

Formulas verified against Stripe unit-economics guidance (checked 2026-07-15).

| ID | Metric | Value | Status | Notes |
|----|--------|-------|--------|-------|
| UES-E1 | Revenue per unit | B2B TBD $8-20/seat-year; B2G project TBD $2k-15k | Yellow | Set in pilot negotiation |
| UES-E2 | Variable cost per unit | ~$0 messaging; infra pennies; payment fees TBD | Green | Doctrine forbids SMS/templates at our cost |
| UES-E3 | Contribution margin per unit | ≈ UES-E1 minus fees | Yellow | Until price locked |
| UES-E4 | Gross margin % | Target ≥80% software | Yellow | TBD after pricing |
| UES-E5 | Fully-loaded CAC | Target $0 paid; founder time + partner intros | Yellow | No paid ads until UES-E7 green |
| UES-E6 | LTV (contribution-based) | TBD multi-year seats | Yellow | Need churn data |
| UES-E7 | LTV:CAC ratio | TBD; do not scale paid until ≥2.5:1 | Yellow | UES-D1 gate |
| UES-E8 | CAC payback (months) | Target under 6 if bootstrapped | Yellow | |

**Cohort view:**

| Cohort / Channel | CAC | LTV | LTV:CAC | Payback | Action |
|------------------|-----|-----|---------|---------|--------|
| Direct B2G pilot | Founder time | TBD | TBD | TBD | Hold until LOI |
| Enterprise L&D | Higher touch | TBD | TBD | TBD | Hold |
| D2C consumer | n/a | n/a | n/a | n/a | Kill for v1 |

---

## 2. Cash Budget and Runway

**Initial capital:** Assume founder sweat + ≤$100 cash until pilot (TBD actual)

| ID | Item | Monthly cost | Notes |
|----|------|--------------|-------|
| UES-F1 | Founder living | TBD / external | Not product burn |
| UES-F2 | Domain | ~$1 amortized | |
| UES-F3 | Hosting (pre-revenue) | $0 Hobby + Supabase free | Hobby non-commercial |
| UES-F4 | Hosting (commercial) | ~$20 Vercel Pro or Cloudflare equiv | Required when monetizing |
| | **Total fixed (product, pre-revenue)** | **≈ $0-5** | Domain only |
| | **Total fixed (commercial)** | **≈ $20-40** | Pro + buffer |

**Variable spend:** LLM coaching $0-15 if enabled (default off); messaging $0.

| Metric | Value |
|--------|-------|
| Cash on hand | TBD |
| Monthly revenue (current) | $0 |
| Monthly fixed overhead (product) | $0-5 pre-revenue; ~$20+ commercial |
| **Operating cashflow (OCF)** | Negative until first paid pilot; path via seats/projects |
| **Runway (months)** | Sweat-equity runway; cash runway TBD |

**Default-alive check:** Default-alive if first paid pilot covers commercial hosting and content time within 90 days. Default-dead if paid messaging is required to acquire users.

---

## 3. Margins Run the Business (not Capital)

**Reinvestment rule:** After first paid pilot, growth spend comes from contribution only.

| Gate | Rule |
|------|------|
| Paid acquisition | Forbidden until UES-E7 green |
| Messaging / SMS | Buyer-funded only |
| Experiment (UES-D4) | Max cost ≤ expected contribution / 5 |
| Tool / vendor | No Meltwater in v1 |

---

## 4. Moat Register

| Moat type | Status | Evidence | UES-M# |
|-----------|--------|----------|--------|
| Distribution | Building | SK / LGU relationships TBD | UES-M1 |
| Data / Information | Building | Localized packs + lesson outcomes | UES-M2 |
| Switching costs | Building | Packs embedded in DRRM workflow | UES-M3 |
| Process / IP | Building | Rule-based lesson design + governance | UES-M4 |

---

## 5. Positioning

**Primary segment:** PH youth leaders / SK and LGU DRRM buyers (UES-D8)

**Avoid competing with:** DoubleVerify / IAS on ad MTF; Meltwater on enterprise listening; NewsGuard human newsroom ratings.

**Category:** Civic / enterprise cognitive resilience training + governed info packs

---

## 6. Raise Triggers (UES-D7)

Raise or grant only if: (1) paid pilot proves completion ≥60%, (2) second LOI in pipeline, (3) TrustOps build needs capital beyond contribution. Otherwise bootstrap.

---

## Self-Check

- [x] Numbers live here, not in BRD
- [x] UES-D1-D8 present including hosting doctrine
- [x] OCF row in §2
- [x] No paid messaging in variable cost thesis
