---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: juniper-networks-apstra-openapi.yml
  format: yaml
  label: Juniper Apstra API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/openapi/juniper-networks-apstra-openapi.yml
- filename: juniper-networks-junos-telemetry-asyncapi.yml
  format: yaml
  label: Junos XML API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/asyncapi/juniper-networks-junos-telemetry-asyncapi.yml
- filename: juniper-networks-mist-openapi.yml
  format: yaml
  label: Juniper Mist API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/openapi/juniper-networks-mist-openapi.yml
- filename: juniper-networks-contrail-openapi.yml
  format: yaml
  label: Juniper Contrail API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/openapi/juniper-networks-contrail-openapi.yml
- filename: juniper-networks-junos-space-openapi.yml
  format: yaml
  label: Junos Space REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/openapi/juniper-networks-junos-space-openapi.yml
- filename: juniper-networks-vsrx-openapi.yml
  format: yaml
  label: Juniper vSRX REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/openapi/juniper-networks-vsrx-openapi.yml
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
description: FinOps framework definition for the Juniper Networks API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Juniper Networks
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Juniper Networks
  PublisherName: Juniper Networks
  ServiceCategory: Developer Tools / API
  ServiceName: Juniper Networks
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
name: Juniper Networks Finops
provider_name: Juniper Networks
provider_slug: juniper-networks
publisher_name: Juniper Networks
service_category: API
slug: juniper-networks-finops
source_filename: juniper-networks-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Juniper Networks\nproviderId: juniper-networks\npublisherName: Juniper Networks\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Automation\n  - Cloud\n  - Data Center\n  - Enterprise\n  - Networking\n  - SDN\n  - Security\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Juniper Networks API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Juniper Networks\n  ServiceCategory: Developer Tools / API\n  ProviderName: Juniper Networks\n  PublisherName: Juniper Networks\n  InvoiceIssuerName: Juniper Networks\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Juniper Apstra API\n    baseURL: https://<apstra-server>/api\n    tags:\n      - Automation\n      - Data Center\n      - Intent-Based Networking\n      - Networking\n    serviceName: Juniper Apstra API\n    serviceCategory: API\n  - name: Junos PyEZ\n    baseURL: netconf://device:830\n    tags:\n      - Automation\n      - Junos\n      - NETCONF\n      - Python\n    serviceName: Junos PyEZ\n    serviceCategory: API\n  - name: Junos XML API\n    baseURL: netconf://device:830\n    tags:\n      - Automation\n      - Junos\n      - NETCONF\n      - XML\n    serviceName: Junos XML API\n    serviceCategory: API\n  - name: Juniper Mist API\n\
  \    baseURL: https://api.mist.com/api/v1\n    tags:\n      - AI\n      - Cloud\n      - Network Management\n      - SD-WAN\n      - Wireless\n    serviceName: Juniper Mist API\n    serviceCategory: API\n  - name: Juniper Contrail API\n    baseURL: https://<contrail-controller>:8082\n    tags:\n      - NFV\n      - Orchestration\n      - SDN\n      - Virtual Networks\n    serviceName: Juniper Contrail API\n    serviceCategory: API\n  - name: Junos Space REST API\n    baseURL: https://<space-server>/api/space\n    tags:\n      - Network Management\n      - Orchestration\n      - REST\n    serviceName: Junos Space REST API\n    serviceCategory: API\n  - name: Juniper JSNAPy\n    baseURL: https://github.com/Juniper/jsnapy\n    tags:\n      - Automation\n      - Configuration Management\n      - Python\n      - Testing\n    serviceName: Juniper JSNAPy\n    serviceCategory: API\n  - name: Juniper vSRX REST API\n    baseURL: https://<vsrx-device>/api\n    tags:\n      - Firewall\n      - REST\n\
  \      - Security\n      - Virtual\n    serviceName: Juniper vSRX REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/finops/juniper-networks-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automation
- Cloud
- Data Center
- Enterprise
- Networking
- SDN
- Security
- FinOps
- Cost Management
- FOCUS
---
