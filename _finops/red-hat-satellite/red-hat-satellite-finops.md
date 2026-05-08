---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: v2.json
  format: json
  label: Red Hat Satellite REST API
  slug: ''
  spec_type: OpenAPI
  url: https://satellite.example.com/apidoc/v2.json
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
description: FinOps framework definition for the Red Hat Satellite API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Red Hat Satellite
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Red Hat Satellite
  PublisherName: Red Hat Satellite
  ServiceCategory: Developer Tools / API
  ServiceName: Red Hat Satellite
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
name: Red Hat Satellite Finops
provider_name: Red Hat Satellite
provider_slug: red-hat-satellite
publisher_name: Red Hat Satellite
service_category: API
slug: red-hat-satellite-finops
source_filename: red-hat-satellite-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red Hat Satellite\nproviderId: red-hat-satellite\npublisherName: Red Hat Satellite\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Configuration Management\n  - Lifecycle Management\n  - Patch Management\n  - Subscription Management\n  - Systems Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Red Hat Satellite API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Red Hat Satellite\n  ServiceCategory: Developer Tools / API\n  ProviderName: Red Hat Satellite\n  PublisherName: Red Hat Satellite\n  InvoiceIssuerName: Red Hat Satellite\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Red Hat Satellite REST API\n    baseURL: https://satellite.example.com/api/v2\n    tags:\n      - Automation\n      - REST API\n      - Systems Management\n    serviceName: Red Hat Satellite REST API\n    serviceCategory: API\n  - name: Red Hat Satellite Hammer CLI\n    baseURL: ''\n    tags:\n      - Automation\n      - CLI\n      - Command Line\n    serviceName: Red Hat Satellite Hammer CLI\n    serviceCategory: API\n  - name: Red Hat Satellite Foreman API\n    baseURL: https://satellite.example.com/api\n    tags:\n      - Foreman\n      - Host Management\n      - Provisioning\n      - REST API\n\
  \    serviceName: Red Hat Satellite Foreman API\n    serviceCategory: API\n  - name: Red Hat Satellite Katello API\n    baseURL: https://satellite.example.com/katello/api\n    tags:\n      - Content Management\n      - Lifecycle Environments\n      - Repositories\n      - REST API\n      - Subscriptions\n    serviceName: Red Hat Satellite Katello API\n    serviceCategory: API\n  - name: Red Hat Satellite Ansible Collection\n    baseURL: ''\n    tags:\n      - Ansible\n      - Automation\n      - Configuration Management\n      - Infrastructure as Code\n    serviceName: Red Hat Satellite Ansible Collection\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/red-hat-satellite/refs/heads/main/finops/red-hat-satellite-finops.yml
sources: []
specification: FinOps Framework
tags:
- Configuration Management
- Lifecycle Management
- Patch Management
- Subscription Management
- Systems Management
- FinOps
- Cost Management
- FOCUS
---
