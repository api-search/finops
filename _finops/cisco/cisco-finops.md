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
description: FinOps framework definition for the Cisco API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cisco
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cisco
  PublisherName: Cisco
  ServiceCategory: Developer Tools / API
  ServiceName: Cisco
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
name: Cisco Finops
provider_name: Cisco
provider_slug: cisco
publisher_name: Cisco
service_category: API
slug: cisco-finops
source_filename: cisco-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cisco\nproviderId: cisco\npublisherName: Cisco\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Collaboration\n  - Enterprise\n  - Networking\n  - Security\n  - SD-WAN\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cisco API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team,\
  \ environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n\
  \      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cisco\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cisco\n  PublisherName: Cisco\n  InvoiceIssuerName: Cisco\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n  \
  \    - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Cisco Meraki Dashboard API\n    baseURL: https://api.meraki.com/api/v1\n    tags:\n      - Cloud Managed\n      - Meraki\n      - Network Management\n      - REST\n    serviceName: Cisco Meraki Dashboard API\n    serviceCategory: API\n  - name: Cisco Webex API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Collaboration\n      - Meetings\n      - Messaging\n      - REST\n      - Webex\n    serviceName: Cisco Webex API\n    serviceCategory: API\n  - name: Cisco Catalyst Center API\n    baseURL: https://sandboxdnac.cisco.com/dna\n    tags:\n      - Catalyst Center\n      - Intent-Based Networking\n      - Network Automation\n      - REST\n    serviceName: Cisco Catalyst Center API\n    serviceCategory: API\n  - name: Cisco\
  \ ACI API\n    baseURL: https://apic-ip/api\n    tags:\n      - ACI\n      - Data Center\n      - Fabric\n      - REST\n      - SDN\n    serviceName: Cisco ACI API\n    serviceCategory: API\n  - name: Cisco ISE API\n    baseURL: https://ise-server/ers\n    tags:\n      - Identity\n      - ISE\n      - Network Access\n      - REST\n      - Security\n    serviceName: Cisco ISE API\n    serviceCategory: API\n  - name: Cisco Intersight API\n    baseURL: https://intersight.com/api/v1\n    tags:\n      - Cloud Operations\n      - Infrastructure\n      - Intersight\n      - REST\n    serviceName: Cisco Intersight API\n    serviceCategory: API\n  - name: Cisco SD-WAN API\n    baseURL: https://vmanage-ip/dataservice\n    tags:\n      - REST\n      - SD-WAN\n      - WAN\n    serviceName: Cisco SD-WAN API\n    serviceCategory: API\n  - name: Cisco ThousandEyes API\n    baseURL: https://api.thousandeyes.com/v7\n    tags:\n      - Digital Experience\n      - Monitoring\n      - Network Visibility\n\
  \      - REST\n      - ThousandEyes\n    serviceName: Cisco ThousandEyes API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco/refs/heads/main/finops/cisco-finops.yml
sources: []
specification: FinOps Framework
tags:
- Collaboration
- Enterprise
- Networking
- Security
- SD-WAN
- FinOps
- Cost Management
- FOCUS
---
