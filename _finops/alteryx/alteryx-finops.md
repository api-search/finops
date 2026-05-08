---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: alteryx-server-api-v3.yml
  format: yaml
  label: Alteryx Server API V3
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alteryx/refs/heads/main/openapi/alteryx-server-api-v3.yml
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
description: FinOps framework definition for the Alteryx API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Alteryx
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Alteryx
  PublisherName: Alteryx
  ServiceCategory: Developer Tools / API
  ServiceName: Alteryx
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
name: Alteryx Finops
provider_name: Alteryx
provider_slug: alteryx
publisher_name: Alteryx
service_category: API
slug: alteryx-finops
source_filename: alteryx-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Alteryx\nproviderId: alteryx\npublisherName: Alteryx\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Automation\n  - Data Engineering\n  - Data Preparation\n  - Data Science\n  - ETL\n  - Machine Learning\n  - Predictive Analytics\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Alteryx API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Alteryx\n  ServiceCategory: Developer Tools / API\n  ProviderName: Alteryx\n  PublisherName: Alteryx\n  InvoiceIssuerName: Alteryx\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in\
  \ API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Alteryx Server API\n    baseURL: https://your-server/webapi\n    tags:\n      - Automation\n      - Jobs\n      - Scheduling\n      - Server\n      - Workflows\n    serviceName: Alteryx Server API\n    serviceCategory: API\n  - name: Alteryx Server API V3\n    baseURL: https://your-server/webapi/v3\n    tags:\n      - Admin\n      - Credentials\n      - OAuth2\n      - Server\n      - Users\n      - Workflows\n    serviceName: Alteryx Server API V3\n    serviceCategory: API\n  - name: Alteryx Server API V1\n    baseURL: https://your-server/webapi/v1\n    tags:\n      - Admin\n      - Audit\n      - Migration\n      - Server\n    serviceName: Alteryx\
  \ Server API V1\n    serviceCategory: API\n  - name: Alteryx Gallery API\n    baseURL: https://gallery.alteryx.com/api\n    tags:\n      - Gallery\n      - Public API\n      - Sharing\n      - Workflows\n    serviceName: Alteryx Gallery API\n    serviceCategory: API\n  - name: Alteryx Connect API\n    baseURL: https://your-connect-server/api\n    tags:\n      - Collaboration\n      - Data Catalog\n      - Governance\n      - Metadata\n    serviceName: Alteryx Connect API\n    serviceCategory: API\n  - name: Alteryx AlteryxEngine API\n    baseURL: https://your-server/api\n    tags:\n      - Designer\n      - Engine\n      - Execution\n      - Workflows\n    serviceName: Alteryx AlteryxEngine API\n    serviceCategory: API\n  - name: Alteryx Designer Cloud API\n    baseURL: https://api.trifacta.com\n    tags:\n      - Cloud\n      - Data Preparation\n      - Pipelines\n      - Transformation\n      - Trifacta\n    serviceName: Alteryx Designer Cloud API\n    serviceCategory: API\nunitEconomics:\n\
  \  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://www.alteryx.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/alteryx/refs/heads/main/finops/alteryx-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Automation
- Data Engineering
- Data Preparation
- Data Science
- ETL
- Machine Learning
- Predictive Analytics
- FinOps
- Cost Management
- FOCUS
---
