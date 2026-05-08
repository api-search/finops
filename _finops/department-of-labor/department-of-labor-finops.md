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
description: FinOps framework definition for the Department of Labor API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Department of Labor
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Department of Labor
  PublisherName: Department of Labor
  ServiceCategory: Developer Tools / API
  ServiceName: Department of Labor
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
name: Department Of Labor Finops
provider_name: Department of Labor
provider_slug: department-of-labor
publisher_name: Department of Labor
service_category: API
slug: department-of-labor-finops
source_filename: department-of-labor-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Department of Labor\nproviderId: department-of-labor\npublisherName: Department of Labor\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - BLS\n  - Employment\n  - Enforcement\n  - Federal Government\n  - Labor\n  - Open Data\n  - Statistics\n  - Wages\n  - Workforce\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Department of Labor API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n\
  \      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n   \
  \   - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Department of Labor\n  ServiceCategory: Developer Tools / API\n  ProviderName: Department of Labor\n  PublisherName: Department of Labor\n  InvoiceIssuerName: Department of Labor\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n  \
  \    - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: DOL Open Data API V4\n    baseURL: https://apiprod.dol.gov/v4\n    tags:\n      - Datasets\n      - DOL Data Portal\n      - Open Data\n      - REST\n    serviceName: DOL Open Data API V4\n    serviceCategory: API\n  - name: BLS Public Data API V2\n    baseURL: https://api.bls.gov/publicAPI/v2\n    tags:\n      - BLS\n      - CPI\n      - Employment\n      - Statistics\n      - Time Series\n      - Wages\n    serviceName: BLS Public Data API V2\n    serviceCategory: API\n  - name: DOL Enforcement Data\n    baseURL: https://data.dol.gov\n    tags:\n      - Enforcement\n\
  \      - MSHA\n      - OFCCP\n      - OSHA\n      - Wage and Hour\n    serviceName: DOL Enforcement Data\n    serviceCategory: API\n  - name: DOL API Sampler\n    baseURL: https://devtools.dol.gov/apisampler\n    tags:\n      - DevTools\n      - Playground\n      - Sampler\n    serviceName: DOL API Sampler\n    serviceCategory: API\n  - name: DOL Open Data Catalog\n    baseURL: https://catalog.data.gov/api/3\n    tags:\n      - CKAN\n      - Datasets\n      - Open Data\n    serviceName: DOL Open Data Catalog\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/department-of-labor/refs/heads/main/finops/department-of-labor-finops.yml
sources: []
specification: FinOps Framework
tags:
- BLS
- Employment
- Enforcement
- Federal Government
- Labor
- Open Data
- Statistics
- Wages
- Workforce
- FinOps
- Cost Management
- FOCUS
---
