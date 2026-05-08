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
description: FOCUS-aligned FinOps placeholder for FourKites. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: FourKites
  ProviderName: FourKites
  PublisherName: FourKites
  ServiceCategory: Logistics
  ServiceName: FourKites
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Fourkites Finops
provider_name: FourKites
provider_slug: fourkites
publisher_name: FourKites
service_category: Logistics
slug: fourkites-finops
source_filename: fourkites-finops.yml
source_heading: FinOps Profile
source_url: https://www.fourkites.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: FourKites\nproviderId: fourkites\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Logistics\n- Supply Chain\n- Visibility\n- Tracking\n- Real-Time\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for FourKites. Pipeline will replace with real billing details.\nnotes: Initial scaffold — billing model has not yet been reconciled.\nsources:\n- https://www.fourkites.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: FourKites\nserviceCategory: Logistics\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n\
  \  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: FourKites\n  ServiceCategory: Logistics\n  ProviderName: FourKites\n  PublisherName: FourKites\n  InvoiceIssuerName: FourKites\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fourkites/refs/heads/main/finops/fourkites-finops.yml
sources:
- https://www.fourkites.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Logistics
- Supply Chain
- Visibility
- Tracking
- Real-Time
- FinOps
- Cost Management
- FOCUS
---
