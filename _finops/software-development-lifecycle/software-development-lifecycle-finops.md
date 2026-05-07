---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: api.github.com.json
  format: json
  label: Code and Review APIs
  slug: code-and-review
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
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
description: FinOps framework definition for the Software Development Lifecycle API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Software Development Lifecycle
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Software Development Lifecycle
  PublisherName: Software Development Lifecycle
  ServiceCategory: Developer Tools / API
  ServiceName: Software Development Lifecycle
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
name: Software Development Lifecycle Finops
provider_name: Software Development Lifecycle
provider_slug: software-development-lifecycle
publisher_name: Software Development Lifecycle
service_category: API
slug: software-development-lifecycle-finops
source_filename: software-development-lifecycle-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Software Development Lifecycle\nproviderId: software-development-lifecycle\npublisherName: Software Development Lifecycle\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Development Process\n  - Project Management\n  - Quality Assurance\n  - Software Engineering\n  - DevOps\n  - Platform Engineering\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Software Development Lifecycle API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to\
  \ engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload\
  \ Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Software Development Lifecycle\n  ServiceCategory: Developer Tools / API\n  ProviderName: Software Development Lifecycle\n  PublisherName: Software Development Lifecycle\n  InvoiceIssuerName: Software Development Lifecycle\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Planning and Tracking APIs\n    baseURL: https://en.wikipedia.org/wiki/Software_project_management\n    tags:\n      - Agile Planning\n      - Backlog Management\n      - Sprint Tracking\n      - Roadmapping\n    serviceName: Planning and Tracking APIs\n    serviceCategory: API\n  - name: Code and Review APIs\n    baseURL: https://api.github.com\n    tags:\n      - Source Control\n      - Code Review\n      - Version Control\n      - Collaboration\n    serviceName: Code and Review\
  \ APIs\n    serviceCategory: API\n  - name: Build and Test APIs\n    baseURL: https://en.wikipedia.org/wiki/Build_automation\n    tags:\n      - Build Automation\n      - Testing\n      - Code Coverage\n      - Quality Gates\n    serviceName: Build and Test APIs\n    serviceCategory: API\n  - name: Security Scanning APIs\n    baseURL: https://en.wikipedia.org/wiki/Static_application_security_testing\n    tags:\n      - SAST\n      - DAST\n      - Security Scanning\n      - DevSecOps\n      - SCA\n    serviceName: Security Scanning APIs\n    serviceCategory: API\n  - name: Deployment and Release APIs\n    baseURL: https://en.wikipedia.org/wiki/CI/CD\n    tags:\n      - CI/CD\n      - Deployment\n      - Infrastructure as Code\n      - Feature Flags\n      - Progressive Delivery\n    serviceName: Deployment and Release APIs\n    serviceCategory: API\n  - name: Monitoring and Observability APIs\n    baseURL: https://en.wikipedia.org/wiki/Observability_(software)\n    tags:\n      - Monitoring\n\
  \      - Observability\n      - APM\n      - Log Management\n      - Tracing\n    serviceName: Monitoring and Observability APIs\n    serviceCategory: API\n  - name: Developer Platform APIs\n    baseURL: https://internaldeveloperplatform.org/\n    tags:\n      - Developer Platform\n      - Internal Developer Portal\n      - Service Catalog\n      - Platform Engineering\n    serviceName: Developer Platform APIs\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/software-development-lifecycle/refs/heads/main/finops/software-development-lifecycle-finops.yml
sources: []
specification: FinOps Framework
tags:
- Development Process
- Project Management
- Quality Assurance
- Software Engineering
- DevOps
- Platform Engineering
- FinOps
- Cost Management
- FOCUS
---
