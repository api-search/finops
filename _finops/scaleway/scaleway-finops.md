---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: scaleway-instance-openapi.yml
  format: yaml
  label: Scaleway Instance API
  slug: scaleway-instance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-instance-openapi.yml
- filename: scaleway-kubernetes-openapi.yml
  format: yaml
  label: Scaleway Kubernetes API
  slug: scaleway-kubernetes-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-kubernetes-openapi.yml
- filename: scaleway-iam-openapi.yml
  format: yaml
  label: Scaleway IAM API
  slug: scaleway-iam-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-iam-openapi.yml
- filename: scaleway-load-balancer-openapi.yml
  format: yaml
  label: Scaleway Load Balancer API
  slug: scaleway-load-balancer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-load-balancer-openapi.yml
- filename: scaleway-database-openapi.yml
  format: yaml
  label: Scaleway Managed Database API
  slug: scaleway-database-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-database-openapi.yml
- filename: scaleway-vpc-openapi.yml
  format: yaml
  label: Scaleway VPC API
  slug: scaleway-vpc-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-vpc-openapi.yml
- filename: scaleway-serverless-containers-openapi.yml
  format: yaml
  label: Scaleway Serverless Containers API
  slug: scaleway-serverless-containers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-serverless-containers-openapi.yml
- filename: scaleway-serverless-functions-openapi.yml
  format: yaml
  label: Scaleway Serverless Functions API
  slug: scaleway-serverless-functions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-serverless-functions-openapi.yml
- filename: scaleway-secret-manager-openapi.yml
  format: yaml
  label: Scaleway Secret Manager API
  slug: scaleway-secret-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-secret-manager-openapi.yml
- filename: scaleway-transactional-email-openapi.yml
  format: yaml
  label: Scaleway Transactional Email API
  slug: scaleway-transactional-email-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-transactional-email-openapi.yml
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
description: FinOps framework definition for the Scaleway API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Scaleway
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Scaleway
  PublisherName: Scaleway
  ServiceCategory: Developer Tools / API
  ServiceName: Scaleway
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
name: Scaleway Finops
provider_name: Scaleway
provider_slug: scaleway
publisher_name: Scaleway
service_category: API
slug: scaleway-finops
source_filename: scaleway-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Scaleway\nproviderId: scaleway\npublisherName: Scaleway\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - Cloud Computing\n  - Containers\n  - Database\n  - European Cloud\n  - Infrastructure\n  - Kubernetes\n  - Serverless\n  - Storage\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Scaleway API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Scaleway\n  ServiceCategory: Developer Tools / API\n  ProviderName: Scaleway\n  PublisherName: Scaleway\n  InvoiceIssuerName: Scaleway\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Scaleway Instance API\n    baseURL: ''\n    tags:\n      - Compute\n      - Images\n      - Instances\n      - Security Groups\n      - Snapshots\n      - Virtual Machines\n    serviceName: Scaleway Instance API\n    serviceCategory: API\n  - name: Scaleway Kubernetes API\n    baseURL: ''\n    tags:\n      - Containers\n      - Kapsule\n      - Kubernetes\n      - Node Pools\n      - Orchestration\n    serviceName: Scaleway Kubernetes API\n    serviceCategory: API\n  - name: Scaleway IAM API\n    baseURL: ''\n    tags:\n      - Access Control\n      - API Keys\n      - Groups\n      - IAM\n      - Identity\n      - Permissions\n      - Policies\n\
  \    serviceName: Scaleway IAM API\n    serviceCategory: API\n  - name: Scaleway Load Balancer API\n    baseURL: ''\n    tags:\n      - Backend\n      - Health Checks\n      - Load Balancing\n      - Networking\n      - SSL\n    serviceName: Scaleway Load Balancer API\n    serviceCategory: API\n  - name: Scaleway Managed Database API\n    baseURL: ''\n    tags:\n      - Backup\n      - Database\n      - MySQL\n      - PostgreSQL\n      - Redis\n      - Relational Database\n    serviceName: Scaleway Managed Database API\n    serviceCategory: API\n  - name: Scaleway VPC API\n    baseURL: ''\n    tags:\n      - Network Isolation\n      - Networking\n      - Private Networks\n      - VPC\n      - Virtual Private Cloud\n    serviceName: Scaleway VPC API\n    serviceCategory: API\n  - name: Scaleway Serverless Containers API\n    baseURL: ''\n    tags:\n      - Containers\n      - CRON\n      - Docker\n      - Serverless\n    serviceName: Scaleway Serverless Containers API\n    serviceCategory:\
  \ API\n  - name: Scaleway Serverless Functions API\n    baseURL: ''\n    tags:\n      - Event-Driven\n      - FaaS\n      - Functions\n      - Serverless\n    serviceName: Scaleway Serverless Functions API\n    serviceCategory: API\n  - name: Scaleway Secret Manager API\n    baseURL: ''\n    tags:\n      - Certificates\n      - Credentials\n      - Secrets\n      - Security\n      - Vault\n    serviceName: Scaleway Secret Manager API\n    serviceCategory: API\n  - name: Scaleway Transactional Email API\n    baseURL: ''\n    tags:\n      - Email\n      - Messaging\n      - Notifications\n      - SMTP\n      - Transactional Email\n    serviceName: Scaleway Transactional Email API\n    serviceCategory: API\n  - name: Scaleway Generative APIs\n    baseURL: ''\n    tags:\n      - AI\n      - Artificial Intelligence\n      - Generative AI\n      - Language Models\n      - LLM\n    serviceName: Scaleway Generative APIs\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n\
  \    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/finops/scaleway-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- Cloud Computing
- Containers
- Database
- European Cloud
- Infrastructure
- Kubernetes
- Serverless
- Storage
- FinOps
- Cost Management
- FOCUS
---
