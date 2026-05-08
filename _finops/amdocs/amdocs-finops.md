---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amdocs-connectx-openapi.yml
  format: yaml
  label: Amdocs connectX BSS API
  slug: amdocs-connectx-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amdocs/refs/heads/main/openapi/amdocs-connectx-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise / Bilateral
description: FinOps scaffold for Amdocs connectX BSS. Amdocs invoices telecom operators under enterprise SaaS contracts; usage telemetry is exposed through tenant dashboards but a public FOCUS-aligned billing schema is not published. Reconcile when Amdocs publishes consumption or chargeback documentation.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Amdocs Limited
  ProviderName: Amdocs
  PublisherName: Amdocs Limited
  ServiceCategory: Telecom Software
  ServiceName: Amdocs connectX BSS API
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter for engagements settled outside a metered API. Real meters cannot be enumerated until Amdocs publishes a metered API billing surface.
  name: contracted_engagement
  unit: varies
name: Amdocs Finops
provider_name: Amdocs
provider_slug: amdocs
publisher_name: Amdocs Limited
service_category: Telecom Software
slug: amdocs-finops
source_filename: amdocs-finops.yml
source_heading: FinOps Profile
source_url: https://devportal.amdocs-dbs.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amdocs\nproviderId: amdocs\npublisherName: Amdocs Limited\nserviceCategory: Telecom Software\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Telecom\n  - BSS\n  - OSS\n  - Billing\n  - Customer Management\n  - MVNO\n  - 5G\n  - SaaS\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps scaffold for Amdocs connectX BSS. Amdocs invoices telecom operators under enterprise SaaS contracts; usage telemetry is exposed through tenant dashboards but a public FOCUS-aligned billing schema is not published. Reconcile when Amdocs publishes consumption or chargeback documentation.\nnotes: >-\n  Amdocs connectX is a B2B cloud-native BSS SaaS platform sold to telecom operators under enterprise master service agreements. Pricing is bespoke per operator (subscriber count, modules enabled, AWS region) and is not published publicly. Rate limits and quotas\
  \ are governed by per-tenant capacity provisioning. Reconcile when Amdocs publishes a public pricing or rate-limit page.\nsources:\n  - https://devportal.amdocs-dbs.com/\n  - https://developer.amdocs-dbs.com/reference/getting-started-with-your-api\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Enterprise / Bilateral\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Amdocs connectX BSS API\n  ServiceCategory: Telecom Software\n  ProviderName: Amdocs\n  PublisherName: Amdocs Limited\n  InvoiceIssuerName: Amdocs Limited\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contracted_engagement\n\
  \    description: >-\n      Placeholder meter for engagements settled outside a metered API. Real\n      meters cannot be enumerated until Amdocs publishes a metered\n      API billing surface.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: >-\n      Without a public usage API, consumers must rely on contract reporting,\n      invoice line items, and any tenant dashboards provided under the\n      partner agreement.\n  - name: Allocation\n    description: >-\n      Allocate spend by purchase order, contract identifier, or business unit\n      receiving the Amdocs service. Tag at the procurement layer, not\n      the API call layer.\n  - name: Optimization\n    description: >-\n      Optimization levers live in commercial negotiation (volume commitments,\n      term length, scope) rather than in API-level caching or throttling.\n  - name: Accountability\n    description: >-\n      Procurement and the business owner of the Amdocs relationship\
  \ own\n      the spend; finance reviews invoice lines on the contract cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amdocs/refs/heads/main/finops/amdocs-finops.yml
sources:
- https://devportal.amdocs-dbs.com/
- https://developer.amdocs-dbs.com/reference/getting-started-with-your-api
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Telecom
- BSS
- OSS
- Billing
- Customer Management
- MVNO
- 5G
- SaaS
- FinOps
- FOCUS
---
