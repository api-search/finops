---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: loops-openapi.yaml
  format: yaml
  label: Loops API
  slug: loops-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/loops/refs/heads/main/openapi/loops-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for Loops. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Loops
  ProviderName: Loops
  PublisherName: Loops
  ServiceCategory: Email Marketing
  ServiceName: Loops
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Loops Finops
provider_name: Loops
provider_slug: loops
publisher_name: Loops
service_category: Email Marketing
slug: loops-finops
source_filename: loops-finops.yml
source_heading: FinOps Profile
source_url: https://loops.so/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Loops\nproviderId: loops\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Email Marketing\n- Transactional\n- Automation\n- SaaS\n- Campaigns\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Loops. Pipeline will replace with real billing details.\nnotes: Initial scaffold — billing model has not yet been reconciled.\nsources:\n- https://loops.so/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Loops\nserviceCategory: Email Marketing\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n \
  \ - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Loops\n  ServiceCategory: Email Marketing\n  ProviderName: Loops\n  PublisherName: Loops\n  InvoiceIssuerName: Loops\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/loops/refs/heads/main/finops/loops-finops.yml
sources:
- https://loops.so/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Email Marketing
- Transactional
- Automation
- SaaS
- Campaigns
- FinOps
- Cost Management
- FOCUS
---
