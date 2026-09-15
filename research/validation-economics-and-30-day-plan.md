# Validation Economics and 30-Day Test Plan

Last updated: September 15, 2026

## Purpose

This model answers a narrow question: can a prescription-spend-led acquisition tool generate qualified interest at economics that might support an individual/family telehealth membership?

It does not claim industry averages. Every number below is an editable assumption. The first test is designed to measure the missing inputs, not prove a forecast.

## Working unit economics

Current price hypotheses from repository research:

| Plan | Candidate retail | Observed wholesale floor | Gross spread before all other costs |
|---|---:|---:|---:|
| Individual Primary Care + Rx | $59/mo | $30/mo | $29/mo |
| Family + Rx | $159/mo | $85/mo | $74/mo |

The family plan uses $159 for modeling; $149 should also be tested. Wholesale costs, service inclusions, family rules, and merchant-of-record treatment must be confirmed before launch.

## Funnel definitions

Use these definitions consistently:

1. **Visitor:** unique eligible landing-page session after bot/internal filtering.
2. **Tool start:** first substantive calculator answer.
3. **Completion:** result successfully rendered.
4. **Lead capture:** consented email or partner inquiry after result.
5. **Membership click-through:** click to verified plan detail or enrollment handoff.
6. **Checkout/intake completion:** completes all nonclinical enrollment steps and, if applicable, intake.
7. **Program/clinical eligibility:** only where a downstream program requires it; a general membership may not have clinical approval at enrollment.
8. **Paid member:** successful nonreversed first payment confirmed server-side.

Do not call a lead or click a “member.”

## Scenario assumptions per 1,000 acquired visitors

These are deliberately broad planning cases. CPC means paid cost or paid-equivalent acquisition cost; partner/organic traffic should be modeled with its actual production or placement cost.

| Assumption | Conservative | Base | Optimistic |
|---|---:|---:|---:|
| Visitors | 1,000 | 1,000 | 1,000 |
| Cost per visitor | $5.00 | $3.00 | $1.75 |
| Traffic/production cost | $5,000 | $3,000 | $1,750 |
| Tool-start rate | 20% | 35% | 50% |
| Starts | 200 | 350 | 500 |
| Completion rate from start | 40% | 60% | 75% |
| Completed results | 80 | 210 | 375 |
| Lead-capture rate from result | 20% | 35% | 50% |
| Leads | 16 | 74 | 188 |
| Membership CTR from result | 8% | 20% | 30% |
| Membership clicks | 6.4 | 42.0 | 112.5 |
| Checkout/intake completion | 20% | 35% | 45% |
| Completed checkout/intake | 1.3 | 14.7 | 50.6 |
| Program/clinical eligibility, if applicable | 90% | 95% | 98% |
| Post-eligibility paid completion | 65% | 80% | 90% |
| Modeled paid members | **0.7** | **11.2** | **44.7** |
| Modeled CAC | **$6,677** | **$269** | **$39** |

The conservative case illustrates the failure mode: curiosity and leads can look respectable while paid conversion makes the model uneconomic. The optimistic case should not be treated as a target until replicated by source and cohort.

## Contribution and retention model

Additional editable assumptions:

| Assumption | Conservative | Base | Optimistic |
|---|---:|---:|---:|
| Individual/family mix | 90% / 10% | 75% / 25% | 60% / 40% |
| Average retail revenue/member-month | $69.00 | $84.00 | $99.00 |
| Average gross spread/member-month | $33.50 | $40.25 | $47.00 |
| Payment cost assumption | 3% + $0.30 | 3% + $0.30 | 3% + $0.30 |
| Payment cost/member-month | $2.37 | $2.82 | $3.27 |
| Support/ops/member-month | $8.00 | $6.00 | $4.00 |
| Refund/bad-debt reserve | 3% of revenue | 2% of revenue | 1% of revenue |
| Reserve/member-month | $2.07 | $1.68 | $0.99 |
| Contribution before platform and acquisition | **$21.06** | **$29.75** | **$38.74** |
| Monthly churn | 15% | 8% | 5% |
| Simple expected lifetime (`1/churn`) | 6.7 mo | 12.5 mo | 20.0 mo |
| Lifetime contribution before fixed/acquisition | **$140** | **$372** | **$775** |
| CAC payback | **317 mo** | **9.0 mo** | **1.0 mo** |
| Lifetime contribution : CAC | **0.02x** | **1.38x** | **19.8x** |

The simple lifetime calculation ignores cohort shape, annual plans, pauses, win-backs, price changes, support spikes, and time value. Replace it with observed cohort contribution as soon as data exists.

### Fixed-cost break-even

Using the observed $249 monthly platform cost:

| Measure | Conservative | Base | Optimistic |
|---|---:|---:|---:|
| Active members needed to cover $249/mo platform | 12 | 9 | 7 |
| Active members needed to cover $249 + $199 first-month Care Services add-on | 22 | 16 | 12 |
| Contribution at 100 active members after $249 platform | $1,857/mo | $2,726/mo | $3,625/mo |

These counts cover modeled fixed platform cost only. They do not recover acquisition, legal/compliance, creative, software, taxes, chargebacks, or owner labor.

### Interpretation

- **Conservative:** stop. No messaging improvement can rescue CAC that exceeds modeled lifetime contribution by this margin.
- **Base:** fragile. The acquisition cost is technically below simple lifetime contribution but leaves little room for fixed costs or forecasting error and requires roughly nine months of retention to recover CAC.
- **Optimistic:** attractive but must be replicated. It likely requires trusted partner traffic or exceptional intent, not generic paid media.

This is why the first test should emphasize existing-audience partners and use paid traffic as a controlled comparison.

## Spreadsheet-ready formulas

```text
starts = visitors * start_rate
completions = starts * completion_rate
leads = completions * lead_capture_rate
membership_clicks = completions * membership_ctr
checkout_completions = membership_clicks * checkout_completion_rate
paid_members = checkout_completions * eligibility_rate * paid_completion_rate
cac = acquisition_cost / paid_members

avg_retail = individual_mix * individual_retail
           + family_mix * family_retail

avg_wholesale = individual_mix * individual_wholesale
              + family_mix * family_wholesale

gross_spread = avg_retail - avg_wholesale
payment_cost = avg_retail * payment_rate + payment_fixed_fee
reserve = avg_retail * refund_bad_debt_rate
monthly_contribution = gross_spread - payment_cost - support_cost - reserve

simple_lifetime_months = 1 / monthly_churn
simple_lifetime_contribution = monthly_contribution / monthly_churn
cac_payback_months = cac / monthly_contribution
platform_break_even_members = ceiling(monthly_platform_cost / monthly_contribution)
```

## What must be measured

- acquisition cost by source, partner, creative, and landing variant;
- unique eligible visitors after bot/internal filtering;
- start, completion, result-to-lead, and result-to-plan-detail rates;
- lead-to-enrollment and source-level paid-member conversion;
- individual/family selection and actual paid mix;
- payment failures, refunds, chargebacks, and reversals;
- 30/60/90/180-day retention by acquisition cohort;
- support contacts and minutes per new/active member;
- downstream eligibility/approval where applicable;
- provider-reported paid member reconciled to our attribution token;
- contribution after all variable costs.

## 30-day validation objective

Determine whether the savings-led proposition produces enough qualified consumer and partner intent to justify obtaining production data rights and negotiating a launch contract.

The test is not intended to validate long-term retention in 30 days.

## Smallest credible prototype

Build the product described in `product/rx-savings-mvp-brief.md` with:

- individual/family mode;
- aggregate prescription spend and optional visit-cost inputs;
- visible, editable scenario math;
- immediate result before lead capture;
- email capture and partner inquiry;
- co-branded partner variants;
- first-party event tracking;
- sample-data-only medication lookup mock for usability sessions, not public benefit results.

## Budget options

Budget ranges exclude owner labor and legal review.

| Option | Cash budget | Use |
|---|---:|---|
| Lean | $750–$1,250 | Prototype tools/assets, partner materials, $250–$500 capped traffic/placement test, interview incentives |
| Standard | $2,500–$4,000 | 2–3 traffic audiences, roughly 600–1,000 paid/paid-equivalent visits depending on actual cost, 10–15 interview incentives, creative variants |
| Expansion | $6,000–$8,000 | Only after Week 3 thresholds are met; replicate winning partner/message and add a second audience |

Do not commit the expansion budget in advance. Release it only against measured evidence.

## Traffic-source plan

### Primary: existing-audience partners

Recruit 3–5 partners across no more than two verticals, preferably:

- one gym/fitness/wellness business;
- one staffing, gig-worker, or membership organization;
- optional broker or small-employer adviser.

Each receives an assigned page, QR code, email copy, and one approved social post. Ask for a specific distribution commitment before customizing the page.

### Secondary: direct consumer control

Run a small, claim-controlled test only if platform eligibility/certification requirements are satisfied. Compare:

- **Savings-led:** “Could one membership cost less than the prescriptions you already pay for?”
- **Access-led:** “Estimate the monthly value of virtual primary care for your household.”

Use contextual/high-intent targeting where possible. Do not target or retarget based on medication, diagnosis, or tool answer.

### Organic and direct outreach

- publish one transparent explainer that links to the calculator;
- share directly with a permissioned personal/professional audience only where appropriate;
- conduct partner outreach with the ROI calculator mock;
- do not count internal/test traffic.

## Day-by-day plan

### Days 1–3 — Lock the test

- choose two partner verticals;
- freeze the Version 1 inputs and calculations;
- create a claims matrix: allowed, qualified, prohibited;
- configure $59 individual and $149/$159 family variants as hypotheses;
- write privacy, consent, and prototype disclosures;
- recruit the first two usability participants and five partner prospects.

### Days 4–7 — Build and instrument

- vibe code the mobile-first calculator under the Base44 constraints;
- implement source/partner attribution and first-party events;
- create neutral and co-branded variants;
- QA zero/high values, individual/family mode, missing config, consent, and mobile accessibility;
- verify that no exact spend or health-derived values enter URLs, pixels, CRM, or logs.

### Days 8–12 — Usability and partner commitment

- run 5 consumer usability sessions;
- show the partner-page and ROI mock to 5 prospective partners;
- require a concrete send/post/QR date from any pilot partner;
- revise confusing copy and steps once, not continuously;
- record objections verbatim and categorize them.

### Days 13–21 — Live traffic test

- launch 2–3 partner pages;
- send one approved email/post/QR placement per partner;
- run the capped consumer control if allowed;
- check data quality daily but avoid optimizing on tiny samples;
- pause any creative that produces misleading expectations or policy warnings.

### Days 22–26 — Interviews and commercial test

- interview at least 10 completed-tool users across high and low spend bands;
- interview at least 5 partner prospects/pilots;
- present the real candidate prices and key limitations;
- ask for a behavioral next step: verified-plan review, pilot follow-up, or scheduled proposal—not only a positive opinion.

### Days 27–30 — Decision

- calculate funnel performance by source and partner;
- compare savings-led and access-led variants;
- summarize top trust objections and requested proof;
- estimate CAC range using observed pre-purchase funnel plus explicit downstream assumptions;
- choose success, revise, or stop;
- only then decide whether to seek formulary integration and a production agreement.

## Events to track

Required events are defined in the product brief. The decision dashboard should show:

- eligible landing views;
- tool starts;
- results;
- lead submits;
- plan-detail/verified-update clicks;
- partner inquiries;
- conversion by page/message/partner;
- median time to result;
- error/abandonment step;
- interview bookings and completed interviews.

Do not send exact spend, medication, condition, or clinical data to ordinary marketing analytics.

## Decision thresholds

Thresholds apply after at least 300 qualified visitors or three real partner distributions. They are decision rules for this test, not industry standards.

| Metric | Success | Revise | Stop / rethink channel |
|---|---:|---:|---:|
| Landing → tool start | ≥30% | 15–29% | <15% after two distinct headlines |
| Start → result | ≥55% | 35–54% | <35% after usability fixes |
| Result → lead | ≥25% | 12–24% | <12% with a useful ungated result |
| Result → verified-plan/update CTA | ≥12% | 5–11% | <5% |
| Completed consumer interviews expressing purchase intent at real price after limitations | ≥5 of 10 | 2–4 of 10 | 0–1 of 10 |
| Pilot partners that actually distribute | ≥2 of 5 prospects | 1 of 5 | 0 of 5 |
| Partner interviews requesting a concrete next step | ≥2 of 5 | 1 of 5 | 0 of 5 |

### Overall success

Proceed to production diligence when:

- at least four of the seven success thresholds are met;
- no material privacy/compliance defect occurred;
- at least one source shows both qualified interest and a plausible path to CAC below modeled lifetime contribution;
- users understand that the tool is not a medication or prescribing guarantee;
- at least two partners demonstrate actual distribution, not just enthusiasm.

### Revise

Run one additional narrowly scoped iteration if users complete the tool but fail at a single explainable step, or if one partner vertical works while another does not.

### Stop or reposition

Stop the consumer membership build if:

- users primarily want a discount card without valuing the membership;
- real-price intent collapses after plan limitations are explained;
- partners will not distribute;
- projected CAC remains above lifetime contribution even under credible retention;
- verified plan rules materially weaken the savings proposition;
- acceptable customer/data ownership terms cannot be obtained.

The software can still be repositioned as a provider comparison or B2B partner tool.

## Interview questions

### Consumer

1. What did you think the tool would tell you before you started?
2. Which result felt useful or untrustworthy?
3. What would you need to verify before paying $59 or $149–$159 per month?
4. Is prescription cost, care access, family coverage, or predictability the primary value?
5. What would make you believe or reject a `$0` medication statement?
6. Would you take the next step today? Why or why not?

### Partner

1. Which audience segment would you send this to?
2. What specific channel and date could you use for a pilot?
3. What brand, support, and compliance risk concerns you?
4. Would you prefer member-paid, employer-paid, rev-share, or fixed-fee economics?
5. What reporting and customer ownership would you require?
6. What evidence would be necessary for a broader rollout?

## Evidence required before a larger build or long contract

- written formulary license and structured update path;
- plan rules and approved marketing language;
- acceptable ownership, CRM, export, transition, and termination rights;
- actual funnel data from at least 300 qualified visitors or equivalent partner reach;
- behavioral intent from consumers and partners at real prices;
- preliminary source-level CAC range;
- reconciled paid-member reporting design;
- support and cancellation workflow;
- privacy/data-flow review and advertising certification path;
- provider migration option and cost at meaningful member counts.

This model supports business exploration and is not legal, medical, accounting, or investment advice.
