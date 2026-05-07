---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD/EUR/GBP/multi-currency
  billingFrequency: Per Policy / Periodic Settlement
  chargeCategories:
  - Purchase
  - Adjustment
  - Refund
  - Tax
  pricingCategory: Take Rate (Premium / Commission)
description: 'FOCUS-aligned FinOps for Chubb Studio: the cost shape for distributors is insurance economics (written premium, commission, ceded premium, claims) rather than per-API-call usage. Chubb does not bill partners for API access; cost flows through the partner agreement and policy-level settlement.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Chubb Limited (or local Chubb underwriting entity)
  PricingCategory: Take Rate
  ProviderName: Chubb
  PublisherName: Chubb Limited
  ServiceCategory: Insurance / Embedded Insurance
  ServiceName: Chubb Studio
layout: finops
meters:
- aggregation: sum
  description: Gross written premium for policies issued through the partner channel
  dimensions:
  - line
  - country
  - partner
  name: written_premium
  unit: policy
- aggregation: sum
  description: Commission / take-rate paid to the distributing partner
  dimensions:
  - line
  - partner
  name: commission
  unit: policy
- aggregation: sum
  description: Claims paid against policies in the partner book
  dimensions:
  - line
  - country
  name: claims_incurred
  unit: claim
- aggregation: sum
  description: API calls against Chubb Studio (operational signal, not a billing meter)
  dimensions:
  - partner
  - environment
  name: api_requests
  unit: request
name: Chubb Finops
provider_name: Chubb
provider_slug: chubb
publisher_name: Chubb Limited
service_category: Insurance / Embedded Insurance
slug: chubb-finops
source_filename: chubb-finops.yml
source_heading: FinOps Profile
source_url: https://www.chubb.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Chubb\nproviderId: chubb\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Embedded Insurance\n  - Insurance\n  - Partner Integration\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Chubb Studio: the cost shape for distributors is insurance\n  economics (written premium, commission, ceded premium, claims) rather than per-API-call usage.\n  Chubb does not bill partners for API access; cost flows through the partner agreement and\n  policy-level settlement.'\nnotes: Chubb does not expose a metered-API billing surface. The FinOps shape below reflects the\n  partner-agreement economics that govern Chubb Studio distribution.\nsources:\n  - https://www.chubb.com/\n  - https://chubbstudio.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Chubb Limited\nserviceCategory: Insurance / Embedded Insurance\nbillingModel:\n  pricingCategory: Take Rate (Premium / Commission)\n  billingFrequency: Per Policy / Periodic Settlement\n  billingCurrency: USD/EUR/GBP/multi-currency\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Refund\n    - Tax\nfocusColumns:\n  ServiceName: Chubb Studio\n  ServiceCategory: Insurance / Embedded Insurance\n  ProviderName: Chubb\n  PublisherName: Chubb Limited\n  InvoiceIssuerName: Chubb Limited (or local Chubb underwriting entity)\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Take Rate\nmeters:\n  - name: written_premium\n    description: Gross written premium for policies issued through the partner channel\n    unit: policy\n    aggregation: sum\n    dimensions:\n      - line\n      - country\n      - partner\n  - name: commission\n    description: Commission / take-rate\
  \ paid to the distributing partner\n    unit: policy\n    aggregation: sum\n    dimensions:\n      - line\n      - partner\n  - name: claims_incurred\n    description: Claims paid against policies in the partner book\n    unit: claim\n    aggregation: sum\n    dimensions:\n      - line\n      - country\n  - name: api_requests\n    description: API calls against Chubb Studio (operational signal, not a billing meter)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - environment\nprinciples:\n  - name: Visibility\n    description: Track partner-channel performance through Chubb Studio dashboards, monthly\n      bordereau reports, and ceded-premium statements.\n  - name: Allocation\n    description: Allocate written-premium, commission, and claims by line of business, country, and\n      partner so each distribution channel can be P&L'd separately.\n  - name: Optimization\n    description: Tune product mix, partner pricing, and underwriting filters to lift\
  \ loss ratio and\n      acquisition margin; consolidate low-volume partners on shared API tenants.\n  - name: Accountability\n    description: Underwriting owns loss ratio; distribution / partnerships owns commission economics;\n      finance owns ceded-premium and claims settlement; technology owns Chubb Studio uptime and\n      integration certification.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chubb/refs/heads/main/finops/chubb-finops.yml
sources:
- https://www.chubb.com/
- https://chubbstudio.com/
specification: FinOps Framework
tags:
- Embedded Insurance
- Insurance
- Partner Integration
- FinOps
- FOCUS
---
