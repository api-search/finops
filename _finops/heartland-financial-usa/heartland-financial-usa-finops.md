---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per Agreement
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Bilateral / Negotiated
description: FOCUS-aligned FinOps stub for Heartland Financial USA. No public billing surface exists; fees are bilateral and bank-grade.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: UMB Financial Corporation
  PricingCategory: Bilateral
  PricingUnit: varies
  ProviderName: Heartland Financial USA
  PublisherName: UMB Financial Corporation
  ServiceCategory: Banking / Financial Services
  ServiceName: Heartland Financial USA
layout: finops
meters:
- aggregation: sum
  description: Negotiated partner fees per the bilateral agreement
  dimensions:
  - service
  - partner_id
  name: partner_fees
  unit: varies
name: Heartland Financial Usa Finops
provider_name: Heartland Financial USA
provider_slug: heartland-financial-usa
publisher_name: UMB Financial Corporation (acquired Heartland Financial USA)
service_category: Banking / Financial Services
slug: heartland-financial-usa-finops
source_filename: heartland-financial-usa-finops.yml
source_heading: FinOps Profile
source_url: https://www.umb.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Heartland Financial USA\nproviderId: heartland-financial-usa\npublisherName: UMB Financial Corporation (acquired Heartland Financial USA)\nserviceCategory: Banking / Financial Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Financial Services\n  - FinOps\n  - FOCUS\nnotes: HTLF was acquired by UMB Financial Corporation; no public API pricing or invoice surface exists.\n  FinOps for any HTLF / UMB integration is governed by a bilateral partner contract. Meters and billing\n  model are placeholders; consumers should align FinOps to the actual invoice line items in their\n  executed agreement.\ndescription: 'FOCUS-aligned FinOps stub for Heartland\
  \ Financial USA. No public billing surface exists;\n  fees are bilateral and bank-grade.'\nsources:\n  - https://www.umb.com/\nbillingModel:\n  pricingCategory: Bilateral / Negotiated\n  billingFrequency: Per Agreement\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Heartland Financial USA\n  ServiceCategory: Banking / Financial Services\n  ProviderName: Heartland Financial USA\n  PublisherName: UMB Financial Corporation\n  InvoiceIssuerName: UMB Financial Corporation\n  PricingCategory: Bilateral\n  PricingUnit: varies\n  BillingCurrency: USD\n  ChargeCategory: Usage\nprinciples:\n  - name: Visibility\n    description: Use the executed partner agreement's reporting and reconciliation schedule to track\n      consumption and fees. No public usage API is exposed.\n  - name: Allocation\n    description: Allocate fees against the consuming product line through the bilateral invoice; reference\n      partner_id or account_id\
  \ columns where supplied.\n  - name: Optimization\n    description: Renegotiation and product fit are the primary cost levers; HTLF/UMB does not publish\n      tiered price breaks.\n  - name: Accountability\n    description: Assign a relationship owner who handles the bilateral contract, fee schedule, and\n      compliance attestations.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Budgeting\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Intersecting Disciplines\nmeters:\n  - name: partner_fees\n    description: Negotiated partner fees per the bilateral agreement\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - partner_id\napis:\n  - name: Heartland Financial\
  \ USA API\n    baseURL: https://api.htlf.com\n    tags:\n      - Banking\n      - Financial Services\n    serviceName: Heartland Financial USA API\n    serviceCategory: Banking / Financial Services\nunitEconomics:\n  - name: Cost per Transaction (per agreement)\n    metric: partner_fees / transactions\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/heartland-financial-usa/refs/heads/main/finops/heartland-financial-usa-finops.yml
sources:
- https://www.umb.com/
specification: FinOps Framework
tags:
- Banking
- Financial Services
- FinOps
- FOCUS
---
