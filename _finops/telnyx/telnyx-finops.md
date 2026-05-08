---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Voice API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Messaging API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Numbers API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Verify API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Fax API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Wireless API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Networking API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx AI API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Billing & Reporting API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for Telnyx. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Telnyx
  ProviderName: Telnyx
  PublisherName: Telnyx
  ServiceCategory: Communications
  ServiceName: Telnyx
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Telnyx Finops
provider_name: Telnyx
provider_slug: telnyx
publisher_name: Telnyx
service_category: Communications
slug: telnyx-finops
source_filename: telnyx-finops.yml
source_heading: FinOps Profile
source_url: https://telnyx.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Telnyx\nproviderId: telnyx\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Communications\n- CPaaS\n- Voice\n- SMS\n- IoT\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Telnyx. Pipeline will replace with real billing details.\nnotes: \"Initial scaffold \\u2014 billing model has not yet been reconciled.\"\nsources:\n- https://telnyx.com/\n- https://developers.telnyx.com\n- https://developers.telnyx.com/api\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Telnyx\nserviceCategory: Communications\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Telnyx\n  ServiceCategory: Communications\n  ProviderName: Telnyx\n  PublisherName: Telnyx\n  InvoiceIssuerName: Telnyx\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/finops/telnyx-finops.yml
sources:
- https://telnyx.com/
- https://developers.telnyx.com
- https://developers.telnyx.com/api
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Communications
- CPaaS
- Voice
- SMS
- IoT
- FinOps
- Cost Management
- FOCUS
---
