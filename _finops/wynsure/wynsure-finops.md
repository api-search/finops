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
description: FinOps framework definition for the Wynsure API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Wynsure
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Wynsure
  PublisherName: Wynsure
  ServiceCategory: Developer Tools / API
  ServiceName: Wynsure
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
name: Wynsure Finops
provider_name: Wynsure
provider_slug: wynsure
publisher_name: Wynsure
service_category: API
slug: wynsure-finops
source_filename: wynsure-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Wynsure\nproviderId: wynsure\npublisherName: Wynsure\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Insurance\n  - InsurTech\n  - Policy Administration\n  - Claims Management\n  - Billing\n  - Underwriting\n  - Enrollment\n  - Life Insurance\n  - Annuities\n  - Health Insurance\n  - Disability Insurance\n  - Group Benefits\n  - Voluntary Benefits\n  - Brokers\n  - Financial Services\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Wynsure API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n\
  \    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting\
  \ for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Wynsure\n  ServiceCategory: Developer Tools / API\n  ProviderName: Wynsure\n  PublisherName: Wynsure\n  InvoiceIssuerName: Wynsure\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n\
  \      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Wynsure REST API\n    baseURL: https://api.wyde.com\n    tags:\n      - Policy Administration\n      - Underwriting\n      - Claims\n      - Billing\n      - Enrollment\n      - Insurance\n      - REST\n    serviceName: Wynsure REST API\n    serviceCategory: API\n  - name: Wynsure Web Services\n    baseURL: https://api.wyde.com\n    tags:\n      - Web Services\n      - SOA\n      - Integration\n      - Insurance\n      - ESB\n    serviceName: Wynsure Web Services\n    serviceCategory: API\n  - name: Wynsure Smart\
  \ Underwriting Platform API\n    baseURL: https://api.wyde.com\n    tags:\n      - Underwriting\n      - Generative AI\n      - Risk\n      - Group Insurance\n      - Insurance\n    serviceName: Wynsure Smart Underwriting Platform API\n    serviceCategory: API\n  - name: Wynsure Billing API\n    baseURL: https://api.wyde.com\n    tags:\n      - Billing\n      - Payments\n      - Commissions\n      - Reconciliation\n      - Insurance\n    serviceName: Wynsure Billing API\n    serviceCategory: API\n  - name: Wynsure Enrollment Acceleration API\n    baseURL: https://api.wyde.com\n    tags:\n      - Enrollment\n      - Brokers\n      - Employers\n      - Members\n      - Group Benefits\n      - Insurance\n    serviceName: Wynsure Enrollment Acceleration API\n    serviceCategory: API\n  - name: Wynsure Sales and Broker Management API\n    baseURL: https://api.wyde.com\n    tags:\n      - Sales\n      - Brokers\n      - Distribution\n      - CRM\n      - Insurance\n    serviceName: Wynsure Sales\
  \ and Broker Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wynsure/refs/heads/main/finops/wynsure-finops.yml
sources: []
specification: FinOps Framework
tags:
- Insurance
- InsurTech
- Policy Administration
- Claims Management
- Billing
- Underwriting
- Enrollment
- Life Insurance
- Annuities
- Health Insurance
- Disability Insurance
- Group Benefits
- Voluntary Benefits
- Brokers
- Financial Services
- FinOps
- Cost Management
- FOCUS
---
