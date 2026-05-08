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
description: FinOps framework definition for the AutoCAD API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: AutoCAD
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: AutoCAD
  PublisherName: AutoCAD
  ServiceCategory: Developer Tools / API
  ServiceName: AutoCAD
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
name: Autocad Finops
provider_name: AutoCAD
provider_slug: autocad
publisher_name: AutoCAD
service_category: API
slug: autocad-finops
source_filename: autocad-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: AutoCAD\nproviderId: autocad\npublisherName: AutoCAD\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - 3D Modeling\n  - Architecture\n  - CAD\n  - Design\n  - Drawing\n  - Engineering\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the AutoCAD API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the\
  \ consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: AutoCAD\n  ServiceCategory: Developer Tools / API\n  ProviderName: AutoCAD\n  PublisherName: AutoCAD\n  InvoiceIssuerName: AutoCAD\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n  \
  \  dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: AutoCAD API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Automation\n      - CAD\n      - Drawing\n      - Entities\n    serviceName: AutoCAD API\n    serviceCategory: API\n  - name: AutoCAD Design Automation API\n    baseURL: https://developer.api.autodesk.com/da/us-east/v3\n    tags:\n      - AutoLISP\n      - Batch Processing\n      - Cloud\n      - Design Automation\n      - Scripting\n    serviceName: AutoCAD Design Automation API\n    serviceCategory: API\n  - name: AutoCAD Data Management API\n    baseURL: https://developer.api.autodesk.com/data/v1\n    tags:\n      - Collaboration\n      - File Management\n      - Storage\n      - Version Control\n    serviceName: AutoCAD\
  \ Data Management API\n    serviceCategory: API\n  - name: AutoCAD Model Derivative API\n    baseURL: https://developer.api.autodesk.com/modelderivative/v2\n    tags:\n      - File Conversion\n      - Metadata\n      - Model Derivative\n      - Thumbnails\n      - Translation\n    serviceName: AutoCAD Model Derivative API\n    serviceCategory: API\n  - name: AutoCAD Webhooks API\n    baseURL: https://developer.api.autodesk.com/webhooks/v1\n    tags:\n      - Events\n      - Notifications\n      - Real-Time\n      - Webhooks\n    serviceName: AutoCAD Webhooks API\n    serviceCategory: API\n  - name: AutoCAD Authentication API\n    baseURL: https://developer.api.autodesk.com/authentication/v2\n    tags:\n      - Authentication\n      - Authorization\n      - OAuth\n      - Security\n    serviceName: AutoCAD Authentication API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active\
  \ Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/autocad/refs/heads/main/finops/autocad-finops.yml
sources: []
specification: FinOps Framework
tags:
- 3D Modeling
- Architecture
- CAD
- Design
- Drawing
- Engineering
- FinOps
- Cost Management
- FOCUS
---
