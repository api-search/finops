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
description: FinOps framework definition for the Centers for Disease Control and Prevention API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Centers for Disease Control and Prevention
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Centers for Disease Control and Prevention
  PublisherName: Centers for Disease Control and Prevention
  ServiceCategory: Developer Tools / API
  ServiceName: Centers for Disease Control and Prevention
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
name: Centers For Disease Control And Prevention Finops
provider_name: Centers for Disease Control and Prevention
provider_slug: centers-for-disease-control-and-prevention
publisher_name: Centers for Disease Control and Prevention
service_category: API
slug: centers-for-disease-control-and-prevention-finops
source_filename: centers-for-disease-control-and-prevention-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Centers for Disease Control and Prevention\nproviderId: centers-for-disease-control-and-prevention\npublisherName: Centers for Disease Control and Prevention\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - CDC\n  - Environmental Health\n  - Epidemiology\n  - Federal Government\n  - Healthcare\n  - Open Data\n  - Public Health\n  - Socrata\n  - Surveillance\n  - WONDER\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Centers for Disease Control and Prevention API surface.\n  Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting\n  across the provider's APIs.\nprinciples:\n\
  \  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n\
  \      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Centers for Disease Control and Prevention\n  ServiceCategory: Developer Tools / API\n  ProviderName: Centers for Disease Control and Prevention\n  PublisherName: Centers for Disease Control and Prevention\n  InvoiceIssuerName: Centers for Disease Control and Prevention\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory:\
  \ Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CDC Socrata Open Data API (data.cdc.gov)\n    baseURL: https://data.cdc.gov/resource/\n    tags:\n      - Chronic Disease\n      - COVID-19\n      - Datasets\n      - Open Data\n      - SODA\n      - Socrata\n      - Surveillance\n    serviceName: CDC Socrata Open Data API (data.cdc.gov)\n    serviceCategory: API\n  - name: CDC WONDER API\n    baseURL: https://wonder.cdc.gov/controller/datarequest/\n\
  \    tags:\n      - Cancer\n      - Mortality\n      - Natality\n      - Query Database\n      - Statistics\n    serviceName: CDC WONDER API\n    serviceCategory: API\n  - name: CDC PLACES / 500 Cities API\n    baseURL: https://chronicdata.cdc.gov/resource/\n    tags:\n      - BRFSS\n      - Census Tract\n      - Chronic Disease\n      - Health Indicators\n      - Small Area Estimation\n    serviceName: CDC PLACES / 500 Cities API\n    serviceCategory: API\n  - name: CDC Environmental Public Health Tracking Network API\n    baseURL: https://ephtracking.cdc.gov:443/apigateway/api/v1\n    tags:\n      - Air Quality\n      - Environmental Health\n      - Exposure\n      - GIS\n      - Water Quality\n    serviceName: CDC Environmental Public Health Tracking Network API\n    serviceCategory: API\n  - name: CDC Public Health Media Library (Content Syndication)\n    baseURL: ''\n    tags:\n      - Content Syndication\n      - Health Content\n      - Media\n      - Multimedia\n    serviceName:\
  \ CDC Public Health Media Library (Content Syndication)\n    serviceCategory: API\n  - name: CDC Open Technology API Index\n    baseURL: ''\n    tags:\n      - Developer Portal\n      - Directory\n      - Open Technology\n    serviceName: CDC Open Technology API Index\n    serviceCategory: API\n  - name: CDC NNDSS / MMWR Socrata Data\n    baseURL: ''\n    tags:\n      - MMWR\n      - NNDSS\n      - Notifiable Disease\n      - Surveillance\n    serviceName: CDC NNDSS / MMWR Socrata Data\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/centers-for-disease-control-and-prevention/refs/heads/main/finops/centers-for-disease-control-and-prevention-finops.yml
sources: []
specification: FinOps Framework
tags:
- CDC
- Environmental Health
- Epidemiology
- Federal Government
- Healthcare
- Open Data
- Public Health
- Socrata
- Surveillance
- WONDER
- FinOps
- Cost Management
- FOCUS
---
