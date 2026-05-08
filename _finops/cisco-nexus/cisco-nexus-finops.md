---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cisco-nexus-nxapi-rest.yml
  format: yaml
  label: Cisco NX-API REST
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-nexus/refs/heads/main/openapi/cisco-nexus-nxapi-rest.yml
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
description: FinOps framework definition for the Cisco Nexus Dashboard API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cisco Nexus Dashboard
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cisco Nexus Dashboard
  PublisherName: Cisco Nexus Dashboard
  ServiceCategory: Developer Tools / API
  ServiceName: Cisco Nexus Dashboard
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
name: Cisco Nexus Finops
provider_name: Cisco Nexus Dashboard
provider_slug: cisco-nexus
publisher_name: Cisco Nexus Dashboard
service_category: API
slug: cisco-nexus-finops
source_filename: cisco-nexus-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cisco Nexus Dashboard\nproviderId: cisco-nexus\npublisherName: Cisco Nexus Dashboard\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Data Center\n  - Infrastructure\n  - Network Automation\n  - Networking\n  - SDN\n  - Switches\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cisco Nexus Dashboard API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cisco Nexus Dashboard\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cisco Nexus Dashboard\n  PublisherName: Cisco Nexus Dashboard\n  InvoiceIssuerName: Cisco Nexus Dashboard\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Cisco NX-API REST\n    baseURL: https://{switch-ip}/api\n    tags:\n      - CLI\n      - Configuration\n      - Monitoring\n      - REST\n    serviceName: Cisco NX-API REST\n    serviceCategory: API\n  - name: Cisco NX-API CLI\n    baseURL: https://{switch-ip}/ins\n    tags:\n      - CLI\n      - Configuration\n      - Show Commands\n    serviceName: Cisco NX-API CLI\n    serviceCategory: API\n  - name: Cisco Nexus Dashboard REST API\n    baseURL: https://{nexus-dashboard}/api/v1\n    tags:\n      - ACI\n      - Dashboard\n      - Fabric Controller\n      - Insights\n      - Orchestration\n    serviceName:\
  \ Cisco Nexus Dashboard REST API\n    serviceCategory: API\n  - name: Cisco Nexus Dashboard Fabric Controller API\n    baseURL: https://{nexus-dashboard}/appcenter/cisco/ndfc/api/v1\n    tags:\n      - EVPN\n      - Fabric Management\n      - LAN\n      - NDFC\n      - SAN\n      - VXLAN\n    serviceName: Cisco Nexus Dashboard Fabric Controller API\n    serviceCategory: API\n  - name: Cisco Nexus Dashboard Orchestrator API\n    baseURL: https://{nexus-dashboard}/appcenter/cisco/ndo/api/v1\n    tags:\n      - ACI\n      - Multi-Site\n      - Orchestrator\n      - Policy Management\n      - Segmentation\n    serviceName: Cisco Nexus Dashboard Orchestrator API\n    serviceCategory: API\n  - name: Cisco Nexus Dashboard Insights API\n    baseURL: https://{nexus-dashboard}/appcenter/cisco/ndi/api/v1\n    tags:\n      - Analytics\n      - Anomaly Detection\n      - Insights\n      - Telemetry\n      - Troubleshooting\n    serviceName: Cisco Nexus Dashboard Insights API\n    serviceCategory: API\n\
  \  - name: Cisco DCNM REST API\n    baseURL: https://{dcnm-server}/rest\n    tags:\n      - DCNM\n      - EVPN\n      - Fabric Management\n      - VXLAN\n    serviceName: Cisco DCNM REST API\n    serviceCategory: API\n  - name: Cisco NETCONF/YANG API\n    baseURL: netconf://{switch-ip}:830\n    tags:\n      - Automation\n      - Model-Driven\n      - NETCONF\n      - YANG\n    serviceName: Cisco NETCONF/YANG API\n    serviceCategory: API\n  - name: Cisco NX-OS RESTCONF API\n    baseURL: https://{switch-ip}/restconf\n    tags:\n      - HTTP\n      - Model-Driven\n      - RESTCONF\n      - YANG\n    serviceName: Cisco NX-OS RESTCONF API\n    serviceCategory: API\n  - name: Cisco NX-OS gNMI/gRPC API\n    baseURL: grpc://{switch-ip}:50051\n    tags:\n      - gNMI\n      - gRPC\n      - Model-Driven\n      - Streaming\n      - Telemetry\n    serviceName: Cisco NX-OS gNMI/gRPC API\n    serviceCategory: API\n  - name: Cisco NX-OS Model-Driven Telemetry API\n    baseURL: grpc://{switch-ip}:50051\n\
  \    tags:\n      - Dial-Out\n      - Monitoring\n      - Streaming\n      - Telemetry\n      - YANG\n    serviceName: Cisco NX-OS Model-Driven Telemetry API\n    serviceCategory: API\n  - name: Cisco NX-OS Python SDK API\n    baseURL: https://{switch-ip}\n    tags:\n      - Automation\n      - On-Box\n      - Python\n      - SDK\n    serviceName: Cisco NX-OS Python SDK API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-nexus/refs/heads/main/finops/cisco-nexus-finops.yml
sources: []
specification: FinOps Framework
tags:
- Data Center
- Infrastructure
- Network Automation
- Networking
- SDN
- Switches
- FinOps
- Cost Management
- FOCUS
---
