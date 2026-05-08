---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Subscription
description: FOCUS-aligned FinOps profile. Tugboat Logic is now part of OneTrust enterprise subscriptions.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Tugboat Logic
  ProviderName: Tugboat Logic
  PublisherName: Tugboat Logic
  ServiceCategory: Compliance & Governance
  ServiceName: Tugboat Logic
layout: finops
meters:
- aggregation: sum
  description: Annual subscription via OneTrust master agreement.
  dimensions:
  - account
  name: subscription
  unit: subscription
name: Tugboat Logic Finops
provider_name: Tugboat Logic
provider_slug: tugboat-logic
publisher_name: Tugboat Logic
service_category: Compliance & Governance
slug: tugboat-logic-finops
source_filename: tugboat-logic-finops.yml
source_heading: FinOps Profile
source_url: https://www.onetrust.com/products/certification-automation/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tugboat Logic\nproviderId: tugboat-logic\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- GRC\n- Compliance\n- SOC 2\n- ISO 27001\n- Security\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Tugboat Logic is now part of OneTrust enterprise subscriptions.\nnotes: Billing handled via OneTrust master subscription agreement.\nsources:\n- https://www.onetrust.com/products/certification-automation/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tugboat Logic\nserviceCategory: Compliance & Governance\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n\
  \  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Tugboat Logic\n  ServiceCategory: Compliance & Governance\n  ProviderName: Tugboat Logic\n  PublisherName: Tugboat Logic\n  InvoiceIssuerName: Tugboat Logic\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: subscription\n  description: Annual subscription via OneTrust master agreement.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tugboat-logic/refs/heads/main/finops/tugboat-logic-finops.yml
sources:
- https://www.onetrust.com/products/certification-automation/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- GRC
- Compliance
- SOC 2
- ISO 27001
- Security
- FinOps
- Cost Management
- FOCUS
---
