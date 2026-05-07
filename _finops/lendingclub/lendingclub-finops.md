---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom Contract
description: 'FOCUS-aligned FinOps scaffold for LendingClub: partner / contract-based API access with no public per-call pricing, so consumer-side spend allocation tracks against the contracted partner or treasury services agreement.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: LendingClub Corporation
  ProviderName: LendingClub
  PublisherName: LendingClub Corporation
  ServiceCategory: Financial Services / API
  ServiceName: LendingClub API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  - environment
  - partner
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - contract
  name: contract_fees
  unit: month
name: Lendingclub Finops
provider_name: LendingClub
provider_slug: lendingclub
publisher_name: LendingClub Corporation
service_category: Financial Services / API
slug: lendingclub-finops
source_filename: lendingclub-finops.yml
source_heading: FinOps Profile
source_url: https://www.lendingclub.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: LendingClub\nproviderId: lendingclub\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Fintech\n  - Personal Loans\n  - Banking\ndescription: 'FOCUS-aligned FinOps scaffold for LendingClub: partner / contract-based API access with\n  no public per-call pricing, so consumer-side spend allocation tracks against the contracted partner\n  or treasury services agreement.'\nnotes: Pricing is contract-driven and not self-serve; meters below describe the consumer-side telemetry\n  shape and should be reconciled against the executed partner agreement.\nsources:\n  - https://www.lendingclub.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ LendingClub Corporation\nserviceCategory: Financial Services / API\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: LendingClub API\n  ServiceCategory: Financial Services / API\n  ProviderName: LendingClub\n  PublisherName: LendingClub Corporation\n  InvoiceIssuerName: LendingClub Corporation\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - environment\n      - partner\n  - name: contract_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Track API call volume and partner-contract draw-down through your own gateway / observability\n      stack; LendingClub does not expose a public usage API.\n  - name: Allocation\n    description: Tag outbound calls by business\
  \ unit (loans, banking, investor) so contracted spend can\n      be charged back to the consuming team.\n  - name: Optimization\n    description: Batch institutional investor data pulls and cache static reference data to stay within\n      contracted volumes and avoid renegotiation.\n  - name: Accountability\n    description: Assign a single contract owner per LendingClub partner agreement and review consumption\n      against contracted volume monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lendingclub/refs/heads/main/finops/lendingclub-finops.yml
sources:
- https://www.lendingclub.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Fintech
- Personal Loans
- Banking
---
