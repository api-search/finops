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
description: FinOps framework definition for the iDenfy API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: iDenfy
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: iDenfy
  PublisherName: iDenfy
  ServiceCategory: Developer Tools / API
  ServiceName: iDenfy
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
name: Idenfy Finops
provider_name: iDenfy
provider_slug: idenfy
publisher_name: iDenfy
service_category: API
slug: idenfy-finops
source_filename: idenfy-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: iDenfy\nproviderId: idenfy\npublisherName: iDenfy\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AML\n  - Compliance\n  - Fraud Detection\n  - Identity Verification\n  - KYB\n  - KYC\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the iDenfy API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the\
  \ consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: iDenfy\n  ServiceCategory: Developer Tools / API\n  ProviderName: iDenfy\n  PublisherName: iDenfy\n  InvoiceIssuerName: iDenfy\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: iDenfy Identity Verification API\n    baseURL: ''\n    tags:\n      - Identity Verification\n      - KYC\n      - Liveness\n    serviceName: iDenfy Identity Verification API\n    serviceCategory: API\n  - name: iDenfy Business Verification API\n    baseURL: ''\n    tags:\n      - Business Verification\n      - KYB\n      - UBO\n    serviceName: iDenfy Business Verification API\n    serviceCategory: API\n  - name: iDenfy AML Screening API\n    baseURL: ''\n    tags:\n      - AML\n      - Compliance\n      - PEP\n      - Sanctions\n    serviceName: iDenfy AML Screening API\n    serviceCategory: API\n  - name: iDenfy Fraud Prevention API\n    baseURL: ''\n    tags:\n      - Fraud Detection\n      - Identity Verification\n\
  \      - Risk Scoring\n    serviceName: iDenfy Fraud Prevention API\n    serviceCategory: API\n  - name: iDenfy Face Authentication API\n    baseURL: ''\n    tags:\n      - Biometrics\n      - Face Authentication\n      - Identity Verification\n    serviceName: iDenfy Face Authentication API\n    serviceCategory: API\n  - name: iDenfy Bank Verification API\n    baseURL: ''\n    tags:\n      - Bank Verification\n      - Open Banking\n    serviceName: iDenfy Bank Verification API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/idenfy/refs/heads/main/finops/idenfy-finops.yml
sources: []
specification: FinOps Framework
tags:
- AML
- Compliance
- Fraud Detection
- Identity Verification
- KYB
- KYC
- FinOps
- Cost Management
- FOCUS
---
