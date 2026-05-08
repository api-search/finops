---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi
  format: yaml
  label: Citrix Virtual Apps and Desktops REST API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.citrix.com/citrix-virtual-apps-and-desktops/citrix-cvad-rest-apis/docs/openapi
- filename: citrix-adc-nitro-openapi.yml
  format: yaml
  label: Citrix ADC (NetScaler) NITRO API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citrix/refs/heads/main/openapi/citrix-adc-nitro-openapi.yml
- filename: openapi
  format: yaml
  label: Citrix DaaS REST API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.citrix.com/citrix-daas/citrix-daas-rest-apis/docs/openapi
- filename: citrix-cloud-openapi.yml
  format: yaml
  label: Citrix Cloud API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citrix/refs/heads/main/openapi/citrix-cloud-openapi.yml
- filename: citrix-storefront-web-openapi.yml
  format: yaml
  label: Citrix StoreFront Web API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citrix/refs/heads/main/openapi/citrix-storefront-web-openapi.yml
- filename: citrix-endpoint-management-openapi.yml
  format: yaml
  label: Citrix Endpoint Management REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citrix/refs/heads/main/openapi/citrix-endpoint-management-openapi.yml
- filename: citrix-secure-private-access-openapi.yml
  format: yaml
  label: Citrix Secure Private Access API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citrix/refs/heads/main/openapi/citrix-secure-private-access-openapi.yml
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
description: FinOps framework definition for the Citrix API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Citrix
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Citrix
  PublisherName: Citrix
  ServiceCategory: Developer Tools / API
  ServiceName: Citrix
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
name: Citrix Finops
provider_name: Citrix
provider_slug: citrix
publisher_name: Citrix
service_category: API
slug: citrix-finops
source_filename: citrix-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Citrix\nproviderId: citrix\npublisherName: Citrix\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Application Delivery\n  - Desktop-As-A-Service\n  - Networking\n  - Virtualization\n  - Workspace\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Citrix API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API\
  \ call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Citrix\n  ServiceCategory: Developer Tools / API\n  ProviderName: Citrix\n  PublisherName: Citrix\n  InvoiceIssuerName: Citrix\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Citrix Virtual Apps and Desktops REST API\n    baseURL: https://{customer-id}.xendesktop.net\n    tags:\n      - Remote Access\n      - VDI\n      - Virtual Desktop\n    serviceName: Citrix Virtual Apps and Desktops REST API\n    serviceCategory: API\n  - name: Citrix Workspace API\n    baseURL: https://api.cloud.com\n    tags:\n      - SSO\n      - User Experience\n      - Workspace\n    serviceName: Citrix Workspace API\n    serviceCategory: API\n  - name: Citrix ADC (NetScaler) NITRO API\n    baseURL: https://{netscaler-ip}/nitro/v1\n    tags:\n      - ADC\n      - Application Delivery\n      - Load Balancing\n      - Networking\n    serviceName: Citrix ADC (NetScaler) NITRO API\n    serviceCategory:\
  \ API\n  - name: Citrix DaaS REST API\n    baseURL: https://api.cloud.com/cvad\n    tags:\n      - Cloud\n      - DaaS\n      - Desktop as a Service\n    serviceName: Citrix DaaS REST API\n    serviceCategory: API\n  - name: Citrix Analytics API\n    baseURL: https://api.analytics.cloud.com\n    tags:\n      - Analytics\n      - Insights\n      - Monitoring\n      - Security\n    serviceName: Citrix Analytics API\n    serviceCategory: API\n  - name: Citrix Cloud API\n    baseURL: https://api.cloud.com\n    tags:\n      - Cloud\n      - Identity\n      - Management\n      - Platform\n    serviceName: Citrix Cloud API\n    serviceCategory: API\n  - name: Citrix Monitor Service OData API\n    baseURL: https://{delivery-controller}/Citrix/Monitor/OData/v4/Data\n    tags:\n      - Analytics\n      - Monitoring\n      - OData\n      - Reporting\n    serviceName: Citrix Monitor Service OData API\n    serviceCategory: API\n  - name: Citrix StoreFront Web API\n    baseURL: https://{storefront-server}/Citrix/Store\n\
  \    tags:\n      - Client\n      - Resources\n      - Sessions\n      - StoreFront\n    serviceName: Citrix StoreFront Web API\n    serviceCategory: API\n  - name: Citrix StoreFront Store Services API\n    baseURL: https://{storefront-server}/Citrix/Store\n    tags:\n      - Customization\n      - Server\n      - StoreFront\n    serviceName: Citrix StoreFront Store Services API\n    serviceCategory: API\n  - name: Citrix StoreFront Authentication SDK\n    baseURL: https://{storefront-server}\n    tags:\n      - Authentication\n      - Identity\n      - StoreFront\n    serviceName: Citrix StoreFront Authentication SDK\n    serviceCategory: API\n  - name: Citrix Endpoint Management REST API\n    baseURL: https://{xms-server}:4443/xenmobile/api/v1\n    tags:\n      - Endpoint Management\n      - MDM\n      - Mobile\n      - UEM\n    serviceName: Citrix Endpoint Management REST API\n    serviceCategory: API\n  - name: Citrix Secure Private Access API\n    baseURL: https://api.cloud.com/accessSecurity\n\
  \    tags:\n      - Access Control\n      - Security\n      - Zero Trust\n      - ZTNA\n    serviceName: Citrix Secure Private Access API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/citrix/refs/heads/main/finops/citrix-finops.yml
sources: []
specification: FinOps Framework
tags:
- Application Delivery
- Desktop-As-A-Service
- Networking
- Virtualization
- Workspace
- FinOps
- Cost Management
- FOCUS
---
