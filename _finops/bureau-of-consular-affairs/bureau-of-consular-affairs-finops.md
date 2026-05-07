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
description: FinOps framework definition for the Bureau of Consular Affairs API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Bureau of Consular Affairs
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Bureau of Consular Affairs
  PublisherName: Bureau of Consular Affairs
  ServiceCategory: Developer Tools / API
  ServiceName: Bureau of Consular Affairs
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
name: Bureau Of Consular Affairs Finops
provider_name: Bureau of Consular Affairs
provider_slug: bureau-of-consular-affairs
publisher_name: Bureau of Consular Affairs
service_category: API
slug: bureau-of-consular-affairs-finops
source_filename: bureau-of-consular-affairs-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Bureau of Consular Affairs\nproviderId: bureau-of-consular-affairs\npublisherName: Bureau of Consular Affairs\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Federal Government\n  - Passports\n  - Travel\n  - Travel Advisories\n  - Visas\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Bureau of Consular Affairs API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Bureau of Consular Affairs\n  ServiceCategory: Developer Tools / API\n  ProviderName: Bureau of Consular Affairs\n  PublisherName: Bureau of Consular Affairs\n  InvoiceIssuerName: Bureau of Consular Affairs\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n\
  \      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Bureau of Consular Affairs Data Catalog (CKAN API)\n    baseURL: https://cadatacatalog.state.gov/api/3/action\n    tags:\n      - CKAN\n      - Data Catalog\n      - Federal Government\n      - Open Data\n    serviceName: Bureau of Consular Affairs Data Catalog (CKAN API)\n    serviceCategory: API\n  - name: Travel Advisories API\n    baseURL: https://travel.state.gov\n    tags:\n      - Federal Government\n      - Travel\n      - Travel Advisories\n    serviceName: Travel Advisories API\n    serviceCategory: API\n  - name: Passport Issuance Statistics\n    baseURL:\
  \ ''\n    tags:\n      - Federal Government\n      - Passports\n      - Statistics\n    serviceName: Passport Issuance Statistics\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bureau-of-consular-affairs/refs/heads/main/finops/bureau-of-consular-affairs-finops.yml
sources: []
specification: FinOps Framework
tags:
- Federal Government
- Passports
- Travel
- Travel Advisories
- Visas
- FinOps
- Cost Management
- FOCUS
---
