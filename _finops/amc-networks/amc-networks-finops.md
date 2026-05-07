---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise / Bilateral
description: FinOps scaffold for AMC Networks. The company does not publish a public API billing surface; advertising and affiliate engagements are invoiced per negotiated insertion order or affiliate agreement. FOCUS mappings remain conceptual until a metered API offering is published.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: AMC Networks Inc.
  ProviderName: AMC Networks
  PublisherName: AMC Networks Inc.
  ServiceCategory: Media & Entertainment
  ServiceName: AMC Networks
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter for engagements settled outside a metered API. Real meters cannot be enumerated until AMC Networks publishes a metered API billing surface.
  name: contracted_engagement
  unit: varies
name: Amc Networks Finops
provider_name: AMC Networks
provider_slug: amc-networks
publisher_name: AMC Networks Inc.
service_category: Media & Entertainment
slug: amc-networks-finops
source_filename: amc-networks-finops.yml
source_heading: FinOps Profile
source_url: https://www.amcnetworks.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AMC Networks\nproviderId: amc-networks\npublisherName: AMC Networks Inc.\nserviceCategory: Media & Entertainment\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Entertainment\n  - Streaming\n  - Cable Television\n  - Advertising\n  - Media\n  - FAST Channels\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps scaffold for AMC Networks. The company does not publish a public API billing surface; advertising and affiliate engagements are invoiced per negotiated insertion order or affiliate agreement. FOCUS mappings remain conceptual until a metered API offering is published.\nnotes: >-\n  AMC Networks does not publish a public API developer portal with documented pricing, rate limits, or quotas. Affiliate access is gated via the affiliate portal and Audience+/AMCN Outcomes ad-tech engagements are negotiated per-deal. Reconcile when public\
  \ API pricing is published.\nsources:\n  - https://www.amcnetworks.com/\n  - https://affiliate.amcnetworks.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Enterprise / Bilateral\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: AMC Networks\n  ServiceCategory: Media & Entertainment\n  ProviderName: AMC Networks\n  PublisherName: AMC Networks Inc.\n  InvoiceIssuerName: AMC Networks Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contracted_engagement\n    description: >-\n      Placeholder meter for engagements settled outside a metered API. Real\n      meters cannot be enumerated\
  \ until AMC Networks publishes a metered\n      API billing surface.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: >-\n      Without a public usage API, consumers must rely on contract reporting,\n      invoice line items, and any tenant dashboards provided under the\n      partner agreement.\n  - name: Allocation\n    description: >-\n      Allocate spend by purchase order, contract identifier, or business unit\n      receiving the AMC Networks service. Tag at the procurement layer, not\n      the API call layer.\n  - name: Optimization\n    description: >-\n      Optimization levers live in commercial negotiation (volume commitments,\n      term length, scope) rather than in API-level caching or throttling.\n  - name: Accountability\n    description: >-\n      Procurement and the business owner of the AMC Networks relationship own\n      the spend; finance reviews invoice lines on the contract cadence.\nmaintainers:\n  - FN: Kin Lane\n \
  \   email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amc-networks/refs/heads/main/finops/amc-networks-finops.yml
sources:
- https://www.amcnetworks.com/
- https://affiliate.amcnetworks.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Entertainment
- Streaming
- Cable Television
- Advertising
- Media
- FAST Channels
- FinOps
- FOCUS
---
