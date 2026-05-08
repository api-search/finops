---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD (FR VAT may apply for EU)
  billingFrequency: Monthly / Annual / PAYG
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription / Usage / License
description: FOCUS-aligned FinOps profile for Carbone. Costs come from one of three tracks — Cloud subscription (Free/Essential/Essential Plus/Advanced/ Advanced Plus/Advanced Ultra), On-Prem annual license (Free/Fit/Unlimited) or AWS Private Cloud per-document usage. The OSS rendering engine remains free for embed.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Carbone
  PricingUnit: plan-month / document
  ProviderName: Carbone
  PublisherName: Carbone
  ServiceCategory: Document Generation
  ServiceName: Carbone
layout: finops
meters:
- aggregation: sum
  description: Carbone Cloud monthly plan fee.
  dimensions:
  - account
  - tier
  name: cloud_subscription
  unit: month
- aggregation: sum
  description: Carbone On-Prem annual license fee.
  dimensions:
  - account
  - tier
  name: on_prem_license
  unit: year
- aggregation: sum
  description: Documents rendered on AWS Private Cloud (usage-based pricing).
  dimensions:
  - account
  name: aws_pc_documents
  unit: document
- aggregation: sum
  description: Total documents rendered (informational).
  dimensions:
  - account
  - template
  name: documents_rendered
  unit: document
- aggregation: sum
  description: MB of JSON data injected (counted toward Cloud accounting).
  dimensions:
  - account
  - template
  name: data_injected
  unit: MB
name: Carbone Finops
provider_name: Carbone
provider_slug: carbone
publisher_name: Carbone
service_category: Document Generation
slug: carbone-finops
source_filename: carbone-finops.yml
source_heading: FinOps Profile
source_url: https://carbone.io/pricing.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Carbone\nproviderId: carbone\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Document Generation\n- PDF\n- Templates\n- Open Source\n- Office\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Carbone. Costs come from one of three\n  tracks — Cloud subscription (Free/Essential/Essential Plus/Advanced/\n  Advanced Plus/Advanced Ultra), On-Prem annual license (Free/Fit/Unlimited)\n  or AWS Private Cloud per-document usage. The OSS rendering engine remains\n  free for embed.\nnotes: >-\n  Carbone documents are accounted per 1 MB of injected JSON, so high-volume\n  small documents may be cheaper than expected; large datasets-per-render\n  may push usage faster than document count alone suggests.\nsources:\n- https://carbone.io/pricing.html\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n\
  \  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Carbone\nserviceCategory: Document Generation\nbillingModel:\n  pricingCategory: Subscription / Usage / License\n  billingFrequency: Monthly / Annual / PAYG\n  billingCurrency: USD (FR VAT may apply for EU)\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Carbone\n  ServiceCategory: Document Generation\n  ProviderName: Carbone\n  PublisherName: Carbone\n  InvoiceIssuerName: Carbone\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: plan-month / document\nmeters:\n- name: cloud_subscription\n  description: Carbone Cloud monthly plan fee.\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n  - tier\n- name: on_prem_license\n  description: Carbone On-Prem annual license fee.\n  unit: year\n  aggregation:\
  \ sum\n  dimensions:\n  - account\n  - tier\n- name: aws_pc_documents\n  description: Documents rendered on AWS Private Cloud (usage-based pricing).\n  unit: document\n  aggregation: sum\n  dimensions:\n  - account\n- name: documents_rendered\n  description: Total documents rendered (informational).\n  unit: document\n  aggregation: sum\n  dimensions:\n  - account\n  - template\n- name: data_injected\n  description: MB of JSON data injected (counted toward Cloud accounting).\n  unit: MB\n  aggregation: sum\n  dimensions:\n  - account\n  - template\nprinciples:\n- name: Visibility\n  description: Use Carbone account dashboard for Cloud usage; integrate AWS Cost Management for AWS PC; track on-prem renders via your own logs.\n- name: Allocation\n  description: Use template IDs and per-team API keys to allocate cost; for AWS PC, tag the AWS account.\n- name: Optimization\n  description: Pick the right deployment track (Cloud vs On-Prem vs AWS PC); right-size Cloud tier; embed OSS engine for\
  \ low-volume / no-egress workloads; use compact JSON to minimise per-MB accounting.\n- name: Accountability\n  description: Assign template / API-key owners; review monthly Cloud usage and AWS PC invoice line items.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carbone/refs/heads/main/finops/carbone-finops.yml
sources:
- https://carbone.io/pricing.html
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Document Generation
- PDF
- Templates
- Open Source
- Office
- FinOps
- Cost Management
- FOCUS
---
