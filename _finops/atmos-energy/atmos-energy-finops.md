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
  - Usage
  - Tax
  pricingCategory: Regulated Utility Tariff
description: FinOps shape for Atmos Energy is not applicable — Atmos is a regulated natural-gas utility, not an API provider. Customer charges are state-tariff-based commodity and distribution rates.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Atmos Energy Corporation
  PricingCategory: Regulated Utility Tariff
  ProviderName: Atmos Energy
  PublisherName: Atmos Energy Corporation
  ServiceCategory: Utilities
  ServiceName: Atmos Energy
  ServiceSubcategory: Natural Gas Distribution
layout: finops
meters:
- aggregation: sum
  description: Natural gas delivered to the customer meter (utility billing meter, not an API meter)
  dimensions:
  - state
  - rate_class
  name: gas_delivered
  unit: Mcf
- aggregation: sum
  description: Fixed and tiered distribution charges per state PUC tariff
  dimensions:
  - state
  - rate_class
  name: distribution_charge
  unit: month
name: Atmos Energy Finops
provider_name: Atmos Energy
provider_slug: atmos-energy
publisher_name: Atmos Energy Corporation
service_category: Utilities / Natural Gas Distribution
slug: atmos-energy-finops
source_filename: atmos-energy-finops.yml
source_heading: FinOps Profile
source_url: https://www.atmosenergy.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Atmos Energy\nproviderId: atmos-energy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Natural Gas\n  - Utilities\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Atmos Energy is not applicable — Atmos is a regulated natural-gas utility,\n  not an API provider. Customer charges are state-tariff-based commodity and distribution rates.\nsources:\n  - https://www.atmosenergy.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: No API billing surface. Atmos invoices are utility bills (therms / Mcf delivered + distribution\n  + tax), not FOCUS-aligned cloud/API charges.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Atmos\
  \ Energy Corporation\nserviceCategory: Utilities / Natural Gas Distribution\nbillingModel:\n  pricingCategory: Regulated Utility Tariff\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Atmos Energy\n  ServiceCategory: Utilities\n  ServiceSubcategory: Natural Gas Distribution\n  ProviderName: Atmos Energy\n  PublisherName: Atmos Energy Corporation\n  InvoiceIssuerName: Atmos Energy Corporation\n  BillingCurrency: USD\n  PricingCategory: Regulated Utility Tariff\nmeters:\n  - name: gas_delivered\n    description: Natural gas delivered to the customer meter (utility billing meter, not an API meter)\n    unit: Mcf\n    aggregation: sum\n    dimensions:\n      - state\n      - rate_class\n  - name: distribution_charge\n    description: Fixed and tiered distribution charges per state PUC tariff\n    unit: month\n    aggregation: sum\n    dimensions:\n      - state\n      - rate_class\nprinciples:\n  - name: Visibility\n\
  \    description: Not applicable to API consumption — utility usage is visible via the customer portal\n      monthly bill.\n  - name: Allocation\n    description: Not applicable — single utility account per premise.\n  - name: Optimization\n    description: Not applicable to API; utility-side levers are conservation and demand-response programs.\n  - name: Accountability\n    description: Not applicable to API.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/atmos-energy/refs/heads/main/finops/atmos-energy-finops.yml
sources:
- https://www.atmosenergy.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Energy
- Natural Gas
- Utilities
- FinOps
- FOCUS
---
