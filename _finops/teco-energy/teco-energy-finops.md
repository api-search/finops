---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: teco-energy-outage-openapi.yml
  format: yaml
  label: Tampa Electric Outage API
  slug: outage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/teco-energy/refs/heads/main/openapi/teco-energy-outage-openapi.yml
- filename: teco-energy-account-openapi.yml
  format: yaml
  label: Tampa Electric Account API
  slug: account-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/teco-energy/refs/heads/main/openapi/teco-energy-account-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract / Partner-Negotiated
description: FOCUS-aligned FinOps shape for TECO Energy's Tampa Electric API surface. Access is partner-gated and not consumption-priced as a developer product; this artifact captures the publisher identity and a placeholder meter only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: TECO Energy, Inc.
  ProviderName: TECO Energy
  PublisherName: TECO Energy, Inc.
  ServiceCategory: Energy / Utilities
  ServiceName: Tampa Electric API Management
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - subscription
  name: api_requests
  unit: request
name: Teco Energy Finops
provider_name: TECO Energy
provider_slug: teco-energy
publisher_name: TECO Energy, Inc.
service_category: Energy / Utilities
slug: teco-energy-finops
source_filename: teco-energy-finops.yml
source_heading: FinOps Profile
source_url: https://developer.tecoenergy.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TECO Energy\nproviderId: teco-energy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Utilities\n  - Electric\n  - Natural Gas\n  - Smart Grid\n  - Tampa Bay\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for TECO Energy's Tampa Electric API surface. Access is\n  partner-gated and not consumption-priced as a developer product; this artifact captures the\n  publisher identity and a placeholder meter only.\nsources:\n  - https://developer.tecoenergy.com/\nnotes: TECO Energy does not publish a developer-API price list. There is no public usage-billing\n  surface to map onto FOCUS columns. Meters and FOCUS values below describe identity only; charge\n  categories, currency conventions, and unit pricing are not reconciled.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TECO Energy, Inc.\nserviceCategory: Energy / Utilities\nbillingModel:\n  pricingCategory: Contract / Partner-Negotiated\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Tampa Electric API Management\n  ServiceCategory: Energy / Utilities\n  ProviderName: TECO Energy\n  PublisherName: TECO Energy, Inc.\n  InvoiceIssuerName: TECO Energy, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - subscription\nprinciples:\n  - name: Visibility\n    description: API usage is visible to the partner through the Azure API Management developer\n      portal; there is no published TECO Energy spend dashboard for API consumption.\n  - name: Allocation\n    description: Allocation is by Azure APIM subscription key\
  \ issued to a specific partner program.\n  - name: Optimization\n    description: Optimization is bounded by the partner's contractual access tier; there are no\n      publicly documented cost levers (committed use, caching tiers) for this API surface.\n  - name: Accountability\n    description: The named partner organization is the accountable owner of API consumption under\n      its TECO Energy access agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/teco-energy/refs/heads/main/finops/teco-energy-finops.yml
sources:
- https://developer.tecoenergy.com/
specification: FinOps Framework
tags:
- Energy
- Utilities
- Electric
- Natural Gas
- Smart Grid
- Tampa Bay
- FinOps
- FOCUS
---
