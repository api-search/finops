---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Xceptor REST API
  slug: ''
  spec_type: OpenAPI
  url: https://api.xceptor.com/v1/openapi.json
- filename: workflows
  format: yaml
  label: Xceptor Workflow API
  slug: ''
  spec_type: Postman
  url: https://www.postman.com/xceptor/workspace/workflows
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
description: FinOps framework definition for the Xceptor API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Xceptor
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Xceptor
  PublisherName: Xceptor
  ServiceCategory: Developer Tools / API
  ServiceName: Xceptor
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
name: Xceptor Finops
provider_name: Xceptor
provider_slug: xceptor
publisher_name: Xceptor
service_category: API
slug: xceptor-finops
source_filename: xceptor-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Xceptor\nproviderId: xceptor\npublisherName: Xceptor\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - API Integration\n  - Data Automation\n  - Data Extraction\n  - Document Processing\n  - ETL\n  - Financial Data\n  - Financial Services\n  - Intelligent Document Processing\n  - Reconciliations\n  - Trade Operations\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Xceptor API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering,\
  \ product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n\
  \      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Xceptor\n  ServiceCategory: Developer Tools / API\n  ProviderName: Xceptor\n  PublisherName: Xceptor\n  InvoiceIssuerName: Xceptor\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Xceptor REST API\n    baseURL: https://api.xceptor.com/v1\n    tags:\n      - Data Processing\n      - Documents\n      - REST\n      - Workflows\n    serviceName: Xceptor REST API\n    serviceCategory: API\n  - name: Xceptor Workflow API\n    baseURL: https://api.xceptor.com/v1/workflows\n    tags:\n      - Automation\n      - Orchestration\n      - Workflows\n    serviceName: Xceptor Workflow API\n    serviceCategory: API\n  - name: Xceptor Document Upload API\n    baseURL: https://api.xceptor.com/v1/documents\n    tags:\n      - Documents\n      - Extraction\n      - OCR\n\
  \      - Upload\n    serviceName: Xceptor Document Upload API\n    serviceCategory: API\n  - name: Xceptor Data Export API\n    baseURL: https://api.xceptor.com/v1/export\n    tags:\n      - Data\n      - Export\n      - Integration\n    serviceName: Xceptor Data Export API\n    serviceCategory: API\n  - name: Xceptor Connector API\n    baseURL: https://api.xceptor.com/v1\n    tags:\n      - Cloud\n      - Connectors\n      - Financial Data\n      - Integration\n      - SWIFT\n    serviceName: Xceptor Connector API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/xceptor/refs/heads/main/finops/xceptor-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Integration
- Data Automation
- Data Extraction
- Document Processing
- ETL
- Financial Data
- Financial Services
- Intelligent Document Processing
- Reconciliations
- Trade Operations
- FinOps
- Cost Management
- FOCUS
---
