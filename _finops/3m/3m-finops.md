---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: 3m-partner-supplier-api-openapi.yml
  format: yaml
  label: 3M Partner and Supplier API
  slug: partner-supplier-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/3m/refs/heads/main/openapi/3m-partner-supplier-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: 3M's Partner and Supplier API is delivered under a commercial trading-partner contract; there is no consumption-based pricing or public billing surface. FinOps mapping is structural only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: 3M Company
  ProviderName: 3M
  PublisherName: 3M Company
  ServiceCategory: Industrial / Supply Chain
  ServiceName: 3M Partner and Supplier API
layout: finops
meters:
- aggregation: count
  description: Master trading-partner contract — not a metered unit; cost flows through goods/services pricing rather than per-API-call.
  dimensions:
  - partner
  name: partner_contract
  unit: contract
name: 3M Finops
provider_name: 3M
provider_slug: 3m
publisher_name: 3M Company
service_category: Industrial / Supply Chain
slug: 3m-finops
source_filename: 3m-finops.yml
source_heading: FinOps Profile
source_url: https://www.3m.com/3M/en_US/company-us/partners-suppliers/api/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: 3M\nproviderId: 3m\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Industrial\n  - Manufacturing\n  - Supply Chain\n  - FinOps\n  - FOCUS\ndescription: 3M's Partner and Supplier API is delivered under a commercial trading-partner contract; there\n  is no consumption-based pricing or public billing surface. FinOps mapping is structural only.\nnotes: No public developer pricing — placeholder only. Costs flow through the master partner agreement,\n  not a metered API invoice.\nsources:\n  - https://www.3m.com/3M/en_US/company-us/partners-suppliers/api/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: 3M Company\nserviceCategory: Industrial / Supply Chain\n\
  billingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: 3M Partner and Supplier API\n  ServiceCategory: Industrial / Supply Chain\n  ProviderName: 3M\n  PublisherName: 3M Company\n  InvoiceIssuerName: 3M Company\n  BillingCurrency: USD\nmeters:\n  - name: partner_contract\n    description: Master trading-partner contract — not a metered unit; cost flows through goods/services\n      pricing rather than per-API-call.\n    unit: contract\n    aggregation: count\n    dimensions:\n      - partner\nprinciples:\n  - name: Visibility\n    description: Track API integration cost as part of partner-onboarding and IT integration spend; 3M\n      does not provide a metered usage feed.\n  - name: Allocation\n    description: Allocate the integration cost to the procurement / supply-chain function that owns the\n      3M trading relationship.\n  - name: Optimization\n    description: Optimize\
  \ by consolidating order/delivery/invoice queries into batch flows rather than\n      polling, in line with the partner contract's throughput expectations.\n  - name: Accountability\n    description: Procurement leadership owns the 3M relationship; IT owns the integration runtime. Review\n      transaction volume against contract terms during partner business reviews.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/3m/refs/heads/main/finops/3m-finops.yml
sources:
- https://www.3m.com/3M/en_US/company-us/partners-suppliers/api/
specification: FinOps Framework
tags:
- Industrial
- Manufacturing
- Supply Chain
- FinOps
- FOCUS
---
