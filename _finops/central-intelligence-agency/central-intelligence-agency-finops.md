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
description: FinOps framework definition for the Central Intelligence Agency API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Central Intelligence Agency
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Central Intelligence Agency
  PublisherName: Central Intelligence Agency
  ServiceCategory: Developer Tools / API
  ServiceName: Central Intelligence Agency
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
name: Central Intelligence Agency Finops
provider_name: Central Intelligence Agency
provider_slug: central-intelligence-agency
publisher_name: Central Intelligence Agency
service_category: API
slug: central-intelligence-agency-finops
source_filename: central-intelligence-agency-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Central Intelligence Agency\nproviderId: central-intelligence-agency\npublisherName: Central Intelligence Agency\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Federal Government\n  - FOIA\n  - Government\n  - Intelligence\n  - National Security\n  - Open Data\n  - World Factbook\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Central Intelligence Agency API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Central Intelligence Agency\n  ServiceCategory: Developer Tools / API\n  ProviderName: Central Intelligence Agency\n  PublisherName: Central Intelligence Agency\n  InvoiceIssuerName: Central Intelligence Agency\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n\
  \      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CIA Public Website\n    baseURL: ''\n    tags:\n      - Federal Government\n      - Intelligence\n      - News\n    serviceName: CIA Public Website\n    serviceCategory: API\n  - name: CIA FOIA Electronic Reading Room (CREST)\n    baseURL: ''\n    tags:\n      - Declassified\n      - Documents\n      - FOIA\n      - Records Search\n      - Transparency\n    serviceName: CIA FOIA Electronic Reading Room (CREST)\n    serviceCategory: API\n  - name: CIA World Factbook (Country Profiles)\n    baseURL: ''\n    tags:\n\
  \      - Country Profiles\n      - Demographics\n      - Geography\n      - Open Data\n      - Reference\n      - World Factbook\n    serviceName: CIA World Factbook (Country Profiles)\n    serviceCategory: API\n  - name: CIA Museum Digital Collection\n    baseURL: ''\n    tags:\n      - Artifacts\n      - History\n      - Museum\n    serviceName: CIA Museum Digital Collection\n    serviceCategory: API\n  - name: Studies in Intelligence Journal\n    baseURL: ''\n    tags:\n      - Analysis\n      - Intelligence\n      - Journal\n      - Publications\n    serviceName: Studies in Intelligence Journal\n    serviceCategory: API\n  - name: CIA Careers Portal\n    baseURL: ''\n    tags:\n      - Careers\n      - Hiring\n      - Jobs\n    serviceName: CIA Careers Portal\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target:\
  \ TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/central-intelligence-agency/refs/heads/main/finops/central-intelligence-agency-finops.yml
sources: []
specification: FinOps Framework
tags:
- Federal Government
- FOIA
- Government
- Intelligence
- National Security
- Open Data
- World Factbook
- FinOps
- Cost Management
- FOCUS
---
