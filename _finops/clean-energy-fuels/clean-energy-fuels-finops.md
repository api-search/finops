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
  - Usage
  - Tax
  pricingCategory: Enterprise Contract
description: 'FinOps placeholder for Clean Energy Fuels: no public API pricing, so meters and FOCUS columns reflect the typical shape of an enterprise partner contract.'
focus_columns:
  BillingCurrency: USD
  PricingCategory: Enterprise Contract
  ProviderName: Clean Energy Fuels
  PublisherName: Clean Energy Fuels Corp.
  ServiceCategory: Energy / Fueling
  ServiceName: Clean Energy Fuels
layout: finops
meters:
- aggregation: sum
  description: Recurring partner integration / data feed subscription fee per the enterprise contract.
  dimensions:
  - contract
  name: contract_subscription
  unit: month
- aggregation: sum
  description: API calls invoked under the partner contract, where usage is metered.
  dimensions:
  - contract
  name: api_calls
  unit: request
name: Clean Energy Fuels Finops
provider_name: Clean Energy Fuels
provider_slug: clean-energy-fuels
publisher_name: Clean Energy Fuels Corp.
service_category: Energy / Fueling
slug: clean-energy-fuels-finops
source_filename: clean-energy-fuels-finops.yml
source_heading: FinOps Profile
source_url: https://www.cleanenergyfuels.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Clean Energy Fuels\nproviderId: clean-energy-fuels\npublisherName: Clean Energy Fuels Corp.\nserviceCategory: Energy / Fueling\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Natural Gas\n  - Renewable\n  - Transportation\nnotes: Clean Energy Fuels is an energy operator, not a software vendor. There is no public API price list;\n  this artifact captures the structural FinOps shape of a partner-contract integration rather than verified\n  invoice line-items.\ndescription: 'FinOps placeholder for Clean Energy Fuels: no public API pricing, so meters and FOCUS columns\n  reflect the typical shape of\
  \ an enterprise partner contract.'\nsources:\n  - https://www.cleanenergyfuels.com\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Clean Energy Fuels\n  ServiceCategory: Energy / Fueling\n  ProviderName: Clean Energy Fuels\n  PublisherName: Clean Energy Fuels Corp.\n  PricingCategory: Enterprise Contract\n  BillingCurrency: USD\nmeters:\n  - name: contract_subscription\n    description: Recurring partner integration / data feed subscription fee per the enterprise contract.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\n  - name: api_calls\n    description: API calls invoked under the partner contract, where usage is metered.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Reconcile usage against the partner contract via the integration\
  \ partner's reporting deliverables.\n  - name: Allocation\n    description: Allocate the contract to the consuming fleet operations team or biogas supply program.\n  - name: Optimization\n    description: Right-size the partner contract scope (data feeds, integration endpoints) at each renewal.\n  - name: Accountability\n    description: Assign a partner-integration owner accountable for renewal and utilization review.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/clean-energy-fuels/refs/heads/main/finops/clean-energy-fuels-finops.yml
sources:
- https://www.cleanenergyfuels.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Natural Gas
- Renewable
- Transportation
---
