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
  pricingCategory: Bilateral / Negotiated (per subsidiary)
description: FOCUS-aligned FinOps stub for Hilltop Holdings. No public billing surface exists at the holding-company level; FinOps tracking happens at the operating-subsidiary level.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Hilltop Holdings subsidiary (PlainsCapital Bank / HilltopSecurities / PrimeLending)
  PricingCategory: Bilateral
  PricingUnit: varies
  ProviderName: Hilltop Holdings
  PublisherName: Hilltop Holdings Inc.
  ServiceCategory: Banking / Insurance / Financial Services
  ServiceName: Hilltop Holdings
layout: finops
meters:
- aggregation: sum
  description: Fees billed by Hilltop subsidiaries under the bilateral agreement
  dimensions:
  - subsidiary
  - service
  name: subsidiary_fees
  unit: varies
name: Hilltop Holdings Finops
provider_name: Hilltop Holdings
provider_slug: hilltop-holdings
publisher_name: Hilltop Holdings Inc.
service_category: Banking / Insurance / Financial Services
slug: hilltop-holdings-finops
source_filename: hilltop-holdings-finops.yml
source_heading: FinOps Profile
source_url: https://www.hilltop.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Hilltop Holdings\nproviderId: hilltop-holdings\npublisherName: Hilltop Holdings Inc.\nserviceCategory: Banking / Insurance / Financial Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Insurance\n  - Financial Services\n  - FinOps\n  - FOCUS\nnotes: Hilltop Holdings is a financial holding company; revenue and fees flow through the operating\n  subsidiaries (PlainsCapital Bank, HilltopSecurities, PrimeLending). There is no holding-company-level\n  invoice surface. Meters and unit economics depend on which subsidiary the consumer integrates with.\ndescription: 'FOCUS-aligned FinOps stub for Hilltop Holdings. No public billing surface exists\
  \ at the\n  holding-company level; FinOps tracking happens at the operating-subsidiary level.'\nsources:\n  - https://www.hilltop.com/\nbillingModel:\n  pricingCategory: Bilateral / Negotiated (per subsidiary)\n  billingFrequency: Per Agreement\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Hilltop Holdings\n  ServiceCategory: Banking / Insurance / Financial Services\n  ProviderName: Hilltop Holdings\n  PublisherName: Hilltop Holdings Inc.\n  InvoiceIssuerName: Hilltop Holdings subsidiary (PlainsCapital Bank / HilltopSecurities / PrimeLending)\n  PricingCategory: Bilateral\n  PricingUnit: varies\n  BillingCurrency: USD\n  ChargeCategory: Usage\nprinciples:\n  - name: Visibility\n    description: Use the executed subsidiary partner agreement's reporting cadence to track consumption\n      and fees; no holding-company-level usage API exists.\n  - name: Allocation\n    description: Allocate fees by subsidiary line\
  \ of business (banking, brokerage, mortgage) and by\n      consuming product within your own organization.\n  - name: Optimization\n    description: Renegotiation and product fit at the subsidiary level are the primary cost levers.\n  - name: Accountability\n    description: Assign one relationship owner per subsidiary partnership; aggregate at the holding-company\n      level for executive review.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Budgeting\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Intersecting Disciplines\nmeters:\n  - name: subsidiary_fees\n    description: Fees billed by Hilltop subsidiaries under the bilateral agreement\n    unit: varies\n    aggregation: sum\n    dimensions:\n\
  \      - subsidiary\n      - service\napis:\n  - name: Hilltop Holdings API\n    baseURL: https://api.hilltop-holdings.com\n    tags:\n      - Banking\n      - Insurance\n      - Financial Services\n    serviceName: Hilltop Holdings API\n    serviceCategory: Banking / Insurance / Financial Services\nunitEconomics:\n  - name: Cost per Subsidiary Service Call\n    metric: subsidiary_fees / subsidiary_calls\n    target: per subsidiary agreement\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hilltop-holdings/refs/heads/main/finops/hilltop-holdings-finops.yml
sources:
- https://www.hilltop.com/
specification: FinOps Framework
tags:
- Banking
- Insurance
- Financial Services
- FinOps
- FOCUS
---
