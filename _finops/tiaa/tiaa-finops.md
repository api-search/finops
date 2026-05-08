---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tiaa-fdx-openapi.yml
  format: yaml
  label: TIAA Financial Data Exchange API
  slug: tiaa-fdx-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tiaa/refs/heads/main/openapi/tiaa-fdx-openapi.yml
- filename: tiaa-sia-openapi.yml
  format: yaml
  label: TIAA Secure Income Account API
  slug: tiaa-sia-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tiaa/refs/heads/main/openapi/tiaa-sia-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract / Bilateral
description: 'FOCUS-aligned FinOps placeholder for TIAA: B2B retirement and recordkeeping APIs delivered under bilateral partner contracts; no public usage-based rate card.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Teachers Insurance and Annuity Association of America
  ProviderName: TIAA
  PublisherName: Teachers Insurance and Annuity Association of America
  ServiceCategory: Financial Services
  ServiceName: TIAA
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - partner
  name: contracted_partner_access
  unit: varies
name: Tiaa Finops
provider_name: TIAA
provider_slug: tiaa
publisher_name: Teachers Insurance and Annuity Association of America
service_category: Financial Services
slug: tiaa-finops
source_filename: tiaa-finops.yml
source_heading: FinOps Profile
source_url: https://www.tiaa.org/public/about-tiaa/working-at-tiaa/api-developer
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TIAA\nproviderId: tiaa\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Finance\n  - Retirement\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for TIAA: B2B retirement and recordkeeping APIs delivered\n  under bilateral partner contracts; no public usage-based rate card.'\nsources:\n  - https://www.tiaa.org/public/about-tiaa/working-at-tiaa/api-developer\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: TIAA APIs are not sold on a usage-based public rate card; FinOps observability is whatever the\n  partner agreement provides (typically invoice-line allocations, not per-call telemetry).\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Teachers Insurance and Annuity Association of America\nserviceCategory: Financial Services\nbillingModel:\n  pricingCategory: Contract / Bilateral\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: TIAA\n  ServiceCategory: Financial Services\n  ProviderName: TIAA\n  PublisherName: Teachers Insurance and Annuity Association of America\n  InvoiceIssuerName: Teachers Insurance and Annuity Association of America\n  BillingCurrency: USD\nmeters:\n  - name: contracted_partner_access\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - api\n      - partner\nprinciples:\n  - name: Visibility\n    description: Rely on the partner-portal dashboards and contractual usage statements TIAA provides;\n      no public usage API exists.\n  - name: Allocation\n    description: Allocate the partner contract cost to the retirement, payroll, or wealth team that owns\n      the integration with TIAA.\n  -\
  \ name: Optimization\n    description: Optimize at the integration design layer — batch FDX aggregation calls, cache participant\n      reference data, and avoid duplicate Payroll360 submissions.\n  - name: Accountability\n    description: A named partnership owner is accountable for the TIAA agreement, data-sharing scope,\n      and renewal cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tiaa/refs/heads/main/finops/tiaa-finops.yml
sources:
- https://www.tiaa.org/public/about-tiaa/working-at-tiaa/api-developer
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Finance
- Retirement
- FinOps
- FOCUS
---
