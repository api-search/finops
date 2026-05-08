---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: atandt-wireless-apis.yaml
  format: yaml
  label: AT&T Wireless APIs
  slug: att-wireless-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/atandt/refs/heads/main/openapi/atandt-wireless-apis.yaml
- filename: atandt-network-apis.yaml
  format: yaml
  label: AT&T 5G Network APIs
  slug: att-network-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/atandt/refs/heads/main/openapi/atandt-network-apis.yaml
- filename: atandt-enterprise-connectivity-apis.yaml
  format: yaml
  label: AT&T Enterprise Connectivity APIs
  slug: att-enterprise-connectivity-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/atandt/refs/heads/main/openapi/atandt-enterprise-connectivity-apis.yaml
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
description: FinOps framework definition for the AT&T API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: AT&T
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: AT&T
  PublisherName: AT&T
  ServiceCategory: Developer Tools / API
  ServiceName: AT&T
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
name: Atandt Finops
provider_name: AT&T
provider_slug: atandt
publisher_name: AT&T
service_category: API
slug: atandt-finops
source_filename: atandt-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: AT&T\nproviderId: atandt\npublisherName: AT&T\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Telecommunications\n  - Fortune 100\n  - Wireless\n  - Wireline\n  - Broadband\n  - Enterprise\n  - 5G\n  - Network\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the AT&T API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: AT&T\n  ServiceCategory: Developer Tools / API\n  ProviderName: AT&T\n  PublisherName: AT&T\n  InvoiceIssuerName: AT&T\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: AT&T Wireless APIs\n    baseURL: https://api.att.com\n    tags:\n      - Wireless\n      - SMS\n      - MMS\n      - Speech\n      - Advertising\n      - OAuth\n    serviceName: AT&T Wireless APIs\n    serviceCategory: API\n  - name: AT&T 5G Network APIs\n    baseURL: https://api.att.com\n    tags:\n      - 5G\n      - CAMARA\n      - Network\n      - Device Status\n      - SIM Swap\n      - Quality of Service\n    serviceName: AT&T 5G Network APIs\n    serviceCategory: API\n  - name: AT&T Enterprise Connectivity APIs\n    baseURL: https://devex-web.att.com\n    tags:\n      - Enterprise\n      - Wireline\n      - AVPN\n      - Service Ordering\n      - Service Qualification\n    serviceName: AT&T Enterprise\
  \ Connectivity APIs\n    serviceCategory: API\n  - name: AT&T MVNO APIs\n    baseURL: https://devex-web.att.com\n    tags:\n      - MVNO\n      - TM Forum\n      - Subscriber Management\n      - Porting\n    serviceName: AT&T MVNO APIs\n    serviceCategory: API\n  - name: AT&T Cloud Voice APIs\n    baseURL: https://devex-web.att.com\n    tags:\n      - Voice\n      - Cloud\n      - Business\n      - UCaaS\n    serviceName: AT&T Cloud Voice APIs\n    serviceCategory: API\n  - name: AT&T eBonding APIs\n    baseURL: https://devex-web.att.com\n    tags:\n      - eBonding\n      - Enterprise\n      - BSS\n      - OSS\n      - Integration\n    serviceName: AT&T eBonding APIs\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/atandt/refs/heads/main/finops/atandt-finops.yml
sources: []
specification: FinOps Framework
tags:
- Telecommunications
- Fortune 100
- Wireless
- Wireline
- Broadband
- Enterprise
- 5G
- Network
- FinOps
- Cost Management
- FOCUS
---
