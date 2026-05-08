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
description: FOCUS-aligned FinOps placeholder for Chameleon. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Chameleon
  ProviderName: Chameleon
  PublisherName: Chameleon
  ServiceCategory: Product
  ServiceName: Chameleon
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Chameleon Finops
provider_name: Chameleon
provider_slug: chameleon
publisher_name: Chameleon
service_category: Product
slug: chameleon-finops
source_filename: chameleon-finops.yml
source_heading: FinOps Profile
source_url: https://www.chameleon.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Chameleon\nproviderId: chameleon\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Product\n- Onboarding\n- In-App\n- Personalization\n- Engagement\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Chameleon. Pipeline will replace with real billing details.\nnotes: Initial scaffold — billing model has not yet been reconciled.\nsources:\n- https://www.chameleon.io/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Chameleon\nserviceCategory: Product\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n\
  \  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Chameleon\n  ServiceCategory: Product\n  ProviderName: Chameleon\n  PublisherName: Chameleon\n  InvoiceIssuerName: Chameleon\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chameleon/refs/heads/main/finops/chameleon-finops.yml
sources:
- https://www.chameleon.io/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Product
- Onboarding
- In-App
- Personalization
- Engagement
- FinOps
- Cost Management
- FOCUS
---
