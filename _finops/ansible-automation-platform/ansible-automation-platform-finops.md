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
description: FinOps framework definition for the Ansible Automation Platform API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Ansible Automation Platform
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Ansible Automation Platform
  PublisherName: Ansible Automation Platform
  ServiceCategory: Developer Tools / API
  ServiceName: Ansible Automation Platform
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
name: Ansible Automation Platform Finops
provider_name: Ansible Automation Platform
provider_slug: ansible-automation-platform
publisher_name: Ansible Automation Platform
service_category: API
slug: ansible-automation-platform-finops
source_filename: ansible-automation-platform-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Ansible Automation Platform\nproviderId: ansible-automation-platform\npublisherName: Ansible Automation Platform\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Automation\n  - Configuration Management\n  - DevOps\n  - Infrastructure as Code\n  - Orchestration\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Ansible Automation Platform API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n\
  \      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n   \
  \   - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Ansible Automation Platform\n  ServiceCategory: Developer Tools / API\n  ProviderName: Ansible Automation Platform\n  PublisherName: Ansible Automation Platform\n  InvoiceIssuerName: Ansible Automation Platform\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Ansible Automation Controller API\n    baseURL: https://controller-host/api/v2/\n    tags:\n      - Automation\n      - Controller\n      - Jobs\n      - REST\n    serviceName: Ansible Automation Controller API\n    serviceCategory: API\n  - name: Ansible Automation Hub API\n    baseURL: https://hub-host/api/galaxy/\n    tags:\n      - Collections\n      - Content Hub\n      - REST\n      - Roles\n    serviceName: Ansible Automation Hub API\n    serviceCategory: API\n  - name: Ansible Event-Driven Automation API\n    baseURL: https://eda-host/api/eda/v1/\n\
  \    tags:\n      - EDA\n      - Event-Driven\n      - REST\n      - Rulebooks\n    serviceName: Ansible Event-Driven Automation API\n    serviceCategory: API\n  - name: Ansible Galaxy API\n    baseURL: https://galaxy.ansible.com/api/v3/\n    tags:\n      - Collections\n      - Community\n      - Galaxy\n      - REST\n      - Roles\n    serviceName: Ansible Galaxy API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ansible-automation-platform/refs/heads/main/finops/ansible-automation-platform-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automation
- Configuration Management
- DevOps
- Infrastructure as Code
- Orchestration
- FinOps
- Cost Management
- FOCUS
---
