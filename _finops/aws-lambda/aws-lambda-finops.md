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
  label: AWS Lambda API
  slug: aws-lambda-api
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/lambda/2015-03-31/openapi.json
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
description: FinOps framework definition for the AWS Lambda API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: AWS Lambda
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: AWS Lambda
  PublisherName: AWS Lambda
  ServiceCategory: Developer Tools / API
  ServiceName: AWS Lambda
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
name: Aws Lambda Finops
provider_name: AWS Lambda
provider_slug: aws-lambda
publisher_name: AWS Lambda
service_category: API
slug: aws-lambda-finops
source_filename: aws-lambda-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: AWS Lambda\nproviderId: aws-lambda\npublisherName: AWS Lambda\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the AWS Lambda API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can\
  \ be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing\
  \ and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: AWS Lambda\n  ServiceCategory: Developer Tools / API\n  ProviderName: AWS Lambda\n  PublisherName: AWS Lambda\n  InvoiceIssuerName: AWS Lambda\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name:\
  \ compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: AWS Lambda API\n    baseURL: https://lambda.{region}.amazonaws.com\n    tags:\n      - Compute\n      - Event-Driven\n      - FaaS\n      - Functions\n      - Serverless\n    serviceName: AWS Lambda API\n    serviceCategory: API\n  - name: AWS Lambda Extensions API\n    baseURL: https://lambda.{region}.amazonaws.com\n    tags:\n      - Extensions\n      - Monitoring\n      - Observability\n      - Serverless\n    serviceName: AWS Lambda Extensions API\n    serviceCategory: API\n  - name: AWS Lambda Telemetry API\n    baseURL: https://lambda.{region}.amazonaws.com\n    tags:\n      - Logging\n      - Monitoring\n      - Observability\n      - Serverless\n      - Telemetry\n    serviceName: AWS Lambda Telemetry API\n    serviceCategory: API\n  - name: AWS Lambda Runtime API\n\
  \    baseURL: https://lambda.{region}.amazonaws.com\n    tags:\n      - Custom Runtime\n      - Functions\n      - Runtime\n      - Serverless\n    serviceName: AWS Lambda Runtime API\n    serviceCategory: API\n  - name: AWS Lambda Logs API\n    baseURL: https://lambda.{region}.amazonaws.com\n    tags:\n      - Logging\n      - Monitoring\n      - Serverless\n    serviceName: AWS Lambda Logs API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aws-lambda/refs/heads/main/finops/aws-lambda-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
