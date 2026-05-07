---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: loadtestservice.json
  format: json
  label: Azure Load Testing API
  slug: azure-load-testing
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/loadtestservice/resource-manager/Microsoft.LoadTestService/stable/2022-12-01/loadtestservice.json
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
description: FinOps framework definition for the Scalability Testing API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Scalability Testing
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Scalability Testing
  PublisherName: Scalability Testing
  ServiceCategory: Developer Tools / API
  ServiceName: Scalability Testing
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
name: Scalability Testing Finops
provider_name: Scalability Testing
provider_slug: scalability-testing
publisher_name: Scalability Testing
service_category: API
slug: scalability-testing-finops
source_filename: scalability-testing-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Scalability Testing\nproviderId: scalability-testing\npublisherName: Scalability Testing\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - API Testing\n  - Load Testing\n  - Performance Testing\n  - Scalability\n  - Stress Testing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Scalability Testing API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Scalability Testing\n  ServiceCategory: Developer Tools / API\n  ProviderName: Scalability Testing\n  PublisherName: Scalability Testing\n  InvoiceIssuerName: Scalability Testing\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n  \
  \  description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Grafana k6 Cloud API\n    baseURL: https://api.k6.io/v3\n    tags:\n      - k6\n      - Load Testing\n      - Performance Testing\n    serviceName: Grafana k6 Cloud API\n    serviceCategory: API\n  - name: BlazeMeter API\n    baseURL: https://a.blazemeter.com/api/v4\n    tags:\n      - BlazeMeter\n      - JMeter\n      - Load Testing\n    serviceName: BlazeMeter API\n    serviceCategory: API\n  - name: Azure Load Testing API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.LoadTestService\n    tags:\n      - Azure\n      -\
  \ Cloud Load Testing\n      - JMeter\n      - Microsoft\n    serviceName: Azure Load Testing API\n    serviceCategory: API\n  - name: Apache JMeter\n    baseURL: ''\n    tags:\n      - Apache\n      - JMeter\n      - Load Testing\n      - Open Source\n    serviceName: Apache JMeter\n    serviceCategory: API\n  - name: Locust Load Testing\n    baseURL: http://localhost:8089\n    tags:\n      - Load Testing\n      - Locust\n      - Open Source\n      - Python\n    serviceName: Locust Load Testing\n    serviceCategory: API\n  - name: Gatling Load Testing\n    baseURL: ''\n    tags:\n      - Gatling\n      - Java\n      - Load Testing\n      - Open Source\n      - Scala\n    serviceName: Gatling Load Testing\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scalability-testing/refs/heads/main/finops/scalability-testing-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Testing
- Load Testing
- Performance Testing
- Scalability
- Stress Testing
- FinOps
- Cost Management
- FOCUS
---
