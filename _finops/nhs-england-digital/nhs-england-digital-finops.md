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
description: FinOps framework definition for the NHS England Digital API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: NHS England Digital
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: NHS England Digital
  PublisherName: NHS England Digital
  ServiceCategory: Developer Tools / API
  ServiceName: NHS England Digital
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
name: Nhs England Digital Finops
provider_name: NHS England Digital
provider_slug: nhs-england-digital
publisher_name: NHS England Digital
service_category: API
slug: nhs-england-digital-finops
source_filename: nhs-england-digital-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: NHS England Digital\nproviderId: nhs-england-digital\npublisherName: NHS England Digital\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Clinical\n  - Demographics\n  - FHIR\n  - Government\n  - Health\n  - Healthcare\n  - NHS\n  - Open Data\n  - Patient Records\n  - Prescriptions\n  - UK\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the NHS England Digital API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: NHS England Digital\n  ServiceCategory: Developer Tools / API\n  ProviderName: NHS England Digital\n  PublisherName: NHS England Digital\n  InvoiceIssuerName: NHS England Digital\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n\
  \      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: NHS England API Platform\n    baseURL: ''\n    tags:\n      - API Platform\n      - Developer Portal\n      - FHIR\n      - Healthcare\n    serviceName: NHS England API Platform\n    serviceCategory: API\n  - name: Personal Demographics Service (PDS) FHIR API\n    baseURL: ''\n    tags:\n      - Demographics\n      - FHIR\n      - Patient Records\n    serviceName: Personal Demographics Service (PDS) FHIR API\n    serviceCategory: API\n  - name: Electronic Prescription Service (EPS) FHIR API\n    baseURL: ''\n    tags:\n      - FHIR\n      - Pharmacy\n\
  \      - Prescriptions\n    serviceName: Electronic Prescription Service (EPS) FHIR API\n    serviceCategory: API\n  - name: e-Referral Service (e-RS) FHIR API\n    baseURL: ''\n    tags:\n      - Appointments\n      - FHIR\n      - Referrals\n    serviceName: e-Referral Service (e-RS) FHIR API\n    serviceCategory: API\n  - name: Summary Care Record (SCR) API\n    baseURL: ''\n    tags:\n      - Clinical\n      - Patient Records\n    serviceName: Summary Care Record (SCR) API\n    serviceCategory: API\n  - name: GP Connect API\n    baseURL: ''\n    tags:\n      - Appointments\n      - Clinical\n      - FHIR\n      - GP\n      - Patient Records\n    serviceName: GP Connect API\n    serviceCategory: API\n  - name: NHS Login API\n    baseURL: ''\n    tags:\n      - Authentication\n      - Identity\n      - OpenID Connect\n    serviceName: NHS Login API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n\
  \  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nhs-england-digital/refs/heads/main/finops/nhs-england-digital-finops.yml
sources: []
specification: FinOps Framework
tags:
- Clinical
- Demographics
- FHIR
- Government
- Health
- Healthcare
- NHS
- Open Data
- Patient Records
- Prescriptions
- UK
- FinOps
- Cost Management
- FOCUS
---
