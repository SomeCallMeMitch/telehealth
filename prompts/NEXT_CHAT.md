# Next Chat Prompt — Leg Up Marketing and Lead-Magnet Build

We are continuing an exploratory telehealth business project. The working repository is:

https://github.com/SomeCallMeMitch/telehealth

Use the GitHub connection to read the repository before doing new work. Treat the repo as the project’s source of truth and update it with durable findings, decisions, specifications, and next steps.

Start with these files:

- README.md
- research/master-findings.md
- research/industry-marketing-landscape.md
- research/providers/leguprx.md
- research/rx-program.md
- research/reseller-ecosystem.md
- research/channel-partner-models.md
- research/research-backlog.md

Do not repeat research already completed unless something needs current verification.

## Current objective

Conduct a focused, commercially realistic deep dive into:

1. Our possible marketing efforts if we use LegUpRx / National Telehealth Providers as an initial fulfillment platform.
2. The best lead magnet or lightweight software tool I could vibe code to acquire and qualify consumers or business partners.
3. A practical MVP specification and validation plan we can use before committing significant time or money.

We are still exploring. No provider has been selected, no launch has been authorized, and LegUp should currently be viewed as a potentially inexpensive validation backend—not necessarily the permanent platform.

## Important context

LegUp’s attractive features include:

- approximately $249/month platform pricing after its trial;
- low wholesale floors for primary care, family care, urgent care, behavioral health, dermatology, and veterinary care;
- approximately $30/month wholesale for Primary Care + Prescription;
- approximately $85/month wholesale for Family + Prescription;
- a large prescription formulary advertised with qualifying medications available for $0 at the pharmacy under program rules;
- a reseller model that can support a branded consumer offer.

The working retail hypotheses have been approximately:

- $59/month for an individual Primary Care + Rx membership;
- $149–$159/month for a Family + Rx membership.

These are hypotheses, not decisions.

The strongest current lead-magnet idea is:

> “See whether the prescriptions you already take are on the $0 list.”

The user could search medications, enter approximate current out-of-pocket spending, and compare potential savings with membership cost.

However, important facts remain unresolved:

- exact formulary licensing/reuse rights;
- drug strengths and quantity limitations;
- monthly or annual benefit caps;
- family-member utilization rules;
- mandatory mail-order rules;
- whether BestChoiceRx / Rx Valet / Shield PBM is the final underlying administrator;
- what claims LegUp will approve for advertising;
- API, feed, or machine-readable formulary access;
- customer-data export and CRM rights.

LegUp’s public partner agreement also contains concerning termination and referral-ownership language. It appears that future commissions or rights to referred customers may be forfeited after termination and that referrals remain LegUp property. We should not build an acquisition engine that becomes trapped inside a vendor we do not control.

Industry research also shows that the loudest affiliate activity is concentrated in GLP-1 and other elective care. The LegUp primary-care and prescription-membership offer is a different value proposition and should not inherit GLP-1 assumptions about demand, traffic, conversion, or payouts.

## Workstream 1 — Marketing strategy

Develop a grounded go-to-market analysis for using LegUp as the initial backend.

Compare at least these routes:

- direct-to-consumer individual membership;
- direct-to-consumer family membership;
- prescription-savings-led acquisition;
- employer or employee-benefit acquisition;
- insurance brokers and benefits advisers;
- gyms, med spas, IV clinics, salons, wellness businesses, and other existing-audience partners;
- staffing firms, gig-worker groups, trade associations, and membership organizations;
- reseller recruitment or a negotiated recurring channel-partner arrangement;
- organic search, comparison content, calculators, and other high-intent educational content;
- carefully controlled paid search, paid social, creator, affiliate, email, QR, and local-partnership tests.

For each viable route, identify:

- primary customer avatar;
- urgent problem or desired outcome;
- message and offer;
- likely trust objections;
- buying journey;
- acquisition channel;
- expected sales cycle;
- plausible revenue model;
- data or proof still needed;
- compliance constraints;
- major failure mode;
- whether the customer relationship remains portable if we leave LegUp.

Produce 5–10 specific campaign or funnel concepts. Rank them by likely speed to evidence, capital required, margin potential, compliance exposure, and defensibility.

Do not assume that the largest theoretical market is the best place to begin. Look for a narrow beachhead with a clear existing expense or pain.

## Workstream 2 — Lead-magnet selection

Compare these possible tools:

1. $0 Prescription Finder
2. Prescription Spend and Membership Savings Calculator
3. Family Healthcare Savings Calculator
4. Telehealth Plan Matcher
5. Employer Supplemental-Benefit Savings Calculator
6. Partner or Reseller ROI Calculator
7. Co-branded lead-capture page for gyms, brokers, med spas, or other partners

Add better concepts if the research supports them.

Score each concept on:

- strength of consumer or partner curiosity;
- purchase intent;
- usefulness without exaggerating savings;
- availability and legal use of required data;
- development complexity;
- privacy and compliance exposure;
- search/SEO potential;
- paid-ad compatibility;
- ability to collect a qualified lead;
- ability to work with a provider other than LegUp later;
- monetization path;
- defensibility.

Recommend one primary MVP and, if helpful, one B2B alternative. Explain why the recommendation is superior to the other candidates.

## Workstream 3 — MVP product brief

For the recommended lead magnet, create a vibe-code-ready product specification covering:

- target user and job to be done;
- value proposition and headline options;
- landing-page structure;
- exact step-by-step user flow;
- inputs, calculations, outputs, disclaimers, and CTAs;
- lead-capture timing;
- individual versus family handling;
- medication name, strength, quantity, and formulary edge cases;
- what can be shown before LegUp grants formulary-reuse rights;
- data model;
- analytics and conversion events;
- source/UTM and partner attribution;
- admin workflow for updating pricing and formulary information;
- error, empty, unavailable, and uncertain-result states;
- mobile-first requirements;
- accessibility requirements;
- privacy-by-design requirements;
- what information must not be placed into ordinary ad pixels or marketing analytics;
- how to keep the product portable across future telehealth providers.

Avoid collecting or retaining health information unless it is necessary. Distinguish ordinary marketing/contact data from potentially sensitive health data. Do not design the tool as medical advice, a diagnosis, an eligibility promise, or a promise that a clinician will prescribe a medication.

### Base44 implementation constraints

If we move into implementation, use:

- React;
- Tailwind;
- shadcn/ui;
- lucide-react;
- react-router-dom;
- react-hook-form;
- recharts where useful;
- Entities SDK from @/entities;
- User methods supplied by the platform;
- Core integrations from @/integrations/Core.

Use createPageUrl('PageName') for internal links. Include null checks and loading states. Do not build authentication pages because authentication is handled by the platform. Prefer small, focused, drop-in components.

Do not begin writing the full application until the concept, data rights, claims, user flow, and minimum validation test are clear. A clickable front-end prototype using clearly labeled sample data may be appropriate before production integration.

## Workstream 4 — LegUp requirements

Create a concise list of questions or proposed contract requirements we need from LegUp before launching the tool or spending meaningfully on acquisition.

Include:

- permission to use and update formulary data;
- API, CSV, or structured data access;
- permitted wording for $0 prescriptions and savings claims;
- lead/customer ownership;
- ability to use our own CRM;
- non-PHI export rights;
- attribution and reporting;
- recurring economics;
- refund and reversal treatment;
- customer portability after termination;
- transition period;
- restrictions on marketing channels or creatives;
- who is responsible for monitoring advertising compliance;
- data-processing and privacy responsibilities;
- whether a master channel or recurring reseller-recruitment agreement can replace the $500 one-time referral bounty.

Separate questions that must be answered before building from those that can wait until after an inexpensive prototype test.

## Workstream 5 — Validation economics

Create a simple funnel model with clearly labeled assumptions.

Include:

- visitor or click volume;
- CPC or content-production cost;
- tool-start rate;
- completion rate;
- lead-capture rate;
- membership click-through;
- checkout/intake completion;
- clinical or program eligibility where applicable;
- paid-member conversion;
- individual/family mix;
- gross spread;
- churn or retention assumptions;
- support, platform, and payment costs;
- CAC payback period;
- break-even member count.

Show conservative, base, and optimistic scenarios. Do not manufacture “industry averages” when reliable evidence is unavailable; use editable assumptions and say what we must measure.

Design a 30-day validation plan with:

- smallest credible prototype;
- traffic sources;
- approximate test budget options;
- messages and audiences;
- events to track;
- success, revise, and stop thresholds;
- customer interviews or partner interviews;
- the evidence required before building a larger application or signing a long contract.

## Compliance and research standards

- Use current sources for changing facts.
- Cite material claims.
- Separate vendor claims, community anecdotes, and independent evidence.
- Do not treat this as legal or medical advice.
- Do not promise that a medication is available, covered, appropriate, or will be prescribed unless the underlying rules and data justify the statement.
- Include FTC disclosure, health-claim, privacy, TCPA/SMS, and advertising-platform considerations where relevant.
- Keep health-intake information out of ordinary marketing pixels unless a qualified privacy review supports the design.
- Build the acquisition asset so it can survive a change of backend provider.

## Requested first response

After reading the repo:

1. Briefly confirm the important constraints and identify only the missing information that would materially change the strategy.
2. Present the ranked LegUp marketing opportunities.
3. Compare and score the lead-magnet candidates.
4. Recommend the first MVP.
5. Produce the initial MVP product brief and 30-day validation plan.
6. Identify the LegUp questions that block a production launch.
7. Recommend which parts can be vibe coded immediately with sample data and which parts must wait for verified data or permission.

Ask only a small number of high-impact clarifying questions. If reasonable assumptions allow progress, state them and proceed.

At the end of the work, update the repository with the strategy, product specification, validation model, and revised backlog.
