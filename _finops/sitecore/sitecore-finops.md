---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sitecore-xm-cloud-rest-api-openapi.yml
  format: yaml
  label: Sitecore XM Cloud REST API
  slug: xm-cloud-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/openapi/sitecore-xm-cloud-rest-api-openapi.yml
- filename: sitecore-cdp-rest-api-openapi.yml
  format: yaml
  label: Sitecore CDP REST API
  slug: cdp-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/openapi/sitecore-cdp-rest-api-openapi.yml
- filename: sitecore-cdp-stream-api-asyncapi.yml
  format: yaml
  label: Sitecore CDP Stream API
  slug: cdp-stream-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/asyncapi/sitecore-cdp-stream-api-asyncapi.yml
- filename: sitecore-personalize-rest-api-openapi.yml
  format: yaml
  label: Sitecore Personalize REST API
  slug: personalize-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/openapi/sitecore-personalize-rest-api-openapi.yml
- filename: sitecore-content-hub-rest-api-openapi.yml
  format: yaml
  label: Sitecore Content Hub REST API
  slug: content-hub-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/openapi/sitecore-content-hub-rest-api-openapi.yml
- filename: sitecore-ordercloud-api-openapi.yml
  format: yaml
  label: Sitecore OrderCloud API
  slug: ordercloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/openapi/sitecore-ordercloud-api-openapi.yml
- filename: sitecore-discover-api-openapi.yml
  format: yaml
  label: Sitecore Discover API
  slug: discover-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/openapi/sitecore-discover-api-openapi.yml
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
description: FinOps framework definition for the sitecore API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: sitecore
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: sitecore
  PublisherName: sitecore
  ServiceCategory: Developer Tools / API
  ServiceName: sitecore
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
name: Sitecore Finops
provider_name: sitecore
provider_slug: sitecore
publisher_name: sitecore
service_category: API
slug: sitecore-finops
source_filename: sitecore-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: sitecore\nproviderId: sitecore\npublisherName: sitecore\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the sitecore API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n\
  \  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n\
  \      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: sitecore\n  ServiceCategory: Developer Tools / API\n  ProviderName: sitecore\n  PublisherName: sitecore\n  InvoiceIssuerName: sitecore\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description:\
  \ Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Sitecore XM Cloud GraphQL Delivery API\n    baseURL: https://edge.sitecorecloud.io/api/graphql\n    tags:\n      - Content Delivery\n      - Digital Experience Platform\n      - GraphQL\n      - Headless CMS\n    serviceName: Sitecore XM Cloud GraphQL Delivery API\n    serviceCategory: API\n  - name: Sitecore XM Cloud Authoring and Management GraphQL API\n    baseURL: https://edge.sitecorecloud.io/api/graphql\n    tags:\n      - Content Management\n      - Digital Experience Platform\n      - GraphQL\n      - Headless CMS\n    serviceName: Sitecore XM Cloud Authoring and Management GraphQL API\n    serviceCategory: API\n  - name: Sitecore XM Cloud REST API\n    baseURL: https://xmapps-api.sitecorecloud.io\n    tags:\n      - Collections\n      - Content Management\n      - Digital Experience Platform\n  \
  \    - REST\n      - Sites\n    serviceName: Sitecore XM Cloud REST API\n    serviceCategory: API\n  - name: Sitecore CDP REST API\n    baseURL: https://api-engage-us.sitecorecloud.io\n    tags:\n      - Customer Data Platform\n      - Guest Data\n      - Personalization\n      - REST\n    serviceName: Sitecore CDP REST API\n    serviceCategory: API\n  - name: Sitecore CDP Stream API\n    baseURL: https://api-engage-us.sitecorecloud.io\n    tags:\n      - Behavioral Data\n      - Customer Data Platform\n      - Event Tracking\n      - Real-Time\n    serviceName: Sitecore CDP Stream API\n    serviceCategory: API\n  - name: Sitecore CDP Batch API\n    baseURL: https://api-engage-us.sitecorecloud.io\n    tags:\n      - Batch Processing\n      - Customer Data Platform\n      - Data Import\n      - Guest Data\n    serviceName: Sitecore CDP Batch API\n    serviceCategory: API\n  - name: Sitecore Personalize REST API\n    baseURL: https://api.boxever.com\n    tags:\n      - Decisioning\n    \
  \  - Experiments\n      - Personalization\n      - REST\n    serviceName: Sitecore Personalize REST API\n    serviceCategory: API\n  - name: Sitecore Content Hub REST API\n    baseURL: https://your-tenant.stylelabs.io/api\n    tags:\n      - Content Hub\n      - Digital Asset Management\n      - Media Management\n      - REST\n    serviceName: Sitecore Content Hub REST API\n    serviceCategory: API\n  - name: Sitecore Content Hub Admin API\n    baseURL: https://your-tenant.stylelabs.io/api/graphql/admin/v1\n    tags:\n      - Administration\n      - Content Hub\n      - Digital Asset Management\n      - GraphQL\n    serviceName: Sitecore Content Hub Admin API\n    serviceCategory: API\n  - name: Sitecore OrderCloud API\n    baseURL: https://api.ordercloud.io/v1\n    tags:\n      - B2B\n      - B2C\n      - Commerce\n      - Order Management\n      - REST\n    serviceName: Sitecore OrderCloud API\n    serviceCategory: API\n  - name: Sitecore Discover API\n    baseURL: https://api.rfksrv.com\n\
  \    tags:\n      - Commerce\n      - Product Discovery\n      - Recommendations\n      - Search\n    serviceName: Sitecore Discover API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/finops/sitecore-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
