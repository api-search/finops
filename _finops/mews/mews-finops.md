---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mews-connector-openapi.yaml
  format: yaml
  label: Mews Connector API
  slug: connector-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mews/refs/heads/main/openapi/mews-connector-openapi.yaml
billing_model:
  billingCurrency: EUR
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Hybrid
description: FOCUS-aligned FinOps profile. Per-property/per-room SaaS plus optional Mews Payments processing volume.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Mews
  ProviderName: Mews
  PublisherName: Mews
  ServiceCategory: Hospitality
  ServiceName: Mews
layout: finops
meters:
- aggregation: sum
  description: Per-property monthly SaaS.
  dimensions:
  - account
  - property
  name: property_saas
  unit: property
- aggregation: sum
  description: Mews Payments processing volume.
  dimensions:
  - property
  name: mews_payments_volume
  unit: EUR
name: Mews Finops
provider_name: Mews
provider_slug: mews
publisher_name: Mews
service_category: Hospitality
slug: mews-finops
source_filename: mews-finops.yml
source_heading: FinOps Profile
source_url: https://www.mews.com/en/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Mews\nproviderId: mews\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Hospitality\n- Hotels\n- PMS\n- Property Management\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Per-property/per-room SaaS plus optional Mews Payments processing\n  volume.\nnotes: EUR/USD/GBP billing depending on region.\nsources:\n- https://www.mews.com/en/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Mews\nserviceCategory: Hospitality\nbillingModel:\n  pricingCategory: Hybrid\n  billingFrequency: Monthly\n  billingCurrency: EUR\n  chargeCategories:\n  - Purchase\n  - Usage\n  -\
  \ Adjustment\nfocusColumns:\n  ServiceName: Mews\n  ServiceCategory: Hospitality\n  ProviderName: Mews\n  PublisherName: Mews\n  InvoiceIssuerName: Mews\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: property_saas\n  description: Per-property monthly SaaS.\n  unit: property\n  aggregation: sum\n  dimensions:\n  - account\n  - property\n- name: mews_payments_volume\n  description: Mews Payments processing volume.\n  unit: EUR\n  aggregation: sum\n  dimensions:\n  - property\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n\
  \  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mews/refs/heads/main/finops/mews-finops.yml
sources:
- https://www.mews.com/en/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Hospitality
- Hotels
- PMS
- Property Management
- FinOps
- Cost Management
- FOCUS
---
