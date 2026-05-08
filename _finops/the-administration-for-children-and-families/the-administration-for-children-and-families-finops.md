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
description: FinOps framework definition for the The Administration for Children and Families API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: The Administration for Children and Families
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: The Administration for Children and Families
  PublisherName: The Administration for Children and Families
  ServiceCategory: Developer Tools / API
  ServiceName: The Administration for Children and Families
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
name: The Administration For Children And Families Finops
provider_name: The Administration for Children and Families
provider_slug: the-administration-for-children-and-families
publisher_name: The Administration for Children and Families
service_category: API
slug: the-administration-for-children-and-families-finops
source_filename: the-administration-for-children-and-families-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: The Administration for Children and Families\nproviderId: the-administration-for-children-and-families\npublisherName: The Administration for Children and Families\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Children\n  - Families\n  - Federal Government\n  - Health And Human Services\n  - Human Services\n  - Social Safety Net\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the The Administration for Children and Families API surface.\n  Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting\n  across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description:\
  \ Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n   \
  \   - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: The Administration for Children and Families\n  ServiceCategory: Developer Tools / API\n  ProviderName: The Administration for Children and Families\n  PublisherName: The Administration for Children and Families\n  InvoiceIssuerName: The Administration for Children and Families\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name:\
  \ api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: TANF Data Portal\n    baseURL: https://tanfdata.acf.hhs.gov/\n    tags:\n      - Federal Government\n      - Human Services\n      - TANF\n    serviceName: TANF Data Portal\n    serviceCategory: API\n  - name: ACF Human Services Interoperability Initiative\n    baseURL: https://acf.gov/\n    tags:\n      - FHIR\n      - Federal Government\n      - Human Services\n      - Interoperability\n\
  \    serviceName: ACF Human Services Interoperability Initiative\n    serviceCategory: API\n  - name: National Data Archive on Child Abuse and Neglect\n    baseURL: https://www.ndacan.acf.hhs.gov/\n    tags:\n      - Child Welfare\n      - Data Archive\n      - Federal Government\n      - Research\n    serviceName: National Data Archive on Child Abuse and Neglect\n    serviceCategory: API\n  - name: ACF Data and Research Portal\n    baseURL: https://acf.gov/\n    tags:\n      - Data\n      - Federal Government\n      - Research\n      - Statistics\n    serviceName: ACF Data and Research Portal\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/the-administration-for-children-and-families/refs/heads/main/finops/the-administration-for-children-and-families-finops.yml
sources: []
specification: FinOps Framework
tags:
- Children
- Families
- Federal Government
- Health And Human Services
- Human Services
- Social Safety Net
- FinOps
- Cost Management
- FOCUS
---
