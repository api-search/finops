---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: project44-tracking-openapi.yml
  format: yaml
  label: project44 Tracking API
  slug: project44-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/project44/refs/heads/main/openapi/project44-tracking-openapi.yml
- filename: project44-shipment-events-asyncapi.yml
  format: yaml
  label: project44 Webhooks API
  slug: project44-webhooks-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/project44/refs/heads/main/asyncapi/project44-shipment-events-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps shape for project44 — an enterprise SaaS platform billed by contract rather than metered API usage.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: project44, Inc.
  ProviderName: project44
  PublisherName: project44, Inc.
  ServiceCategory: Supply Chain Visibility
  ServiceName: project44
layout: finops
meters:
- aggregation: sum
  name: subscription_fee
  unit: month
name: Project44 Finops
provider_name: project44
provider_slug: project44
publisher_name: project44, Inc.
service_category: Supply Chain Visibility
slug: project44-finops
source_filename: project44-finops.yml
source_heading: FinOps Profile
source_url: https://www.project44.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: project44\nproviderId: project44\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Supply Chain\n  - Logistics\n  - Visibility\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for project44 — an enterprise SaaS platform billed by contract\n  rather than metered API usage.\nnotes: project44 does not publish a public billing or usage-metering surface. Cost is governed by an\n  enterprise subscription contract.\nsources:\n  - https://www.project44.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: project44, Inc.\nserviceCategory: Supply Chain Visibility\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: project44\n  ServiceCategory: Supply Chain Visibility\n  ProviderName: project44\n  PublisherName: project44, Inc.\n  InvoiceIssuerName: project44, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subscription_fee\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Subscription-line cost only; no public consumption telemetry. Customers track shipment-volume\n      and integration counts inside the project44 portal.\n  - name: Allocation\n    description: Allocate the contract by business unit, lane, or carrier program internally; project44\n      does not expose per-call cost dimensions externally.\n  - name: Optimization\n    description: Renegotiate scope, tiers, and integration count at renewal; consolidate overlapping\n      visibility programs.\n  - name: Accountability\n    description: Spend is owned by the supply-chain / logistics function that signs the master subscription\n\
  \      agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/project44/refs/heads/main/finops/project44-finops.yml
sources:
- https://www.project44.com/
specification: FinOps Framework
tags:
- Supply Chain
- Logistics
- Visibility
- FinOps
- FOCUS
---
