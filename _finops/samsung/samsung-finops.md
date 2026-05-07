---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: samsung-smartthings-openapi.yml
  format: yaml
  label: SmartThings API
  slug: smartthings
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/samsung/refs/heads/main/openapi/samsung-smartthings-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Free / Partner-Negotiated
description: FOCUS-aligned FinOps artifact for Samsung. Pricing is gated; meters and principles describe the expected billing surface. Samsung exposes developer programs (SmartThings, Bixby, Tizen, Knox) through device partner agreements. Public API usage is generally free but partner-onboarded; commercial terms are negotiated through Samsung's developer relations team and not published as public price sheets.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Samsung Electronics Co., Ltd.
  ProviderName: Samsung
  PublisherName: Samsung Electronics Co., Ltd.
  ServiceCategory: Consumer Electronics / IoT Platform
  ServiceName: Samsung
  ServiceSubcategory: Device / IoT Platform
layout: finops
meters:
- aggregation: sum
  dimensions:
  - program
  - client_id
  name: api_requests
  unit: request
- aggregation: max
  dimensions:
  - program
  - device_family
  name: device_count
  unit: device
name: Samsung Finops
provider_name: Samsung
provider_slug: samsung
publisher_name: Samsung Electronics Co., Ltd.
service_category: Consumer Electronics / IoT Platform
slug: samsung-finops
source_filename: samsung-finops.yml
source_heading: FinOps Profile
source_url: https://developer.samsung.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Samsung\nproviderId: samsung\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- Consumer Electronics\n- Devices\n- IoT\n- Mobile\n- Samsung\n- SmartThings\n- FinOps\n- FOCUS\ndescription: FOCUS-aligned FinOps artifact for Samsung. Pricing is gated; meters and principles describe\n  the expected billing surface. Samsung exposes developer programs (SmartThings, Bixby, Tizen, Knox) through\n  device partner agreements. Public API usage is generally free but partner-onboarded; commercial terms\n  are negotiated through Samsung's developer relations team and not published as public price sheets.\nsources:\n- https://developer.samsung.com/\n- https://focus.finops.org/focus-specification/v1-3/\n- https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Samsung Electronics Co., Ltd.\nserviceCategory: Consumer Electronics / IoT Platform\nbillingModel:\n  pricingCategory: Free / Partner-Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\nfocusColumns:\n  ServiceName: Samsung\n  ServiceCategory: Consumer Electronics / IoT Platform\n  ServiceSubcategory: Device / IoT Platform\n  ProviderName: Samsung\n  PublisherName: Samsung Electronics Co., Ltd.\n  InvoiceIssuerName: Samsung Electronics Co., Ltd.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: api_requests\n  unit: request\n  aggregation: sum\n  dimensions:\n  - program\n  - client_id\n- name: device_count\n  unit: device\n  aggregation: max\n  dimensions:\n  - program\n  - device_family\nprinciples:\n- name: Visibility\n  description: Each Samsung developer program (SmartThings, Bixby,\
  \ Knox, Tizen) exposes its own dashboard;\n    aggregate usage across programs in a partner-side data store since Samsung does not provide a unified\n    usage API.\n- name: Allocation\n  description: Allocate by program and client_id; tag downstream spend by Samsung partner agreement.\n- name: Optimization\n  description: Use webhooks and event subscriptions instead of polling devices; cache device metadata;\n    consolidate registrations under a single partner account where program rules permit.\n- name: Accountability\n  description: The Samsung partner / developer-relations contact is accountable for program-level terms.\nnotes: Samsung exposes developer programs (SmartThings, Bixby, Tizen, Knox) through device partner agreements.\n  Public API usage is generally free but partner-onboarded; commercial terms are negotiated through Samsung's\n  developer relations team and not published as public price sheets.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/samsung/refs/heads/main/finops/samsung-finops.yml
sources:
- https://developer.samsung.com/
- https://focus.finops.org/focus-specification/v1-3/
- https://www.finops.org/framework/
specification: FinOps Framework
tags:
- Consumer Electronics
- Devices
- IoT
- Mobile
- Samsung
- SmartThings
- FinOps
- FOCUS
---
