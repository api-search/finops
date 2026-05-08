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
  - Purchase
  - Usage
  - Tax
  - Adjustment
  chargeFrequency: Milestone
  pricingCategory: Contract / Milestone
description: 'FOCUS-aligned FinOps for Cubic: contract-priced transit and defense systems with embedded APIs; spend is tracked as project / milestone delivery rather than per-call usage.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Cubic Corporation
  PricingCategory: Custom Contract
  ProviderName: Cubic Corporation
  PublisherName: Cubic Corporation
  ServiceCategory: Transportation & Defense Systems
  ServiceName: Cubic Corporation
layout: finops
meters:
- aggregation: sum
  description: Delivered milestones under a Cubic systems contract
  dimensions:
  - program
  - division
  name: contract_milestones
  unit: milestone
- aggregation: max
  description: Cubic-installed endpoints (fare gates, ATM training systems, etc.)
  dimensions:
  - site
  - region
  name: deployed_endpoints
  unit: endpoint
- aggregation: sum
  description: API calls within delivered systems (not separately billed; observed for capacity)
  dimensions:
  - api
  - tenant
  name: api_requests
  unit: request
name: Cubic Finops
provider_name: Cubic Corporation
provider_slug: cubic
publisher_name: Cubic Corporation
service_category: Transportation & Defense Systems
slug: cubic-finops
source_filename: cubic-finops.yml
source_heading: FinOps Profile
source_url: https://www.cubic.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cubic Corporation\nproviderId: cubic\npublisherName: Cubic Corporation\nserviceCategory: Transportation & Defense Systems\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Defense\n  - Transportation\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Cubic: contract-priced transit and defense systems with embedded\n  APIs; spend is tracked as project / milestone delivery rather than per-call usage.'\nsources:\n  - https://www.cubic.com/\nnotes: No public pricing. Treat Cubic spend as project-based; reconcile against the contract milestone\n  schedule.\nprinciples:\n  - name: Visibility\n    description: Track\
  \ Cubic spend through contract milestones and delivered-system commissioning rather\n      than API-call telemetry.\n  - name: Allocation\n    description: Allocate to the transit agency / mission program owning the contract; tag delivered\n      stations / endpoints by route / theater.\n  - name: Optimization\n    description: Negotiate scope at contract milestones; consolidate vendor systems across modes / theaters\n      to reduce duplicate licensing.\n  - name: Accountability\n    description: Program management and finance jointly own the Cubic contract; review milestone burn-down\n      and change-orders quarterly.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Forecasting\n      - Budgeting\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Workload Optimization\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing\
  \ and Chargeback\nbillingModel:\n  pricingCategory: Contract / Milestone\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n  chargeFrequency: Milestone\nfocusColumns:\n  ServiceName: Cubic Corporation\n  ServiceCategory: Transportation & Defense Systems\n  ProviderName: Cubic Corporation\n  PublisherName: Cubic Corporation\n  InvoiceIssuerName: Cubic Corporation\n  PricingCategory: Custom Contract\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract_milestones\n    description: Delivered milestones under a Cubic systems contract\n    unit: milestone\n    aggregation: sum\n    dimensions:\n      - program\n      - division\n  - name: deployed_endpoints\n    description: Cubic-installed endpoints (fare gates, ATM training systems, etc.)\n    unit: endpoint\n    aggregation: max\n    dimensions:\n      - site\n      - region\n  - name: api_requests\n    description: API calls\
  \ within delivered systems (not separately billed; observed for capacity)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - tenant\napis:\n  - name: Cubic Corporation API\n    baseURL: https://api.cubic.com\n    tags:\n      - Defense\n      - Transportation\n      - Technology\n    serviceName: Cubic Corporation API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Deployed Endpoint\n    metric: billed_cost / deployed_endpoints\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cubic/refs/heads/main/finops/cubic-finops.yml
sources:
- https://www.cubic.com/
specification: FinOps Framework
tags:
- Defense
- Transportation
- FinOps
- FOCUS
---
