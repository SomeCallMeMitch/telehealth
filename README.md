# Telehealth Reseller / Distribution Research

This repository is the working source of truth for evaluating telehealth resale, white-label, partner-distribution, and eventual platform opportunities.

## Current thesis

There may be **three distinct businesses** here:

1. **B2C telehealth membership brand** — acquire consumers and resell primary care, urgent care, prescription savings, family plans, and selected elective services.
2. **B2B channel-partner business** — recruit businesses to become telehealth resellers/partners and earn recurring economics rather than a one-time referral bounty.
3. **Longer-term software/platform business** — own the customer relationship, lead-generation tools, app, CRM/data layer, and eventually move from a turnkey reseller such as LegUpRx to direct clinical infrastructure such as Beluga, Karpa, OpenLoop, Wheel, or another provider.

The current leading low-cost test platform is **LegUpRx**, primarily because of its unusually low entry cost and the economics of its primary-care + prescription program. However, its current partner agreement contains concerning customer/referral ownership and termination language, so the business should be structured so that LegUp is a fulfillment layer, not the asset itself.

## Key current findings

- LegUpRx monthly platform: approximately **$249/month** after trial.
- Care Services is a **$199 one-time add-on** on the monthly plan; annual package bundles additional services.
- Current wholesale care floors observed:
  - Primary Care: $25/mo
  - Primary Care + Rx: $30/mo
  - Family Primary Care: $75/mo
  - Family + Rx: $85/mo
  - Urgent Care: $20/mo
  - Urgent + Rx: $25/mo
  - Behavioral Health + Rx: $15/mo
  - Dermatology: $25/mo
  - Vet Care: $15/mo
- LegUp/National Telehealth Providers appears to power a real reseller ecosystem.
- LegUp's prescription program advertises hundreds to roughly 1,000 eligible medications at **$0 at the pharmacy** when prescribed and used under program rules.
- A LegUp/NTP reseller publicly identifies **BestChoiceRx** as the pharmacy-network provider behind its $0 medication program.
- LegUp's partner agreement says future commissions/referral rights may be forfeited at termination and referrals remain LegUp property. This is a major diligence issue.
- **Karpa** publicly takes a more ownership-friendly position: customers/patients/data are described as belonging to the brand, with export/offboarding language. This needs to be confirmed contractually for the exact plan purchased.
- **National Telehealth Providers is a DBA of Leg Up Recovery Franchising**, not an independent wholesaler that obviously can be bypassed.
- LegUp-related legal disclosures show underlying clinical organizations may include **Beluga Health**, among others.
- **Beluga Health** works directly with DTC telehealth brands and may provide a plausible migration path after traction.
- LegUp currently offers roughly **$500 for referring a new partner business**. A potentially better opportunity is a negotiated recurring channel-partner override.

## Repo layout

- `research/providers/` — provider/platform profiles
- `research/rx-program.md` — $0 prescription program investigation
- `research/reseller-ecosystem.md` — LegUp/NTP reseller brands and evidence of scale
- `research/channel-partner-models.md` — referral / override models
- `research/research-backlog.md` — prioritized next research questions
- `prompts/NEXT_CHAT.md` — handoff prompt for the next research chat

## Working principle

Keep the **brand, domain, CRM, lead-gen app, email/SMS list, analytics, and acquisition data** independent of any telehealth vendor wherever legally and technically possible. The long-term asset should be the distribution/customer-acquisition system, not a single vendor relationship.


## Current strategy decision — September 15, 2026

The first recommended live MVP is a **provider-neutral Prescription Cost & Telehealth Savings Check** using aggregate spending and transparent hypothetical scenarios. A drug-level **$0 Prescription Finder** remains the strongest upgrade, but it must wait for written formulary reuse rights, structured data, exact benefit rules, and approved claim language.

Initial validation should be partner-first: co-branded pages for a small number of businesses with existing audiences, plus a capped direct-consumer control. Broad paid acquisition should not scale until customer ownership and source-level unit economics are proven.

New work products:

- [LegUp Go-to-Market Strategy](research/legup-go-to-market-strategy.md)
- [Prescription Savings MVP Product Brief](product/rx-savings-mvp-brief.md)
- [Validation Economics and 30-Day Plan](research/validation-economics-and-30-day-plan.md)
- [LegUp Launch Requirements](research/legup-launch-requirements.md)
