---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openstack-keystone-openapi.yml
  format: yaml
  label: OpenStack Identity (Keystone) API
  slug: keystone
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openstack/refs/heads/main/openapi/openstack-keystone-openapi.yml
- filename: openstack-nova-openapi.yml
  format: yaml
  label: OpenStack Compute (Nova) API
  slug: nova
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openstack/refs/heads/main/openapi/openstack-nova-openapi.yml
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
description: FinOps framework definition for the OpenStack API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: OpenStack
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: OpenStack
  PublisherName: OpenStack
  ServiceCategory: Developer Tools / API
  ServiceName: OpenStack
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
name: Openstack Finops
provider_name: OpenStack
provider_slug: openstack
publisher_name: OpenStack
service_category: API
slug: openstack-finops
source_filename: openstack-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: OpenStack\nproviderId: openstack\npublisherName: OpenStack\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Platform\n  - Infrastructure as a Service\n  - Open Source\n  - Virtualization\n  - Linux Foundation\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the OpenStack API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: OpenStack\n  ServiceCategory: Developer Tools / API\n  ProviderName: OpenStack\n  PublisherName: OpenStack\n  InvoiceIssuerName: OpenStack\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: OpenStack Identity (Keystone) API\n    baseURL: https://{keystone-host}:5000/v3\n    tags:\n      - Identity\n      - Authentication\n      - Authorization\n      - Service Catalog\n    serviceName: OpenStack Identity (Keystone) API\n    serviceCategory: API\n  - name: OpenStack Compute (Nova) API\n    baseURL: https://{nova-host}/compute/v2.1\n    tags:\n      - Compute\n      - Virtual Machines\n      - Bare Metal\n    serviceName: OpenStack Compute (Nova) API\n    serviceCategory: API\n  - name: OpenStack Networking (Neutron) API\n    baseURL: https://{neutron-host}/networking/v2.0\n    tags:\n      - Networking\n      - SDN\n      - Security Groups\n    serviceName:\
  \ OpenStack Networking (Neutron) API\n    serviceCategory: API\n  - name: OpenStack Block Storage (Cinder) API\n    baseURL: https://{cinder-host}/volume/v3\n    tags:\n      - Block Storage\n      - Volumes\n      - Snapshots\n    serviceName: OpenStack Block Storage (Cinder) API\n    serviceCategory: API\n  - name: OpenStack Object Storage (Swift) API\n    baseURL: https://{swift-host}/v1/AUTH_{tenant_id}\n    tags:\n      - Object Storage\n      - Containers\n      - Replication\n    serviceName: OpenStack Object Storage (Swift) API\n    serviceCategory: API\n  - name: OpenStack Image (Glance) API\n    baseURL: https://{glance-host}/image/v2\n    tags:\n      - Images\n      - Disk Images\n    serviceName: OpenStack Image (Glance) API\n    serviceCategory: API\n  - name: OpenStack Orchestration (Heat) API\n    baseURL: https://{heat-host}/heat-api/v1\n    tags:\n      - Orchestration\n      - Infrastructure as Code\n    serviceName: OpenStack Orchestration (Heat) API\n    serviceCategory:\
  \ API\n  - name: OpenStack Load Balancer (Octavia) API\n    baseURL: https://{octavia-host}/load-balancer/v2\n    tags:\n      - Load Balancer\n      - LBaaS\n    serviceName: OpenStack Load Balancer (Octavia) API\n    serviceCategory: API\n  - name: OpenStack DNS (Designate) API\n    baseURL: https://{designate-host}/dns/v2\n    tags:\n      - DNS\n      - DNSaaS\n    serviceName: OpenStack DNS (Designate) API\n    serviceCategory: API\n  - name: OpenStack Database (Trove) API\n    baseURL: https://{trove-host}/database/v1.0\n    tags:\n      - Database\n      - DBaaS\n    serviceName: OpenStack Database (Trove) API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openstack/refs/heads/main/finops/openstack-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Platform
- Infrastructure as a Service
- Open Source
- Virtualization
- Linux Foundation
- FinOps
- Cost Management
- FOCUS
---
