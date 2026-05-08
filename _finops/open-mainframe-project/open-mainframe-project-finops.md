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
description: FinOps framework definition for the Open Mainframe Project API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Open Mainframe Project
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Open Mainframe Project
  PublisherName: Open Mainframe Project
  ServiceCategory: Developer Tools / API
  ServiceName: Open Mainframe Project
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
name: Open Mainframe Project Finops
provider_name: Open Mainframe Project
provider_slug: open-mainframe-project
publisher_name: Open Mainframe Project
service_category: API
slug: open-mainframe-project-finops
source_filename: open-mainframe-project-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Open Mainframe Project\nproviderId: open-mainframe-project\npublisherName: Open Mainframe Project\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Native\n  - Education\n  - Enterprise\n  - IBM Z\n  - Linux Foundation\n  - Linux on Z\n  - Mainframe\n  - Open Source\n  - z/OS\n  - z/VM\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Open Mainframe Project API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product,\
  \ and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n     \
  \ - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Open Mainframe Project\n  ServiceCategory: Developer Tools / API\n  ProviderName: Open Mainframe Project\n  PublisherName: Open Mainframe Project\n  InvoiceIssuerName: Open Mainframe Project\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Zowe\n    baseURL: ''\n    tags:\n      - API Mediation\n      - CLI\n      - Mainframe\n      - REST APIs\n      - z/OS\n    serviceName: Zowe\n    serviceCategory: API\n  - name: Feilong\n    baseURL: ''\n    tags:\n      - Cloud Connector\n      - REST APIs\n      - z/VM\n    serviceName: Feilong\n    serviceCategory: API\n  - name: Galasa\n    baseURL: ''\n    tags:\n      - Integration Testing\n      - Mainframe\n      - Test Automation\n    serviceName: Galasa\n    serviceCategory: API\n  - name: Tessia\n    baseURL: ''\n \
  \   tags:\n      - Automation\n      - Linux on Z\n      - Provisioning\n    serviceName: Tessia\n    serviceCategory: API\n  - name: GenevaERS\n    baseURL: ''\n    tags:\n      - Analytics\n      - Data Extraction\n      - z/OS\n    serviceName: GenevaERS\n    serviceCategory: API\n  - name: COBOL Check\n    baseURL: ''\n    tags:\n      - COBOL\n      - Testing\n      - TDD\n    serviceName: COBOL Check\n    serviceCategory: API\n  - name: zopen Community\n    baseURL: ''\n    tags:\n      - Open Source\n      - Package Management\n      - z/OS\n    serviceName: zopen Community\n    serviceCategory: API\n  - name: Ambitus\n    baseURL: ''\n    tags:\n      - Community\n      - Education\n      - Linux on Z\n      - z/OS\n    serviceName: Ambitus\n    serviceCategory: API\n  - name: CBT Tape\n    baseURL: ''\n    tags:\n      - Mainframe\n      - MVS\n      - Software Library\n      - z/OS\n    serviceName: CBT Tape\n    serviceCategory: API\n  - name: COBOL Programming Course\n    baseURL:\
  \ ''\n    tags:\n      - COBOL\n      - Education\n      - Training\n    serviceName: COBOL Programming Course\n    serviceCategory: API\n  - name: Software Discovery Tool\n    baseURL: ''\n    tags:\n      - Discovery\n      - IBM Z\n      - Open Source\n    serviceName: Software Discovery Tool\n    serviceCategory: API\n  - name: Mainframe Open Education\n    baseURL: ''\n    tags:\n      - Community\n      - Education\n      - Mentorship\n    serviceName: Mainframe Open Education\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/open-mainframe-project/refs/heads/main/finops/open-mainframe-project-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Native
- Education
- Enterprise
- IBM Z
- Linux Foundation
- Linux on Z
- Mainframe
- Open Source
- z/OS
- z/VM
- FinOps
- Cost Management
- FOCUS
---
