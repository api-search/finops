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
description: FinOps framework definition for the Ansible Playbooks API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Ansible Playbooks
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Ansible Playbooks
  PublisherName: Ansible Playbooks
  ServiceCategory: Developer Tools / API
  ServiceName: Ansible Playbooks
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
name: Ansible Playbooks Finops
provider_name: Ansible Playbooks
provider_slug: ansible-playbooks
publisher_name: Ansible Playbooks
service_category: API
slug: ansible-playbooks-finops
source_filename: ansible-playbooks-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Ansible Playbooks\nproviderId: ansible-playbooks\npublisherName: Ansible Playbooks\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Ansible\n  - Automation\n  - Configuration Management\n  - DevOps\n  - Infrastructure As Code\n  - Orchestration\n  - Playbooks\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Ansible Playbooks API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Ansible Playbooks\n  ServiceCategory: Developer Tools / API\n  ProviderName: Ansible Playbooks\n  PublisherName: Ansible Playbooks\n  InvoiceIssuerName: Ansible Playbooks\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Ansible Automation Platform API\n    baseURL: https://your-aap-instance/api/v2/\n    tags:\n      - Ansible\n      - Automation\n      - Enterprise\n      - Jobs\n      - Orchestration\n      - Playbooks\n      - Red Hat\n    serviceName: Ansible Automation Platform API\n    serviceCategory: API\n  - name: AWX API\n    baseURL: https://your-awx-instance/api/v2/\n    tags:\n      - Ansible\n      - Automation\n      - AWX\n      - Open Source\n      - Playbooks\n    serviceName: AWX API\n    serviceCategory: API\n  - name: Ansible Runner API\n    baseURL: https://pypi.org/project/ansible-runner/\n  \
  \  tags:\n      - Ansible\n      - Automation\n      - Library\n      - Playbooks\n      - Python\n    serviceName: Ansible Runner API\n    serviceCategory: API\n  - name: Ansible Galaxy API\n    baseURL: https://galaxy.ansible.com/api/\n    tags:\n      - Ansible\n      - Collections\n      - Community\n      - Galaxy\n      - Roles\n    serviceName: Ansible Galaxy API\n    serviceCategory: API\n  - name: Ansible Automation Hub API\n    baseURL: https://console.redhat.com/api/automation-hub/\n    tags:\n      - Ansible\n      - Certified Content\n      - Collections\n      - Enterprise\n      - Red Hat\n    serviceName: Ansible Automation Hub API\n    serviceCategory: API\n  - name: Ansible Semaphore API\n    baseURL: https://your-semaphore-instance/api/\n    tags:\n      - Ansible\n      - Open Source\n      - Playbooks\n      - Semaphore\n      - Workflow\n    serviceName: Ansible Semaphore API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost\
  \ / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n    X: apievangelist\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ansible-playbooks/refs/heads/main/finops/ansible-playbooks-finops.yml
sources: []
specification: FinOps Framework
tags:
- Ansible
- Automation
- Configuration Management
- DevOps
- Infrastructure As Code
- Orchestration
- Playbooks
- FinOps
- Cost Management
- FOCUS
---
