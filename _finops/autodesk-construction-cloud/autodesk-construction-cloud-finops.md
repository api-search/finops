---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: acc-admin-openapi.yml
  format: yaml
  label: Autodesk Construction Cloud Admin API
  slug: acc-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/openapi/acc-admin-openapi.yml
- filename: acc-issues-openapi.yml
  format: yaml
  label: Autodesk Construction Cloud Issues API
  slug: acc-issues-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/openapi/acc-issues-openapi.yml
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
description: FinOps framework definition for the Autodesk Construction Cloud API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Autodesk Construction Cloud
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Autodesk Construction Cloud
  PublisherName: Autodesk Construction Cloud
  ServiceCategory: Developer Tools / API
  ServiceName: Autodesk Construction Cloud
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
name: Autodesk Construction Cloud Finops
provider_name: Autodesk Construction Cloud
provider_slug: autodesk-construction-cloud
publisher_name: Autodesk Construction Cloud
service_category: API
slug: autodesk-construction-cloud-finops
source_filename: autodesk-construction-cloud-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Autodesk Construction Cloud\nproviderId: autodesk-construction-cloud\npublisherName: Autodesk Construction Cloud\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Construction\n  - BIM\n  - Project Management\n  - AEC\n  - CAD\n  - Architecture\n  - Engineering\n  - Field Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Autodesk Construction Cloud API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Autodesk Construction Cloud\n  ServiceCategory: Developer Tools / API\n  ProviderName: Autodesk Construction Cloud\n  PublisherName: Autodesk Construction Cloud\n  InvoiceIssuerName: Autodesk Construction Cloud\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n\
  \      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Autodesk Construction Cloud Admin API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - ACC\n      - Administration\n      - BIM\n      - Construction\n      - Project Management\n    serviceName: Autodesk Construction Cloud Admin API\n    serviceCategory: API\n  - name: Autodesk Construction Cloud Issues API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - BIM\n      - Construction\n      - Field Management\n      - Issues\n      - Quality\n    serviceName: Autodesk Construction\
  \ Cloud Issues API\n    serviceCategory: API\n  - name: Autodesk Construction Cloud Cost Management API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - ACC\n      - Budget\n      - Construction\n      - Contracts\n      - Cost Management\n    serviceName: Autodesk Construction Cloud Cost Management API\n    serviceCategory: API\n  - name: Autodesk Construction Cloud Model Coordination API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - BIM\n      - Clash Detection\n      - Construction\n      - IFC\n      - Model Coordination\n    serviceName: Autodesk Construction Cloud Model Coordination API\n    serviceCategory: API\n  - name: Autodesk Construction Cloud RFIs API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - ACC\n      - Construction\n      - Document Management\n      - RFI\n    serviceName: Autodesk Construction Cloud RFIs API\n    serviceCategory: API\n  - name: Autodesk Construction Cloud Submittals API\n    baseURL:\
  \ https://developer.api.autodesk.com\n    tags:\n      - ACC\n      - Construction\n      - Document Management\n      - Submittals\n    serviceName: Autodesk Construction Cloud Submittals API\n    serviceCategory: API\n  - name: Autodesk Construction Cloud Data Connector API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - ACC\n      - Analytics\n      - Construction\n      - Data Export\n    serviceName: Autodesk Construction Cloud Data Connector API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/finops/autodesk-construction-cloud-finops.yml
sources: []
specification: FinOps Framework
tags:
- Construction
- BIM
- Project Management
- AEC
- CAD
- Architecture
- Engineering
- Field Management
- FinOps
- Cost Management
- FOCUS
---
