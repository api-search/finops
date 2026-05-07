---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Veritas Volume Manager REST API
  slug: ''
  spec_type: OpenAPI
  url: https://api.veritas.com/vvm/v1/openapi.json
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
description: FinOps framework definition for the Veritas Volume Manager API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Veritas Volume Manager
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Veritas Volume Manager
  PublisherName: Veritas Volume Manager
  ServiceCategory: Developer Tools / API
  ServiceName: Veritas Volume Manager
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
name: Veritas Volume Manager Finops
provider_name: Veritas Volume Manager
provider_slug: veritas-volume-manager
publisher_name: Veritas Volume Manager
service_category: API
slug: veritas-volume-manager-finops
source_filename: veritas-volume-manager-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Veritas Volume Manager\nproviderId: veritas-volume-manager\npublisherName: Veritas Volume Manager\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Disaster Recovery\n  - Enterprise Storage\n  - File Systems\n  - Storage\n  - Volume Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Veritas Volume Manager API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Veritas Volume Manager\n  ServiceCategory: Developer Tools / API\n  ProviderName: Veritas Volume Manager\n  PublisherName: Veritas Volume Manager\n  InvoiceIssuerName: Veritas Volume Manager\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Veritas Volume Manager REST API\n    baseURL: https://api.veritas.com/vvm/v1\n    tags:\n      - Disk Groups\n      - Snapshots\n      - Storage Pools\n      - Volumes\n    serviceName: Veritas Volume Manager REST API\n    serviceCategory: API\n  - name: VxVM Command Line API\n    baseURL: ''\n    tags:\n      - Administration\n      - CLI\n      - Scripting\n    serviceName: VxVM Command Line API\n    serviceCategory: API\n  - name: Storage Foundation API\n    baseURL: https://api.veritas.com/sf/v1\n    tags:\n      - Enterprise\n      - High Availability\n      - Storage Foundation\n\
  \    serviceName: Storage Foundation API\n    serviceCategory: API\n  - name: Veritas InfoScale REST API\n    baseURL: ''\n    tags:\n      - Cluster Management\n      - High Availability\n      - Infoscale\n      - REST\n      - Storage Configuration\n    serviceName: Veritas InfoScale REST API\n    serviceCategory: API\n  - name: Veritas InfoScale 9.0 REST API\n    baseURL: ''\n    tags:\n      - Enterprise\n      - Infoscale\n      - REST\n      - Storage Management\n    serviceName: Veritas InfoScale 9.0 REST API\n    serviceCategory: API\n  - name: InfoScale Operations Manager Web Services API\n    baseURL: ''\n    tags:\n      - Management\n      - Monitoring\n      - Operations Manager\n      - VIOM\n      - Web Services\n    serviceName: InfoScale Operations Manager Web Services API\n    serviceCategory: API\n  - name: InfoScale for Kubernetes API\n    baseURL: ''\n    tags:\n      - Cloud Native\n      - Containers\n      - CSI\n      - Kubernetes\n      - Openshift\n    serviceName:\
  \ InfoScale for Kubernetes API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n  - name: Veritas Technologies LLC\n    email: api-support@veritas.com\n    url: https://www.veritas.com\n  - name: API Team\n    email: api-team@veritas.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veritas-volume-manager/refs/heads/main/finops/veritas-volume-manager-finops.yml
sources: []
specification: FinOps Framework
tags:
- Disaster Recovery
- Enterprise Storage
- File Systems
- Storage
- Volume Management
- FinOps
- Cost Management
- FOCUS
---
