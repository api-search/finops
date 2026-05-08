---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: FOCUS-aligned FinOps placeholder for Southwest Airlines. There is no public developer billing surface; partner integrations are contracted and invoiced outside any per-call FinOps regime.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Southwest Airlines Co.
  ProviderName: Southwest Airlines
  PublisherName: Southwest Airlines Co.
  ServiceCategory: Travel & Distribution
  ServiceName: Southwest Airlines
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter; actual billable units are defined per partnership agreement (e.g. distribution segments, loyalty transactions).
  name: contracted_partnership
  unit: varies
name: Southwest Airlines Finops
provider_name: Southwest Airlines
provider_slug: southwest-airlines
publisher_name: Southwest Airlines Co.
service_category: Travel & Distribution
slug: southwest-airlines-finops
source_filename: southwest-airlines-finops.yml
source_heading: FinOps Profile
source_url: https://www.southwest.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Southwest Airlines\nproviderId: southwest-airlines\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Fortune 500\n  - Airlines\n  - Aviation\n  - Travel\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Southwest Airlines. There is no\n  public developer billing surface; partner integrations are contracted and invoiced\n  outside any per-call FinOps regime.\nsources:\n  - https://www.southwest.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Southwest Airlines Co.\nserviceCategory: Travel & Distribution\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Purchase\nfocusColumns:\n  ServiceName: Southwest Airlines\n  ServiceCategory: Travel & Distribution\n  ProviderName: Southwest Airlines\n  PublisherName: Southwest Airlines Co.\n  InvoiceIssuerName: Southwest Airlines Co.\n  BillingCurrency: USD\nmeters:\n  - name: contracted_partnership\n    description: Placeholder meter; actual billable units are defined per partnership\n      agreement (e.g. distribution segments, loyalty transactions).\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: No public usage API or cost dashboard. Visibility relies on contract\n      reporting deliverables agreed in the partnership.\n  - name: Allocation\n    description: Spend on Southwest partnership integrations is allocated against\n      the contracting business unit (corporate travel, distribution, loyalty).\n  - name: Optimization\n    description: Optimization is contractual rather than technical — renegotiating\n      volume tiers, segment commitments,\
  \ or distribution mix.\n  - name: Accountability\n    description: Owned by the contracting team's procurement / vendor manager;\n      Southwest does not expose self-serve cost controls.\nnotes: No public per-call billing or FinOps surface; entry exists for catalog\n  completeness only.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/southwest-airlines/refs/heads/main/finops/southwest-airlines-finops.yml
sources:
- https://www.southwest.com/
specification: FinOps Framework
tags:
- Fortune 500
- Airlines
- Aviation
- Travel
- FinOps
- FOCUS
---
