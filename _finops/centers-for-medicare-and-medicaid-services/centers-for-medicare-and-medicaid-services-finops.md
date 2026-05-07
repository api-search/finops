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
description: FinOps framework definition for the Centers for Medicare and Medicaid Services API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Centers for Medicare and Medicaid Services
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Centers for Medicare and Medicaid Services
  PublisherName: Centers for Medicare and Medicaid Services
  ServiceCategory: Developer Tools / API
  ServiceName: Centers for Medicare and Medicaid Services
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
name: Centers For Medicare And Medicaid Services Finops
provider_name: Centers for Medicare and Medicaid Services
provider_slug: centers-for-medicare-and-medicaid-services
publisher_name: Centers for Medicare and Medicaid Services
service_category: API
slug: centers-for-medicare-and-medicaid-services-finops
source_filename: centers-for-medicare-and-medicaid-services-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Centers for Medicare and Medicaid Services\nproviderId: centers-for-medicare-and-medicaid-services\npublisherName: Centers for Medicare and Medicaid Services\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - BCDA\n  - Blue Button\n  - CMS\n  - Claims\n  - DPC\n  - FHIR\n  - Federal Government\n  - Healthcare\n  - Interoperability\n  - Marketplace\n  - Medicaid\n  - Medicare\n  - Open Data\n  - Provider Data\n  - Socrata\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Centers for Medicare and Medicaid Services API surface.\n  Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics\
  \ reporting\n  across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n\
  \  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Centers for Medicare and Medicaid Services\n  ServiceCategory: Developer Tools / API\n  ProviderName: Centers for Medicare and Medicaid Services\n  PublisherName: Centers for Medicare and Medicaid Services\n  InvoiceIssuerName: Centers for Medicare and Medicaid Services\n  PricingCategory: Usage-Based\n  PricingUnit:\
  \ request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CMS Blue Button 2.0 API\n    baseURL: https://api.bluebutton.cms.gov/v2/fhir/\n    tags:\n      - Blue Button\n      - Claims\n      - FHIR\n      - Medicare\n      - OAuth 2.0\n      - Patient Access\n    serviceName: CMS Blue Button 2.0 API\n    serviceCategory: API\n  - name: CMS Beneficiary Claims Data\
  \ API (BCDA)\n    baseURL: https://api.bcda.cms.gov/api/v2/\n    tags:\n      - ACO\n      - BCDA\n      - Bulk FHIR\n      - Claims\n      - Medicare\n      - Shared Savings\n    serviceName: CMS Beneficiary Claims Data API (BCDA)\n    serviceCategory: API\n  - name: CMS Data at the Point of Care (DPC) API\n    baseURL: https://api.dpc.cms.gov/api/v1/\n    tags:\n      - Bulk FHIR\n      - Claims\n      - FFS\n      - Point of Care\n      - Providers\n    serviceName: CMS Data at the Point of Care (DPC) API\n    serviceCategory: API\n  - name: CMS Socrata Open Data API (data.cms.gov)\n    baseURL: https://data.cms.gov/data.json\n    tags:\n      - Datasets\n      - Medicare\n      - Open Data\n      - Provider Data\n      - SODA\n      - Socrata\n    serviceName: CMS Socrata Open Data API (data.cms.gov)\n    serviceCategory: API\n  - name: CMS Provider Data Catalog API (Care Compare)\n    baseURL: https://data.cms.gov/provider-data/api/1/\n    tags:\n      - Care Compare\n      - Dialysis\
  \ Compare\n      - Hospital Compare\n      - Nursing Home Compare\n      - Provider Data\n      - Quality\n    serviceName: CMS Provider Data Catalog API (Care Compare)\n    serviceCategory: API\n  - name: NPPES NPI Registry API\n    baseURL: https://npiregistry.cms.hhs.gov/api/\n    tags:\n      - Credentialing\n      - NPI\n      - NPPES\n      - Provider Identifier\n      - Provider Registry\n    serviceName: NPPES NPI Registry API\n    serviceCategory: API\n  - name: Healthcare.gov Marketplace API\n    baseURL: https://marketplace.api.healthcare.gov/api/v1/\n    tags:\n      - ACA\n      - Exchange\n      - Marketplace\n      - Plan Finder\n      - QHP\n    serviceName: Healthcare.gov Marketplace API\n    serviceCategory: API\n  - name: CMS Quality Payment Program (QPP) Measures API\n    baseURL: ''\n    tags:\n      - MIPS\n      - Measures\n      - Quality\n      - QPP\n      - Value-Based\n    serviceName: CMS Quality Payment Program (QPP) Measures API\n    serviceCategory: API\n\
  \  - name: Medicare Coverage Database (MCD) API\n    baseURL: ''\n    tags:\n      - Coverage\n      - LCD\n      - MAC\n      - NCD\n      - Policy\n    serviceName: Medicare Coverage Database (MCD) API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/centers-for-medicare-and-medicaid-services/refs/heads/main/finops/centers-for-medicare-and-medicaid-services-finops.yml
sources: []
specification: FinOps Framework
tags:
- BCDA
- Blue Button
- CMS
- Claims
- DPC
- FHIR
- Federal Government
- Healthcare
- Interoperability
- Marketplace
- Medicaid
- Medicare
- Open Data
- Provider Data
- Socrata
- FinOps
- Cost Management
- FOCUS
---
