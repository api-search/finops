---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: xiaomi-open-api-openapi.yml
  format: yaml
  label: Xiaomi Open API
  slug: xiaomi-open-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xiaomi/refs/heads/main/openapi/xiaomi-open-api-openapi.yml
- filename: xiaomi-galaxy-fds-openapi.yml
  format: yaml
  label: Xiaomi Galaxy FDS API
  slug: xiaomi-galaxy-fds
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xiaomi/refs/heads/main/openapi/xiaomi-galaxy-fds-openapi.yml
- filename: xiaomi-mimo-api-openapi.yml
  format: yaml
  label: Xiaomi MiMo AI API
  slug: xiaomi-mimo-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xiaomi/refs/heads/main/openapi/xiaomi-mimo-api-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Contact Sales
description: Xiaomi's developer APIs are partner-gated with no public price card, so the FinOps surface is a placeholder pending direct commercial engagement.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Xiaomi Corporation
  ProviderName: Xiaomi
  PublisherName: Xiaomi Corporation
  ServiceCategory: Consumer Electronics / IoT
  ServiceName: Xiaomi
layout: finops
meters:
- aggregation: sum
  description: Placeholder request meter; actual billable lines depend on the partner agreement.
  name: api_requests
  unit: varies
name: Xiaomi Finops
provider_name: Xiaomi
provider_slug: xiaomi
publisher_name: Xiaomi Corporation
service_category: Consumer Electronics / IoT
slug: xiaomi-finops
source_filename: xiaomi-finops.yml
source_heading: FinOps Profile
source_url: https://dev.mi.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Xiaomi\nproviderId: xiaomi\npublisherName: Xiaomi Corporation\nserviceCategory: Consumer Electronics / IoT\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Consumer Electronics\n  - IoT\n  - Mobile\n  - FinOps\n  - FOCUS\ndescription: Xiaomi's developer APIs are partner-gated with no public price card, so the\n  FinOps surface is a placeholder pending direct commercial engagement.\nsources:\n  - https://dev.mi.com/\n  - https://developer.xiaomi.com/\nnotes: |\n  No public pricing or invoice line-item documentation is available for Xiaomi developer\n  APIs. Meters and FOCUS columns below are minimal placeholders until\
  \ terms are issued\n  under the Mi developer / partner program.\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Xiaomi\n  ServiceCategory: Consumer Electronics / IoT\n  ProviderName: Xiaomi\n  PublisherName: Xiaomi Corporation\n  InvoiceIssuerName: Xiaomi Corporation\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    description: Placeholder request meter; actual billable lines depend on the partner\n      agreement.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Until a partner agreement is signed, there is no usage telemetry surface\n      for Xiaomi APIs; rely on internal client-side counters.\n  - name: Allocation\n    description: Tag any client-side calls with consuming team, app, and region so that\n      negotiated commitments can be allocated post-contract.\n  - name:\
  \ Optimization\n    description: Negotiate volume tiers and regional pricing (CN vs Global) directly during\n      partner onboarding.\n  - name: Accountability\n    description: Spend ownership sits with the business unit signing the Mi partner\n      agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/xiaomi/refs/heads/main/finops/xiaomi-finops.yml
sources:
- https://dev.mi.com/
- https://developer.xiaomi.com/
specification: FinOps Framework
tags:
- Consumer Electronics
- IoT
- Mobile
- FinOps
- FOCUS
---
