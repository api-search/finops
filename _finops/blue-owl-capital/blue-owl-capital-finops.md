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
  pricingCategory: Fund Fees (Management + Incentive)
description: 'FOCUS-aligned FinOps placeholder for Blue Owl Capital: not a developer-facing platform. Spend with Blue Owl is captured as fund-level fees (management fee + incentive fee) across its Credit, Real Assets, and GP Strategic Capital platforms.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Blue Owl Capital Inc.
  ProviderName: Blue Owl Capital
  PublisherName: Blue Owl Capital Inc.
  ServiceCategory: Alternative Asset Management
  ServiceName: Blue Owl Capital
layout: finops
meters:
- aggregation: sum
  dimensions:
  - platform
  - fund
  name: management_fees
  unit: USD
- aggregation: sum
  dimensions:
  - platform
  - fund
  name: incentive_fees
  unit: USD
- aggregation: avg
  dimensions:
  - platform
  name: aum_under_management
  unit: USD
name: Blue Owl Capital Finops
provider_name: Blue Owl Capital
provider_slug: blue-owl-capital
publisher_name: Blue Owl Capital Inc.
service_category: Alternative Asset Management
slug: blue-owl-capital-finops
source_filename: blue-owl-capital-finops.yml
source_heading: FinOps Profile
source_url: https://www.blueowl.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Blue Owl Capital\nproviderId: blue-owl-capital\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Alternative Asset Management\n  - Private Credit\ndescription: 'FOCUS-aligned FinOps placeholder for Blue Owl Capital: not a developer-facing platform.\n  Spend with Blue Owl is captured as fund-level fees (management fee + incentive fee) across its\n  Credit, Real Assets, and GP Strategic Capital platforms.'\nsources:\n  - https://www.blueowl.com\nnotes: Blue Owl has no public API billing surface; this artifact exists for symmetry and should be\n  revisited only if a developer offering launches.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Blue Owl Capital Inc.\nserviceCategory: Alternative Asset Management\nbillingModel:\n  pricingCategory: Fund Fees (Management + Incentive)\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Blue Owl Capital\n  ServiceCategory: Alternative Asset Management\n  ProviderName: Blue Owl Capital\n  PublisherName: Blue Owl Capital Inc.\n  InvoiceIssuerName: Blue Owl Capital Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: management_fees\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - platform\n      - fund\n  - name: incentive_fees\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - platform\n      - fund\n  - name: aum_under_management\n    unit: USD\n    aggregation: avg\n    dimensions:\n      - platform\nprinciples:\n  - name: Visibility\n    description: Use LP capital-account statements and quarterly fund reports from Blue Owl\n      Investor\
  \ Relations.\n  - name: Allocation\n    description: Map fund commitments to consuming entities through the LP reporting pack.\n  - name: Optimization\n    description: Negotiate side-letter fee discounts at commitment time; consolidate commitments\n      across affiliates to reach fee-tier breakpoints.\n  - name: Accountability\n    description: Designate an LP-relations owner per fund commitment; review quarterly fund\n      performance and fee burn.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/blue-owl-capital/refs/heads/main/finops/blue-owl-capital-finops.yml
sources:
- https://www.blueowl.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Alternative Asset Management
- Private Credit
---
