# LegUpRx Prescription Program Research

## Why this matters

The prescription program may be the strongest consumer-facing hook in the entire opportunity. The current LegUp materials indicate that qualifying members can receive a large formulary of medications at **$0 at the pharmacy** when prescribed and used under program rules.

This initially sounds too good to be true, so the goal of this file is to separate what is confirmed from what still needs verification.

## What the supplied LegUp materials show

The LegUp medication/pricing document reviewed in September 2026 states:

- Primary Care + Prescription Discount Program has a **$30/month minimum wholesale price** to the patient.
- Certain listed medications show a **Care Service Price of $0**.
- The document states that the $0 Care Service Price requires the patient to purchase the Primary Care Service + Prescription Discount Program subscription.
- It states that the medications listed at $0 remain $0 at the pharmacy, regardless of how many prescriptions are filled that month, subject to the program terms.
- The formulary spans many common categories, including:
  - antibiotics/antivirals;
  - cardiovascular drugs;
  - diabetes drugs;
  - respiratory drugs;
  - mental-health drugs;
  - thyroid drugs;
  - many other generics.

The same materials distinguish this prescription-benefit formulary from elective cash-pay medications such as GLP-1s, peptides, NAD+, TRT, and branded drugs.

## Likely mechanism

The prescriptions are not economically free. The patient pays $0 at the point of sale because a prescription-benefit / pharmacy-network arrangement pays or offsets the negotiated cash cost behind the scenes.

A known LegUp/National Telehealth Providers reseller, **Fit For Duty Rx**, publicly identifies its pharmacy network as powered by **BestChoiceRx** and has displayed a formulary with hundreds of medications at $0 across 70,000+ pharmacies.

This suggests the model is roughly:

1. member pays recurring subscription;
2. benefit program receives recurring revenue;
3. member presents program credentials or uses program routing at a participating pharmacy;
4. pharmacy processes the negotiated benefit;
5. program/network absorbs or prepays the negotiated generic-drug cost;
6. member owes $0 for qualifying drug/dose/quantity.

This can work economically because many common generic medications have very low negotiated acquisition costs and not every member fills multiple prescriptions every month.

## Important distinction: benefit coverage vs prescribing

A medication appearing on the formulary does **not** mean a LegUp/NTP clinician will prescribe it.

These are separate questions:

- **Benefit question:** If a valid prescription exists, is this drug/dose/quantity covered at $0?
- **Clinical question:** Will a licensed clinician prescribe it for this specific patient under applicable law and clinical standards?

Marketing should not collapse these into a promise that clinicians will prescribe every drug on the formulary.

## Known / likely restrictions

Programs of this type commonly include restrictions such as:

- specific drug, strength, and quantity limits;
- participating pharmacy requirements;
- inability to combine the benefit with insurance on the same claim;
- formulary changes;
- mail-order requirements for some chronic medications;
- monthly benefit caps or fair-use limitations in some program designs.

Some BestChoiceRx materials from unrelated employer programs show monthly benefit credits/caps and mail-order rules, but it has **not** been established that those exact limits apply to LegUp's current program.

## Questions that need direct answers from LegUp

1. Is **BestChoiceRx** the pharmacy-benefit provider for the program being sold to LegUp partners?
2. How many unique medications/formulations are currently truly $0?
3. Is there any monthly or annual dollar cap per member?
4. Are there per-drug quantity limits?
5. Are chronic medications required to move to mail order after initial fills?
6. Can a member fill multiple qualifying prescriptions in one month at $0?
7. Does every covered family member on the $85 wholesale Family + Rx plan receive the full benefit?
8. Is there any family-level fair-use or utilization cap?
9. Which national chains participate?
10. Can an insured member choose to use this cash/discount benefit instead of insurance for a particular prescription?
11. Can the formulary change during an active annual membership?
12. Who actually settles the pharmacy claim financially: BestChoiceRx, LegUp/NTP, another PBM/administrator, or a combination?
13. Is there a downloadable machine-readable formulary we can legally use in our own app/search experience?
14. Are there marketing-language restrictions around the words **free**, **$0**, **covered**, or **included**?

## September 15, 2026 BestChoiceRx / Rx Valet findings

### Operator and PBM identity

BestChoiceRx is not an isolated LegUp-branded product.

Evidence found:

- the BestChoiceRx site's footer identifies **Rx Valet, LLC**;
- BestChoiceRx's Terms refer to **BestChoice Rx LLC**;
- the New York Department of Financial Services directory lists **Rx Valet, LLC dba Shield PBM** as a PBM organization at 1580 Atkinson Road, Lawrenceville, Georgia;
- Shield PBM and BestChoiceRx share Rx Valet branding, group/member login patterns, and overlapping program mechanics.

The naming is not perfectly clean, so the contracting entity must be confirmed before relying on it. The durable finding is that **Rx Valet / Shield PBM appears to be the underlying operator family behind BestChoiceRx**.

### How the $0-at-pharmacy mechanism works

BestChoiceRx's own public explanation is more specific than a generic discount-card model:

1. For a selected retail pharmacy, the member can prepay and receive a pharmacy-specific voucher.
2. For a formulary drug, the member is asked for the applicable member amount and “the program will pay the difference” as part of the membership.
3. The member may owe $0 at the pharmacy counter after the program/voucher is processed.
4. For ongoing medication, the member may be directed to home delivery for up to a 90-day supply.
5. The ordinary discount-card option is separate and does **not** include special formulary pricing.

This supports the working theory that $0 is point-of-sale cost sharing funded by group/member revenue and negotiated pharmacy pricing, not a claim that the medication has no economic cost.

### Group / B2B distribution is built into the product

BestChoiceRx's FAQ states that the program is included in a medical program and “is not available on an individual basis.” Its login supports member/group IDs supplied by an employer, health-benefits plan, or group organization.

This is important: a direct group relationship appears commercially plausible. Rx Valet / Shield PBM should be contacted as a potential direct vendor or upstream source, separately from LegUp.

### Network and mail-order claims

Company-published materials claim:

- BestChoiceRx / Rx Valet access at roughly 70,000 retail pharmacies;
- Shield PBM access at more than 65,000 retail pharmacies;
- Advanced Pharmacy, LLC as BestChoiceRx's exclusive mail-order distributor;
- home delivery in up to 90-day supplies;
- insured or Medicare members cannot use insurance as payment for a BestChoiceRx transaction.

The 65,000 versus 70,000 figures may reflect different programs, dates, or marketing definitions. They should not be treated as an independently verified exact network size.

### Is LegUp's arrangement proprietary?

Current evidence suggests the underlying capability is probably **configurable group-benefit infrastructure**, not a technology unique to LegUp:

- BestChoiceRx supports employer/group IDs;
- Rx Valet operates multiple branded programs and domains;
- branded/group variants such as HVBA use the same underlying interface and program language;
- separate employer enrollment materials show Shield PBM / BestChoiceRx embedded in other benefit packages.

This is an inference, not proof that LegUp uses an off-the-shelf contract or that an identical $0 formulary is available at the same price. The specific LegUp formulary, caps, family rules, and per-member economics may still be custom.

### Limits still not resolved

The public BestChoiceRx pages reviewed did not establish:

- LegUp's per-member/per-month cost;
- monthly or annual benefit credits for the LegUp group;
- exact quantity limits;
- whether every covered family member has an independent benefit;
- mandatory mail-order timing;
- whether all listed retail pharmacies process the same $0 formulary;
- the legal right to reuse formulary data in a consumer-facing app.

### Direct-vendor diligence questions

Contact Rx Valet / Shield PBM and ask:

1. Do you sell the BestChoiceRx formulary benefit directly to membership organizations, telehealth brands, or employers?
2. Minimum group size and implementation fee?
3. PEPM price for individual and family coverage?
4. Are plans fully insured, discount programs, prepaid benefits, or another structure?
5. Exact retail network and BIN/PCN/Group routing?
6. Who funds and settles the pharmacy claim?
7. Monthly/annual benefit credit or utilization cap?
8. Drug/strength/quantity limits?
9. Retail-to-mail-order transition rules?
10. Can a telehealth brand receive a custom formulary, branded portal, API, eligibility feed, and reporting?
11. Can formulary data be licensed for a medication-search tool?
12. Contract termination, member-data export, and transition rights?

### Sources

- https://www.bestchoicerx.com/
- https://www.bestchoicerx.com/en/faq
- https://www.bestchoicerx.com/en/term-of-use
- https://www.shieldpbm.com/
- https://www.shieldpbm.com/about-us.php
- https://www.myrxvalet.com/en/faq
- https://myportal.dfs.ny.gov/companydirectory/dir_det.jsp?c=c&filekey=dir&frst=dir_srch_optiono&naic=N10683&search_type=CPAT_NUM&search_value=10683&source=o
- https://play.google.com/store/apps/details?id=com.rxvalet
- https://resources.planstin.com/blog/rxvalet-how-does-it-work

## Lead-magnet opportunity

Potential acquisition tool:

### "$0 Prescription Finder"

User searches one or more medications and receives:

- whether the medication appears on the current qualifying formulary;
- dosage/quantity notes where applicable;
- estimated current monthly out-of-pocket spend entered by the user;
- projected savings compared with membership cost;
- CTA into individual or family telehealth membership.

Example positioning:

> "See whether the medications you already take are on the $0 list."

This may be a stronger acquisition hook than generic "telehealth for $59/month" advertising because it can convert an existing expense into a savings calculation.

## Sources

- User-supplied LegUp medication and care-service pricing PDF (10 pages)
- https://fitfordutyrx.com/formulary
- https://www.bestchoicerx.com/
- https://leguprx.com/

## Status

**Highly promising, but caps/limits/provider structure still need verification before using aggressive marketing claims.**
