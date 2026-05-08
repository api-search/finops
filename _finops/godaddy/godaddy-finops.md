---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: godaddy-domains-openapi.json
  format: json
  label: GoDaddy Domains API
  slug: domains
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-domains-openapi.json
- filename: godaddy-certificates-openapi.json
  format: json
  label: GoDaddy Certificates API
  slug: certificates
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-certificates-openapi.json
- filename: godaddy-shoppers-openapi.json
  format: json
  label: GoDaddy Shoppers API
  slug: shoppers
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-shoppers-openapi.json
- filename: godaddy-subscriptions-openapi.json
  format: json
  label: GoDaddy Subscriptions API
  slug: subscriptions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-subscriptions-openapi.json
- filename: godaddy-orders-openapi.json
  format: json
  label: GoDaddy Orders API
  slug: orders
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-orders-openapi.json
- filename: godaddy-aftermarket-openapi.json
  format: json
  label: GoDaddy Aftermarket API
  slug: aftermarket
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-aftermarket-openapi.json
- filename: godaddy-abuse-openapi.json
  format: json
  label: GoDaddy Abuse API
  slug: abuse
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-abuse-openapi.json
- filename: godaddy-agreements-openapi.json
  format: json
  label: GoDaddy Agreements API
  slug: agreements
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-agreements-openapi.json
- filename: godaddy-countries-openapi.json
  format: json
  label: GoDaddy Countries API
  slug: countries
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-countries-openapi.json
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
description: FinOps framework definition for the GoDaddy API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: GoDaddy
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: GoDaddy
  PublisherName: GoDaddy
  ServiceCategory: Developer Tools / API
  ServiceName: GoDaddy
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
name: Godaddy Finops
provider_name: GoDaddy
provider_slug: godaddy
publisher_name: GoDaddy
service_category: API
slug: godaddy-finops
source_filename: godaddy-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: GoDaddy\nproviderId: godaddy\npublisherName: GoDaddy\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Aftermarket\n  - Certificates\n  - DNS\n  - Domains\n  - Hosting\n  - Registrar\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the GoDaddy API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the\
  \ consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: GoDaddy\n  ServiceCategory: Developer Tools / API\n  ProviderName: GoDaddy\n  PublisherName: GoDaddy\n  InvoiceIssuerName: GoDaddy\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n  \
  \  dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: GoDaddy Domains API\n    baseURL: https://api.godaddy.com\n    tags:\n      - Domains\n      - DNS\n      - Registrar\n    serviceName: GoDaddy Domains API\n    serviceCategory: API\n  - name: GoDaddy Certificates API\n    baseURL: https://api.godaddy.com\n    tags:\n      - Certificates\n      - SSL\n    serviceName: GoDaddy Certificates API\n    serviceCategory: API\n  - name: GoDaddy Shoppers API\n    baseURL: https://api.godaddy.com\n    tags:\n      - Shoppers\n      - Accounts\n    serviceName: GoDaddy Shoppers API\n    serviceCategory: API\n  - name: GoDaddy Subscriptions API\n    baseURL: https://api.godaddy.com\n    tags:\n      - Subscriptions\n      - Billing\n    serviceName: GoDaddy Subscriptions\
  \ API\n    serviceCategory: API\n  - name: GoDaddy Orders API\n    baseURL: https://api.godaddy.com\n    tags:\n      - Orders\n      - Billing\n    serviceName: GoDaddy Orders API\n    serviceCategory: API\n  - name: GoDaddy Aftermarket API\n    baseURL: https://api.godaddy.com\n    tags:\n      - Aftermarket\n      - Auctions\n      - Domains\n    serviceName: GoDaddy Aftermarket API\n    serviceCategory: API\n  - name: GoDaddy Abuse API\n    baseURL: https://api.godaddy.com\n    tags:\n      - Abuse\n      - Trust and Safety\n    serviceName: GoDaddy Abuse API\n    serviceCategory: API\n  - name: GoDaddy Agreements API\n    baseURL: https://api.godaddy.com\n    tags:\n      - Agreements\n      - Legal\n    serviceName: GoDaddy Agreements API\n    serviceCategory: API\n  - name: GoDaddy Countries API\n    baseURL: https://api.godaddy.com\n    tags:\n      - Countries\n      - Reference Data\n    serviceName: GoDaddy Countries API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost\
  \ per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/finops/godaddy-finops.yml
sources: []
specification: FinOps Framework
tags:
- Aftermarket
- Certificates
- DNS
- Domains
- Hosting
- Registrar
- FinOps
- Cost Management
- FOCUS
---
