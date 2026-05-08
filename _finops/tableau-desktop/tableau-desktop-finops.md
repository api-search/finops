---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tableau-desktop-openapi.yml
  format: yaml
  label: Tableau REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tableau-desktop/refs/heads/main/openapi/tableau-desktop-openapi.yml
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
description: FinOps framework definition for the Tableau Desktop API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Tableau Desktop
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Tableau Desktop
  PublisherName: Tableau Desktop
  ServiceCategory: Developer Tools / API
  ServiceName: Tableau Desktop
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
name: Tableau Desktop Finops
provider_name: Tableau Desktop
provider_slug: tableau-desktop
publisher_name: Tableau Desktop
service_category: API
slug: tableau-desktop-finops
source_filename: tableau-desktop-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Tableau Desktop\nproviderId: tableau-desktop\npublisherName: Tableau Desktop\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Analytics\n  - Business Intelligence\n  - Data Visualization\n  - Desktop Application\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Tableau Desktop API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Tableau Desktop\n  ServiceCategory: Developer Tools / API\n  ProviderName: Tableau Desktop\n  PublisherName: Tableau Desktop\n  InvoiceIssuerName: Tableau Desktop\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the\
  \ network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Tableau REST API\n    baseURL: https://tableau-server/api/3.22\n    tags:\n      - Cloud\n      - Publishing\n      - REST\n      - Server\n      - Workbooks\n    serviceName: Tableau REST API\n    serviceCategory: API\n  - name: Tableau Extensions API\n    baseURL: https://tableau.github.io/extensions-api/\n    tags:\n      - Dashboard\n      - Extensions\n      - JavaScript\n      - Web Components\n    serviceName: Tableau Extensions API\n    serviceCategory: API\n  - name: Tableau Hyper API\n    baseURL: https://tableau.github.io/hyper-db/\n    tags:\n      - Data Extract\n      - Database\n      - ETL\n      - Hyper\n      - SQL\n   \
  \ serviceName: Tableau Hyper API\n    serviceCategory: API\n  - name: Tableau Embedding API\n    baseURL: https://help.tableau.com/current/api/embedding_api/\n    tags:\n      - Embedding\n      - Integration\n      - JavaScript\n      - Web Components\n    serviceName: Tableau Embedding API\n    serviceCategory: API\n  - name: Tableau Metadata API\n    baseURL: https://help.tableau.com/current/api/metadata_api/\n    tags:\n      - Data Governance\n      - GraphQL\n      - Lineage\n      - Metadata\n    serviceName: Tableau Metadata API\n    serviceCategory: API\n  - name: Tableau Server Client (Python)\n    baseURL: https://tableau.github.io/server-client-python/\n    tags:\n      - Automation\n      - Python\n      - REST API\n      - Server\n    serviceName: Tableau Server Client (Python)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost\
  \ / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tableau-desktop/refs/heads/main/finops/tableau-desktop-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- Data Visualization
- Desktop Application
- FinOps
- Cost Management
- FOCUS
---
