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
description: FOCUS-aligned FinOps placeholder for Kameleoon. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Kameleoon
  ProviderName: Kameleoon
  PublisherName: Kameleoon
  ServiceCategory: A/B Testing
  ServiceName: Kameleoon
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Kameleoon Finops
provider_name: Kameleoon
provider_slug: kameleoon
publisher_name: Kameleoon
service_category: A/B Testing
slug: kameleoon-finops
source_filename: kameleoon-finops.yml
source_heading: FinOps Profile
source_url: https://www.kameleoon.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Kameleoon\nproviderId: kameleoon\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- A/B Testing\n- Experimentation\n- Personalization\n- AI\n- Server-Side\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Kameleoon. Pipeline will replace with real billing details.\nnotes: Initial scaffold — billing model has not yet been reconciled.\nsources:\n- https://www.kameleoon.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Kameleoon\nserviceCategory: A/B Testing\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n\
  \  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Kameleoon\n  ServiceCategory: A/B Testing\n  ProviderName: Kameleoon\n  PublisherName: Kameleoon\n  InvoiceIssuerName: Kameleoon\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kameleoon/refs/heads/main/finops/kameleoon-finops.yml
sources:
- https://www.kameleoon.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- A/B Testing
- Experimentation
- Personalization
- AI
- Server-Side
- FinOps
- Cost Management
- FOCUS
---
