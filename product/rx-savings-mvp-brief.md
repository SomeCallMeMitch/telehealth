# MVP Product Brief — Prescription Cost & Telehealth Savings Check

Last updated: September 15, 2026

## Product decision

Build a mobile-first, provider-neutral calculator that helps a person compare current prescription and routine-care spending with a configurable telehealth membership.

Version 1 must **not** determine whether a named medication is covered or `$0`. It uses aggregate spend and explicitly hypothetical coverage scenarios. A future verified-formulary module can add drug, strength, form, and quantity lookup after written data rights and plan rules are obtained.

## Target user and job to be done

### Primary user

An uninsured, underinsured, self-employed, high-deductible, or budget-conscious adult who pays recurring out-of-pocket prescription costs and is evaluating predictable virtual-care access.

### Secondary user

A household decision-maker comparing an individual plan with a family plan.

### Partner user

A gym, wellness business, staffing firm, broker, employer, trade association, or membership group that wants a co-branded educational tool for its audience.

### Job to be done

> When I am paying recurring prescription and routine-care costs, help me understand whether a telehealth membership is worth investigating, without pretending you know that my medication is eligible or that a clinician will prescribe it.

## Value proposition

The product converts a vague monthly membership into a transparent break-even comparison based on spending the user already recognizes.

It should answer three questions:

1. What am I paying now?
2. What would the candidate membership cost?
3. What would need to be eligible or avoided for the membership to break even?

## Headline options

Use the first headline for the initial test. Avoid `$0`, “free,” “covered,” and named medication claims until the supporting rights and rules are approved.

1. **Could one membership cost less than the prescriptions you already pay for?**
2. **Estimate your prescription and telehealth break-even point in two minutes.**
3. **See when a virtual-care membership might pay for itself.**
4. **Turn your current healthcare spending into a simple monthly comparison.**
5. **For families: compare recurring prescription and routine-care costs in one place.**

Supporting copy:

> Enter estimates—not medical records—to see transparent scenarios. This tool does not determine medication eligibility, coverage, prescribing, or medical suitability.

## MVP scope

### Included in the live validation MVP

- single-page landing experience;
- individual and family modes;
- aggregate monthly prescription spend by household member or total;
- optional expected routine/urgent-care visits and current out-of-pocket cost per visit;
- configurable individual and family membership prices;
- hypothetical percentage-of-spend scenarios;
- monthly and annual comparison;
- break-even explanation;
- optional lead capture after a useful result;
- co-branding and source/partner attribution;
- first-party, privacy-safe analytics events;
- admin configuration for price hypotheses and copy versions;
- explicit disclaimers and uncertain-result states.

### Excluded from the live MVP

- clinical intake;
- diagnosis, treatment, prescribing, or eligibility advice;
- insurance-benefit determination;
- live formulary or pharmacy-network data;
- medication-name storage;
- payment or enrollment;
- ad retargeting based on calculator answers;
- automated email/SMS containing medication names or health details;
- claims that savings will occur.

### Clickable prototype only

A clearly labeled sample mode may demonstrate a future medication lookup. It must use fictional/sample data and display a persistent banner:

> Prototype only — sample data, not a benefit or medication-eligibility result.

## Landing-page structure

1. **Hero** — headline, one-sentence explanation, “Check my numbers” CTA.
2. **Trust strip** — “No diagnosis,” “No medication promise,” “Estimates only,” “About 2 minutes.”
3. **How it works** — enter spending → compare scenarios → choose whether to learn more.
4. **Calculator** — progressive, one decision per screen on mobile.
5. **Results** — current spend, membership price, scenarios, break-even explanation.
6. **Plan detail preview** — only verified inclusions and exclusions.
7. **FAQ** — membership versus insurance, prescribing independence, pharmacy/formulary uncertainty, cancellation.
8. **Optional lead capture** — save/email a summary or request verified updates.
9. **Compliance footer** — privacy, terms, affiliate/financial disclosure, no-medical-advice language, effective date.

## User flow

### Flow A — Individual

1. Land with partner and campaign attribution stored separately from health-derived inputs.
2. Select **Just me**.
3. Enter estimated monthly out-of-pocket prescription spending as either an exact amount or range.
4. Optionally enter routine/urgent-care visits expected per year and typical out-of-pocket cost.
5. Select **Show my comparison**.
6. View a result immediately; do not gate the first useful result with email.
7. Adjust the scenario slider for the share of entered prescription spend that might qualify in a hypothetical program.
8. View transparent monthly and annual math plus break-even point.
9. Choose one CTA:
   - “Send me this estimate”; or
   - “Notify me when verified medication lookup is available”; or
   - after production approval, “Review verified plan details.”
10. If contact details are submitted, use a separate consent block for email and a distinct unchecked consent for marketing SMS.

### Flow B — Family

1. Select **My household**.
2. Enter household size, capped only by the current configured plan rule after verification.
3. Choose either total household prescription spend or add anonymous “Person 1 / Person 2” spend rows.
4. Optionally add estimated household routine/urgent-care visits and costs.
5. View individual-versus-family membership comparison only if both are plausible; never recommend based only on margin.
6. Explain the assumptions and unresolved family-benefit rules.
7. Offer the same post-result CTA and consent flow.

### Flow C — Partner-branded page

1. Load verified partner logo/name from configuration.
2. Preserve `partner_id`, `campaign_id`, first-touch UTM, and last-touch UTM.
3. Show the same calculator and compliance language; partners cannot freely edit regulated claims.
4. Attribute result views, leads, and outbound clicks to the partner.
5. Provide the partner only aggregated reporting unless contracts, consent, and privacy review authorize lead-level sharing.

## Inputs

| Input | Required | Storage rule | Notes |
|---|---|---|---|
| Mode: individual/family | Yes | Analytics may store | Not medical data by itself |
| Monthly prescription spend | Yes | Prefer session-only; analytics receive a coarse band | User estimate, not a receipt |
| Household size | Family only | Coarse value permitted | Do not request names or dates of birth |
| Estimated visits/year | No | Session-only or coarse band | No symptoms or conditions |
| Typical cost/visit | No | Session-only or coarse band | Editable |
| Scenario share | Yes | Analytics may store selected band | Explicitly hypothetical before verified data |
| State | No in prototype; later if needed | Store only when operationally necessary | May affect service availability |
| Email | No | CRM | Ordinary contact data; separate from health answers |
| Mobile number | No | CRM with consent evidence | Never precheck SMS consent |
| Partner/campaign IDs | Automatic | Attribution store | Sanitize and allowlist |

Do not collect medication name, strength, quantity, condition, diagnosis, symptom, clinician, pharmacy, insurance ID, prescription number, date of birth, or medical record in Version 1.

## Calculations

All prices and assumptions must be configuration values with effective dates.

### Base variables

- `monthly_rx_spend`
- `visits_per_year`
- `cost_per_visit`
- `membership_monthly_price`
- `scenario_offset_rate` — 0%, 25%, 50%, or 75% in the live MVP
- `estimated_visit_cost_avoided_rate` — default 0% unless a verified benefit and comparison basis exist

### Formulas

```text
annual_current_rx = monthly_rx_spend * 12
annual_current_visits = visits_per_year * cost_per_visit
annual_current_total = annual_current_rx + annual_current_visits

hypothetical_rx_offset = annual_current_rx * scenario_offset_rate
hypothetical_visit_offset = annual_current_visits * estimated_visit_cost_avoided_rate
annual_membership_cost = membership_monthly_price * 12

illustrative_net_difference =
  hypothetical_rx_offset
  + hypothetical_visit_offset
  - annual_membership_cost

rx_break_even_per_month =
  max(0, annual_membership_cost - hypothetical_visit_offset) / 12
```

The result must call `illustrative_net_difference` a **scenario**, not “your savings.” The user must be able to see and change every assumption.

### Results

Show:

- entered current monthly/annual spend;
- configured membership monthly/annual cost;
- hypothetical amount offset at selected scenario;
- illustrative difference;
- prescription-spend break-even point;
- a plain-language explanation of what is and is not known;
- “last updated” date for prices and plan information.

Do not show:

- guaranteed savings;
- medication coverage/eligibility;
- expected health outcome;
- “recommended medication”;
- probability that a clinician will prescribe;
- unsupported comparison with insurance.

## Lead-capture timing and CTAs

Give the user a complete initial result before asking for contact information. This creates a cleaner value exchange and lets completion rate be measured independently of lead friction.

### Pre-production CTA hierarchy

1. **Primary:** “Send me this estimate”
2. **Secondary:** “Notify me when verified lookup is available”
3. **Partner page:** “Ask about offering this to my members/employees”

### Production CTA hierarchy, only after approval

1. “Review verified plan details”
2. “Continue to secure enrollment”
3. “Talk to support”

The product must not say “see if you qualify” when it is only measuring economic interest.

## Medication, strength, quantity, and formulary edge cases

These apply to the later verified-formulary module.

- Normalize brand/generic display but preserve the source formulary identity.
- A drug-name match without strength, form, and quantity match is **not** a positive result.
- Multiple matching variants require the user to choose a variant; no default positive match.
- Misspellings may offer suggestions but cannot convert to an eligibility result automatically.
- Combination products must match all active ingredients and formulation.
- Extended-release and immediate-release products are distinct.
- Tablets, capsules, liquids, creams, injectables, and devices are distinct.
- Quantity and day-supply limits must be part of the result.
- Pharmacy-network or mail-order restrictions must appear adjacent to the result.
- A stale or unavailable formulary version produces **Unable to verify**, not “not covered.”
- A no-match result means “not found in this version,” not “never eligible.”
- Family results must identify whether limits are per person, per household, or unknown.
- Every result must show source/version/effective date.
- Always separate benefit eligibility from clinical prescribing.

## What can be shown before formulary permission

- aggregate spend comparison;
- membership price hypothesis clearly labeled;
- hypothetical offset scenarios;
- break-even point;
- general explanation that some programs use formularies with drug/strength/quantity rules;
- sample-mode UX using fictional data;
- waitlist for a verified lookup.

Do not reproduce, scrape, transcribe, or display a real LegUp/BestChoiceRx formulary without written authorization covering use, updates, and presentation.

## Data model

Names are conceptual and should map to Base44 Entities. Use least-privilege access and retention rules.

### `PricingConfig`

- `id`
- `provider_key` — neutral internal key
- `plan_key`
- `display_name`
- `audience_type` — individual/family/group
- `monthly_retail_price`
- `monthly_wholesale_cost` — admin only
- `max_household_size`
- `effective_from`
- `effective_to`
- `status` — draft/approved/retired
- `source_reference`
- `approved_copy_version`

### `CalculatorSession`

- `id` — random, nonsemantic
- `created_at`
- `mode`
- `rx_spend_band` — not exact amount
- `visit_band`
- `scenario_band`
- `result_band`
- `pricing_config_id`
- `partner_id`
- `campaign_id`
- `first_touch_utm_id`
- `last_touch_utm_id`
- `consent_state`
- `expires_at`

Exact calculator values should remain client/session-side for Version 1 unless a documented business need and privacy review justify retention.

### `Lead`

- `id`
- `email`
- `phone` — optional
- `first_name` — optional
- `lead_type` — consumer/partner/employer/broker
- `partner_id`
- `campaign_id`
- `email_consent_at`
- `sms_consent_at`
- `consent_copy_version`
- `source_session_id`
- `status`
- `created_at`

Do not copy spend bands, medication data, or inferred conditions into the ordinary CRM lead record.

### `Partner`

- `id`
- `name`
- `slug`
- `vertical`
- `logo_file`
- `brand_colors`
- `approved_headline_id`
- `status`
- `reporting_access_level`
- `commercial_terms_reference`

### `Campaign` and `AttributionTouch`

- sanitized source, medium, campaign, content, term;
- partner and creative IDs;
- first/last touch timestamps;
- landing variant;
- no medication, condition, or free-text health value in URL parameters.

### Future `FormularyVersion`

- provider/administrator key;
- version ID and effective date;
- source file hash;
- license/reference;
- ingestion timestamp;
- approved/published/retired status;
- quality-check results.

### Future `FormularyItem`

- normalized ingredient name;
- source display name;
- dosage form;
- strength value/unit;
- quantity/day-supply rule;
- retail/mail-order rule;
- member amount;
- cap/fair-use note;
- source row ID;
- formulary version ID;
- verification status.

## Analytics and conversion events

Use a first-party event store for funnel analysis. Third-party marketing pixels may receive only page/campaign events that do not reveal tool answers.

| Event | Allowed properties | Never include |
|---|---|---|
| `landing_view` | page variant, partner ID, sanitized UTM | Health inputs |
| `calculator_start` | individual/family, page variant | Exact spend |
| `calculator_step_complete` | step name, elapsed band | Field values |
| `result_view` | result band, scenario band, price config ID | Medication or exact costs |
| `lead_form_view` | CTA variant | Calculator answers |
| `lead_submit` | lead type, consent flags, partner ID | Health-derived inputs |
| `plan_detail_click` | plan key, partner ID | Search/query data |
| `enrollment_handoff` | approved plan key, opaque attribution token | Health inputs or PHI |
| `error_view` | error code, app version | User-entered free text |

Primary funnel metrics:

- landing-to-start;
- start-to-result;
- result-to-lead;
- result-to-plan-detail click;
- handoff-to-paid member once trustworthy server-side reporting exists;
- performance by partner, campaign, page variant, individual/family mode, and coarse spend band.

## Source, UTM, and partner attribution

- Validate all query parameters against length and character limits.
- Store first and last touch separately.
- Convert external parameters to internal opaque IDs before enrollment handoff.
- Define attribution window and precedence before paying partners.
- Do not place medication names, search terms, spend, state, or household details in URLs.
- Partners should use assigned links/QR codes; manual partner-code entry is a fallback.
- Deduplicate leads and paid members without exposing clinical identifiers.

## Admin workflow

### Price and copy updates

1. Admin creates a draft configuration with source reference and effective date.
2. A second reviewer confirms math, plan wording, and approved claims.
3. Preview shows all affected pages and calculations.
4. Publish creates an immutable version and audit entry.
5. Rollback selects a prior approved version; no silent overwrites.

### Future formulary updates

1. Upload authorized CSV/API snapshot through `UploadFile` or approved integration.
2. Validate schema, row count, duplicates, missing strength/form/quantity, and effective date.
3. Compare against current version and flag additions/removals/changes.
4. Test a fixed set of known positive, negative, ambiguous, and expired cases.
5. Require human approval.
6. Publish atomically and retain prior version for audit/rollback.
7. Expire results/caches from the old version.

## Error, empty, unavailable, and uncertain states

- **Empty:** explain the minimum input and keep the CTA disabled.
- **Zero spend:** show membership cost and non-savings value without inventing a positive result.
- **Very high spend:** show the arithmetic but add that actual eligible amounts may be far lower.
- **Config unavailable:** “We cannot calculate this plan right now”; never fall back to a hidden default price.
- **Network error:** preserve local inputs and offer retry.
- **No partner found:** load neutral branding and keep the invalid code out of analytics.
- **Future no drug match:** “Not found in the current data” with version date and verification option.
- **Future ambiguous match:** request strength/form/quantity; do not guess.
- **Future stale feed:** disable positive eligibility results.
- **Lead failure:** keep the result visible and provide a retry; do not submit twice.

## Mobile-first requirements

- one primary question per screen;
- numeric keyboard for currency fields;
- 44px minimum touch targets;
- progress indicator with text, not color alone;
- sticky primary action that does not obscure disclosures;
- result cards readable at 320px width;
- no horizontal tables in the consumer flow;
- load critical calculator UI without waiting for nonessential analytics;
- preserve state during accidental navigation and browser back.

## Accessibility requirements

Target WCAG 2.2 AA:

- semantic headings, labels, fieldsets, and error summaries;
- full keyboard operation and visible focus;
- screen-reader announcements for step and result changes;
- no color-only status;
- adequate contrast and scalable text;
- reduced-motion support;
- plain-language disclosures adjacent to claims;
- charts, if used, require text equivalents and should not be necessary to understand results.

## Privacy by design

- collect aggregate financial estimates, not medical histories;
- make medication lookup local/session-only by default if later added;
- separate contact/consent data from calculator events;
- use short retention for anonymous sessions;
- no session replay on calculator or result pages unless a qualified privacy review expressly approves it;
- no ad-pixel custom events containing health-derived values;
- no free-text health fields;
- no health data in URL, referrer, email subject, SMS, logs, crash reports, or support-ticket titles;
- encrypt data in transit and at rest; restrict admin access and log exports;
- publish a clear privacy notice describing first-party analytics, partners, retention, and deletion requests;
- assess whether HIPAA, FTC Health Breach Notification Rule, state consumer-health laws, TCPA, CAN-SPAM, and other requirements apply to the actual role and data flows.

HHS OCR warns regulated entities to evaluate third-party tracking technologies, and FTC guidance addresses consumer health information even where HIPAA may not apply. These boundaries require counsel/privacy review; calling the site “non-HIPAA” is not a control.

## Information prohibited from ordinary pixels and marketing analytics

- medication names or search strings;
- strength, dosage form, quantity, day supply;
- diagnosis, condition, symptom, treatment interest, or clinician request;
- pharmacy or prescription identifiers;
- exact prescription spending or inferred medication burden;
- household member health details;
- clinical/program eligibility;
- enrollment/intake answers;
- any user ID that directly links these values to contact information.

## Portability requirements

- use `ProviderAdapter` and configuration records rather than LegUp-specific logic;
- keep normalized plan and formulary schemas independent of a vendor;
- store source rights/version metadata with every imported dataset;
- own domain, content, code, analytics, CRM, consent records, and partner links;
- use opaque enrollment handoff tokens and maintain mapping outside the provider;
- make provider price, plan rules, state coverage, and CTA URL replaceable without changing pages;
- support side-by-side provider configurations in admin even if only one is active;
- never use a provider's customer ID as the primary identity in our systems.

## Base44 implementation constraints

If implementation begins, use only the approved stack:

- React, Tailwind, shadcn/ui;
- lucide-react icons that exist;
- react-router-dom and `createPageUrl('PageName')` for internal links;
- react-hook-form;
- recharts only if a chart adds clarity;
- Entities SDK from `@/entities` for list, filter, create, bulkCreate, update, delete, and schema operations;
- User methods supplied by the platform;
- Core integrations from `@/integrations/Core`, including `UploadFile`, `InvokeLLM`, `SendEmail`, `GenerateImage`, and `ExtractDataFromUploadedFile` when appropriate.

Implementation rules:

- no authentication pages;
- null checks at every data boundary;
- visible `Loader2` loading state for all fetches/actions;
- small, focused, drop-in components;
- avoid `try/catch` unless explicitly required;
- do not call an LLM to make medication eligibility or savings decisions;
- do not persist exact inputs unless explicitly enabled after privacy review.

Suggested components:

- `SavingsHero`
- `CalculatorModeSelector`
- `PrescriptionSpendStep`
- `VisitCostStep`
- `SavingsScenarioStep`
- `SavingsResult`
- `AssumptionDisclosure`
- `LeadCaptureCard`
- `PartnerBrandHeader`
- `PricingConfigAdmin`
- future `FormularyImportReview`

Suggested pages:

- `SavingsCheck`
- `SavingsResult` only if shareable results are implemented without exposing inputs in URL
- `PartnerSavingsCheck`
- `PartnerROI`
- `AdminPricing`
- future `AdminFormulary`

## Acceptance criteria for the prototype

- A first-time mobile user can reach a meaningful result in under two minutes.
- The result is mathematically reproducible from visible inputs and assumptions.
- No positive medication, coverage, prescribing, or savings guarantee appears.
- Results render correctly for $0, low, and high spend and for individual/family modes.
- A user can complete the calculator without giving contact information.
- Contact consent is separate from calculator use and SMS consent is not prechecked.
- Invalid/missing config never produces a default claim.
- No prohibited health-derived value appears in URLs, pixel payloads, or CRM records.
- Partner and campaign attribution survive the flow.
- The provider can be changed through configuration, not component rewrites.

## Production launch gates

Do not activate live benefit results or enrollment until all gates are passed:

1. Signed formulary/data license and update mechanism.
2. Verified drug/strength/form/quantity, caps, family, pharmacy, and mail-order rules.
3. Written approved claim language and creative approval process.
4. Customer/lead ownership, CRM, export, portability, transition, and termination terms.
5. Data-processing map, privacy review, retention/deletion rules, and incident responsibilities.
6. Accurate prices, refund/cancellation terms, service availability, and support ownership.
7. Server-side attribution and paid-member reporting.
8. Required advertising certifications and platform approvals.
9. Healthcare-counsel review of compensation and benefit positioning.

This specification is for product and business planning, not legal or medical advice.
