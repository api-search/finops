---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: courier-openapi.yml
  format: yaml
  label: Courier Send API
  slug: courier-send-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/openapi/courier-openapi.yml
- filename: courier-openapi.yml
  format: yaml
  label: Courier User Profiles API
  slug: courier-user-profiles-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/openapi/courier-openapi.yml
- filename: courier-openapi.yml
  format: yaml
  label: Courier Lists API
  slug: courier-lists-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/openapi/courier-openapi.yml
- filename: courier-openapi.yml
  format: yaml
  label: Courier Events API
  slug: courier-events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/openapi/courier-openapi.yml
- filename: courier-openapi.yml
  format: yaml
  label: Courier Brands API
  slug: courier-brands-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/openapi/courier-openapi.yml
- filename: courier-openapi.yml
  format: yaml
  label: Courier Authentication API
  slug: courier-authentication-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/openapi/courier-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for Courier. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Courier
  ProviderName: Courier
  PublisherName: Courier
  ServiceCategory: Notifications
  ServiceName: Courier
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Courier Finops
provider_name: Courier
provider_slug: courier
publisher_name: Courier
service_category: Notifications
slug: courier-finops
source_filename: courier-finops.yml
source_heading: FinOps Profile
source_url: https://www.courier.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Courier\nproviderId: courier\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Notifications\n- Email\n- SMS\n- Push\n- API\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Courier. Pipeline will replace with real billing details.\nnotes: \"Initial scaffold \\u2014 billing model has not yet been reconciled.\"\nsources:\n- https://www.courier.com/\n- https://www.courier.com/docs\n- https://www.courier.com/docs/reference\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Courier\nserviceCategory: Notifications\nbillingModel:\n  pricingCategory: To Be Reconciled\n \
  \ billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Courier\n  ServiceCategory: Notifications\n  ProviderName: Courier\n  PublisherName: Courier\n  InvoiceIssuerName: Courier\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/finops/courier-finops.yml
sources:
- https://www.courier.com/
- https://www.courier.com/docs
- https://www.courier.com/docs/reference
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Notifications
- Email
- SMS
- Push
- API
- FinOps
- Cost Management
- FOCUS
---
