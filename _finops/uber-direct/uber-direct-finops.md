---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for Uber Direct. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Uber Direct
  ProviderName: Uber Direct
  PublisherName: Uber Direct
  ServiceCategory: Logistics
  ServiceName: Uber Direct
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Uber Direct Finops
provider_name: Uber Direct
provider_slug: uber-direct
publisher_name: Uber Direct
service_category: Logistics
slug: uber-direct-finops
source_filename: uber-direct-finops.yml
source_heading: FinOps Profile
source_url: https://www.uber.com/us/en/business/services/deliveries/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Uber Direct\nproviderId: uber-direct\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Logistics\n- Last Mile\n- Delivery\n- Uber\n- API\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Uber Direct. Pipeline will replace with real billing details.\nnotes: Initial scaffold — billing model has not yet been reconciled.\nsources:\n- https://www.uber.com/us/en/business/services/deliveries/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Uber Direct\nserviceCategory: Logistics\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Uber Direct\n  ServiceCategory: Logistics\n  ProviderName: Uber Direct\n  PublisherName: Uber Direct\n  InvoiceIssuerName: Uber Direct\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/uber-direct/refs/heads/main/finops/uber-direct-finops.yml
sources:
- https://www.uber.com/us/en/business/services/deliveries/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Logistics
- Last Mile
- Delivery
- Uber
- API
- FinOps
- Cost Management
- FOCUS
---
