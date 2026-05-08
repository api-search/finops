---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: taylor-morrison-home-search-openapi.yml
  format: yaml
  label: Taylor Morrison Home Search API
  slug: taylor-morrison-home-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/taylor-morrison-home/refs/heads/main/openapi/taylor-morrison-home-search-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Custom / Contact Sales
description: FinOps placeholder for Taylor Morrison Home Corporation. No public API billing surface; commercial relationships (trade, realtor, lender, vendor) are settled through standard AP processes against Taylor Morrison invoices.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Taylor Morrison Home Corporation
  ProviderName: Taylor Morrison
  PublisherName: Taylor Morrison Home Corporation
  ServiceCategory: Homebuilding
  ServiceName: Taylor Morrison
layout: finops
meters:
- aggregation: sum
  name: custom_engagement
  unit: varies
name: Taylor Morrison Home Finops
provider_name: taylor-morrison-home
provider_slug: taylor-morrison-home
publisher_name: Taylor Morrison Home Corporation
service_category: Homebuilding
slug: taylor-morrison-home-finops
source_filename: taylor-morrison-home-finops.yml
source_heading: FinOps Profile
source_url: https://www.taylormorrison.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: taylor-morrison-home\nproviderId: taylor-morrison-home\npublisherName: Taylor Morrison Home Corporation\nserviceCategory: Homebuilding\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Homebuilding\n  - Real Estate\n  - FinOps\n  - FOCUS\ndescription: FinOps placeholder for Taylor Morrison Home Corporation. No public API billing\n  surface; commercial relationships (trade, realtor, lender, vendor) are settled through standard\n  AP processes against Taylor Morrison invoices.\nsources:\n  - https://www.taylormorrison.com/\nnotes: No public billing telemetry. Meter list collapsed to custom engagement.\nbillingModel:\n  pricingCategory:\
  \ Custom / Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Taylor Morrison\n  ServiceCategory: Homebuilding\n  ProviderName: Taylor Morrison\n  PublisherName: Taylor Morrison Home Corporation\n  InvoiceIssuerName: Taylor Morrison Home Corporation\n  BillingCurrency: USD\nmeters:\n  - name: custom_engagement\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility into commercial activity with Taylor Morrison flows through the partner\n      relationship (trade portal, realtor program, lender program), not a public usage API.\n  - name: Allocation\n    description: Allocation is handled in the partner's own AP system against Taylor Morrison\n      invoices and contract line items.\n  - name: Optimization\n    description: Optimization is addressed through contract negotiation and trade-program review\n      with the Taylor Morrison commercial team.\n\
  \  - name: Accountability\n    description: Accountability sits with the partner-side commercial owner of the Taylor Morrison\n      relationship.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/taylor-morrison-home/refs/heads/main/finops/taylor-morrison-home-finops.yml
sources:
- https://www.taylormorrison.com/
specification: FinOps Framework
tags:
- Homebuilding
- Real Estate
- FinOps
- FOCUS
---
