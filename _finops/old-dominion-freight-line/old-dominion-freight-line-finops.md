---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: old-dominion-freight-line-bill-of-lading-api-openapi.yml
  format: yaml
  label: ODFL Bill of Lading API
  slug: bill-of-lading-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/old-dominion-freight-line/refs/heads/main/openapi/old-dominion-freight-line-bill-of-lading-api-openapi.yml
- filename: old-dominion-freight-line-pickup-api-openapi.yml
  format: yaml
  label: ODFL Pickup API
  slug: pickup-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/old-dominion-freight-line/refs/heads/main/openapi/old-dominion-freight-line-pickup-api-openapi.yml
- filename: old-dominion-freight-line-tracking-api-openapi.yml
  format: yaml
  label: ODFL Tracking API
  slug: tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/old-dominion-freight-line/refs/heads/main/openapi/old-dominion-freight-line-tracking-api-openapi.yml
- filename: old-dominion-freight-line-document-api-openapi.yml
  format: yaml
  label: ODFL Document API
  slug: document-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/old-dominion-freight-line/refs/heads/main/openapi/old-dominion-freight-line-document-api-openapi.yml
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
description: FinOps framework definition for the Old Dominion Freight Line API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Old Dominion Freight Line
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Old Dominion Freight Line
  PublisherName: Old Dominion Freight Line
  ServiceCategory: Developer Tools / API
  ServiceName: Old Dominion Freight Line
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
name: Old Dominion Freight Line Finops
provider_name: Old Dominion Freight Line
provider_slug: old-dominion-freight-line
publisher_name: Old Dominion Freight Line
service_category: API
slug: old-dominion-freight-line-finops
source_filename: old-dominion-freight-line-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Old Dominion Freight Line\nproviderId: old-dominion-freight-line\npublisherName: Old Dominion Freight Line\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Freight\n  - Less-Than-Truckload\n  - Logistics\n  - Shipping\n  - Transportation\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Old Dominion Freight Line API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  -\
  \ name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n\
  \  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Old Dominion Freight Line\n  ServiceCategory: Developer Tools / API\n  ProviderName: Old Dominion Freight Line\n  PublisherName: Old Dominion Freight Line\n  InvoiceIssuerName: Old Dominion Freight Line\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n   \
  \   - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: ODFL Bill of Lading API\n    baseURL: https://www.odfl.com\n    tags:\n      - Bill of Lading\n      - Documents\n      - Freight\n      - Shipping\n    serviceName: ODFL Bill of Lading API\n    serviceCategory: API\n  - name: ODFL Pickup API\n    baseURL: https://www.odfl.com\n    tags:\n      - Freight\n      - Logistics\n      - Pickup\n      - Shipping\n    serviceName: ODFL Pickup API\n    serviceCategory: API\n  - name: ODFL Tracking API\n    baseURL: https://www.odfl.com\n    tags:\n      - Freight\n      - Shipping\n      - Tracking\n    serviceName: ODFL\
  \ Tracking API\n    serviceCategory: API\n  - name: ODFL Document API\n    baseURL: https://www.odfl.com\n    tags:\n      - Documents\n      - Freight\n      - Shipping\n    serviceName: ODFL Document API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/old-dominion-freight-line/refs/heads/main/finops/old-dominion-freight-line-finops.yml
sources: []
specification: FinOps Framework
tags:
- Freight
- Less-Than-Truckload
- Logistics
- Shipping
- Transportation
- FinOps
- Cost Management
- FOCUS
---
