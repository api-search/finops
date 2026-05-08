---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: onesignal-openapi.yml
  format: yaml
  label: OneSignal Messages API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/onesignal/refs/heads/main/openapi/onesignal-openapi.yml
- filename: onesignal-openapi.yml
  format: yaml
  label: OneSignal Users & Subscriptions API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/onesignal/refs/heads/main/openapi/onesignal-openapi.yml
- filename: onesignal-openapi.yml
  format: yaml
  label: OneSignal Segments API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/onesignal/refs/heads/main/openapi/onesignal-openapi.yml
- filename: onesignal-openapi.yml
  format: yaml
  label: OneSignal Apps & Keys API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/onesignal/refs/heads/main/openapi/onesignal-openapi.yml
- filename: onesignal-openapi.yml
  format: yaml
  label: OneSignal Exports & Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/onesignal/refs/heads/main/openapi/onesignal-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for OneSignal. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: OneSignal
  ProviderName: OneSignal
  PublisherName: OneSignal
  ServiceCategory: Notifications
  ServiceName: OneSignal
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Onesignal Finops
provider_name: OneSignal
provider_slug: onesignal
publisher_name: OneSignal
service_category: Notifications
slug: onesignal-finops
source_filename: onesignal-finops.yml
source_heading: FinOps Profile
source_url: https://onesignal.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: OneSignal\nproviderId: onesignal\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Notifications\n- Push\n- Email\n- SMS\n- Mobile\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for OneSignal. Pipeline will replace with real billing details.\nnotes: \"Initial scaffold \\u2014 billing model has not yet been reconciled.\"\nsources:\n- https://onesignal.com/\n- https://documentation.onesignal.com/\n- https://documentation.onesignal.com/reference\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: OneSignal\nserviceCategory: Notifications\nbillingModel:\n  pricingCategory:\
  \ To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: OneSignal\n  ServiceCategory: Notifications\n  ProviderName: OneSignal\n  PublisherName: OneSignal\n  InvoiceIssuerName: OneSignal\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin\
  \ Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/onesignal/refs/heads/main/finops/onesignal-finops.yml
sources:
- https://onesignal.com/
- https://documentation.onesignal.com/
- https://documentation.onesignal.com/reference
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Notifications
- Push
- Email
- SMS
- Mobile
- FinOps
- Cost Management
- FOCUS
---
