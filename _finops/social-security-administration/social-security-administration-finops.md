---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ssa-field-office-openapi.yml
  format: yaml
  label: SSA Field Office Address API
  slug: field-office-address-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/social-security-administration/refs/heads/main/openapi/ssa-field-office-openapi.yml
- filename: ssa-resident-station-openapi.yml
  format: yaml
  label: SSA Resident Station Address API
  slug: resident-station-address-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/social-security-administration/refs/heads/main/openapi/ssa-resident-station-openapi.yml
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
description: FinOps framework definition for the Social Security Administration API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Social Security Administration
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Social Security Administration
  PublisherName: Social Security Administration
  ServiceCategory: Developer Tools / API
  ServiceName: Social Security Administration
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
name: Social Security Administration Finops
provider_name: Social Security Administration
provider_slug: social-security-administration
publisher_name: Social Security Administration
service_category: API
slug: social-security-administration-finops
source_filename: social-security-administration-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Social Security Administration\nproviderId: social-security-administration\npublisherName: Social Security Administration\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Federal Government\n  - Social Security\n  - Government API\n  - Open Data\n  - OASDI\n  - Disability Benefits\n  - Retirement Benefits\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Social Security Administration API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible\
  \ to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload\
  \ Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Social Security Administration\n  ServiceCategory: Developer Tools / API\n  ProviderName: Social Security Administration\n  PublisherName: Social Security Administration\n  InvoiceIssuerName: Social Security Administration\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SSA Field Office Address API\n    baseURL: ''\n    tags:\n      - Field Offices\n      - Location Services\n      - Government Data\n      - Open Data\n    serviceName: SSA Field Office Address API\n    serviceCategory: API\n  - name: SSA Resident Station Address API\n    baseURL: ''\n    tags:\n      - Resident Stations\n      - Location Services\n      - Government Data\n      - Open Data\n    serviceName: SSA Resident Station Address API\n    serviceCategory: API\n  - name:\
  \ SSA OASDI Open Data API\n    baseURL: ''\n    tags:\n      - OASDI\n      - Beneficiary Statistics\n      - Open Data\n      - Benefits Data\n    serviceName: SSA OASDI Open Data API\n    serviceCategory: API\n  - name: SSA eCBSV Verification API\n    baseURL: ''\n    tags:\n      - SSN Verification\n      - Identity Verification\n      - Financial Services\n      - Consent Based\n    serviceName: SSA eCBSV Verification API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/social-security-administration/refs/heads/main/finops/social-security-administration-finops.yml
sources: []
specification: FinOps Framework
tags:
- Federal Government
- Social Security
- Government API
- Open Data
- OASDI
- Disability Benefits
- Retirement Benefits
- FinOps
- Cost Management
- FOCUS
---
