---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: starbucks-starbucks-api-openapi.yml
  format: yaml
  label: Starbucks API
  slug: starbucks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/starbucks/refs/heads/main/openapi/starbucks-starbucks-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: Starbucks does not operate a public, metered API program. There is no public price list, meter set, or invoice surface for API consumption — all integrations are private partner contracts outside the FOCUS-billable surface.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Starbucks Corporation
  ProviderName: Starbucks
  PublisherName: Starbucks Corporation
  ServiceCategory: Food & Beverage / Retail
  ServiceName: Starbucks
layout: finops
meters:
- aggregation: sum
  description: Placeholder for contractual line items defined per partner agreement.
  name: contracted_engagement
  unit: varies
name: Starbucks Finops
provider_name: Starbucks
provider_slug: starbucks
publisher_name: Starbucks Corporation
service_category: Food & Beverage / Retail
slug: starbucks-finops
source_filename: starbucks-finops.yml
source_heading: FinOps Profile
source_url: https://www.starbucks.com/business
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Starbucks\nproviderId: starbucks\npublisherName: Starbucks Corporation\nserviceCategory: Food & Beverage / Retail\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Food Service\n  - Loyalty\ndescription: Starbucks does not operate a public, metered API program. There is no public price list,\n  meter set, or invoice surface for API consumption — all integrations are private partner contracts\n  outside the FOCUS-billable surface.\nsources:\n  - https://www.starbucks.com/business\nnotes: No public pricing or billing surface to reconcile. Meters, FOCUS columns, and principles are deferred\n  until\
  \ a partner contract defines them.\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Starbucks\n  ServiceCategory: Food & Beverage / Retail\n  ProviderName: Starbucks\n  PublisherName: Starbucks Corporation\n  InvoiceIssuerName: Starbucks Corporation\n  BillingCurrency: USD\nmeters:\n  - name: contracted_engagement\n    description: Placeholder for contractual line items defined per partner agreement.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility is whatever telemetry (usage reports, invoice line items) the partner contract\n      with Starbucks Technology grants — there is no public usage API.\n  - name: Allocation\n    description: Cost allocation is contract-by-contract; tag the partnership engagement in your own\n      ERP / cost system rather than relying on a Starbucks-provided breakdown.\n  - name: Optimization\n\
  \    description: Optimization happens at contract renewal, not via dynamic plan changes — there is no\n      public pay-as-you-go surface to optimize against.\n  - name: Accountability\n    description: A single business owner of the Starbucks partnership relationship should own the engagement\n      cost line and renewal cycle.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/starbucks/refs/heads/main/finops/starbucks-finops.yml
sources:
- https://www.starbucks.com/business
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Food Service
- Loyalty
---
