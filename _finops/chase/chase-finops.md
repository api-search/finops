---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: chase-account-and-customer-information-api-openapi.yml
  format: yaml
  label: Chase Account and Customer Information API
  slug: account-and-customer-information-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-account-and-customer-information-api-openapi.yml
- filename: chase-account-aggregation-user-consent-api-openapi.yml
  format: yaml
  label: Chase Account Aggregation User Consent API
  slug: account-aggregation-user-consent-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-account-aggregation-user-consent-api-openapi.yml
- filename: chase-rewards-balance-api-openapi.yml
  format: yaml
  label: Chase Rewards Balance API
  slug: rewards-balance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-rewards-balance-api-openapi.yml
- filename: chase-loyalty-pay-with-points-order-service-api-openapi.yml
  format: yaml
  label: Chase Loyalty Pay with Points Order Service API
  slug: loyalty-pay-with-points-order-service-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-loyalty-pay-with-points-order-service-api-openapi.yml
- filename: chase-loyalty-pay-with-points-enrollment-service-api-openapi.yml
  format: yaml
  label: Chase Loyalty Pay with Points Enrollment Service API
  slug: loyalty-pay-with-points-enrollment-service-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-loyalty-pay-with-points-enrollment-service-api-openapi.yml
- filename: chase-loyalty-pci-merchant-relationship-manager-api-openapi.yml
  format: yaml
  label: Chase Loyalty PCI Merchant Relationship Manager API
  slug: loyalty-pci-merchant-relationship-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-loyalty-pci-merchant-relationship-manager-api-openapi.yml
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
description: FinOps framework definition for the Chase API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Chase
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Chase
  PublisherName: Chase
  ServiceCategory: Developer Tools / API
  ServiceName: Chase
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
name: Chase Finops
provider_name: Chase
provider_slug: chase
publisher_name: Chase
service_category: API
slug: chase-finops
source_filename: chase-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Chase\nproviderId: chase\npublisherName: Chase\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Account Aggregation\n  - Banking\n  - Consent\n  - Credit Cards\n  - FDX\n  - Financial Services\n  - Loyalty\n  - Open Banking\n  - Pay with Points\n  - Rewards\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Chase API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  -\
  \ name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n\
  \  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Chase\n  ServiceCategory: Developer Tools / API\n  ProviderName: Chase\n  PublisherName: Chase\n  InvoiceIssuerName: Chase\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Chase Account and Customer Information API\n    baseURL: https://api.chase.com/aggregation/fdx\n    tags:\n      - Account Aggregation\n      - FDX\n      - Open Banking\n    serviceName: Chase Account and Customer Information API\n    serviceCategory: API\n  - name: Chase Account Aggregation User Consent API\n    baseURL: https://api.chase.com/aggregation/consent\n    tags:\n      - Consent\n      - FDX\n      - Open Banking\n    serviceName: Chase Account Aggregation User Consent API\n    serviceCategory: API\n  - name: Chase Rewards Balance API\n    baseURL: https://api.chase.com/loyalty/rewards-balance\n    tags:\n      - Loyalty\n      - Rewards\n\
  \    serviceName: Chase Rewards Balance API\n    serviceCategory: API\n  - name: Chase Loyalty Pay with Points Order Service API\n    baseURL: https://api.chase.com/loyalty/pay-with-points/orders\n    tags:\n      - Loyalty\n      - Payments\n      - Rewards\n    serviceName: Chase Loyalty Pay with Points Order Service API\n    serviceCategory: API\n  - name: Chase Loyalty Pay with Points Enrollment Service API\n    baseURL: https://api.chase.com/loyalty/pay-with-points/enrollment\n    tags:\n      - Loyalty\n      - Payments\n      - Rewards\n    serviceName: Chase Loyalty Pay with Points Enrollment Service API\n    serviceCategory: API\n  - name: Chase Loyalty PCI Merchant Relationship Manager API\n    baseURL: https://api.chase.com/loyalty/merchant-relationship-manager\n    tags:\n      - Loyalty\n      - Merchants\n      - PCI\n    serviceName: Chase Loyalty PCI Merchant Relationship Manager API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric:\
  \ billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/finops/chase-finops.yml
sources: []
specification: FinOps Framework
tags:
- Account Aggregation
- Banking
- Consent
- Credit Cards
- FDX
- Financial Services
- Loyalty
- Open Banking
- Pay with Points
- Rewards
- FinOps
- Cost Management
- FOCUS
---
