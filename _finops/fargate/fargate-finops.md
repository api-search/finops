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
  label: Amazon ECS API (Fargate)
  slug: amazon-ecs-api-fargate
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/ecs/2014-11-13/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon EKS API (Fargate)
  slug: amazon-eks-api-fargate
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/eks/2017-11-01/openapi.yaml
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
description: FinOps framework definition for the AWS Fargate API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: AWS Fargate
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: AWS Fargate
  PublisherName: AWS Fargate
  ServiceCategory: Developer Tools / API
  ServiceName: AWS Fargate
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
name: Fargate Finops
provider_name: AWS Fargate
provider_slug: fargate
publisher_name: AWS Fargate
service_category: API
slug: fargate-finops
source_filename: fargate-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: AWS Fargate\nproviderId: fargate\npublisherName: AWS Fargate\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Compute\n  - Containers\n  - Docker\n  - Kubernetes\n  - Serverless\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the AWS Fargate API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the\
  \ consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: AWS Fargate\n  ServiceCategory: Developer Tools / API\n  ProviderName: AWS Fargate\n  PublisherName: AWS Fargate\n  InvoiceIssuerName: AWS Fargate\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Amazon ECS API (Fargate)\n    baseURL: https://ecs.{region}.amazonaws.com\n    tags:\n      - Containers\n      - ECS\n      - Fargate\n      - Orchestration\n      - Serverless\n    serviceName: Amazon ECS API (Fargate)\n    serviceCategory: API\n  - name: Amazon EKS API (Fargate)\n    baseURL: https://eks.{region}.amazonaws.com\n    tags:\n      - Containers\n      - EKS\n      - Fargate\n      - Kubernetes\n      - Serverless\n    serviceName: Amazon EKS API (Fargate)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target:\
  \ TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fargate/refs/heads/main/finops/fargate-finops.yml
sources: []
specification: FinOps Framework
tags:
- Compute
- Containers
- Docker
- Kubernetes
- Serverless
- FinOps
- Cost Management
- FOCUS
---
