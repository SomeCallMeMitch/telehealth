# LegUp Go-to-Market Strategy and Lead-Magnet Decision

Last updated: September 15, 2026

## Decision summary

LegUpRx should be treated as a possible low-cost fulfillment layer for market validation, not as the business asset. The brand, domain, CRM, analytics, audience, partner relationships, and acquisition tools should remain independent and portable.

The recommended sequence is:

1. **Validate demand through existing-audience partners** using a provider-agnostic prescription-spend calculator and co-branded pages.
2. **Use a small direct-to-consumer test** to compare prescription-savings messaging with generic telehealth messaging.
3. **Add drug-level formulary search only after written data and claim permission.**
4. **Negotiate customer ownership and recurring channel economics before meaningful scale.**

The first live MVP should be a **Prescription Cost & Telehealth Savings Check**, not a production `$0 Prescription Finder`. It can ask for aggregate spending and model transparent scenarios without asserting that a medication qualifies. Once formulary rights and rules are documented, the same product can add a verified medication lookup.

## Constraints that materially affect the strategy

- The observed LegUp wholesale floors and candidate retail prices are hypotheses until confirmed in a signed plan and current price sheet.
- The reseller ecosystem proves launchability, not repeatable demand. No credible public CAC, conversion, retention, utilization, or active-member benchmark has been found.
- LegUp's public agreement raises customer/referral ownership and post-termination commission concerns.
- The `$0` benefit still lacks verified strength, quantity, utilization, family, cap, mail-order, and formulary-change rules.
- Formulary reuse rights and machine-readable access are unresolved.
- Medication appearance on a benefit formulary is not a promise that a clinician will prescribe it.
- FTC guidance requires objective and implied health-related advertising claims to be truthful, non-misleading, and supported before dissemination. Material qualifications must be clear and conspicuous, not hidden in fine print. See the [FTC Health Products Compliance Guidance](https://www.ftc.gov/business-guidance/resources/health-products-compliance-guidance).
- Google currently treats US telemedicine advertising as restricted and requires applicable healthcare certification; certification and creative eligibility must be confirmed before relying on paid search. See [Google's Healthcare and medicines policy](https://support.google.com/adspolicy/answer/176031?hl=en).
- Health-derived data should not flow into ordinary ad pixels. HHS OCR has specific guidance for regulated entities using tracking technologies, and the FTC's Health Breach Notification Rule can reach some health apps outside HIPAA. See [HHS tracking-technology guidance](https://www.hhs.gov/hipaa/for-professionals/privacy/guidance/hipaa-online-tracking/index.html) and [FTC consumer health information guidance](https://www.ftc.gov/business-guidance/resources/collecting-using-or-sharing-consumer-health-information-look-hipaa-ftcs-health-breach-notification).

## Missing information that could change the recommendation

Only four unknowns would materially change the initial strategy:

1. **Verified plan rules and data license.** A current structured formulary with explicit reuse rights would move the `$0 Prescription Finder` ahead of the general calculator.
2. **Customer and data portability.** An acceptable contract addendum could make LegUp suitable for more than a short validation test.
3. **Observed reseller cohorts.** Defensible conversion, retention, and support data could justify a larger consumer test or disqualify it.
4. **Channel agreement.** A recurring master-channel arrangement would increase the priority of partner recruitment versus selling memberships ourselves.

Progress does not require waiting for those answers. The no-claims prototype, partner interviews, message tests, and provider-agnostic data model can begin now.

## Ranked marketing opportunities

Scores use a 1–5 scale, where 5 is best. For compliance, a higher score means lower exposure and easier control. These are strategic judgments, not measured performance.

| Rank | Opportunity | Speed to evidence | Low capital | Margin potential | Compliance control | Defensibility | Total /25 | Recommendation |
|---:|---|---:|---:|---:|---:|---:|---:|---|
| 1 | Existing-audience partners with co-branded calculator/page | 5 | 5 | 4 | 4 | 4 | **22** | Start here; 3–5 partners can produce useful evidence quickly |
| 2 | Reseller recruitment under a negotiated recurring channel agreement | 3 | 5 | 5 | 3 | 5 | **21** | Validate interest now; do not scale on a one-time $500 bounty |
| 3 | Employers, brokers, staffing firms, and associations | 2 | 4 | 5 | 4 | 5 | **20** | Strong second beachhead; longer sale but better distribution |
| 4 | Organic high-intent calculators and educational content | 2 | 4 | 4 | 3 | 4 | **17** | Build compounding traffic, but do not expect 30-day SEO proof |
| 5 | Prescription-savings-led DTC acquisition | 4 | 3 | 4 | 2 | 3 | **16** | Test messaging now; live drug-level claims must wait |
| 6 | DTC family membership | 3 | 3 | 5 | 3 | 2 | **16** | Attractive spread; needs proof that households value all components |
| 7 | DTC individual membership | 4 | 2 | 3 | 4 | 2 | **15** | Useful control offer; generic telehealth is weakly differentiated |
| 8 | Broad paid search/social/affiliate scale | 5 | 1 | 2 | 1 | 1 | **10** | Use only as a capped learning test after certification/creative review |

### Why existing-audience partners rank first

The narrow beachhead is a business that already has trust and repeat customer contact but lacks a healthcare benefit: a gym, wellness business, staffing firm, broker, association, or gig-worker community. The partner supplies distribution; the calculator supplies a concrete reason to engage; and a co-branded page tests the proposition without first solving broad consumer CAC.

This route also reveals two markets at once: consumer interest and partner willingness to distribute. It remains useful if the fulfillment vendor changes.

## Route-by-route go-to-market analysis

### 1. Existing-audience wellness partners

- **Avatar:** owner/operator of a gym, med spa, IV clinic, salon, chiropractic or wellness business with an email/SMS list.
- **Urgent problem:** add recurring value and differentiation without building clinical operations.
- **Message/offer:** “Give members a simple way to estimate whether virtual care and prescription benefits could reduce household healthcare spending.”
- **Trust objections:** brand risk, unclear support responsibility, healthcare compliance, fear of promoting something customers cannot use.
- **Journey/channel:** direct outreach or warm introduction → 20-minute discovery → co-branded preview → 14-day list/QR test → review results.
- **Sales cycle/revenue:** 1–4 weeks; membership spread, partner rev-share if approved, or fixed marketing service fee.
- **Proof needed:** list size, send/scan rate, calculator completion, qualified interest, enrollments, support burden.
- **Compliance:** use approved copy; do not imply medication eligibility or medical outcomes; disclose financial relationships.
- **Failure mode:** partner likes the concept but does not promote it.
- **Portability:** high if contacts, consent, page, analytics, and attribution remain in our systems.

### 2. Staffing, gig-worker, trade, and membership groups

- **Avatar:** agency owner, trade-association leader, 1099 platform, or membership-community operator serving people with uneven access to care.
- **Problem:** retention/recruiting benefit without the cost or complexity of comprehensive health insurance.
- **Offer:** low-cost supplemental virtual-care membership, explicitly not a replacement for insurance.
- **Trust objections:** benefit adequacy, state availability, member complaints, enrollment administration, confusing it with insurance.
- **Journey/channel:** targeted outbound → benefit brief/calculator → stakeholder demo → small member cohort → broader rollout.
- **Sales cycle/revenue:** 3–10 weeks; PMPM spread, employer/group sponsorship, or member-paid offer.
- **Proof needed:** employer eligibility and billing mechanics, utilization, group pricing, implementation effort, cancellation rules.
- **Compliance:** benefit descriptions must be exact; avoid insurance language; counsel review for compensation and group arrangements.
- **Failure mode:** long procurement cycle overwhelms a small team.
- **Portability:** high with a vendor-neutral benefit description, group roster process, and contract.

### 3. Insurance brokers and benefits advisers

- **Avatar:** broker serving small employers and workforces with gaps in primary-care access or high out-of-pocket costs.
- **Problem:** needs credible supplemental options and proof the benefit is understandable and usable.
- **Offer:** employer savings/use-case calculator, broker-ready one-pager, and pilot process.
- **Trust objections:** carrier conflict, E&O exposure, benefit quality, commissions, renewal support.
- **Journey/channel:** broker interview → approved materials → one client pilot → renewal/expansion.
- **Sales cycle/revenue:** 1–4 months; group margin or counsel-approved channel compensation.
- **Proof needed:** implementation guide, state coverage, service-level commitments, utilization and complaint data.
- **Compliance:** exact role disclosures and counsel-approved compensation; never position as comprehensive insurance.
- **Failure mode:** no defensible group documentation from LegUp.
- **Portability:** high if broker and employer contracts are ours and the fulfillment layer can be replaced.

### 4. Reseller recruitment / master channel

- **Avatar:** marketer or operator with an audience and willingness to launch a telehealth offer.
- **Problem:** wants a new recurring product without sourcing clinical/pharmacy infrastructure.
- **Offer:** vertical funnel, ROI calculator, launch kit, and onboarding—conditional on a master-channel agreement.
- **Trust objections:** actual reseller success, customer ownership, compliance support, hidden costs, supplier stability.
- **Journey/channel:** educational content/outbound → ROI model → qualification call → vendor diligence → launch support.
- **Sales cycle/revenue:** 2–8 weeks; $500 activation bounty plus recurring platform share/override sought.
- **Proof needed:** recruited-account reporting, retention, attribution, commission survival, legal structure.
- **Compliance:** compensation and sub-partner practices require healthcare counsel; all creatives need oversight.
- **Failure mode:** building the channel while LegUp owns the accounts and can end the economics.
- **Portability:** medium to high only if partner relationships and tracking remain ours and vendor routing is replaceable.

### 5. Prescription-savings-led DTC

- **Avatar:** uninsured, underinsured, self-employed, or high-deductible consumer paying recurring cash costs for common medications.
- **Problem:** predictable monthly prescription cost and inconvenient access to routine care.
- **Offer:** “Estimate whether a telehealth membership could offset costs you already pay.”
- **Trust objections:** “Will my exact drug/strength/quantity qualify?”, “Is this insurance?”, pharmacy access, cancellation, clinician independence.
- **Journey/channel:** search/content/ad → calculator → result → optional lead capture → verified plan details → enrollment.
- **Sales cycle/revenue:** same session to 14 days; individual/family membership spread.
- **Proof needed:** licensed formulary, plan rules, pharmacy routing, claim language, conversion and retention.
- **Compliance:** highest sensitivity around `$0`, “covered,” savings, prescribing, tracking, and ad-platform certification.
- **Failure mode:** high curiosity but poor paid conversion once limitations and membership cost appear.
- **Portability:** high if the calculator compares configurable providers and does not use LegUp-specific IDs.

### 6. Family-membership DTC

- **Avatar:** parent or household decision-maker with several potential users and recurring Rx/urgent-care spending.
- **Problem:** one unexpected visit or several small recurring costs create budget uncertainty.
- **Offer:** household calculator comparing current spending with an illustrative family membership.
- **Trust objections:** who counts as family, eight-person rule, separate Rx benefits, pediatric access, caps, state coverage.
- **Journey/channel:** partner/content/ad → family mode → household estimate → FAQ → enrollment.
- **Sales cycle/revenue:** one session to 30 days; observed hypothesis is $149–$159 retail against an $85 floor.
- **Proof needed:** family-member eligibility and utilization rules, price sensitivity, cancellation, support burden.
- **Compliance:** all household and plan-limit statements must match current terms.
- **Failure mode:** strong gross spread but weak perceived value for low-utilizing households.
- **Portability:** medium to high; family definitions and prices must be configuration, not code.

### 7. Generic individual DTC membership

- **Avatar:** self-employed or uninsured adult seeking convenient primary care.
- **Problem:** access and predictable price.
- **Offer:** simple monthly virtual-care membership with transparent inclusions.
- **Trust objections:** comparison with urgent-care apps, insurance, existing employer benefits, quality and availability.
- **Journey/channel:** high-intent content/search → comparison → membership detail → enrollment.
- **Sales cycle/revenue:** same session to 14 days; observed hypothesis is $59 retail against a $30 floor.
- **Proof needed:** service differentiation, utilization, response times, retention.
- **Compliance:** more controllable than drug-level promotion, but clinical access claims must still be exact.
- **Failure mode:** generic offer cannot support paid CAC.
- **Portability:** high when service attributes are provider configuration.

### 8. Organic comparison content and SEO

- **Avatar:** consumer or partner researching prescription costs, telehealth memberships, or supplemental benefits.
- **Problem:** difficult comparison and unclear terms.
- **Offer:** calculators, plain-language explainers, transparent limitations, and provider comparisons.
- **Trust objections:** affiliate bias and stale formularies/prices.
- **Journey/channel:** search → article/tool → result → email or provider CTA.
- **Sales cycle/revenue:** days to months; membership margin, qualified referral, or future software lead.
- **Proof needed:** keyword demand, ranking feasibility, content-to-tool conversion.
- **Compliance:** date-stamp and source claims; disclose compensation; never publish stale drug eligibility as current.
- **Failure mode:** substantial content effort before meaningful traffic.
- **Portability:** very high.

### 9. Paid search, social, creators, affiliates, email, QR, and local media

- **Avatar:** varies by test; use narrow pain-based cohorts, not broad “everyone needs healthcare.”
- **Offer:** one claim-controlled message per campaign, routed through the calculator.
- **Trust objections:** same as DTC plus skepticism created by ad context.
- **Journey/channel:** capped ad/creator/partner placement → tool → result → consented follow-up.
- **Sales cycle/revenue:** fast evidence; membership spread if conversion survives.
- **Proof needed:** certification, approval-adjusted conversion, source-level CAC, reversals, retention.
- **Compliance:** preapprove creatives and affiliates; clear disclosures; do not pass health inputs into pixels; honor email/SMS consent and opt-outs.
- **Failure mode:** cheap leads but expensive paid members, policy disapprovals, or noncompliant partner copy.
- **Portability:** medium; first-party content and lists are portable, ad accounts and platform permissions are not.

## Campaign and funnel concepts

| Concept | Audience | Hook | Primary evidence produced | Initial channel |
|---|---|---|---|---|
| 1. Prescription Budget Check | Consumers with recurring Rx spend | “Could one membership cost less than what you already pay?” | Start, completion, spend bands, CTA rate | Partner email/QR and small search test |
| 2. Family Break-Even Check | Household decision-makers | “Estimate the spend level where a family plan might pay for itself.” | Family demand and price sensitivity | Parent/community partners |
| 3. Gym Member Health Perk | Gym members | Co-branded “member benefit” savings check | Partner distribution and consumer trust | Email, front-desk QR, app push |
| 4. Staffing Day-One Access | Temp/1099 workforce | “Virtual-care access without waiting for traditional benefits.” | Employer interest and member activation | Staffing-owner outreach |
| 5. Broker Benefit Gap Audit | Benefits brokers | Identify clients that may need a low-cost supplement | Qualified employer pipeline | Broker interviews/outbound |
| 6. Partner Audience ROI | Wellness operators/marketers | Estimate revenue and member value from a co-branded offer | Partner intent and economics | Direct outbound/LinkedIn |
| 7. Prescription FAQ Content Cluster | High-intent organic searchers | Plain-language limits, pharmacy flow, and break-even examples | Keyword and content-to-tool demand | SEO |
| 8. Local Partner QR Pilot | Salon, med spa, clinic, pharmacy-adjacent audience | “Scan for a 2-minute cost check.” | Offline scans and completion | Counter card/poster |
| 9. Two-Headline DTC Test | Consumers | Savings-led vs. access-led positioning | Message-level CTR and tool start | Capped compliant ads |
| 10. Reseller Launch Readiness Score | Prospective resellers | “Is your audience ready for a telehealth add-on?” | Qualified reseller pipeline | Content/outbound |

## Lead-magnet scorecard

Each criterion is scored 1–5, where 5 is best. “Data rights,” “easy build,” and “privacy safety” reward concepts that can be launched with fewer unresolved dependencies. No external benchmark is implied.

| Concept | Curiosity | Intent | Honest utility | Data rights | Easy build | Privacy safety | SEO | Paid-ad fit | Lead quality | Portability | Monetization | Defensibility | Total /60 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Partner / Reseller ROI Calculator | 4 | 5 | 4 | 5 | 5 | 5 | 3 | 5 | 5 | 5 | 5 | 4 | **55** |
| Co-branded Partner Lead Page | 3 | 4 | 4 | 5 | 5 | 5 | 2 | 5 | 5 | 5 | 5 | 3 | **51** |
| Prescription Spend & Membership Savings Calculator | 4 | 4 | 4 | 5 | 5 | 4 | 4 | 4 | 4 | 5 | 4 | 3 | **50** |
| Employer Supplemental-Benefit Calculator | 3 | 5 | 4 | 3 | 4 | 5 | 3 | 4 | 5 | 5 | 5 | 4 | **50** |
| Family Healthcare Savings Calculator | 3 | 4 | 4 | 4 | 4 | 5 | 3 | 4 | 4 | 5 | 4 | 3 | **47** |
| `$0 Prescription Finder` | 5 | 5 | 5 | 1 | 3 | 2 | 5 | 2 | 5 | 4 | 5 | 4 | **46** |
| Telehealth Plan Matcher | 3 | 3 | 3 | 3 | 4 | 4 | 4 | 3 | 4 | 5 | 3 | 3 | **42** |

### Primary MVP recommendation

Build the **Prescription Cost & Telehealth Savings Check** first. It wins because it:

- preserves most of the prescription-savings curiosity;
- can be truthful without a licensed formulary;
- produces measurable demand evidence in weeks;
- supports both individual and family offers;
- works on partner-branded pages;
- can later accept provider-specific formularies without changing the core product;
- avoids storing medication names in the initial version.

The `$0 Prescription Finder` is the best **second-stage feature**, not the best first live product. Its score is suppressed by the exact issues that could create legal, trust, and maintenance failures: rights, rules, health-data handling, and ad compatibility.

### B2B alternative

Build a small **Partner Audience ROI Calculator** as a companion, not a separate platform. It can model audience size, reach, conversion assumptions, price, partner share, and expected recurring revenue. It should label every number as an editable scenario and avoid promising returns. The output should route to a qualification call and record the partner's vertical, audience size, and distribution capability.

## What can be prototyped now

- provider-neutral landing page and headline tests;
- individual/family aggregate-spend calculator;
- scenario slider showing 0%, 25%, 50%, and 75% of entered spend hypothetically offset;
- explicit break-even math and “what must be verified” copy;
- co-branded page configuration and partner attribution;
- UTM capture and privacy-safe funnel events;
- lead capture for a saved result or verified-benefit update;
- partner ROI calculator;
- admin mocks for prices and formulary versions;
- a clearly labeled fictional/sample medication dataset for usability testing only;
- customer and partner interview scripts.

## What must wait for verified data or permission

- live medication eligibility or `$0` results;
- use of LegUp, BestChoiceRx, Rx Valet, or Shield PBM formulary data;
- strength, form, quantity, pharmacy, family, cap, or mail-order determinations;
- claims that a named medication is covered or costs `$0`;
- any implication that a clinician will prescribe a searched medication;
- production enrollment handoff, final pricing, refund language, or benefit comparison;
- paid search based on prescription/telemedicine claims until certification and creative eligibility are confirmed;
- retargeting based on tool answers;
- material acquisition spend before customer ownership, CRM, export, termination, and attribution rights are resolved;
- reseller recruitment at scale before a recurring channel agreement and counsel review.

## Decision

Proceed with a clickable, sample-data prototype and a real aggregate-spend validation tool. Begin with three to five existing-audience partners and a small DTC control. Do not present drug-level results or spend meaningfully on acquisition until LegUp supplies the data, permissions, claims, and ownership terms described in the product brief.

This is business research, not legal or medical advice. Healthcare counsel and a qualified privacy review are required before production launch.
