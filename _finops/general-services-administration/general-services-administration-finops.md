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
description: FinOps framework definition for the General Services Administration API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: General Services Administration
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: General Services Administration
  PublisherName: General Services Administration
  ServiceCategory: Developer Tools / API
  ServiceName: General Services Administration
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
name: General Services Administration Finops
provider_name: General Services Administration
provider_slug: general-services-administration
publisher_name: General Services Administration
service_category: API
slug: general-services-administration-finops
source_filename: general-services-administration-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: General Services Administration\nproviderId: general-services-administration\npublisherName: General Services Administration\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Federal Government\n  - Procurement\n  - Acquisition\n  - Open Data\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the General Services Administration API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: General Services Administration\n  ServiceCategory: Developer Tools / API\n  ProviderName: General Services Administration\n  PublisherName: General Services Administration\n  InvoiceIssuerName: General Services Administration\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n  \
  \    - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Acquisition Gateway Listings API\n    baseURL: ''\n    tags:\n      - Acquisition\n    serviceName: Acquisition Gateway Listings API\n    serviceCategory: API\n  - name: Analytics.usa.gov API\n    baseURL: ''\n    tags:\n      - Analytics\n    serviceName: Analytics.usa.gov API\n    serviceCategory: API\n  - name: api.data.gov Admin API\n    baseURL: ''\n    tags:\n      - API Management\n    serviceName: api.data.gov Admin API\n    serviceCategory: API\n  - name: api.data.gov Metrics API\n    baseURL: ''\n    tags:\n      - API Management\n\
  \      - Metrics\n    serviceName: api.data.gov Metrics API\n    serviceCategory: API\n  - name: Contract-Awarded Labor Category (CALC) API\n    baseURL: ''\n    tags:\n      - Acquisition\n      - Pricing\n    serviceName: Contract-Awarded Labor Category (CALC) API\n    serviceCategory: API\n  - name: Data.gov CKAN API\n    baseURL: ''\n    tags:\n      - Open Data\n      - Catalog\n    serviceName: Data.gov CKAN API\n    serviceCategory: API\n  - name: GSA Fleet Vehicles / Vehicle Leasing\n    baseURL: ''\n    tags:\n      - Fleet\n      - Vehicles\n    serviceName: GSA Fleet Vehicles / Vehicle Leasing\n    serviceCategory: API\n  - name: IT Collect Public API\n    baseURL: ''\n    tags:\n      - IT\n      - Open Data\n    serviceName: IT Collect Public API\n    serviceCategory: API\n  - name: Per Diem API\n    baseURL: ''\n    tags:\n      - Travel\n      - Reimbursement\n    serviceName: Per Diem API\n    serviceCategory: API\n  - name: Regulations.gov API\n    baseURL: ''\n    tags:\n\
  \      - Regulations\n      - Open Government\n    serviceName: Regulations.gov API\n    serviceCategory: API\n  - name: SAM.gov Entity/Exclusions Extracts Download API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Procurement\n    serviceName: SAM.gov Entity/Exclusions Extracts Download API\n    serviceCategory: API\n  - name: SAM.gov Entity Management API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Procurement\n    serviceName: SAM.gov Entity Management API\n    serviceCategory: API\n  - name: SAM.gov Exclusions API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Procurement\n    serviceName: SAM.gov Exclusions API\n    serviceCategory: API\n  - name: SAM.gov Federal Hierarchy FOUO API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Federal Hierarchy\n    serviceName: SAM.gov Federal Hierarchy FOUO API\n    serviceCategory: API\n  - name: SAM.gov Federal Hierarchy Public API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Federal Hierarchy\n    serviceName:\
  \ SAM.gov Federal Hierarchy Public API\n    serviceCategory: API\n  - name: SAM.gov Get Opportunities Public API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Opportunities\n    serviceName: SAM.gov Get Opportunities Public API\n    serviceCategory: API\n  - name: SAM.gov Opportunity Management API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Opportunities\n    serviceName: SAM.gov Opportunity Management API\n    serviceCategory: API\n  - name: SAM.gov Product Service Codes (PSC) API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Reference Data\n    serviceName: SAM.gov Product Service Codes (PSC) API\n    serviceCategory: API\n  - name: SAM.gov Public Location Services API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Reference Data\n    serviceName: SAM.gov Public Location Services API\n    serviceCategory: API\n  - name: SAM.gov Assistance Listings Public API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Assistance\n    serviceName: SAM.gov Assistance\
  \ Listings Public API\n    serviceCategory: API\n  - name: SAM.gov Acquisition Subaward Reporting Public API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Procurement\n    serviceName: SAM.gov Acquisition Subaward Reporting Public API\n    serviceCategory: API\n  - name: SAM.gov Assistance Subaward Reporting Public API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Assistance\n    serviceName: SAM.gov Assistance Subaward Reporting Public API\n    serviceCategory: API\n  - name: SAM.gov Contract Awards API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Procurement\n    serviceName: SAM.gov Contract Awards API\n    serviceCategory: API\n  - name: SAM.gov Subaward Reporting Bulk Upload API\n    baseURL: ''\n    tags:\n      - SAM.gov\n      - Procurement\n    serviceName: SAM.gov Subaward Reporting Bulk Upload API\n    serviceCategory: API\n  - name: Search.gov Clicks API\n    baseURL: ''\n    tags:\n      - Search\n      - Analytics\n    serviceName: Search.gov Clicks\
  \ API\n    serviceCategory: API\n  - name: Search.gov Results API\n    baseURL: ''\n    tags:\n      - Search\n    serviceName: Search.gov Results API\n    serviceCategory: API\n  - name: Search.gov Type-Ahead Suggestions API\n    baseURL: ''\n    tags:\n      - Search\n    serviceName: Search.gov Type-Ahead Suggestions API\n    serviceCategory: API\n  - name: Site Scanning API\n    baseURL: ''\n    tags:\n      - Federal Websites\n      - Scanning\n    serviceName: Site Scanning API\n    serviceCategory: API\n  - name: TMSS 2.0 Rate Query API\n    baseURL: ''\n    tags:\n      - Logistics\n      - Shipping\n    serviceName: TMSS 2.0 Rate Query API\n    serviceCategory: API\n  - name: Sustainable Facilities Tool API\n    baseURL: ''\n    tags:\n      - Sustainability\n      - Facilities\n    serviceName: Sustainable Facilities Tool API\n    serviceCategory: API\n  - name: Touchpoints API\n    baseURL: ''\n    tags:\n      - Feedback\n      - Customer Experience\n    serviceName: Touchpoints\
  \ API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/general-services-administration/refs/heads/main/finops/general-services-administration-finops.yml
sources: []
specification: FinOps Framework
tags:
- Federal Government
- Procurement
- Acquisition
- Open Data
- FinOps
- Cost Management
- FOCUS
---
