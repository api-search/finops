---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: solaris-zones-management-openapi.yml
  format: yaml
  label: Solaris Zones Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-zones-management-openapi.yml
- filename: solaris-zone-configuration-openapi.yml
  format: yaml
  label: Zone Configuration API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-zone-configuration-openapi.yml
- filename: solaris-zone-administration-openapi.yml
  format: yaml
  label: Zone Administration API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-zone-administration-openapi.yml
- filename: solaris-zone-monitoring-openapi.yml
  format: yaml
  label: Zone Monitoring API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-zone-monitoring-openapi.yml
- filename: solaris-rad-zonemgr-openapi.yml
  format: yaml
  label: RAD Zone Management REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-rad-zonemgr-openapi.yml
- filename: solaris-zone-stats-openapi.yml
  format: yaml
  label: Zones Monitoring Statistics API (libzonestat)
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-zone-stats-openapi.yml
- filename: solaris-kernel-zones-openapi.yml
  format: yaml
  label: Oracle Solaris Kernel Zones API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-kernel-zones-openapi.yml
- filename: solaris-statsstore-openapi.yml
  format: yaml
  label: Oracle Solaris StatsStore and Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-statsstore-openapi.yml
- filename: solaris-unified-archives-openapi.yml
  format: yaml
  label: Oracle Solaris Unified Archives Zones API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-unified-archives-openapi.yml
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
description: FinOps framework definition for the Solaris Zones API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Solaris Zones
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Solaris Zones
  PublisherName: Solaris Zones
  ServiceCategory: Developer Tools / API
  ServiceName: Solaris Zones
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
name: Solaris Zones Finops
provider_name: Solaris Zones
provider_slug: solaris-zones
publisher_name: Solaris Zones
service_category: API
slug: solaris-zones-finops
source_filename: solaris-zones-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Solaris Zones\nproviderId: solaris-zones\npublisherName: Solaris Zones\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Containers\n  - Kernel Zones\n  - Operating Systems\n  - Oracle\n  - RAD\n  - Resource Management\n  - Solaris\n  - StatsStore\n  - Virtualization\n  - Zones\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Solaris Zones API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in\
  \ near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Solaris Zones\n  ServiceCategory: Developer Tools / API\n  ProviderName: Solaris Zones\n  PublisherName: Solaris Zones\n  InvoiceIssuerName: Solaris Zones\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Solaris Zones Management API\n    baseURL: https://solaris-host.example.com/api/v1\n    tags:\n      - Containers\n      - Oracle\n      - Solaris\n      - Virtualization\n      - Zones\n    serviceName: Solaris Zones Management API\n    serviceCategory: API\n  - name: Zone Configuration API\n    baseURL: https://solaris-host.example.com/api/v1/zones\n    tags:\n      - Configuration\n      - Networking\n      - Resources\n    serviceName: Zone Configuration API\n    serviceCategory: API\n  - name: Zone Administration API\n    baseURL: https://solaris-host.example.com/api/v1/zones/admin\n\
  \    tags:\n      - Administration\n      - Lifecycle\n      - Management\n    serviceName: Zone Administration API\n    serviceCategory: API\n  - name: Zone Monitoring API\n    baseURL: https://solaris-host.example.com/api/v1/zones/monitoring\n    tags:\n      - Metrics\n      - Monitoring\n      - Performance\n    serviceName: Zone Monitoring API\n    serviceCategory: API\n  - name: RAD Zone Management REST API\n    baseURL: https://solaris-host.example.com/api/com.oracle.solaris.rad.zonemgr\n    tags:\n      - Management\n      - RAD\n      - Remote Administration\n      - REST API\n      - Zones\n    serviceName: RAD Zone Management REST API\n    serviceCategory: API\n  - name: Zones Monitoring Statistics API (libzonestat)\n    baseURL: https://solaris-host.example.com/api/v1/zones/stats\n    tags:\n      - CPU\n      - Libzonestat\n      - Memory\n      - Monitoring\n      - Resource Utilization\n      - Statistics\n    serviceName: Zones Monitoring Statistics API (libzonestat)\n\
  \    serviceCategory: API\n  - name: Oracle Solaris Kernel Zones API\n    baseURL: https://solaris-host.example.com/api/v1/zones/kernel\n    tags:\n      - Isolation\n      - Kernel Zones\n      - Security\n      - Virtualization\n    serviceName: Oracle Solaris Kernel Zones API\n    serviceCategory: API\n  - name: Oracle Solaris StatsStore and Analytics API\n    baseURL: https://solaris-host.example.com/api/v1/statsstore\n    tags:\n      - Analytics\n      - Monitoring\n      - Performance\n      - REST API\n      - StatsStore\n      - Web Interface\n    serviceName: Oracle Solaris StatsStore and Analytics API\n    serviceCategory: API\n  - name: Oracle Solaris Unified Archives Zones API\n    baseURL: https://solaris-host.example.com/api/v1/zones/archives\n    tags:\n      - Backup\n      - Cloning\n      - Migration\n      - Recovery\n      - Unified Archives\n    serviceName: Oracle Solaris Unified Archives Zones API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K\
  \ Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n  - FN: Oracle Corporation\n    email: solaris-feedback@oracle.com\n    url: https://www.oracle.com/solaris/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/finops/solaris-zones-finops.yml
sources: []
specification: FinOps Framework
tags:
- Containers
- Kernel Zones
- Operating Systems
- Oracle
- RAD
- Resource Management
- Solaris
- StatsStore
- Virtualization
- Zones
- FinOps
- Cost Management
- FOCUS
---
