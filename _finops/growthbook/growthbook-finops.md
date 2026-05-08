---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: growthbook-openapi.yaml
  format: yaml
  label: GrowthBook REST API
  slug: growthbook-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/growthbook/refs/heads/main/openapi/growthbook-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for GrowthBook. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: GrowthBook
  ProviderName: GrowthBook
  PublisherName: GrowthBook
  ServiceCategory: A/B Testing
  ServiceName: GrowthBook
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Growthbook Finops
provider_name: GrowthBook
provider_slug: growthbook
publisher_name: GrowthBook
service_category: A/B Testing
slug: growthbook-finops
source_filename: growthbook-finops.yml
source_heading: FinOps Profile
source_url: https://www.growthbook.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: GrowthBook\nproviderId: growthbook\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- A/B Testing\n- Feature Flags\n- Open Source\n- Experimentation\n- Analytics\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for GrowthBook. Pipeline will replace with real billing details.\nnotes: Initial scaffold — billing model has not yet been reconciled.\nsources:\n- https://www.growthbook.io/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: GrowthBook\nserviceCategory: A/B Testing\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: GrowthBook\n  ServiceCategory: A/B Testing\n  ProviderName: GrowthBook\n  PublisherName: GrowthBook\n  InvoiceIssuerName: GrowthBook\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/growthbook/refs/heads/main/finops/growthbook-finops.yml
sources:
- https://www.growthbook.io/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- A/B Testing
- Feature Flags
- Open Source
- Experimentation
- Analytics
- FinOps
- Cost Management
- FOCUS
---
