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
description: FinOps framework definition for the Certero API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Certero
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Certero
  PublisherName: Certero
  ServiceCategory: Developer Tools / API
  ServiceName: Certero
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
name: Certero Finops
provider_name: Certero
provider_slug: certero
publisher_name: Certero
service_category: API
slug: certero-finops
source_filename: certero-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Certero\nproviderId: certero\npublisherName: Certero\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Management\n  - FinOps\n  - Hardware Asset Management\n  - IT Asset Management\n  - ITAM\n  - License Management\n  - SaaS Management\n  - Software Asset Management\n  - Software Licensing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Certero API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance\
  \ teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Certero\n  ServiceCategory: Developer Tools / API\n  ProviderName: Certero\n  PublisherName: Certero\n  InvoiceIssuerName: Certero\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CerteroX ITAM\n    baseURL: ''\n    tags:\n      - Asset Discovery\n      - CMDB\n      - Hardware\n      - ITAM\n      - Lifecycle\n    serviceName: CerteroX ITAM\n    serviceCategory: API\n  - name: CerteroX SAM\n    baseURL: ''\n    tags:\n      - Compliance\n      - License Optimization\n      - SAM\n      - Software Asset Management\n    serviceName: CerteroX SAM\n    serviceCategory: API\n  - name: CerteroX SaaS\n    baseURL: ''\n    tags:\n      - SaaS Management\n      - Shadow IT\n      - Subscriptions\n    serviceName: CerteroX SaaS\n    serviceCategory: API\n  - name: CerteroX Cloud\n    baseURL: ''\n  \
  \  tags:\n      - Cloud Cost\n      - FinOps\n      - Multi-Cloud\n    serviceName: CerteroX Cloud\n    serviceCategory: API\n  - name: CerteroX Command Center / AI\n    baseURL: ''\n    tags:\n      - AI\n      - Analytics\n      - Dashboard\n      - Reporting\n    serviceName: CerteroX Command Center / AI\n    serviceCategory: API\n  - name: Certero ServiceNow Integration\n    baseURL: ''\n    tags:\n      - CMDB\n      - Connector\n      - ITSM\n      - ServiceNow\n    serviceName: Certero ServiceNow Integration\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/certero/refs/heads/main/finops/certero-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Management
- FinOps
- Hardware Asset Management
- IT Asset Management
- ITAM
- License Management
- SaaS Management
- Software Asset Management
- Software Licensing
- FinOps
- Cost Management
- FOCUS
---
