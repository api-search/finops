---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mcafee-epo-openapi.yml
  format: yaml
  label: McAfee ePO API
  slug: mcafee-epo-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mcafee/refs/heads/main/openapi/mcafee-epo-openapi.yml
- filename: mcafee-mvision-openapi.yml
  format: yaml
  label: McAfee MVISION API
  slug: mcafee-mvision-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mcafee/refs/heads/main/openapi/mcafee-mvision-openapi.yml
- filename: mcafee-web-gateway-openapi.yml
  format: yaml
  label: McAfee Web Gateway API
  slug: mcafee-web-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mcafee/refs/heads/main/openapi/mcafee-web-gateway-openapi.yml
- filename: mcafee-esm-openapi.yml
  format: yaml
  label: McAfee ESM API
  slug: mcafee-esm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mcafee/refs/heads/main/openapi/mcafee-esm-openapi.yml
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
description: FinOps framework definition for the McAfee (Trellix) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: McAfee (Trellix)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: McAfee (Trellix)
  PublisherName: McAfee (Trellix)
  ServiceCategory: Developer Tools / API
  ServiceName: McAfee (Trellix)
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
name: Mcafee Finops
provider_name: McAfee (Trellix)
provider_slug: mcafee
publisher_name: McAfee (Trellix)
service_category: API
slug: mcafee-finops
source_filename: mcafee-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: McAfee (Trellix)\nproviderId: mcafee\npublisherName: McAfee (Trellix)\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Antivirus\n  - Cybersecurity\n  - Endpoint Protection\n  - Security\n  - Threat Intelligence\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the McAfee (Trellix) API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: McAfee (Trellix)\n  ServiceCategory: Developer Tools / API\n  ProviderName: McAfee (Trellix)\n  PublisherName: McAfee (Trellix)\n  InvoiceIssuerName: McAfee (Trellix)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: McAfee ePO API\n    baseURL: https://your-epo-server:8443/remote\n    tags:\n      - Endpoint Management\n      - Policy Orchestrator\n      - Security Management\n    serviceName: McAfee ePO API\n    serviceCategory: API\n  - name: McAfee MVISION API\n    baseURL: https://api.mvision.mcafee.com\n    tags:\n      - Cloud Security\n      - EDR\n      - MVISION\n      - Threat Detection\n    serviceName: McAfee MVISION API\n    serviceCategory: API\n  - name: McAfee Threat Intelligence Exchange (TIE) API\n    baseURL: https://your-tie-server/api\n    tags:\n      - Malware Analysis\n      - Reputation\n      - Threat Intelligence\n    serviceName:\
  \ McAfee Threat Intelligence Exchange (TIE) API\n    serviceCategory: API\n  - name: McAfee Data Exchange Layer (DXL) API\n    baseURL: https://your-dxl-broker\n    tags:\n      - Data Exchange\n      - Fabric\n      - Integration\n      - Messaging\n    serviceName: McAfee Data Exchange Layer (DXL) API\n    serviceCategory: API\n  - name: McAfee Web Gateway API\n    baseURL: https://your-mwg-server/Konfigurator/REST\n    tags:\n      - Proxy\n      - Web Gateway\n      - Web Security\n    serviceName: McAfee Web Gateway API\n    serviceCategory: API\n  - name: McAfee ESM API\n    baseURL: https://your-esm-server/rs/esm\n    tags:\n      - Log Management\n      - Security Events\n      - SIEM\n    serviceName: McAfee ESM API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n\
  \    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mcafee/refs/heads/main/finops/mcafee-finops.yml
sources: []
specification: FinOps Framework
tags:
- Antivirus
- Cybersecurity
- Endpoint Protection
- Security
- Threat Intelligence
- FinOps
- Cost Management
- FOCUS
---
