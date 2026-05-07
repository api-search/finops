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
  - Tax
  - Adjustment
  - Refund
  chargeFrequency: Recurring
  pricingCategory: Cost of Goods + Distributor Agreement
description: 'FOCUS-aligned FinOps for Dana Incorporated aftermarket APIs: distributor API access included in the distributor agreement; spend tracks parts (cost-of-goods) rather than API calls.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Dana Incorporated
  PricingCategory: Cost of Goods
  ProviderName: Dana Incorporated
  PublisherName: Dana Incorporated
  ServiceCategory: Automotive Aftermarket
  ServiceName: Dana Incorporated
layout: finops
meters:
- aggregation: sum
  description: Aftermarket part orders placed via API
  dimensions:
  - distributor
  - product_line
  - branch
  name: parts_orders
  unit: order
- aggregation: sum
  description: Individual part units ordered
  dimensions:
  - product_line
  - sku
  name: parts_units
  unit: part
- aggregation: sum
  description: API calls against the Dana Aftermarket API (not separately billed; observed for capacity)
  dimensions:
  - api
  - distributor
  name: api_requests
  unit: request
name: Dana Incorporated Finops
provider_name: Dana Incorporated
provider_slug: dana-incorporated
publisher_name: Dana Incorporated
service_category: Automotive Aftermarket
slug: dana-incorporated-finops
source_filename: dana-incorporated-finops.yml
source_heading: FinOps Profile
source_url: https://www.danaincorporated.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Dana Incorporated\nproviderId: dana-incorporated\npublisherName: Dana Incorporated\nserviceCategory: Automotive Aftermarket\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Aftermarket\n  - Auto Parts\n  - Automotive\n  - Drivetrain\n  - Electrified Propulsion\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Dana Incorporated aftermarket APIs: distributor API access included\n  in the distributor agreement; spend tracks parts (cost-of-goods) rather than API calls.'\nsources:\n  - https://www.danaincorporated.com/\nnotes: No separate API pricing; cost tracks parts ordered via the distributor agreement.\n\
  principles:\n  - name: Visibility\n    description: Track parts orders, returns, and core charges via the distributor portal and Dana Aftermarket\n      API order endpoints.\n  - name: Allocation\n    description: Tag orders by branch / shop / business unit to attribute aftermarket parts spend.\n  - name: Optimization\n    description: Consolidate orders to hit volume tiers; use API inventory checks before ordering to\n      avoid backorder fees; manage core returns promptly.\n  - name: Accountability\n    description: Distributor / branch ops owns parts purchasing; finance reviews monthly distributor\n      statements for chargebacks and rebate accruals.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Forecasting\n      - Budgeting\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n  - name: Manage the FinOps Practice\n  \
  \  capabilities:\n      - Invoicing and Chargeback\nbillingModel:\n  pricingCategory: Cost of Goods + Distributor Agreement\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Dana Incorporated\n  ServiceCategory: Automotive Aftermarket\n  ProviderName: Dana Incorporated\n  PublisherName: Dana Incorporated\n  InvoiceIssuerName: Dana Incorporated\n  PricingCategory: Cost of Goods\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: parts_orders\n    description: Aftermarket part orders placed via API\n    unit: order\n    aggregation: sum\n    dimensions:\n      - distributor\n      - product_line\n      - branch\n  - name: parts_units\n    description: Individual part units ordered\n    unit: part\n    aggregation: sum\n    dimensions:\n      - product_line\n      - sku\n  - name: api_requests\n    description: API calls against\
  \ the Dana Aftermarket API (not separately billed; observed for capacity)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - distributor\napis:\n  - name: Dana Aftermarket API\n    baseURL: https://api.danaaftermarket.com\n    tags:\n      - Aftermarket\n      - Auto Parts\n      - Drivetrain\n      - eCommerce\n      - Supply Chain\n    serviceName: Dana Aftermarket API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Part\n    metric: billed_cost / parts_units\n    target: TBD\n  - name: Cost per Order\n    metric: billed_cost / parts_orders\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dana-incorporated/refs/heads/main/finops/dana-incorporated-finops.yml
sources:
- https://www.danaincorporated.com/
specification: FinOps Framework
tags:
- Aftermarket
- Auto Parts
- Automotive
- Drivetrain
- Electrified Propulsion
- FinOps
- FOCUS
---
