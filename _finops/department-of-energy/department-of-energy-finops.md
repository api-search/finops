---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: department-of-energy-openapi.yml
  format: yaml
  label: EIA Open Data API V2
  slug: eia-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/department-of-energy/refs/heads/main/openapi/department-of-energy-openapi.yml
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
description: FinOps framework definition for the Department of Energy API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Department of Energy
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Department of Energy
  PublisherName: Department of Energy
  ServiceCategory: Developer Tools / API
  ServiceName: Department of Energy
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
name: Department Of Energy Finops
provider_name: Department of Energy
provider_slug: department-of-energy
publisher_name: Department of Energy
service_category: API
slug: department-of-energy-finops
source_filename: department-of-energy-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Department of Energy\nproviderId: department-of-energy\npublisherName: Department of Energy\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Buildings\n  - Electricity\n  - Energy\n  - Federal Government\n  - Open Data\n  - Renewables\n  - Research\n  - Solar\n  - Statistics\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Department of Energy API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams\
  \ in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Department of Energy\n  ServiceCategory: Developer Tools / API\n  ProviderName: Department of Energy\n  PublisherName: Department of Energy\n  InvoiceIssuerName: Department of Energy\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n\
  \      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: EIA Open Data API V2\n    baseURL: https://api.eia.gov/v2\n    tags:\n      - Coal\n      - Electricity\n      - Energy Statistics\n      - Natural Gas\n      - Petroleum\n      - Renewables\n    serviceName: EIA Open Data API V2\n    serviceCategory: API\n  - name: OSTI DOE PAGES API\n    baseURL: https://www.osti.gov/pages/api/v1\n    tags:\n      - Bibliographic\n      - OSTI\n      - Publications\n      - Research\n    serviceName: OSTI DOE PAGES API\n    serviceCategory: API\n  - name: OSTI ELINK API\n    baseURL: https://www.osti.gov/elink\n    tags:\n\
  \      - ELINK\n      - Metadata\n      - OSTI\n      - Submission\n    serviceName: OSTI ELINK API\n    serviceCategory: API\n  - name: NREL/NLR Developer Network APIs\n    baseURL: https://developer.nlr.gov/api\n    tags:\n      - Alternative Fuels\n      - Buildings\n      - Electricity\n      - Geothermal\n      - NREL\n      - Renewables\n      - Solar\n      - Transportation\n    serviceName: NREL/NLR Developer Network APIs\n    serviceCategory: API\n  - name: Buildings Performance Database API\n    baseURL: https://api.example.com\n    tags:\n      - BPD\n      - Benchmarking\n      - Buildings\n      - Energy Efficiency\n    serviceName: Buildings Performance Database API\n    serviceCategory: API\n  - name: Department of Energy Open Data Catalog\n    baseURL: https://catalog.data.gov/api/3\n    tags:\n      - CKAN\n      - Datasets\n      - Open Data\n    serviceName: Department of Energy Open Data Catalog\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n\
  \    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/department-of-energy/refs/heads/main/finops/department-of-energy-finops.yml
sources: []
specification: FinOps Framework
tags:
- Buildings
- Electricity
- Energy
- Federal Government
- Open Data
- Renewables
- Research
- Solar
- Statistics
- FinOps
- Cost Management
- FOCUS
---
