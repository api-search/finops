---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cloudinary-openapi.yml
  format: yaml
  label: Cloudinary Upload API
  slug: upload
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cloudinary/refs/heads/main/openapi/cloudinary-openapi.yml
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
description: FinOps framework definition for the Cloudinary API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cloudinary
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cloudinary
  PublisherName: Cloudinary
  ServiceCategory: Developer Tools / API
  ServiceName: Cloudinary
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
name: Cloudinary Finops
provider_name: Cloudinary
provider_slug: cloudinary
publisher_name: Cloudinary
service_category: API
slug: cloudinary-finops
source_filename: cloudinary-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cloudinary\nproviderId: cloudinary\npublisherName: Cloudinary\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Asset Management\n  - Digital Asset Management\n  - Image Processing\n  - Image Transformation\n  - Media\n  - SaaS\n  - Video Processing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cloudinary API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cloudinary\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cloudinary\n  PublisherName: Cloudinary\n  InvoiceIssuerName: Cloudinary\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Cloudinary Upload API\n    baseURL: https://api.cloudinary.com/v1_1\n    tags:\n      - Asset Upload\n      - Image Processing\n      - Media\n      - Transformation\n    serviceName: Cloudinary Upload API\n    serviceCategory: API\n  - name: Cloudinary Admin API\n    baseURL: https://api.cloudinary.com/v1_1\n    tags:\n      - Administration\n      - Asset Management\n      - Folders\n      - Metadata\n      - Webhooks\n    serviceName: Cloudinary Admin API\n    serviceCategory: API\n  - name: Cloudinary Search API\n    baseURL: https://api.cloudinary.com/v1_1\n    tags:\n      - Asset Discovery\n      - Search\n      - Visual Search\n\
  \    serviceName: Cloudinary Search API\n    serviceCategory: API\n  - name: Cloudinary Provisioning API\n    baseURL: https://api.cloudinary.com/v1_1/provisioning\n    tags:\n      - Account Management\n      - API Keys\n      - Provisioning\n      - Users\n    serviceName: Cloudinary Provisioning API\n    serviceCategory: API\n  - name: Cloudinary Permissions API\n    baseURL: https://api.cloudinary.com/v1_1\n    tags:\n      - Access Control\n      - Permissions\n      - RBAC\n      - Roles\n    serviceName: Cloudinary Permissions API\n    serviceCategory: API\n  - name: Cloudinary Transformation URL API\n    baseURL: https://res.cloudinary.com\n    tags:\n      - Delivery\n      - Image Transformation\n      - URL API\n      - Video Transformation\n    serviceName: Cloudinary Transformation URL API\n    serviceCategory: API\n  - name: Cloudinary Notifications and Webhooks\n    baseURL: ''\n    tags:\n      - Events\n      - Notifications\n      - Webhooks\n    serviceName: Cloudinary\
  \ Notifications and Webhooks\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudinary/refs/heads/main/finops/cloudinary-finops.yml
sources: []
specification: FinOps Framework
tags:
- Asset Management
- Digital Asset Management
- Image Processing
- Image Transformation
- Media
- SaaS
- Video Processing
- FinOps
- Cost Management
- FOCUS
---
