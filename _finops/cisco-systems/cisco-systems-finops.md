---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cisco-systems-cisco-api-openapi.yml
  format: yaml
  label: Cisco DevNet API Catalog
  slug: devnet-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-systems/refs/heads/main/openapi/cisco-systems-cisco-api-openapi.yml
- filename: openapiSpec
  format: yaml
  label: Cisco Meraki Dashboard
  slug: meraki
  spec_type: OpenAPI
  url: https://api.meraki.com/api/v1/openapiSpec
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
description: FinOps framework definition for the Cisco Systems API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cisco Systems
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cisco Systems
  PublisherName: Cisco Systems
  ServiceCategory: Developer Tools / API
  ServiceName: Cisco Systems
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
name: Cisco Systems Finops
provider_name: Cisco Systems
provider_slug: cisco-systems
publisher_name: Cisco Systems
service_category: API
slug: cisco-systems-finops
source_filename: cisco-systems-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cisco Systems\nproviderId: cisco-systems\npublisherName: Cisco Systems\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Collaboration\n  - Infrastructure\n  - Networking\n  - Security\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cisco Systems API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call\
  \ with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n    \
  \  - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cisco Systems\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cisco Systems\n  PublisherName: Cisco Systems\n  InvoiceIssuerName: Cisco Systems\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Cisco DevNet API Catalog\n    baseURL: https://developer.cisco.com/api\n    tags:\n      - Collaboration\n      - DevNet\n      - Infrastructure\n      - Networking\n      - Security\n    serviceName: Cisco DevNet API Catalog\n    serviceCategory: API\n  - name: Cisco Catalyst Center\n    baseURL: ''\n    tags:\n      - Catalyst\n      - DNA Center\n      - Network Management\n      - SDN\n    serviceName: Cisco Catalyst Center\n    serviceCategory: API\n  - name: Cisco Meraki Dashboard\n    baseURL: https://api.meraki.com/api/v1\n    tags:\n      - Cloud Managed\n      - Dashboard\n      - Wireless\n    serviceName: Cisco Meraki Dashboard\n    serviceCategory: API\n  - name:\
  \ Cisco Webex Platform\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Collaboration\n      - Meetings\n      - Messaging\n      - Webex\n    serviceName: Cisco Webex Platform\n    serviceCategory: API\n  - name: Cisco Secure Firewall Management Center\n    baseURL: ''\n    tags:\n      - Firewall\n      - FTD\n      - Security\n    serviceName: Cisco Secure Firewall Management Center\n    serviceCategory: API\n  - name: Cisco ThousandEyes API\n    baseURL: https://api.thousandeyes.com/v7\n    tags:\n      - Digital Experience\n      - Network Monitoring\n      - Observability\n    serviceName: Cisco ThousandEyes API\n    serviceCategory: API\n  - name: Cisco AppDynamics API\n    baseURL: ''\n    tags:\n      - APM\n      - Application Monitoring\n      - Observability\n    serviceName: Cisco AppDynamics API\n    serviceCategory: API\n  - name: Cisco Intersight API\n    baseURL: https://intersight.com/api/v1\n    tags:\n      - Cloud Management\n      - HyperFlex\n      - Infrastructure\n\
  \      - UCS\n    serviceName: Cisco Intersight API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-systems/refs/heads/main/finops/cisco-systems-finops.yml
sources: []
specification: FinOps Framework
tags:
- Collaboration
- Infrastructure
- Networking
- Security
- FinOps
- Cost Management
- FOCUS
---
