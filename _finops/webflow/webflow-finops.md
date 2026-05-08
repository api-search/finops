---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: webflow-data-api-openapi.yml
  format: yaml
  label: Webflow Data API
  slug: data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-data-api-openapi.yml
- filename: webflow-meta-openapi.yml
  format: yaml
  label: Webflow Meta API
  slug: meta-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-meta-openapi.yml
- filename: webflow-sites-openapi.yml
  format: yaml
  label: Webflow Sites API
  slug: sites-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-sites-openapi.yml
- filename: webflow-pages-openapi.yml
  format: yaml
  label: Webflow Pages API
  slug: pages-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-pages-openapi.yml
- filename: webflow-collections-openapi.yml
  format: yaml
  label: Webflow Collections API
  slug: collections-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-collections-openapi.yml
- filename: webflow-items-openapi.yml
  format: yaml
  label: Webflow CMS Items API
  slug: items-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-items-openapi.yml
- filename: webflow-components-openapi.yml
  format: yaml
  label: Webflow Components API
  slug: components-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-components-openapi.yml
- filename: webflow-assets-openapi.yml
  format: yaml
  label: Webflow Assets API
  slug: assets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-assets-openapi.yml
- filename: webflow-forms-openapi.yml
  format: yaml
  label: Webflow Forms API
  slug: forms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-forms-openapi.yml
- filename: webflow-products-openapi.yml
  format: yaml
  label: Webflow Products and SKUs API
  slug: products-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-products-openapi.yml
- filename: webflow-orders-openapi.yml
  format: yaml
  label: Webflow Orders API
  slug: orders-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-orders-openapi.yml
- filename: webflow-inventory-openapi.yml
  format: yaml
  label: Webflow Inventory API
  slug: inventory-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-inventory-openapi.yml
- filename: webflow-ecommerce-settings-openapi.yml
  format: yaml
  label: Webflow Ecommerce Settings API
  slug: ecommerce-settings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-ecommerce-settings-openapi.yml
- filename: webflow-webhooks-openapi.yml
  format: yaml
  label: Webflow Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-webhooks-openapi.yml
- filename: webflow-custom-code-openapi.yml
  format: yaml
  label: Webflow Custom Code API
  slug: custom-code-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-custom-code-openapi.yml
- filename: webflow-comments-openapi.yml
  format: yaml
  label: Webflow Comments API
  slug: comments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-comments-openapi.yml
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
description: FinOps framework definition for the Webflow API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Webflow
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Webflow
  PublisherName: Webflow
  ServiceCategory: Developer Tools / API
  ServiceName: Webflow
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
name: Webflow Finops
provider_name: Webflow
provider_slug: webflow
publisher_name: Webflow
service_category: API
slug: webflow-finops
source_filename: webflow-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Webflow\nproviderId: webflow\npublisherName: Webflow\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - CMS\n  - Ecommerce\n  - No-Code\n  - Web Development\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Webflow API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Webflow\n  ServiceCategory: Developer Tools / API\n  ProviderName: Webflow\n  PublisherName: Webflow\n  InvoiceIssuerName: Webflow\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n \
  \     - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Webflow Data API\n    baseURL: ''\n    tags:\n      - CMS\n      - Content Management\n      - Ecommerce\n      - Sites\n    serviceName: Webflow Data API\n    serviceCategory: API\n  - name: Webflow Designer Extension API\n    baseURL: ''\n    tags:\n      - Designer\n      - Extensions\n      - Plugins\n    serviceName: Webflow Designer Extension API\n    serviceCategory: API\n  - name: Webflow Meta API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Authentication\n      - Meta\n      - Tokens\n    serviceName: Webflow Meta API\n    serviceCategory: API\n  - name: Webflow Sites API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Domains\n      - Publishing\n      - Sites\n    serviceName: Webflow Sites\
  \ API\n    serviceCategory: API\n  - name: Webflow Pages API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Content\n      - DOM\n      - Pages\n    serviceName: Webflow Pages API\n    serviceCategory: API\n  - name: Webflow Collections API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - CMS\n      - Collections\n      - Fields\n    serviceName: Webflow Collections API\n    serviceCategory: API\n  - name: Webflow CMS Items API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - CMS\n      - Content Management\n      - Items\n    serviceName: Webflow CMS Items API\n    serviceCategory: API\n  - name: Webflow Components API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Components\n      - Design\n      - Reusable\n    serviceName: Webflow Components API\n    serviceCategory: API\n  - name: Webflow Assets API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Assets\n      - Files\n      - Media\n    serviceName: Webflow Assets\
  \ API\n    serviceCategory: API\n  - name: Webflow Forms API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Forms\n      - Submissions\n    serviceName: Webflow Forms API\n    serviceCategory: API\n  - name: Webflow Products and SKUs API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Ecommerce\n      - Products\n      - SKUs\n    serviceName: Webflow Products and SKUs API\n    serviceCategory: API\n  - name: Webflow Orders API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Ecommerce\n      - Fulfillment\n      - Orders\n    serviceName: Webflow Orders API\n    serviceCategory: API\n  - name: Webflow Inventory API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Ecommerce\n      - Inventory\n      - Stock\n    serviceName: Webflow Inventory API\n    serviceCategory: API\n  - name: Webflow Ecommerce Settings API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Configuration\n      - Ecommerce\n      - Settings\n    serviceName:\
  \ Webflow Ecommerce Settings API\n    serviceCategory: API\n  - name: Webflow Webhooks API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Events\n      - Notifications\n      - Webhooks\n    serviceName: Webflow Webhooks API\n    serviceCategory: API\n  - name: Webflow Custom Code API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Custom Code\n      - JavaScript\n      - Scripts\n    serviceName: Webflow Custom Code API\n    serviceCategory: API\n  - name: Webflow Comments API\n    baseURL: https://api.webflow.com/v2\n    tags:\n      - Collaboration\n      - Comments\n    serviceName: Webflow Comments API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/finops/webflow-finops.yml
sources: []
specification: FinOps Framework
tags:
- CMS
- Ecommerce
- No-Code
- Web Development
- FinOps
- Cost Management
- FOCUS
---
