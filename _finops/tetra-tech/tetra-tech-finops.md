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
description: FinOps framework definition for the Tetra Tech API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Tetra Tech
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Tetra Tech
  PublisherName: Tetra Tech
  ServiceCategory: Developer Tools / API
  ServiceName: Tetra Tech
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
name: Tetra Tech Finops
provider_name: Tetra Tech
provider_slug: tetra-tech
publisher_name: Tetra Tech
service_category: API
slug: tetra-tech-finops
source_filename: tetra-tech-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Tetra Tech\nproviderId: tetra-tech\npublisherName: Tetra Tech\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Analytics\n  - Consulting\n  - Data Management\n  - Engineering\n  - Environment\n  - Infrastructure\n  - Water\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Tetra Tech API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Tetra Tech\n  ServiceCategory: Developer Tools / API\n  ProviderName: Tetra Tech\n  PublisherName: Tetra Tech\n  InvoiceIssuerName: Tetra Tech\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Cosmos Mobile Data Platform API\n    baseURL: https://cosmos.tetratech.com/\n    tags:\n      - Data Collection\n      - Field Data\n      - Mobile\n      - Webhooks\n    serviceName: Cosmos Mobile Data Platform API\n    serviceCategory: API\n  - name: Tetra Tech Data Discovery Tool API\n    baseURL: https://github.com/tetratech/DataDiscoveryTool\n    tags:\n      - Environmental\n      - Open Source\n      - USEPA\n      - Water Quality\n    serviceName: Tetra Tech Data Discovery Tool API\n    serviceCategory: API\n  - name: baytrends Water Quality Trend API\n    baseURL: https://github.com/tetratech/baytrends\n    tags:\n      - Chesapeake Bay\n      - Environmental\n\
  \      - Open Source\n      - R Package\n      - Water Quality\n    serviceName: baytrends Water Quality Trend API\n    serviceCategory: API\n  - name: Tetra Tech Delta Data Management Services\n    baseURL: https://www.tetratech.com/\n    tags:\n      - Analytics\n      - Data Management\n      - Digital Transformation\n      - Enterprise\n    serviceName: Tetra Tech Delta Data Management Services\n    serviceCategory: API\n  - name: WaterNet Water Network Management API\n    baseURL: https://www.tetratech.com/\n    tags:\n      - SaaS\n      - Water Infrastructure\n      - Utilities\n    serviceName: WaterNet Water Network Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tetra-tech/refs/heads/main/finops/tetra-tech-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Consulting
- Data Management
- Engineering
- Environment
- Infrastructure
- Water
- FinOps
- Cost Management
- FOCUS
---
