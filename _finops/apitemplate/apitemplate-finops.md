---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription (output-tiered)
description: FOCUS-aligned FinOps profile for APITemplate.io. Billing is a flat monthly tier fee; PDF-only and combined PDF+Image tracks let teams pay only for what they need. Annual billing is 15-30% cheaper than monthly. Pay-as- you-go overage is available on Enterprise.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: APITemplate.io
  PricingUnit: plan-month
  ProviderName: APITemplate.io
  PublisherName: APITemplate.io
  ServiceCategory: Document Generation
  ServiceName: APITemplate.io
layout: finops
meters:
- aggregation: sum
  description: Flat monthly plan fee (PDF-only or combined).
  dimensions:
  - account
  - track
  - tier
  name: plan_subscription
  unit: month
- aggregation: sum
  description: PDFs generated against monthly bundle.
  dimensions:
  - account
  - template
  name: pdfs_generated
  unit: pdf
- aggregation: sum
  description: Images generated against monthly bundle (combined plans).
  dimensions:
  - account
  - template
  name: images_generated
  unit: image
- aggregation: sum
  description: PAYG overage on Enterprise.
  dimensions:
  - account
  name: payg_overage
  unit: output
name: Apitemplate Finops
provider_name: APITemplate.io
provider_slug: apitemplate
publisher_name: APITemplate.io
service_category: Document Generation
slug: apitemplate-finops
source_filename: apitemplate-finops.yml
source_heading: FinOps Profile
source_url: https://apitemplate.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: APITemplate.io\nproviderId: apitemplate\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Document Generation\n- PDF\n- Images\n- Templates\n- API\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for APITemplate.io. Billing is a flat monthly\n  tier fee; PDF-only and combined PDF+Image tracks let teams pay only for\n  what they need. Annual billing is 15-30% cheaper than monthly. Pay-as-\n  you-go overage is available on Enterprise.\nnotes: >-\n  Right-sizing the track (PDF-only vs combined) is the highest-leverage\n  optimisation, followed by stepping up tier for sustained usage.\nsources:\n- https://apitemplate.io/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n\
  \  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: APITemplate.io\nserviceCategory: Document Generation\nbillingModel:\n  pricingCategory: Subscription (output-tiered)\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\nfocusColumns:\n  ServiceName: APITemplate.io\n  ServiceCategory: Document Generation\n  ProviderName: APITemplate.io\n  PublisherName: APITemplate.io\n  InvoiceIssuerName: APITemplate.io\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: plan-month\nmeters:\n- name: plan_subscription\n  description: Flat monthly plan fee (PDF-only or combined).\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n  - track\n  - tier\n- name: pdfs_generated\n  description: PDFs generated against monthly bundle.\n  unit: pdf\n  aggregation: sum\n  dimensions:\n  - account\n  - template\n- name: images_generated\n  description: Images generated against\
  \ monthly bundle (combined plans).\n  unit: image\n  aggregation: sum\n  dimensions:\n  - account\n  - template\n- name: payg_overage\n  description: PAYG overage on Enterprise.\n  unit: output\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Use APITemplate dashboard usage page; export per-template counts for chargeback.\n- name: Allocation\n  description: Use template naming and AWS S3 storage option to allocate output cost by team.\n- name: Optimization\n  description: Pick PDF-only vs combined track based on actual mix; switch to annual for ~15-30% effective discount; right-size template count.\n- name: Accountability\n  description: Assign template / API-key owners; alert at 75% of monthly bundle.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apitemplate/refs/heads/main/finops/apitemplate-finops.yml
sources:
- https://apitemplate.io/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Document Generation
- PDF
- Images
- Templates
- API
- FinOps
- Cost Management
- FOCUS
---
