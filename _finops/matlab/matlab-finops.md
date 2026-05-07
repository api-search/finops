---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi-productionserver
  format: yaml
  label: MATLAB Production Server RESTful API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/mathworks-ref-arch/openapi-productionserver
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
description: FinOps framework definition for the MATLAB API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: MATLAB
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: MATLAB
  PublisherName: MATLAB
  ServiceCategory: Developer Tools / API
  ServiceName: MATLAB
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
name: Matlab Finops
provider_name: MATLAB
provider_slug: matlab
publisher_name: MATLAB
service_category: API
slug: matlab-finops
source_filename: matlab-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: MATLAB\nproviderId: matlab\npublisherName: MATLAB\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Data Analysis\n  - Engineering\n  - Machine Learning\n  - Numerical Analysis\n  - Scientific Computing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the MATLAB API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: MATLAB\n  ServiceCategory: Developer Tools / API\n  ProviderName: MATLAB\n  PublisherName: MATLAB\n  InvoiceIssuerName: MATLAB\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: MATLAB Engine API for Python\n    baseURL: https://www.mathworks.com/help/matlab/apiref\n    tags:\n      - Engine\n      - Integration\n      - Python\n    serviceName: MATLAB Engine API for Python\n    serviceCategory: API\n  - name: MATLAB Engine API for Java\n    baseURL: https://www.mathworks.com/help/matlab/apiref\n    tags:\n      - Engine\n      - Integration\n      - Java\n    serviceName: MATLAB Engine API for Java\n    serviceCategory: API\n  - name: MATLAB Engine API for C++\n    baseURL: https://www.mathworks.com/help/matlab/apiref\n    tags:\n      - C++\n      - Engine\n      - Integration\n    serviceName: MATLAB Engine API for C++\n    serviceCategory: API\n  - name: MATLAB Engine\
  \ API for C and Fortran\n    baseURL: https://www.mathworks.com/help/matlab/apiref\n    tags:\n      - C\n      - Engine\n      - Fortran\n      - Integration\n    serviceName: MATLAB Engine API for C and Fortran\n    serviceCategory: API\n  - name: MATLAB Engine API for .NET\n    baseURL: https://www.mathworks.com/help/matlab/apiref\n    tags:\n      - .NET\n      - Engine\n      - Integration\n    serviceName: MATLAB Engine API for .NET\n    serviceCategory: API\n  - name: MATLAB RESTful Web Services\n    baseURL: https://www.mathworks.com/products/matlab-production-server.html\n    tags:\n      - Production\n      - REST\n      - Web Services\n    serviceName: MATLAB RESTful Web Services\n    serviceCategory: API\n  - name: MATLAB Production Server RESTful API\n    baseURL: https://www.mathworks.com/help/mps\n    tags:\n      - Deployment\n      - Enterprise\n      - Production Server\n      - REST\n    serviceName: MATLAB Production Server RESTful API\n    serviceCategory: API\n  -\
  \ name: MATLAB Web App Server\n    baseURL: https://www.mathworks.com/help/webappserver\n    tags:\n      - Deployment\n      - Server\n      - Web Apps\n    serviceName: MATLAB Web App Server\n    serviceCategory: API\n  - name: MATLAB Data API for C++\n    baseURL: https://www.mathworks.com/help/matlab/apiref\n    tags:\n      - C++\n      - Data\n      - Types\n    serviceName: MATLAB Data API for C++\n    serviceCategory: API\n  - name: MATLAB HTTP Interface\n    baseURL: https://www.mathworks.com/help/matlab\n    tags:\n      - Client\n      - HTTP\n      - REST\n    serviceName: MATLAB HTTP Interface\n    serviceCategory: API\n  - name: MATLAB MEX API\n    baseURL: https://www.mathworks.com/help/matlab/apiref\n    tags:\n      - C\n      - C++\n      - Extensions\n      - Fortran\n      - MEX\n    serviceName: MATLAB MEX API\n    serviceCategory: API\n  - name: MATLAB Compiler SDK API\n    baseURL: https://www.mathworks.com/help/compiler_sdk\n    tags:\n      - Compiler\n      -\
  \ Deployment\n      - Integration\n      - SDK\n    serviceName: MATLAB Compiler SDK API\n    serviceCategory: API\n  - name: ThingSpeak REST API\n    baseURL: https://api.thingspeak.com\n    tags:\n      - Analytics\n      - Channels\n      - IoT\n      - REST\n    serviceName: ThingSpeak REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/matlab/refs/heads/main/finops/matlab-finops.yml
sources: []
specification: FinOps Framework
tags:
- Data Analysis
- Engineering
- Machine Learning
- Numerical Analysis
- Scientific Computing
- FinOps
- Cost Management
- FOCUS
---
