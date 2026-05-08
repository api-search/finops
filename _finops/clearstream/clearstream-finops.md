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
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Clearstream API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Clearstream
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Clearstream
  PublisherName: Clearstream
  ServiceCategory: Developer Tools / API
  ServiceName: Clearstream
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Clearstream Finops
provider_name: Clearstream
provider_slug: clearstream
publisher_name: Clearstream
service_category: API
slug: clearstream-finops
source_filename: clearstream-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Clearstream\nproviderId: clearstream\npublisherName: Clearstream\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Capital Markets\n  - Collateral Management\n  - Custody\n  - Financial Services\n  - ISO 15022\n  - ISO 20022\n  - Post-Trade Infrastructure\n  - Securities\n  - Settlement\n  - SWIFT\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Clearstream API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Clearstream\n  ServiceCategory: Developer Tools / API\n  ProviderName: Clearstream\n  PublisherName: Clearstream\n  InvoiceIssuerName: Clearstream\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Clearstream Xact via SWIFT\n    baseURL: ''\n    tags:\n      - Custody\n      - ISO 15022\n      - ISO 20022\n      - Settlement\n      - SWIFT\n    serviceName: Clearstream Xact via SWIFT\n    serviceCategory: API\n  - name: Clearstream Xact File Transfer\n    baseURL: ''\n    tags:\n      - File Transfer\n      - ISO 20022\n      - SWIFTNet FileAct\n      - Settlement\n    serviceName: Clearstream Xact File Transfer\n    serviceCategory: API\n  - name: Clearstream Xact Web Portal\n    baseURL: ''\n    tags:\n      - Asset Servicing\n      - Custody\n      - Settlement\n   \
  \   - Web Portal\n    serviceName: Clearstream Xact Web Portal\n    serviceCategory: API\n  - name: Clearstream CASCADE (CSD)\n    baseURL: ''\n    tags:\n      - CSD\n      - Domestic Settlement\n      - Germany\n      - SWIFT\n    serviceName: Clearstream CASCADE (CSD)\n    serviceCategory: API\n  - name: Clearstream Vestima\n    baseURL: ''\n    tags:\n      - Funds\n      - ISO 20022\n      - Order Routing\n    serviceName: Clearstream Vestima\n    serviceCategory: API\n  - name: Clearstream CmaX (Triparty Collateral)\n    baseURL: ''\n    tags:\n      - Collateral Management\n      - Margin\n      - Triparty\n    serviceName: Clearstream CmaX (Triparty Collateral)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/clearstream/refs/heads/main/finops/clearstream-finops.yml
sources: []
specification: FinOps Framework
tags:
- Capital Markets
- Collateral Management
- Custody
- Financial Services
- ISO 15022
- ISO 20022
- Post-Trade Infrastructure
- Securities
- Settlement
- SWIFT
- FinOps
- Cost Management
- FOCUS
---
