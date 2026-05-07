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
description: FinOps framework definition for the Cerner (Oracle Health) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cerner (Oracle Health)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cerner (Oracle Health)
  PublisherName: Cerner (Oracle Health)
  ServiceCategory: Developer Tools / API
  ServiceName: Cerner (Oracle Health)
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
name: Cerner Finops
provider_name: Cerner (Oracle Health)
provider_slug: cerner
publisher_name: Cerner (Oracle Health)
service_category: API
slug: cerner-finops
source_filename: cerner-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cerner (Oracle Health)\nproviderId: cerner\npublisherName: Cerner (Oracle Health)\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Cerner Millennium\n  - Code Console\n  - EHR\n  - Electronic Health Records\n  - FHIR\n  - HL7\n  - Healthcare\n  - Interoperability\n  - OAuth 2.0\n  - Oracle Health\n  - Patient Access\n  - Provider Directory\n  - SMART on FHIR\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cerner (Oracle Health) API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description:\
  \ Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n   \
  \   - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cerner (Oracle Health)\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cerner (Oracle Health)\n  PublisherName: Cerner (Oracle Health)\n  InvoiceIssuerName: Cerner (Oracle Health)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n  \
  \  aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle Health Millennium Platform FHIR R4 API\n    baseURL: ''\n    tags:\n      - CMS Interoperability\n      - FHIR\n      - HL7\n      - Patient Access\n      - R4\n      - USCDI\n    serviceName: Oracle Health Millennium Platform FHIR R4 API\n    serviceCategory: API\n  - name: Oracle Health Millennium FHIR DSTU2 API\n    baseURL: ''\n    tags:\n      - DSTU2\n      - FHIR\n      - Legacy\n      - SMART on FHIR\n    serviceName: Oracle Health Millennium FHIR\
  \ DSTU2 API\n    serviceCategory: API\n  - name: Oracle Health Code Console (Developer Portal)\n    baseURL: ''\n    tags:\n      - Code Console\n      - Developer Portal\n      - OAuth 2.0\n      - Registration\n      - Sandbox\n    serviceName: Oracle Health Code Console (Developer Portal)\n    serviceCategory: API\n  - name: Oracle Health Millennium Bulk FHIR API\n    baseURL: ''\n    tags:\n      - Bulk Data\n      - FHIR\n      - Flat FHIR\n      - Population Health\n    serviceName: Oracle Health Millennium Bulk FHIR API\n    serviceCategory: API\n  - name: Cerner CareAware Integration APIs\n    baseURL: ''\n    tags:\n      - CareAware\n      - Device Integration\n      - HL7 v2\n      - Medical Device\n    serviceName: Cerner CareAware Integration APIs\n    serviceCategory: API\n  - name: Oracle Health SMART on FHIR App Launch\n    baseURL: ''\n    tags:\n      - App Launch\n      - Clinician App\n      - Patient App\n      - SMART on FHIR\n    serviceName: Oracle Health SMART\
  \ on FHIR App Launch\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cerner/refs/heads/main/finops/cerner-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cerner Millennium
- Code Console
- EHR
- Electronic Health Records
- FHIR
- HL7
- Healthcare
- Interoperability
- OAuth 2.0
- Oracle Health
- Patient Access
- Provider Directory
- SMART on FHIR
- FinOps
- Cost Management
- FOCUS
---
