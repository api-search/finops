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
description: FOCUS-aligned FinOps profile. Sprinto is sold as an annual subscription.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Sprinto
  ProviderName: Sprinto
  PublisherName: Sprinto
  ServiceCategory: Compliance & Governance
  ServiceName: Sprinto
layout: finops
meters:
- aggregation: sum
  description: Annual subscription line item.
  dimensions:
  - account
  name: subscription
  unit: subscription
name: Sprinto Finops
provider_name: Sprinto
provider_slug: sprinto
publisher_name: Sprinto
service_category: Compliance & Governance
slug: sprinto-finops
source_filename: sprinto-finops.yml
source_heading: FinOps Profile
source_url: https://sprinto.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sprinto\nproviderId: sprinto\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- GRC\n- Compliance\n- SOC 2\n- ISO 27001\n- Security\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Sprinto is sold as an annual subscription.\nnotes: Plan includes API access.\nsources:\n- https://sprinto.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Sprinto\nserviceCategory: Compliance & Governance\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Sprinto\n\
  \  ServiceCategory: Compliance & Governance\n  ProviderName: Sprinto\n  PublisherName: Sprinto\n  InvoiceIssuerName: Sprinto\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: subscription\n  description: Annual subscription line item.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sprinto/refs/heads/main/finops/sprinto-finops.yml
sources:
- https://sprinto.com/
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
