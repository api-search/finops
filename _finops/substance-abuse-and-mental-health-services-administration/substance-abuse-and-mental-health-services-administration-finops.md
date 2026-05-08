---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: samhsa-treatment-locator-openapi.yml
  format: yaml
  label: SAMHSA Behavioral Health Treatment Services Locator API
  slug: samhsa-treatment-locator-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/substance-abuse-and-mental-health-services-administration/refs/heads/main/openapi/samhsa-treatment-locator-openapi.yml
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
description: FinOps framework definition for the Substance Abuse and Mental Health Services Administration API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Substance Abuse and Mental Health Services Administration
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Substance Abuse and Mental Health Services Administration
  PublisherName: Substance Abuse and Mental Health Services Administration
  ServiceCategory: Developer Tools / API
  ServiceName: Substance Abuse and Mental Health Services Administration
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
name: Substance Abuse And Mental Health Services Administration Finops
provider_name: Substance Abuse and Mental Health Services Administration
provider_slug: substance-abuse-and-mental-health-services-administration
publisher_name: Substance Abuse and Mental Health Services Administration
service_category: API
slug: substance-abuse-and-mental-health-services-administration-finops
source_filename: substance-abuse-and-mental-health-services-administration-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Substance Abuse and Mental Health Services Administration\nproviderId: substance-abuse-and-mental-health-services-administration\npublisherName: Substance Abuse and Mental Health Services Administration\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Federal Government\n  - Public Health\n  - Behavioral Health\n  - Substance Use Disorders\n  - Mental Health\n  - Open Data\n  - Healthcare\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Substance Abuse and Mental Health Services Administration\n  API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics\n  reporting\
  \ across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name:\
  \ Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Substance Abuse and Mental Health Services Administration\n  ServiceCategory: Developer Tools / API\n  ProviderName: Substance Abuse and Mental Health Services Administration\n  PublisherName: Substance Abuse and Mental Health Services Administration\n  InvoiceIssuerName: Substance Abuse and Mental Health Services Administration\n\
  \  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SAMHSA Behavioral Health Treatment Services Locator API\n    baseURL: ''\n    tags:\n      - Treatment Facilities\n      - Behavioral Health\n      - Substance Use Disorders\n      - Mental Health\n      - Open Data\n    serviceName: SAMHSA Behavioral Health\
  \ Treatment Services Locator API\n    serviceCategory: API\n  - name: SAMHSA Data Portal\n    baseURL: ''\n    tags:\n      - Open Data\n      - Survey Data\n      - NSDUH\n      - Statistics\n      - Public Health\n    serviceName: SAMHSA Data Portal\n    serviceCategory: API\n  - name: SAMHSA Mental Health Client Level Data\n    baseURL: ''\n    tags:\n      - Mental Health\n      - Client Data\n      - Statistics\n      - Open Data\n    serviceName: SAMHSA Mental Health Client Level Data\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/substance-abuse-and-mental-health-services-administration/refs/heads/main/finops/substance-abuse-and-mental-health-services-administration-finops.yml
sources: []
specification: FinOps Framework
tags:
- Federal Government
- Public Health
- Behavioral Health
- Substance Use Disorders
- Mental Health
- Open Data
- Healthcare
- FinOps
- Cost Management
- FOCUS
---
