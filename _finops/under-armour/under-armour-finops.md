---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mapmyfitness-openapi.yml
  format: yaml
  label: MapMyFitness API
  slug: mapmyfitness-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/under-armour/refs/heads/main/openapi/mapmyfitness-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Refund
  - Adjustment
  pricingCategory: Custom Contract
description: 'FOCUS-aligned FinOps for Under Armour: B2B-only commerce / partner integrations under custom contracts; no public usage-meter or per-API price sheet.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Under Armour, Inc.
  ProviderName: Under Armour
  PublisherName: Under Armour, Inc.
  ServiceCategory: Apparel / Commerce
  ServiceName: Under Armour Integration
layout: finops
meters:
- aggregation: sum
  description: Active partner / commerce integration contract period
  name: contract_term
  unit: month
name: Under Armour Finops
provider_name: Under Armour
provider_slug: under-armour
publisher_name: Under Armour, Inc.
service_category: Apparel / Commerce
slug: under-armour-finops
source_filename: under-armour-finops.yml
source_heading: FinOps Profile
source_url: https://about.underarmour.com/en/contact/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Under Armour\nproviderId: under-armour\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Fitness\n  - Apparel\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Under Armour: B2B-only commerce / partner integrations under custom\n  contracts; no public usage-meter or per-API price sheet.'\nnotes: Under Armour has no public developer portal or pricing surface. Meters and FOCUS columns are placeholders\n  pending reconciliation against actual partner-contract invoices.\nsources:\n  - https://about.underarmour.com/en/contact/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Under Armour,\
  \ Inc.\nserviceCategory: Apparel / Commerce\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Refund\n    - Adjustment\nfocusColumns:\n  ServiceName: Under Armour Integration\n  ServiceCategory: Apparel / Commerce\n  ProviderName: Under Armour\n  PublisherName: Under Armour, Inc.\n  InvoiceIssuerName: Under Armour, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_term\n    description: Active partner / commerce integration contract period\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Reconcile spend from partner-contract statements; Under Armour does not expose a public\n      usage telemetry surface.\n  - name: Allocation\n    description: Allocate to the consuming line of business (DTC, wholesale, sponsorship) per the contract\n      scope.\n  - name: Optimization\n    description: Re-scope contract on renewal based on actual order\
  \ / data volume; consolidate retail\n      partner connections where possible.\n  - name: Accountability\n    description: Commerce / partner-management owners review contract performance and renewal terms.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/under-armour/refs/heads/main/finops/under-armour-finops.yml
sources:
- https://about.underarmour.com/en/contact/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Fitness
- Apparel
- FinOps
- FOCUS
---
