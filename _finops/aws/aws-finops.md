---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Amazon EC2
  slug: amazon-ec2
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/ec2/2016-11-15/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon S3
  slug: amazon-s3
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/s3/2006-03-01/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon Lambda
  slug: amazon-lambda
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/lambda/2015-03-31/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon DynamoDB
  slug: amazon-dynamodb
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/dynamodb/2012-08-10/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon RDS
  slug: amazon-rds
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/rds/2014-10-31/openapi.yaml
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
description: FinOps framework definition for the Amazon Web Services (AWS) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Web Services (AWS)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Amazon Web Services (AWS)
  PublisherName: Amazon Web Services (AWS)
  ServiceCategory: Developer Tools / API
  ServiceName: Amazon Web Services (AWS)
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
name: Aws Finops
provider_name: Amazon Web Services (AWS)
provider_slug: aws
publisher_name: Amazon Web Services (AWS)
service_category: API
slug: aws-finops
source_filename: aws-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Amazon Web Services (AWS)\nproviderId: aws\npublisherName: Amazon Web Services (AWS)\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Computing\n  - IaaS\n  - Infrastructure\n  - PaaS\n  - Platform as a Service\n  - Serverless\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Amazon Web Services (AWS) API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Amazon Web Services (AWS)\n  ServiceCategory: Developer Tools / API\n  ProviderName: Amazon Web Services (AWS)\n  PublisherName: Amazon Web Services (AWS)\n  InvoiceIssuerName: Amazon Web Services (AWS)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      -\
  \ consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Amazon EC2\n    baseURL: https://ec2.amazonaws.com\n    tags:\n      - Compute\n      - Infrastructure\n      - Virtual Machines\n    serviceName: Amazon EC2\n    serviceCategory: API\n  - name: Amazon S3\n    baseURL: https://s3.amazonaws.com\n    tags:\n      - Data Lake\n      - Object Storage\n      - Storage\n    serviceName: Amazon S3\n    serviceCategory: API\n  - name: Amazon Lambda\n    baseURL: https://lambda.amazonaws.com\n    tags:\n      - Compute\n      - Functions\n      - Serverless\n    serviceName: Amazon Lambda\n    serviceCategory: API\n  - name:\
  \ Amazon DynamoDB\n    baseURL: https://dynamodb.amazonaws.com\n    tags:\n      - Database\n      - Key-Value\n      - NoSQL\n    serviceName: Amazon DynamoDB\n    serviceCategory: API\n  - name: Amazon RDS\n    baseURL: https://rds.amazonaws.com\n    tags:\n      - Database\n      - Managed Service\n      - Relational\n    serviceName: Amazon RDS\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aws/refs/heads/main/finops/aws-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Computing
- IaaS
- Infrastructure
- PaaS
- Platform as a Service
- Serverless
- FinOps
- Cost Management
- FOCUS
---
