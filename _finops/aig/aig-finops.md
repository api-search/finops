---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD/EUR/GBP
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Insurance Premium
description: FOCUS-aligned shape for AIG. The cost surface is insurance premium and broker commission, not API consumption. APIs are integration plumbing under broker / distribution agreements.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: American International Group, Inc.
  ProviderName: AIG
  PublisherName: American International Group, Inc.
  ServiceCategory: Insurance
  ServiceName: AIG Insurance Programs
layout: finops
meters:
- aggregation: sum
  description: Premium paid per policy / line of business
  dimensions:
  - line_of_business
  - policy
  - territory
  - effective_year
  name: insurance_premium
  unit: USD
- aggregation: count
  description: Number of in-force policies with AIG
  dimensions:
  - line_of_business
  - territory
  name: policy_count
  unit: policy
- aggregation: sum
  description: API requests against AIG broker / distribution endpoints (customer-side telemetry only)
  dimensions:
  - integration
  - environment
  name: api_requests
  unit: request
name: Aig Finops
provider_name: AIG
provider_slug: aig
publisher_name: American International Group, Inc.
service_category: Insurance
slug: aig-finops
source_filename: aig-finops.yml
source_heading: FinOps Profile
source_url: https://www.aig.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AIG\nproviderId: aig\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: American International Group, Inc.\nserviceCategory: Insurance\ntags:\n  - Insurance\n  - Financial Services\n  - Property Casualty\n  - Cyber Insurance\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned shape for AIG. The cost surface is insurance premium and broker commission,\n  not API consumption. APIs are integration plumbing under broker / distribution agreements.\nnotes: No API rate card; meters reflect the insurance-program economics customers actually book against\n  AIG (premium, taxes, fees) rather than per-call API costs.\nsources:\n\
  \  - https://www.aig.com/\nbillingModel:\n  pricingCategory: Insurance Premium\n  billingFrequency: Annual\n  billingCurrency: USD/EUR/GBP\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: AIG Insurance Programs\n  ServiceCategory: Insurance\n  ProviderName: AIG\n  PublisherName: American International Group, Inc.\n  InvoiceIssuerName: American International Group, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: insurance_premium\n    description: Premium paid per policy / line of business\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - line_of_business\n      - policy\n      - territory\n      - effective_year\n  - name: policy_count\n    description: Number of in-force policies with AIG\n    unit: policy\n    aggregation: count\n    dimensions:\n      - line_of_business\n      - territory\n  - name: api_requests\n    description: API requests against AIG broker / distribution endpoints (customer-side\
  \ telemetry only)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - integration\n      - environment\nprinciples:\n  - name: Visibility\n    description: Track AIG spend at the policy / line-of-business level using the broker statement and\n      AIG-issued invoices; instrument API integrations client-side since AIG does not expose unified\n      usage telemetry.\n  - name: Allocation\n    description: Allocate premium by business unit, geography, and line of business; tie technology\n      integration costs to the program they serve.\n  - name: Optimization\n    description: Optimize through coverage-program design (deductibles, retentions, captives), broker\n      negotiation, and consolidating integrations across AIG lines to reduce duplicated technology effort.\n  - name: Accountability\n    description: Risk management / corporate insurance leadership owns AIG spend; align reviews with\n      the policy-renewal cycle.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aig/refs/heads/main/finops/aig-finops.yml
sources:
- https://www.aig.com/
specification: FinOps Framework
tags:
- Insurance
- Financial Services
- Property Casualty
- Cyber Insurance
- FinOps
- FOCUS
---
