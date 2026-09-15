# LegUp Requirements Before Prototype, Launch, and Scale

Last updated: September 15, 2026

## Purpose

This is the minimum diligence list for using LegUpRx / National Telehealth Providers behind the proposed acquisition tool. It separates questions that block only production from questions that block even a credible data-connected build.

## Phase 1 — Does not block a sample-data prototype

No LegUp permission is needed to prototype provider-neutral calculator math, co-branded page behavior, attribution, lead capture, or a fictional formulary UI.

Before showing any real LegUp or BestChoiceRx medication data in the prototype, obtain:

1. Written permission to use the formulary in a customer-facing search/calculator.
2. A sample authorized CSV/API/feed with stable identifiers.
3. Data definitions for drug, strength, dosage form, quantity/day supply, pharmacy channel, member amount, and effective date.
4. Written rules for what the prototype may call `$0`, eligible, included, covered, or savings.
5. Confirmation of whether LegUp, BestChoiceRx, Rx Valet, Shield PBM, or another party owns/licences the data and can grant these rights.

If those answers are unavailable, keep the medication experience in fictional sample-data mode.

## Phase 2 — Blocks a public production launch

### Formulary and benefit rules

- current machine-readable formulary and update frequency;
- additions/removals/change notice and effective dates;
- drug, strength, form, quantity, refill, and day-supply limits;
- monthly/annual benefit credit, cap, fair-use, or utilization limits;
- retail versus mandatory mail-order rules and timing;
- participating pharmacy network and material exceptions;
- whether insured/Medicare members may use the benefit instead of insurance;
- exact family-member eligibility and whether limits are individual or household-level;
- resolution process and responsibility when a pharmacy rejects a claim.

### Claims and creative control

- approved wording for `$0`, “at the pharmacy,” “included,” “covered,” “free,” and “save”;
- required proximity and prominence of limitations;
- approved explanation that benefit eligibility and prescribing are separate;
- prohibited channels, keywords, audiences, creatives, testimonials, or partner practices;
- creative review turnaround and version-control process;
- who monitors advertising compliance and who must remediate partner/affiliate violations;
- who is responsible for Google/LegitScript or other required certification.

### Commercial and customer terms

- final wholesale floors, retail restrictions, setup/platform fees, and price-change notice;
- merchant of record, payment processing, taxes, refunds, chargebacks, reversals, and failed payments;
- cancellation effective date and partial-period handling;
- service availability by state, member eligibility, support scope, and response-time commitments;
- our right to own and use brand, domain, content, code, analytics, and prospect data;
- clear separation of clinical-record ownership from marketing/customer-relationship ownership;
- right to use our own CRM and consent system;
- export of non-PHI customer/contact, subscription, attribution, and transaction data;
- server-side paid-member and cancellation reporting with our attribution token;
- right to communicate with customers we originated about nonclinical account matters;
- customer portability, transition assistance, and 90–180 day wind-down after termination;
- survival of earned commissions and protection from forfeiture after termination without cause.

### Privacy and security

- each party's role for HIPAA and other applicable consumer-health privacy laws;
- whether a BAA, data-processing agreement, or other addendum is required;
- permitted data fields and purposes for lead/enrollment transfer;
- data minimization, retention, deletion, access control, breach notification, and incident cooperation;
- prohibition on using our leads for unrelated marketing without explicit consent;
- subprocessor/vendor list and responsibilities across LegUp/NTP, clinical groups, PBM/pharmacy network, and technology vendors;
- approved secure handoff method that does not place health data in URLs or ordinary analytics.

## Phase 3 — Blocks meaningful acquisition spend or reseller scale

Before spending materially or recruiting resellers, require:

1. Amendment of the public customer/referral ownership and post-termination forfeiture terms.
2. Long-lived attribution and reporting for customers and recruited businesses.
3. Reconciliation procedure for active, cancelled, refunded, and disputed accounts.
4. A master-channel agreement that replaces or supplements the one-time `$500` referral bounty.
5. Recurring economics tied to legitimate channel/marketing services, subject to healthcare-counsel review.
6. Defined channel territory or account protection where appropriate.
7. Limits on unilateral price, product, and commission changes for originated accounts.
8. Continued payment/survival terms if either party terminates.
9. Partner creative controls, training, audit, suspension, and remediation process.
10. An anonymized reseller-performance pack: active partners, transacting partners, median tenure, cohort retention, conversion, support load, and employer deployments.

## Proposed recurring channel structure for discussion

This is a negotiation concept, not a legal conclusion:

- `$500` activation bounty for each new paying partner business;
- recurring share of the recruited partner's platform subscription;
- possible additional share of LegUp net revenue attributable to recruited partners if counsel approves;
- 24–36 month or active-life attribution;
- master channel ID and account-level reporting;
- commissions surviving ordinary termination for accounts originated while the agreement was active;
- no patient-level compensation unless qualified healthcare counsel confirms the exact structure is lawful.

## Evidence request

Ask LegUp for documents, not only verbal assurances:

- current signed-form agreement/addendum;
- current benefit summary and formulary data dictionary;
- redacted sample eligibility/member materials;
- approved-claims and prohibited-claims guide;
- sample reporting export/API documentation;
- data-flow and vendor/subprocessor diagram;
- refund/cancellation/support policy;
- reseller cohort metrics with definitions;
- channel-agreement term sheet.

## Decision rule

- **Prototype:** proceed now with provider-neutral math and fictional sample data.
- **Public calculator:** proceed without drug-level results if privacy/copy controls are in place.
- **Live formulary result or enrollment:** wait for Phase 2 documentation.
- **Material paid acquisition or reseller recruitment:** wait for Phase 3 contract protection.

This is business diligence, not legal advice. Final contracts, compensation, privacy, and advertising should be reviewed by qualified counsel.
