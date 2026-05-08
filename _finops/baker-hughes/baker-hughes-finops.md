---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Enterprise License (Custom)
description: 'FOCUS-aligned FinOps shape for Baker Hughes digital platforms (Cordant, BHC3 AI Suite): enterprise license + custom-negotiated. Public meter or rate-card data is not available; this artifact describes the dimensions a customer should track inside their own contract.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Baker Hughes Company
  PricingCategory: Enterprise License
  PricingUnit: contract-year
  ProviderName: Baker Hughes
  PublisherName: Baker Hughes Company
  ServiceCategory: Industrial / Energy Software
  ServiceName: Baker Hughes Digital Platforms
layout: finops
meters:
- aggregation: sum
  description: Annual enterprise platform license (Cordant / BHC3 AI Suite)
  dimensions:
  - tenant
  - product
  name: platform_license
  unit: contract-year
- aggregation: max
  description: Assets (wells, equipment, plants) under platform monitoring; common contract dimension
  dimensions:
  - asset_class
  - site
  name: monitored_assets
  unit: asset
- aggregation: sum
  description: BHC3 AI application seats / use-case licenses
  dimensions:
  - application
  - business_unit
  name: ai_application_seats
  unit: seat
- aggregation: sum
  description: API call volume — tracked for capacity-management, not per-call billed
  dimensions:
  - api
  - tenant
  name: api_calls
  unit: request
name: Baker Hughes Finops
provider_name: Baker Hughes
provider_slug: baker-hughes
publisher_name: Baker Hughes Company
service_category: Industrial / Energy Software
slug: baker-hughes-finops
source_filename: baker-hughes-finops.yml
source_heading: FinOps Profile
source_url: https://www.bakerhughes.com/cordant
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Baker Hughes\nproviderId: baker-hughes\npublisherName: Baker Hughes Company\nserviceCategory: Industrial / Energy Software\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy Technology\n  - Industrial IoT\n  - Oil And Gas\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Baker Hughes digital platforms (Cordant, BHC3 AI Suite):\n  enterprise license + custom-negotiated. Public meter or rate-card data is not available; this artifact\n  describes the dimensions a customer should track inside their own contract.'\nnotes: No public pricing. Replace meter assumptions with the meters defined in the executed Baker Hughes\n  contract once available.\n\
  sources:\n  - https://www.bakerhughes.com/cordant\n  - https://www.bakerhughes.com/bhc3\nprinciples:\n  - name: Visibility\n    description: Negotiate access to a contract-level usage report from Baker Hughes Digital (assets monitored,\n      models scored, telemetry ingested) so consumption can be tracked alongside the fixed license fee.\n  - name: Allocation\n    description: Tag the platform license to the operations or asset-management business unit that owns\n      the production assets being monitored; allocate AI-application costs by use case (predictive maintenance,\n      production optimization, etc.).\n  - name: Optimization\n    description: Right-size the asset-monitoring scope each renewal — only instrument assets where the\n      AI model has demonstrated downtime or yield improvement above the per-asset license cost.\n  - name: Accountability\n    description: Assign a named platform owner inside the asset-management or digital function; review\n      contract utilization\
  \ before each annual true-up.\nbillingModel:\n  pricingCategory: Enterprise License (Custom)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Baker Hughes Digital Platforms\n  ServiceCategory: Industrial / Energy Software\n  ProviderName: Baker Hughes\n  PublisherName: Baker Hughes Company\n  InvoiceIssuerName: Baker Hughes Company\n  PricingCategory: Enterprise License\n  PricingUnit: contract-year\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: platform_license\n    description: Annual enterprise platform license (Cordant / BHC3 AI Suite)\n    unit: contract-year\n    aggregation: sum\n    dimensions:\n      - tenant\n      - product\n  - name: monitored_assets\n    description: Assets (wells, equipment, plants) under platform monitoring; common contract dimension\n    unit: asset\n    aggregation: max\n    dimensions:\n      - asset_class\n\
  \      - site\n  - name: ai_application_seats\n    description: BHC3 AI application seats / use-case licenses\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - application\n      - business_unit\n  - name: api_calls\n    description: API call volume — tracked for capacity-management, not per-call billed\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - tenant\napis:\n  - name: Baker Hughes Cordant Industrial Platform\n    baseURL: ''\n    tags:\n      - Asset Performance Management\n      - Industrial IoT\n      - Process Optimization\n      - Emissions Management\n    serviceName: Baker Hughes Cordant Industrial Platform\n    serviceCategory: API\n  - name: Baker Hughes BHC3 AI Suite\n    baseURL: ''\n    tags:\n      - Artificial Intelligence\n      - Energy\n      - Oil And Gas\n      - Predictive Maintenance\n    serviceName: Baker Hughes BHC3 AI Suite\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Monitored Asset\n    metric:\
  \ platform_license / monitored_assets\n    target: align to per-asset downtime / yield uplift\n  - name: Cost per AI Use Case\n    metric: ai_application_cost / instrumented_use_cases\n    target: TBD per business unit\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/baker-hughes/refs/heads/main/finops/baker-hughes-finops.yml
sources:
- https://www.bakerhughes.com/cordant
- https://www.bakerhughes.com/bhc3
specification: FinOps Framework
tags:
- Energy Technology
- Industrial IoT
- Oil And Gas
- FinOps
- FOCUS
---
