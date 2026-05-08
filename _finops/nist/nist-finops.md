---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nist-nvd-cve-openapi.yml
  format: yaml
  label: NIST National Vulnerability Database (NVD) API
  slug: nist-nvd-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nist/refs/heads/main/openapi/nist-nvd-cve-openapi.yml
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
description: FinOps framework definition for the National Institute of Standards and Technology (NIST) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: National Institute of Standards and Technology (NIST)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: National Institute of Standards and Technology (NIST)
  PublisherName: National Institute of Standards and Technology (NIST)
  ServiceCategory: Developer Tools / API
  ServiceName: National Institute of Standards and Technology (NIST)
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
name: Nist Finops
provider_name: National Institute of Standards and Technology (NIST)
provider_slug: nist
publisher_name: National Institute of Standards and Technology (NIST)
service_category: API
slug: nist-finops
source_filename: nist-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: National Institute of Standards and Technology (NIST)\nproviderId: nist\npublisherName: National Institute of Standards and Technology (NIST)\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cybersecurity\n  - Government\n  - Measurements\n  - Research\n  - Scientific Data\n  - Standards\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the National Institute of Standards and Technology (NIST)\n  API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics\n  reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs\
  \ visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n   \
  \   - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: National Institute of Standards and Technology (NIST)\n  ServiceCategory: Developer Tools / API\n  ProviderName: National Institute of Standards and Technology (NIST)\n  PublisherName: National Institute of Standards and Technology (NIST)\n  InvoiceIssuerName: National Institute of Standards and Technology (NIST)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n\
  \  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: NIST National Vulnerability Database (NVD) API\n    baseURL: https://services.nvd.nist.gov/rest/json\n    tags:\n      - CVE\n      - Cybersecurity\n      - Security\n      - Vulnerabilities\n    serviceName: NIST National Vulnerability Database (NVD) API\n    serviceCategory: API\n  - name: NIST Chemistry WebBook API\n    baseURL: https://webbook.nist.gov/cgi\n    tags:\n\
  \      - Chemistry\n      - Physical Properties\n      - Scientific Data\n    serviceName: NIST Chemistry WebBook API\n    serviceCategory: API\n  - name: NIST Data Gateway\n    baseURL: https://data.nist.gov\n    tags:\n      - Open Data\n      - Research Data\n      - Scientific Data\n    serviceName: NIST Data Gateway\n    serviceCategory: API\n  - name: NIST Time API\n    baseURL: ''\n    tags:\n      - Standards\n      - Synchronization\n      - Time\n    serviceName: NIST Time API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nist/refs/heads/main/finops/nist-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cybersecurity
- Government
- Measurements
- Research
- Scientific Data
- Standards
- FinOps
- Cost Management
- FOCUS
---
