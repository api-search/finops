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
description: FinOps framework definition for the Department of Justice API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Department of Justice
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Department of Justice
  PublisherName: Department of Justice
  ServiceCategory: Developer Tools / API
  ServiceName: Department of Justice
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
name: Department Of Justice Finops
provider_name: Department of Justice
provider_slug: department-of-justice
publisher_name: Department of Justice
service_category: API
slug: department-of-justice-finops
source_filename: department-of-justice-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Department of Justice\nproviderId: department-of-justice\npublisherName: Department of Justice\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Bureau of Justice Statistics\n  - Crime\n  - Federal Government\n  - FOIA\n  - Justice\n  - News\n  - Open Data\n  - Press Releases\n  - Statistics\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Department of Justice API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product,\
  \ and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n     \
  \ - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Department of Justice\n  ServiceCategory: Developer Tools / API\n  ProviderName: Department of Justice\n  PublisherName: Department of Justice\n  InvoiceIssuerName: Department of Justice\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: DOJ News API\n    baseURL: https://www.justice.gov/api/v1\n    tags:\n      - Blog\n      - News\n      - Office of Public Affairs\n      - Press Releases\n      - Speeches\n    serviceName: DOJ News API\n    serviceCategory: API\n  - name: FOIA.gov Annual Report API\n    baseURL: https://www.foia.gov/api\n    tags:\n      - Annual Report\n      - FOIA\n      - XML\n    serviceName: FOIA.gov Annual Report API\n    serviceCategory: API\n  - name: BJS National Crime Victimization Survey (NCVS) API\n    baseURL: https://bjs.ojp.gov/api\n\
  \    tags:\n      - BJS\n      - Crime\n      - NCVS\n      - Statistics\n      - Victimization\n    serviceName: BJS National Crime Victimization Survey (NCVS) API\n    serviceCategory: API\n  - name: BJS NIBRS National Estimates API\n    baseURL: https://bjs.ojp.gov/api\n    tags:\n      - BJS\n      - Crime\n      - National Estimates\n      - NIBRS\n      - Statistics\n    serviceName: BJS NIBRS National Estimates API\n    serviceCategory: API\n  - name: DOJ Open Data Catalog\n    baseURL: https://catalog.data.gov/api/3\n    tags:\n      - CKAN\n      - Datasets\n      - Open Data\n    serviceName: DOJ Open Data Catalog\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/department-of-justice/refs/heads/main/finops/department-of-justice-finops.yml
sources: []
specification: FinOps Framework
tags:
- Bureau of Justice Statistics
- Crime
- Federal Government
- FOIA
- Justice
- News
- Open Data
- Press Releases
- Statistics
- FinOps
- Cost Management
- FOCUS
---
