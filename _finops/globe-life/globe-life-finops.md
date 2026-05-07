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
  - Purchase
  - Refund
  - Adjustment
  pricingCategory: Insurance Premium
description: 'FinOps framing for Globe Life: insurance carrier with policyholder-facing premium revenue rather than API consumption costs. Not a typical FinOps-billed surface.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Globe Life Inc.
  ProviderName: Globe Life
  PublisherName: Globe Life Inc.
  ServiceCategory: Insurance
  ServiceName: Globe Life
layout: finops
meters:
- aggregation: sum
  description: Monthly insurance premium charged per active policy
  dimensions:
  - product_line
  - state
  name: policy_premium
  unit: policy-month
- aggregation: sum
  description: Insurance claim payouts (revenue offset, not API cost)
  name: claims_paid
  unit: claim
name: Globe Life Finops
provider_name: Globe Life
provider_slug: globe-life
publisher_name: Globe Life Inc.
service_category: Insurance
slug: globe-life-finops
source_filename: globe-life-finops.yml
source_heading: FinOps Profile
source_url: https://www.globelifeinsurance.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Globe Life\nproviderId: globe-life\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Insurance\n  - Life Insurance\ndescription: 'FinOps framing for Globe Life: insurance carrier with policyholder-facing premium revenue\n  rather than API consumption costs. Not a typical FinOps-billed surface.'\nnotes: Reconcile only if Globe Life launches a developer-facing platform with consumption pricing.\nsources:\n  - https://www.globelifeinsurance.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Globe Life Inc.\nserviceCategory: Insurance\nbillingModel:\n  pricingCategory: Insurance Premium\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\n    - Refund\n    - Adjustment\nfocusColumns:\n  ServiceName: Globe Life\n  ServiceCategory: Insurance\n  ProviderName: Globe Life\n  PublisherName: Globe Life Inc.\n  InvoiceIssuerName: Globe Life Inc.\n  BillingCurrency: USD\nmeters:\n  - name: policy_premium\n    description: Monthly insurance premium charged per active policy\n    unit: policy-month\n    aggregation: sum\n    dimensions:\n      - product_line\n      - state\n  - name: claims_paid\n    description: Insurance claim payouts (revenue offset, not API cost)\n    unit: claim\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track active policies and premium ledgers via Globe Life policyholder statements.\n  - name: Allocation\n    description: For corporate-paid group policies, allocate premium cost to the covered employee population.\n  - name: Optimization\n    description: Review coverage adequacy and term selection at renewal; consolidate riders where\
  \ possible.\n  - name: Accountability\n    description: HR/benefits team owns group-policy spend; individual policyholders own personal premiums.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/globe-life/refs/heads/main/finops/globe-life-finops.yml
sources:
- https://www.globelifeinsurance.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Insurance
- Life Insurance
---
