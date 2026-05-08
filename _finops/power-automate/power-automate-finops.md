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
description: FinOps framework definition for the Microsoft Power Automate API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Power Automate
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Power Automate
  PublisherName: Microsoft Power Automate
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Power Automate
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
name: Power Automate Finops
provider_name: Microsoft Power Automate
provider_slug: power-automate
publisher_name: Microsoft Power Automate
service_category: API
slug: power-automate-finops
source_filename: power-automate-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Power Automate\nproviderId: power-automate\npublisherName: Microsoft Power Automate\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Workflow Automation\n  - Enterprise\n  - Low-Code\n  - RPA\n  - Cloud Flows\n  - Desktop Flows\n  - AI\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Power Automate API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Power Automate\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Power Automate\n  PublisherName: Microsoft Power Automate\n  InvoiceIssuerName: Microsoft Power Automate\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n\
  \      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Power Automate\n    baseURL: ''\n    tags:\n      - Workflow Automation\n      - Cloud Flows\n      - Desktop Flows\n      - Connectors\n    serviceName: Microsoft Power Automate\n    serviceCategory: API\n  - name: Power Automate Desktop Flows Public API\n    baseURL: ''\n    tags:\n      - Desktop Flows\n      - RPA\n      - Automation\n    serviceName: Power Automate Desktop Flows Public API\n    serviceCategory: API\n  - name: Power Automate Cloud Flows API\n    baseURL: ''\n    tags:\n      - Cloud Flows\n      - Dataverse\n      - Automation\n\
  \    serviceName: Power Automate Cloud Flows API\n    serviceCategory: API\n  - name: Power Automate Custom Connectors\n    baseURL: ''\n    tags:\n      - Custom Connectors\n      - Integration\n      - Extensibility\n    serviceName: Power Automate Custom Connectors\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/power-automate/refs/heads/main/finops/power-automate-finops.yml
sources: []
specification: FinOps Framework
tags:
- Workflow Automation
- Enterprise
- Low-Code
- RPA
- Cloud Flows
- Desktop Flows
- AI
- FinOps
- Cost Management
- FOCUS
---
