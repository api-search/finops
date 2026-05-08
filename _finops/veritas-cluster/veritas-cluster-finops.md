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
  label: Veritas Cluster Server REST API
  slug: ''
  spec_type: OpenAPI
  url: https://vcs-server:14150/api/docs/openapi.json
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
description: FinOps framework definition for the Veritas Cluster Server API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Veritas Cluster Server
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Veritas Cluster Server
  PublisherName: Veritas Cluster Server
  ServiceCategory: Developer Tools / API
  ServiceName: Veritas Cluster Server
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
name: Veritas Cluster Finops
provider_name: Veritas Cluster Server
provider_slug: veritas-cluster
publisher_name: Veritas Cluster Server
service_category: API
slug: veritas-cluster-finops
source_filename: veritas-cluster-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Veritas Cluster Server\nproviderId: veritas-cluster\npublisherName: Veritas Cluster Server\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Clustering\n  - Containers\n  - Disaster Recovery\n  - Failover\n  - High Availability\n  - InfoScale\n  - Infrastructure Management\n  - Kubernetes\n  - Storage Management\n  - Veritas\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Veritas Cluster Server API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs\
  \ visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n   \
  \   - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Veritas Cluster Server\n  ServiceCategory: Developer Tools / API\n  ProviderName: Veritas Cluster Server\n  PublisherName: Veritas Cluster Server\n  InvoiceIssuerName: Veritas Cluster Server\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Veritas Cluster Server REST API\n    baseURL: https://{vcs-management-server}:14150/api/v1\n    tags:\n      - Cluster Management\n      - Resources\n      - REST\n      - Service Groups\n    serviceName: Veritas Cluster Server REST API\n    serviceCategory: API\n  - name: Veritas Cluster Server Python API\n    baseURL: https://{vcs-management-server}:14150\n    tags:\n      - Automation\n      - Python\n      - Scripting\n      - SDK\n    serviceName: Veritas Cluster Server Python API\n    serviceCategory:\
  \ API\n  - name: Veritas Cluster Server Java API\n    baseURL: ''\n    tags:\n      - Enterprise Integration\n      - Java\n      - SDK\n    serviceName: Veritas Cluster Server Java API\n    serviceCategory: API\n  - name: Veritas Cluster Server Command Line Interface\n    baseURL: ''\n    tags:\n      - Administration\n      - CLI\n      - Command Line\n      - Monitoring\n    serviceName: Veritas Cluster Server Command Line Interface\n    serviceCategory: API\n  - name: Veritas Cluster Server SNMP Agent\n    baseURL: ''\n    tags:\n      - Alerting\n      - Monitoring\n      - SNMP\n      - Traps\n    serviceName: Veritas Cluster Server SNMP Agent\n    serviceCategory: API\n  - name: Veritas InfoScale REST API\n    baseURL: https://{infoscale-rest-server}:14150/infoscale/api/2.0\n    tags:\n      - Cluster Management\n      - InfoScale\n      - REST\n      - Storage Management\n      - Volume Management\n    serviceName: Veritas InfoScale REST API\n    serviceCategory: API\n  - name:\
  \ Veritas InfoScale Operations Manager Web Services API\n    baseURL: https://{management-server}:14161/vom/api\n    tags:\n      - Management\n      - Monitoring\n      - Operations Manager\n      - REST\n      - VIOM\n      - Web Services\n    serviceName: Veritas InfoScale Operations Manager Web Services API\n    serviceCategory: API\n  - name: Veritas InfoScale for Kubernetes Environments\n    baseURL: ''\n    tags:\n      - Containers\n      - CSI\n      - Kubernetes\n      - Monitoring\n      - OpenShift\n      - Prometheus\n      - Storage Provisioning\n    serviceName: Veritas InfoScale for Kubernetes Environments\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    X-github: kinlane\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veritas-cluster/refs/heads/main/finops/veritas-cluster-finops.yml
sources: []
specification: FinOps Framework
tags:
- Clustering
- Containers
- Disaster Recovery
- Failover
- High Availability
- InfoScale
- Infrastructure Management
- Kubernetes
- Storage Management
- Veritas
- FinOps
- Cost Management
- FOCUS
---
