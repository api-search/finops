---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: aflac-enterprise-connect-openapi.yml
  format: yaml
  label: Aflac Enterprise Connect API
  slug: enterprise-connect-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aflac/refs/heads/main/openapi/aflac-enterprise-connect-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Refund
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Aflac: premium-based insurance billing for supplemental policies plus broker/employer integration agreements.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Aflac Incorporated
  ProviderName: Aflac
  PublisherName: Aflac Incorporated
  ServiceCategory: Insurance / Supplemental Benefits
  ServiceName: Aflac
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  - state
  - employer
  name: active_policies
  unit: policy
- aggregation: sum
  dimensions:
  - product
  - state
  name: monthly_premiums
  unit: USD
- aggregation: sum
  dimensions:
  - product
  - state
  name: claims_paid
  unit: USD
- aggregation: sum
  dimensions:
  - partner
  name: broker_integration_fees
  unit: USD
name: Aflac Finops
provider_name: aflac
provider_slug: aflac
publisher_name: Aflac Incorporated
service_category: Insurance / Supplemental Benefits
slug: aflac-finops
source_filename: aflac-finops.yml
source_heading: FinOps Profile
source_url: https://www.aflac.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: aflac\nproviderId: aflac\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: Aflac bills via insurance premiums (state-filed) and broker/employer integration fees;\n  it does not bill per API call.\ntags:\n  - FinOps\n  - FOCUS\n  - Insurance\n  - Voluntary Benefits\ndescription: 'FOCUS-aligned FinOps for Aflac: premium-based insurance billing for supplemental\n  policies plus broker/employer integration agreements.'\nsources:\n  - https://www.aflac.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Aflac Incorporated\nserviceCategory: Insurance / Supplemental Benefits\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Refund\n    - Adjustment\nfocusColumns:\n  ServiceName: Aflac\n  ServiceCategory: Insurance / Supplemental Benefits\n  ProviderName: Aflac\n  PublisherName: Aflac Incorporated\n  InvoiceIssuerName: Aflac Incorporated\n  BillingCurrency: USD\nmeters:\n  - name: active_policies\n    unit: policy\n    aggregation: max\n    dimensions:\n      - product\n      - state\n      - employer\n  - name: monthly_premiums\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - product\n      - state\n  - name: claims_paid\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - product\n      - state\n  - name: broker_integration_fees\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - partner\nprinciples:\n  - name: Visibility\n    description: Track active-policy counts and premium volume via the Aflac employer/broker\n      portal; reconcile against payroll deductions.\n  - name: Allocation\n    description: Tag\
  \ premiums by employer group, division, and product line for benefits cost\n      reporting.\n  - name: Optimization\n    description: Review benefit utilization and renewal pricing annually; right-size product\n      offerings by employee segment.\n  - name: Accountability\n    description: Assign benefits-program owner; review enrollment, premium, and claim variance\n      monthly.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aflac/refs/heads/main/finops/aflac-finops.yml
sources:
- https://www.aflac.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Insurance
- Voluntary Benefits
---
