---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: library-of-congress-loc-gov-json-api-openapi.yml
  format: yaml
  label: Library of Congress loc.gov JSON API
  slug: loc-gov-json-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/library-of-congress/refs/heads/main/openapi/library-of-congress-loc-gov-json-api-openapi.yml
- filename: library-of-congress-chronicling-america-api-openapi.yml
  format: yaml
  label: Library of Congress Chronicling America API
  slug: chronicling-america-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/library-of-congress/refs/heads/main/openapi/library-of-congress-chronicling-america-api-openapi.yml
- filename: library-of-congress-congress-gov-api-openapi.yml
  format: yaml
  label: Library of Congress Congress.gov API
  slug: congress-gov-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/library-of-congress/refs/heads/main/openapi/library-of-congress-congress-gov-api-openapi.yml
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
description: FinOps framework definition for the Library of Congress API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Library of Congress
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Library of Congress
  PublisherName: Library of Congress
  ServiceCategory: Developer Tools / API
  ServiceName: Library of Congress
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
name: Library Of Congress Finops
provider_name: Library of Congress
provider_slug: library-of-congress
publisher_name: Library of Congress
service_category: API
slug: library-of-congress-finops
source_filename: library-of-congress-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Library of Congress\nproviderId: library-of-congress\npublisherName: Library of Congress\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Cultural Heritage\n  - Federal Government\n  - Library\n  - Legislative\n  - Newspapers\n  - Search\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Library of Congress API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Library of Congress\n  ServiceCategory: Developer Tools / API\n  ProviderName: Library of Congress\n  PublisherName: Library of Congress\n  InvoiceIssuerName: Library of Congress\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Library of Congress loc.gov JSON API\n    baseURL: https://www.loc.gov\n    tags:\n      - Collections\n      - Library\n      - Metadata\n      - Search\n    serviceName: Library of Congress loc.gov JSON API\n    serviceCategory: API\n  - name: Library of Congress Chronicling America API\n    baseURL: https://chroniclingamerica.loc.gov\n    tags:\n      - Historic\n      - Library\n      - Newspapers\n      - Search\n    serviceName: Library of Congress Chronicling America API\n    serviceCategory: API\n  - name: Library of Congress Congress.gov API\n    baseURL: https://api.congress.gov/v3\n    tags:\n\
  \      - Bills\n      - Congress\n      - Legislative\n      - Members\n    serviceName: Library of Congress Congress.gov API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/library-of-congress/refs/heads/main/finops/library-of-congress-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cultural Heritage
- Federal Government
- Library
- Legislative
- Newspapers
- Search
- FinOps
- Cost Management
- FOCUS
---
