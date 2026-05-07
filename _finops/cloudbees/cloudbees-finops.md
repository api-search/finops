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
description: FinOps framework definition for the CloudBees API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CloudBees
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: CloudBees
  PublisherName: CloudBees
  ServiceCategory: Developer Tools / API
  ServiceName: CloudBees
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
name: Cloudbees Finops
provider_name: CloudBees
provider_slug: cloudbees
publisher_name: CloudBees
service_category: API
slug: cloudbees-finops
source_filename: cloudbees-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CloudBees\nproviderId: cloudbees\npublisherName: CloudBees\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - CI/CD\n  - Continuous Delivery\n  - Continuous Integration\n  - DevOps\n  - Feature Flags\n  - Feature Management\n  - Jenkins\n  - Release Orchestration\n  - Software Delivery\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the CloudBees API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams\
  \ in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CloudBees\n  ServiceCategory: Developer Tools / API\n  ProviderName: CloudBees\n  PublisherName: CloudBees\n  InvoiceIssuerName: CloudBees\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CloudBees CI REST API\n    baseURL: https://example.cloudbees.com\n    tags:\n      - CI/CD\n      - Continuous Integration\n      - Jenkins\n      - Pipelines\n    serviceName: CloudBees CI REST API\n    serviceCategory: API\n  - name: CloudBees CD/RO REST API\n    baseURL: https://example-cd.cloudbees.com/rest/v1.0\n    tags:\n      - Continuous Delivery\n      - DevOps\n      - Pipelines\n      - Release Orchestration\n    serviceName: CloudBees CD/RO REST API\n    serviceCategory: API\n  - name: CloudBees Feature Management REST API\n    baseURL: https://x-api.rollout.io/public-api\n    tags:\n\
  \      - Experimentation\n      - Feature Flags\n      - Feature Management\n    serviceName: CloudBees Feature Management REST API\n    serviceCategory: API\n  - name: CloudBees Unify Platform API\n    baseURL: ''\n    tags:\n      - DevOps\n      - Platform\n      - Software Delivery\n    serviceName: CloudBees Unify Platform API\n    serviceCategory: API\n  - name: CloudBees CD/RO Jenkins Plugin Steps\n    baseURL: ''\n    tags:\n      - Continuous Delivery\n      - Jenkins\n      - Plugin\n    serviceName: CloudBees CD/RO Jenkins Plugin Steps\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudbees/refs/heads/main/finops/cloudbees-finops.yml
sources: []
specification: FinOps Framework
tags:
- CI/CD
- Continuous Delivery
- Continuous Integration
- DevOps
- Feature Flags
- Feature Management
- Jenkins
- Release Orchestration
- Software Delivery
- FinOps
- Cost Management
- FOCUS
---
