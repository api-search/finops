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
  pricingCategory: Subscription (merge-tiered)
description: FOCUS-aligned FinOps profile for Documint. Billing is a flat monthly subscription per tier; each generated document counts as a merge against the plan's monthly bundle. REST API gating to Platinum+ is itself a cost decision — teams that need automation must step up to the API tier.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Documint
  PricingUnit: plan-month
  ProviderName: Documint
  PublisherName: Documint
  ServiceCategory: Document Generation
  ServiceName: Documint
layout: finops
meters:
- aggregation: sum
  description: Flat monthly Documint plan fee.
  dimensions:
  - account
  - tier
  name: plan_subscription
  unit: month
- aggregation: sum
  description: Documents generated (1 merge per document).
  dimensions:
  - account
  - template
  - integration
  name: merges
  unit: merge
- aggregation: max
  description: Active templates in account (informational; tier-bound).
  dimensions:
  - account
  name: templates
  unit: template
name: Documint Finops
provider_name: Documint
provider_slug: documint
publisher_name: Documint
service_category: Document Generation
slug: documint-finops
source_filename: documint-finops.yml
source_heading: FinOps Profile
source_url: https://documint.me/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Documint\nproviderId: documint\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Document Generation\n- PDF\n- Templates\n- API\n- Workflow\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Documint. Billing is a flat monthly\n  subscription per tier; each generated document counts as a merge against\n  the plan's monthly bundle. REST API gating to Platinum+ is itself a cost\n  decision — teams that need automation must step up to the API tier.\nnotes: >-\n  Documint does not store payload data, simplifying compliance posture.\n  Optimisation focuses on selecting the right tier (UI/integration vs.\n  REST API) and right-sizing the merge bundle.\nsources:\n- https://documint.me/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n \
  \ frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Documint\nserviceCategory: Document Generation\nbillingModel:\n  pricingCategory: Subscription (merge-tiered)\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\nfocusColumns:\n  ServiceName: Documint\n  ServiceCategory: Document Generation\n  ProviderName: Documint\n  PublisherName: Documint\n  InvoiceIssuerName: Documint\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: plan-month\nmeters:\n- name: plan_subscription\n  description: Flat monthly Documint plan fee.\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n  - tier\n- name: merges\n  description: Documents generated (1 merge per document).\n  unit: merge\n  aggregation: sum\n  dimensions:\n  - account\n  - template\n  - integration\n- name: templates\n  description:\
  \ Active templates in account (informational; tier-bound).\n  unit: template\n  aggregation: max\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Use Documint dashboard usage page; export merge counts per template.\n- name: Allocation\n  description: Use template naming or per-integration API keys to allocate cost.\n- name: Optimization\n  description: Right-size tier; use UI on lower tiers + REST only when automation required; consolidate similar templates.\n- name: Accountability\n  description: Assign template / integration owners; alert on monthly merge burn.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/documint/refs/heads/main/finops/documint-finops.yml
sources:
- https://documint.me/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Document Generation
- PDF
- Templates
- API
- Workflow
- FinOps
- Cost Management
- FOCUS
---
