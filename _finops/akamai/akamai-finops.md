---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: akamai-edgekv-openapi.json
  format: json
  label: Akamai EdgeKV API
  slug: akamai-edgekv-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/akamai/refs/heads/main/openapi/akamai-edgekv-openapi.json
- filename: akamai-edgeworkers-openapi.json
  format: json
  label: Akamai EdgeWorkers API
  slug: akamai-edgeworkers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/akamai/refs/heads/main/openapi/akamai-edgeworkers-openapi.json
- filename: akamai-network-lists-openapi.json
  format: json
  label: Akamai Network Lists API
  slug: akamai-network-lists-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/akamai/refs/heads/main/openapi/akamai-network-lists-openapi.json
- filename: akamai-papi-openapi.json
  format: json
  label: Akamai Property Manager API
  slug: akamai-property-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/akamai/refs/heads/main/openapi/akamai-papi-openapi.json
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
description: FinOps framework definition for the Akamai API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Akamai
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Akamai
  PublisherName: Akamai
  ServiceCategory: Developer Tools / API
  ServiceName: Akamai
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
name: Akamai Finops
provider_name: Akamai
provider_slug: akamai
publisher_name: Akamai
service_category: API
slug: akamai-finops
source_filename: akamai-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Akamai\nproviderId: akamai\npublisherName: Akamai\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - CDN\n  - Cloud\n  - Edge Computing\n  - Networks\n  - Platform\n  - Security\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Akamai API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Akamai\n  ServiceCategory: Developer Tools / API\n  ProviderName: Akamai\n  PublisherName: Akamai\n  InvoiceIssuerName: Akamai\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Akamai Access Revocation API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Access Revocation API\n    serviceCategory: API\n  - name: Akamai Adaptive Acceleration API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Adaptive Acceleration API\n    serviceCategory: API\n  - name: Akamai MFA API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai MFA API\n    serviceCategory: API\n  - name: Akamai Alerts API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Alerts API\n    serviceCategory: API\n  - name: Akamai API Endpoint Definition API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai API Endpoint Definition API\n    serviceCategory: API\n  - name: Akamai API Keys and Traffic Management\
  \ API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai API Keys and Traffic Management API\n    serviceCategory: API\n  - name: Akamai Application Security API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Application Security API\n    serviceCategory: API\n  - name: Akamai Aura Infrastructure API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Aura Infrastructure API\n    serviceCategory: API\n  - name: Akamai Aura LCDN Content Control API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Aura LCDN Content Control API\n    serviceCategory: API\n  - name: Akamai Aura LCDN Content Delivery API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Aura LCDN Content Delivery API\n    serviceCategory: API\n  - name: Akamai Aura LCDN Deployment API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Aura LCDN Deployment API\n    serviceCategory: API\n  - name: Akamai Aura LCDN Mapping API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Aura LCDN\
  \ Mapping API\n    serviceCategory: API\n  - name: Akamai Aura LCDN Services API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Aura LCDN Services API\n    serviceCategory: API\n  - name: Akamai Aura Log Streaming API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Aura Log Streaming API\n    serviceCategory: API\n  - name: Akamai Aura Network Policy API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Aura Network Policy API\n    serviceCategory: API\n  - name: Akamai Aura Secret Management API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Aura Secret Management API\n    serviceCategory: API\n  - name: Akamai Case Management API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Case Management API\n    serviceCategory: API\n  - name: Akamai Certificate Provisioning System API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Certificate Provisioning System API\n    serviceCategory: API\n  - name: Akamai Client Access Control API\n    baseURL:\
  \ ''\n    tags: []\n    serviceName: Akamai Client Access Control API\n    serviceCategory: API\n  - name: Akamai Cloud Access Manager API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Cloud Access Manager API\n    serviceCategory: API\n  - name: Akamai Cloud Wrapper Configuration API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Cloud Wrapper Configuration API\n    serviceCategory: API\n  - name: Akamai Cloudlets API V3\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Cloudlets API V3\n    serviceCategory: API\n  - name: Akamai CloudTest API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai CloudTest API\n    serviceCategory: API\n  - name: Akamai Contract API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Contract API\n    serviceCategory: API\n  - name: Akamai CP Codes and Reporting Groups API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai CP Codes and Reporting Groups API\n    serviceCategory: API\n  - name: Akamai DataStream 2 API\
  \ V2\n    baseURL: ''\n    tags: []\n    serviceName: Akamai DataStream 2 API V2\n    serviceCategory: API\n  - name: Akamai Edge Diagnostics API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Edge Diagnostics API\n    serviceCategory: API\n  - name: Akamai Edge DNS API V2\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Edge DNS API V2\n    serviceCategory: API\n  - name: Akamai EdgeKV API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai EdgeKV API\n    serviceCategory: API\n  - name: Akamai EdgeWorkers API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai EdgeWorkers API\n    serviceCategory: API\n  - name: Akamai Enhanced Content Control Utility (ECCU) API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Enhanced Content Control Utility (ECCU) API\n    serviceCategory: API\n  - name: Akamai Enterprise Application Access API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Enterprise Application Access API\n    serviceCategory: API\n  - name:\
  \ Akamai Event Center API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Event Center API\n    serviceCategory: API\n  - name: Akamai Event Viewer API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Event Viewer API\n    serviceCategory: API\n  - name: Akamai Fast Purge API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Fast Purge API\n    serviceCategory: API\n  - name: Akamai Firewall Rules Notification API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Firewall Rules Notification API\n    serviceCategory: API\n  - name: Akamai Global Traffic Management API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Global Traffic Management API\n    serviceCategory: API\n  - name: Akamai Global Traffic Management Load Feedback API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Global Traffic Management Load Feedback API\n    serviceCategory: API\n  - name: Akamai Global Traffic Management Reporting API\n    baseURL: ''\n    tags: []\n    serviceName:\
  \ Akamai Global Traffic Management Reporting API\n    serviceCategory: API\n  - name: Akamai Identity and Access Management API V3\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Identity and Access Management API V3\n    serviceCategory: API\n  - name: Akamai Identity Cloud Authentication API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Identity Cloud Authentication API\n    serviceCategory: API\n  - name: Akamai Identity Cloud Configuration API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Identity Cloud Configuration API\n    serviceCategory: API\n  - name: Akamai Identity Cloud Custom Provider API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Identity Cloud Custom Provider API\n    serviceCategory: API\n  - name: Akamai Identity Cloud Entity and EntityType API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Identity Cloud Entity and EntityType API\n    serviceCategory: API\n  - name: Akamai Identity Cloud Hosted Login API\n    baseURL:\
  \ ''\n    tags: []\n    serviceName: Akamai Identity Cloud Hosted Login API\n    serviceCategory: API\n  - name: Akamai Identity Cloud SIEM Event Service API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Identity Cloud SIEM Event Service API\n    serviceCategory: API\n  - name: Akamai Identity Cloud Social API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Identity Cloud Social API\n    serviceCategory: API\n  - name: Akamai Identity Cloud Webhooks V3 API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Identity Cloud Webhooks V3 API\n    serviceCategory: API\n  - name: Akamai Image and Video Manager API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Image and Video Manager API\n    serviceCategory: API\n  - name: Akamai Invoicing API V4\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Invoicing API V4\n    serviceCategory: API\n  - name: Akamai Ion\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Ion\n    serviceCategory: API\n  - name:\
  \ Akamai IoT OTA Updates API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai IoT OTA Updates API\n    serviceCategory: API\n  - name: Akamai IoT Token Access Control API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai IoT Token Access Control API\n    serviceCategory: API\n  - name: Akamai Linode API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Linode API\n    serviceCategory: API\n  - name: Akamai Live Archive Management API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Live Archive Management API\n    serviceCategory: API\n  - name: Akamai Media Delivery Reports API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Media Delivery Reports API\n    serviceCategory: API\n  - name: Akamai Media Services Live Reports API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Media Services Live Reports API\n    serviceCategory: API\n  - name: Akamai Media Services Live Stream Provisioning API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai\
  \ Media Services Live Stream Provisioning API\n    serviceCategory: API\n  - name: Akamai mPulse API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai mPulse API\n    serviceCategory: API\n  - name: Akamai Mutual TLS Edge Truststore API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Mutual TLS Edge Truststore API\n    serviceCategory: API\n  - name: Akamai Mutual TLS Origin Keystore API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Mutual TLS Origin Keystore API\n    serviceCategory: API\n  - name: Akamai NetStorage Configuration API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai NetStorage Configuration API\n    serviceCategory: API\n  - name: Akamai NetStorage Usage API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai NetStorage Usage API\n    serviceCategory: API\n  - name: Akamai Network Lists API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Network Lists API\n    serviceCategory: API\n  - name: Akamai Prolexic Analytics API\n   \
  \ baseURL: ''\n    tags: []\n    serviceName: Akamai Prolexic Analytics API\n    serviceCategory: API\n  - name: Akamai Prolexic IP Protect Configuration API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Prolexic IP Protect Configuration API\n    serviceCategory: API\n  - name: Akamai Property Manager API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Property Manager API\n    serviceCategory: API\n  - name: Akamai Reporting API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Reporting API\n    serviceCategory: API\n  - name: Akamai Sandbox API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Sandbox API\n    serviceCategory: API\n  - name: Akamai Script Management API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Script Management API\n    serviceCategory: API\n  - name: Akamai Secure Internet Access Enterprise Configuration API V3\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Secure Internet Access Enterprise Configuration API V3\n\
  \    serviceCategory: API\n  - name: Akamai Secure Internet Access Enterprise Reporting API V3\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Secure Internet Access Enterprise Reporting API V3\n    serviceCategory: API\n  - name: Akamai Service-Level Agreement API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Service-Level Agreement API\n    serviceCategory: API\n  - name: Akamai SIEM Integration API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai SIEM Integration API\n    serviceCategory: API\n  - name: Akamai Single Sign-On Configuration API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Single Sign-On Configuration API\n    serviceCategory: API\n  - name: Akamai Site Shield API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Site Shield API\n    serviceCategory: API\n  - name: Akamai Test Center API\n    baseURL: ''\n    tags: []\n    serviceName: Akamai Test Center API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n\
  \    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/akamai/refs/heads/main/finops/akamai-finops.yml
sources: []
specification: FinOps Framework
tags:
- CDN
- Cloud
- Edge Computing
- Networks
- Platform
- Security
- FinOps
- Cost Management
- FOCUS
---
