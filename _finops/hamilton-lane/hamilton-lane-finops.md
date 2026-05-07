---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps placeholder for Hamilton Lane: institutional Cobalt-based subscription model, no public per-API pricing. Meters describe subscription seats and API utilization for allocation across investment teams.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Hamilton Lane Incorporated
  PricingCategory: Subscription
  PricingUnit: seat
  ProviderName: Hamilton Lane
  PublisherName: Hamilton Lane Incorporated
  ServiceCategory: Private Markets Data / Analytics
  ServiceName: Hamilton Lane Cobalt
layout: finops
meters:
- aggregation: max
  description: Cobalt platform user seats
  dimensions:
  - team
  - role
  name: cobalt_seats
  unit: seat-month
- aggregation: sum
  description: Hamilton Lane / Cobalt API request volume (allocation meter)
  dimensions:
  - endpoint
  - team
  - dataset
  name: api_requests
  unit: request
name: Hamilton Lane Finops
provider_name: Hamilton Lane
provider_slug: hamilton-lane
publisher_name: Hamilton Lane Incorporated
service_category: Private Markets Data / Analytics Subscription
slug: hamilton-lane-finops
source_filename: hamilton-lane-finops.yml
source_heading: FinOps Profile
source_url: https://www.hamiltonlane.com/en-us
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Hamilton Lane\nproviderId: hamilton-lane\npublisherName: Hamilton Lane Incorporated\nserviceCategory: Private Markets Data / Analytics Subscription\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Private Markets\n  - Asset Management\n  - Investment\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Hamilton Lane: institutional Cobalt-based\n  subscription model, no public per-API pricing. Meters describe subscription seats and API\n  utilization for allocation across investment teams.'\nnotes: No public commercial model is published. Reconcile against the customer's Cobalt\
  \ subscription\n  agreement.\nsources:\n  - https://www.hamiltonlane.com/en-us\nprinciples:\n  - name: Visibility\n    description: Track Cobalt seat utilization and API call volume via the Cobalt admin console.\n  - name: Allocation\n    description: Allocate Cobalt subscription cost across investment teams (private equity,\n      private credit, real assets, infrastructure) using seat assignments.\n  - name: Optimization\n    description: Right-size seat counts; consolidate API consumption through a central data team\n      rather than per-analyst direct calls.\n  - name: Accountability\n    description: Designate a Cobalt program owner; review seat utilization and renewal terms\n      annually.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n\
  \      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Hamilton Lane Cobalt\n  ServiceCategory: Private Markets Data / Analytics\n  ProviderName: Hamilton Lane\n  PublisherName: Hamilton Lane Incorporated\n  InvoiceIssuerName: Hamilton Lane Incorporated\n  PricingCategory: Subscription\n  PricingUnit: seat\n  BillingCurrency: USD\n  ChargeCategory:\
  \ Purchase\nmeters:\n  - name: cobalt_seats\n    description: Cobalt platform user seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - team\n      - role\n  - name: api_requests\n    description: Hamilton Lane / Cobalt API request volume (allocation meter)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - team\n      - dataset\napis:\n  - name: Hamilton Lane API\n    baseURL: https://api.hamiltonlane.com\n    tags:\n      - Private Markets\n      - Asset Management\n      - Investment\n    serviceName: Hamilton Lane API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Seat\n    metric: billed_cost / cobalt_seats\n    target: TBD\n  - name: Cost per Active Investment Team\n    metric: billed_cost / active_teams\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hamilton-lane/refs/heads/main/finops/hamilton-lane-finops.yml
sources:
- https://www.hamiltonlane.com/en-us
specification: FinOps Framework
tags:
- Private Markets
- Asset Management
- Investment
- FinOps
- Cost Management
- FOCUS
---
