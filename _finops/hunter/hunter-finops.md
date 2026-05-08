---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Domain Search API
  slug: domain-search
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Email Finder API
  slug: email-finder
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Email Verifier API
  slug: email-verifier
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Email Count API
  slug: email-count
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Account API
  slug: account
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Discover API
  slug: discover
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Email Enrichment API
  slug: email-enrichment
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Company Enrichment API
  slug: company-enrichment
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Combined Enrichment API
  slug: combined-enrichment
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Leads API
  slug: leads
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Leads Lists API
  slug: leads-lists
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Campaigns API
  slug: campaigns
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Logo API
  slug: logo
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
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
description: FinOps framework definition for the Hunter API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Hunter
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Hunter
  PublisherName: Hunter
  ServiceCategory: Developer Tools / API
  ServiceName: Hunter
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
name: Hunter Finops
provider_name: Hunter
provider_slug: hunter
publisher_name: Hunter
service_category: API
slug: hunter-finops
source_filename: hunter-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Hunter\nproviderId: hunter\npublisherName: Hunter\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Contact Discovery\n  - Email\n  - Email Verification\n  - Lead Generation\n  - Prospecting\n  - Sales Intelligence\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Hunter API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Hunter\n  ServiceCategory: Developer Tools / API\n  ProviderName: Hunter\n  PublisherName: Hunter\n  InvoiceIssuerName: Hunter\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Hunter Domain Search API\n    baseURL: https://api.hunter.io/v2\n    tags:\n      - Contact Discovery\n      - Domain\n      - Email\n      - Search\n    serviceName: Hunter Domain Search API\n    serviceCategory: API\n  - name: Hunter Email Finder API\n    baseURL: https://api.hunter.io/v2\n    tags:\n      - Contact Discovery\n      - Email\n      - Finder\n      - Lead Generation\n    serviceName: Hunter Email Finder API\n    serviceCategory: API\n  - name: Hunter Email Verifier API\n    baseURL: https://api.hunter.io/v2\n    tags:\n      - Data Quality\n      - Email\n      - Validation\n      - Verification\n    serviceName: Hunter Email Verifier API\n    serviceCategory: API\n\
  \  - name: Hunter Email Count API\n    baseURL: https://api.hunter.io/v2\n    tags:\n      - Analytics\n      - Count\n      - Email\n    serviceName: Hunter Email Count API\n    serviceCategory: API\n  - name: Hunter Account API\n    baseURL: https://api.hunter.io/v2\n    tags:\n      - Account\n      - Management\n      - Usage\n    serviceName: Hunter Account API\n    serviceCategory: API\n  - name: Hunter Discover API\n    baseURL: https://api.hunter.io/v2\n    tags:\n      - Companies\n      - Discover\n      - Lead Generation\n      - Prospecting\n    serviceName: Hunter Discover API\n    serviceCategory: API\n  - name: Hunter Email Enrichment API\n    baseURL: https://api.hunter.io/v2\n    tags:\n      - Data\n      - Email\n      - Enrichment\n      - People\n    serviceName: Hunter Email Enrichment API\n    serviceCategory: API\n  - name: Hunter Company Enrichment API\n    baseURL: https://api.hunter.io/v2\n    tags:\n      - Company\n      - Data\n      - Enrichment\n      -\
  \ Firmographic\n    serviceName: Hunter Company Enrichment API\n    serviceCategory: API\n  - name: Hunter Combined Enrichment API\n    baseURL: https://api.hunter.io/v2\n    tags:\n      - Combined\n      - Company\n      - Enrichment\n      - People\n    serviceName: Hunter Combined Enrichment API\n    serviceCategory: API\n  - name: Hunter Leads API\n    baseURL: https://api.hunter.io/v2\n    tags:\n      - Contacts\n      - CRM\n      - Leads\n      - Management\n    serviceName: Hunter Leads API\n    serviceCategory: API\n  - name: Hunter Leads Lists API\n    baseURL: https://api.hunter.io/v2\n    tags:\n      - Leads\n      - Lists\n      - Management\n      - Organization\n    serviceName: Hunter Leads Lists API\n    serviceCategory: API\n  - name: Hunter Campaigns API\n    baseURL: https://api.hunter.io/v2\n    tags:\n      - Automation\n      - Campaigns\n      - Email Outreach\n      - Sequences\n    serviceName: Hunter Campaigns API\n    serviceCategory: API\n  - name: Hunter\
  \ Logo API\n    baseURL: https://logos.hunter.io\n    tags:\n      - Branding\n      - Company\n      - Images\n      - Logo\n    serviceName: Hunter Logo API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/finops/hunter-finops.yml
sources: []
specification: FinOps Framework
tags:
- Contact Discovery
- Email
- Email Verification
- Lead Generation
- Prospecting
- Sales Intelligence
- FinOps
- Cost Management
- FOCUS
---
