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
  - Adjustment
  pricingCategory: Fund Fees (Management + Carry) / Contract
description: 'FOCUS-aligned FinOps placeholder for Blackstone: not a developer-facing platform. Spend with Blackstone is captured as fund-level fees (management fee + carried interest) and any portfolio-company contracts, not API consumption.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: The Blackstone Group Inc.
  ProviderName: Blackstone
  PublisherName: The Blackstone Group Inc.
  ServiceCategory: Alternative Asset Management
  ServiceName: Blackstone
layout: finops
meters:
- aggregation: sum
  dimensions:
  - fund
  - vintage
  name: management_fees
  unit: USD
- aggregation: sum
  dimensions:
  - fund
  - vintage
  name: carried_interest
  unit: USD
- aggregation: count
  dimensions:
  - portfolio_company
  - region
  name: portfolio_company_contracts
  unit: contract
name: Blackstone Finops
provider_name: Blackstone
provider_slug: blackstone
publisher_name: The Blackstone Group Inc.
service_category: Alternative Asset Management
slug: blackstone-finops
source_filename: blackstone-finops.yml
source_heading: FinOps Profile
source_url: https://www.blackstone.com/our-businesses/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Blackstone\nproviderId: blackstone\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Alternative Assets\n  - Investment Management\ndescription: 'FOCUS-aligned FinOps placeholder for Blackstone: not a developer-facing platform.\n  Spend with Blackstone is captured as fund-level fees (management fee + carried interest) and any\n  portfolio-company contracts, not API consumption.'\nsources:\n  - https://www.blackstone.com/our-businesses/\nnotes: Blackstone has no public API billing surface; this artifact exists for symmetry with peer\n  providers and should be revisited only if a developer offering launches.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: The Blackstone Group Inc.\nserviceCategory: Alternative Asset Management\nbillingModel:\n  pricingCategory: Fund Fees (Management + Carry) / Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Blackstone\n  ServiceCategory: Alternative Asset Management\n  ProviderName: Blackstone\n  PublisherName: The Blackstone Group Inc.\n  InvoiceIssuerName: The Blackstone Group Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: management_fees\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - fund\n      - vintage\n  - name: carried_interest\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - fund\n      - vintage\n  - name: portfolio_company_contracts\n    unit: contract\n    aggregation: count\n    dimensions:\n      - portfolio_company\n      - region\nprinciples:\n  - name: Visibility\n    description: Use LP capital-account statements\
  \ and quarterly fund reporting from Blackstone\n      Investor Relations; no API telemetry exists.\n  - name: Allocation\n    description: Map fund commitments and side-letter terms to consuming entities through the LP\n      reporting pack.\n  - name: Optimization\n    description: Negotiate side-letter fee discounts at commitment time; consolidate commitments\n      across affiliates to reach fee-tier breakpoints.\n  - name: Accountability\n    description: Designate an LP-relations owner per fund commitment; review fund performance and\n      fee burn each quarter.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/blackstone/refs/heads/main/finops/blackstone-finops.yml
sources:
- https://www.blackstone.com/our-businesses/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Alternative Assets
- Investment Management
---
