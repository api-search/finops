---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: checkpoint-management-api-openapi.yml
  format: yaml
  label: Check Point Management API
  slug: management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-management-api-openapi.yml
- filename: checkpoint-gaia-api-openapi.yml
  format: yaml
  label: Check Point Gaia API
  slug: gaia-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-gaia-api-openapi.yml
- filename: checkpoint-cloudguard-api-openapi.yml
  format: yaml
  label: Check Point CloudGuard API
  slug: cloudguard-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-cloudguard-api-openapi.yml
- filename: checkpoint-identity-awareness-api-openapi.yml
  format: yaml
  label: Check Point Identity Awareness API
  slug: identity-awareness-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-identity-awareness-api-openapi.yml
- filename: checkpoint-harmony-email-api-openapi.yml
  format: yaml
  label: Check Point Harmony Email API
  slug: harmony-email-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-harmony-email-api-openapi.yml
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
description: FinOps framework definition for the Check Point API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Check Point
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Check Point
  PublisherName: Check Point
  ServiceCategory: Developer Tools / API
  ServiceName: Check Point
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
name: Checkpoint Finops
provider_name: Check Point
provider_slug: checkpoint
publisher_name: Check Point
service_category: API
slug: checkpoint-finops
source_filename: checkpoint-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Check Point\nproviderId: checkpoint\npublisherName: Check Point\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Security\n  - Cybersecurity\n  - Endpoint Security\n  - Firewall\n  - Identity Awareness\n  - Mobile Security\n  - Network Security\n  - Security\n  - Threat Prevention\n  - WAF\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Check Point API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Check Point\n  ServiceCategory: Developer Tools / API\n  ProviderName: Check Point\n  PublisherName: Check Point\n  InvoiceIssuerName: Check Point\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Check Point Management API\n    baseURL: https://management.example.com/web_api\n    tags:\n      - Firewall\n      - Management\n      - Network Security\n    serviceName: Check Point Management API\n    serviceCategory: API\n  - name: Check Point Gaia API\n    baseURL: https://gateway.example.com/gaia_api\n    tags:\n      - Gaia\n      - Operating System\n    serviceName: Check Point Gaia API\n    serviceCategory: API\n  - name: Check Point CloudGuard API\n    baseURL: https://api.dome9.com/v2\n    tags:\n      - Cloud Security\n      - Compliance\n      - Posture Management\n\
  \    serviceName: Check Point CloudGuard API\n    serviceCategory: API\n  - name: Check Point Identity Awareness API\n    baseURL: https://gateway.example.com/_IA_MU_Agent\n    tags:\n      - Identity\n      - Network Security\n    serviceName: Check Point Identity Awareness API\n    serviceCategory: API\n  - name: Check Point Spark Management API\n    baseURL: ''\n    tags:\n      - SMB\n      - Spark\n    serviceName: Check Point Spark Management API\n    serviceCategory: API\n  - name: Check Point Zero Touch API\n    baseURL: ''\n    tags:\n      - Deployment\n      - Zero Touch\n    serviceName: Check Point Zero Touch API\n    serviceCategory: API\n  - name: Check Point Harmony Email API\n    baseURL: https://smart-api.avanan.net/v2.0\n    tags:\n      - Email Security\n      - Harmony\n    serviceName: Check Point Harmony Email API\n    serviceCategory: API\n  - name: Check Point Threat Hunting API\n    baseURL: ''\n    tags:\n      - Threat Hunting\n      - Threat Intelligence\n\
  \    serviceName: Check Point Threat Hunting API\n    serviceCategory: API\n  - name: Check Point CloudGuard WAF API\n    baseURL: ''\n    tags:\n      - WAF\n      - Web Security\n    serviceName: Check Point CloudGuard WAF API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/finops/checkpoint-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Security
- Cybersecurity
- Endpoint Security
- Firewall
- Identity Awareness
- Mobile Security
- Network Security
- Security
- Threat Prevention
- WAF
- FinOps
- Cost Management
- FOCUS
---
