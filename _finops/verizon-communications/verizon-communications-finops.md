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
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Contract / Custom
description: FOCUS-aligned FinOps shape for Verizon Communications API products. Verizon does not publish self-service rates for its Network APIs, ThingSpace IoT, 5G Edge, TM Forum, or Voice (CPaaS) APIs; billing is governed by the enterprise master service agreement and per-product schedules.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Verizon Communications, Inc.
  ProviderName: Verizon Communications
  PublisherName: Verizon Communications, Inc.
  ServiceCategory: Telecommunications
  ServiceName: Verizon Communications APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api_product
  - environment
  name: api_requests
  unit: request
- aggregation: max
  dimensions:
  - api_product
  - region
  name: connected_devices
  unit: device-month
- aggregation: sum
  dimensions:
  - direction
  - region
  name: voice_minutes
  unit: minute
name: Verizon Communications Finops
provider_name: Verizon Communications
provider_slug: verizon-communications
publisher_name: Verizon Communications, Inc.
service_category: Telecommunications
slug: verizon-communications-finops
source_filename: verizon-communications-finops.yml
source_heading: FinOps Profile
source_url: https://www.verizon.com/business/products/internet-of-things/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Verizon Communications\nproviderId: verizon-communications\npublisherName: Verizon Communications, Inc.\nserviceCategory: Telecommunications\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Telecommunications\n  - Network APIs\n  - IoT\n  - 5G\ndescription: FOCUS-aligned FinOps shape for Verizon Communications API products. Verizon does not\n  publish self-service rates for its Network APIs, ThingSpace IoT, 5G Edge, TM Forum, or Voice (CPaaS)\n  APIs; billing is governed by the enterprise master service agreement and per-product schedules.\nsources:\n  - https://www.verizon.com/business/products/internet-of-things/\nnotes: No public unit\
  \ prices or invoice line definitions were available at reconciliation time.\n  The meter list captures the categories Verizon contracts typically bill against.\nbillingModel:\n  pricingCategory: Contract / Custom\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Verizon Communications APIs\n  ServiceCategory: Telecommunications\n  ProviderName: Verizon Communications\n  PublisherName: Verizon Communications, Inc.\n  InvoiceIssuerName: Verizon Communications, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_product\n      - environment\n  - name: connected_devices\n    unit: device-month\n    aggregation: max\n    dimensions:\n      - api_product\n      - region\n  - name: voice_minutes\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - direction\n      - region\nprinciples:\n \
  \ - name: Visibility\n    description: Verizon does not expose a public usage API for these products; consumption is reported\n      through the Verizon Enterprise Center / My Business invoice and the per-product portals (e.g.\n      ThingSpace dashboard).\n  - name: Allocation\n    description: Tag spend at the contract / billing-account level using the cost-center mapping in\n      My Business; sub-account splits typically require a separate billing account from Verizon.\n  - name: Optimization\n    description: Optimization levers are commercial — committed-volume rate cards in the master\n      agreement, retiring unused SIMs / lines, and consolidating ThingSpace device pools.\n  - name: Accountability\n    description: Spend ownership sits with the named Verizon Business account executive on the\n      consumer side; finance reconciles against the My Business monthly invoice.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/verizon-communications/refs/heads/main/finops/verizon-communications-finops.yml
sources:
- https://www.verizon.com/business/products/internet-of-things/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Telecommunications
- Network APIs
- IoT
- 5G
---
