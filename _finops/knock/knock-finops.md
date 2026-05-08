---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: knock-openapi.json
  format: json
  label: Knock Workflows API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Messages API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Users API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Objects API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Feeds API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Guides API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Schedules API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Preferences API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for Knock. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Knock
  ProviderName: Knock
  PublisherName: Knock
  ServiceCategory: Notifications
  ServiceName: Knock
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Knock Finops
provider_name: Knock
provider_slug: knock
publisher_name: Knock
service_category: Notifications
slug: knock-finops
source_filename: knock-finops.yml
source_heading: FinOps Profile
source_url: https://knock.app/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Knock\nproviderId: knock\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Notifications\n- Email\n- SMS\n- Push\n- Workflows\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Knock. Pipeline will replace with real billing details.\nnotes: \"Initial scaffold \\u2014 billing model has not yet been reconciled.\"\nsources:\n- https://knock.app/\n- https://docs.knock.app/\n- https://docs.knock.app/reference\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Knock\nserviceCategory: Notifications\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Knock\n  ServiceCategory: Notifications\n  ProviderName: Knock\n  PublisherName: Knock\n  InvoiceIssuerName: Knock\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/finops/knock-finops.yml
sources:
- https://knock.app/
- https://docs.knock.app/
- https://docs.knock.app/reference
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Notifications
- Email
- SMS
- Push
- Workflows
- FinOps
- Cost Management
- FOCUS
---
