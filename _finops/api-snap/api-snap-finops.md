---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: api-snap-openapi.yml
  format: yaml
  label: QR Code API
  slug: qr
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Screenshot API
  slug: screenshot
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Image Resize API
  slug: resize
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: PDF API
  slug: pdf
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Markdown API
  slug: markdown
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: URL Metadata API
  slug: meta
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Hash API
  slug: hash
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: JWT Decode API
  slug: jwt-decode
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Base64 API
  slug: base64
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: UUID API
  slug: uuid
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Color API
  slug: color
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Lorem Ipsum API
  slug: lorem
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Placeholder Image API
  slug: placeholder
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
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
description: FinOps framework definition for the API Snap API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: API Snap
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: API Snap
  PublisherName: API Snap
  ServiceCategory: Developer Tools / API
  ServiceName: API Snap
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
name: Api Snap Finops
provider_name: API Snap
provider_slug: api-snap
publisher_name: API Snap
service_category: API
slug: api-snap-finops
source_filename: api-snap-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: API Snap\nproviderId: api-snap\npublisherName: API Snap\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - API Utilities\n  - Developer Tools\n  - QR Codes\n  - Screenshots\n  - Image Processing\n  - PDF Generation\n  - Markdown\n  - URL Metadata\n  - Hashing\n  - JWT\n  - Base64\n  - UUID\n  - Color Conversion\n  - Lorem Ipsum\n  - Placeholder Images\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the API Snap API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption\
  \ costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n\
  \      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: API Snap\n  ServiceCategory: Developer Tools / API\n  ProviderName: API Snap\n  PublisherName: API Snap\n  InvoiceIssuerName: API Snap\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n\
  \      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: QR Code API\n    baseURL: https://api-snap.com/api\n    tags:\n      - QR Codes\n      - Image Generation\n      - Encoding\n    serviceName: QR Code API\n    serviceCategory: API\n  - name: Screenshot API\n    baseURL: https://api-snap.com/api\n    tags:\n      - Screenshots\n      - Browser Automation\n      - Web Capture\n    serviceName: Screenshot API\n    serviceCategory: API\n  - name: Image Resize API\n    baseURL: https://api-snap.com/api\n    tags:\n      - Image Processing\n      - Image Resize\n      - Format Conversion\n    serviceName:\
  \ Image Resize API\n    serviceCategory: API\n  - name: PDF API\n    baseURL: https://api-snap.com/api\n    tags:\n      - PDF\n      - Document Generation\n      - HTML to PDF\n    serviceName: PDF API\n    serviceCategory: API\n  - name: Markdown API\n    baseURL: https://api-snap.com/api\n    tags:\n      - Markdown\n      - HTML\n      - Content Conversion\n    serviceName: Markdown API\n    serviceCategory: API\n  - name: URL Metadata API\n    baseURL: https://api-snap.com/api\n    tags:\n      - URL Metadata\n      - Open Graph\n      - Link Preview\n    serviceName: URL Metadata API\n    serviceCategory: API\n  - name: Hash API\n    baseURL: https://api-snap.com/api\n    tags:\n      - Hashing\n      - Cryptography\n      - Security\n    serviceName: Hash API\n    serviceCategory: API\n  - name: JWT Decode API\n    baseURL: https://api-snap.com/api\n    tags:\n      - JWT\n      - Tokens\n      - Security\n    serviceName: JWT Decode API\n    serviceCategory: API\n  - name: Base64\
  \ API\n    baseURL: https://api-snap.com/api\n    tags:\n      - Base64\n      - Encoding\n      - Decoding\n    serviceName: Base64 API\n    serviceCategory: API\n  - name: UUID API\n    baseURL: https://api-snap.com/api\n    tags:\n      - UUID\n      - Identifiers\n      - ID Generation\n    serviceName: UUID API\n    serviceCategory: API\n  - name: Color API\n    baseURL: https://api-snap.com/api\n    tags:\n      - Color\n      - Color Conversion\n      - Design Utilities\n    serviceName: Color API\n    serviceCategory: API\n  - name: Lorem Ipsum API\n    baseURL: https://api-snap.com/api\n    tags:\n      - Lorem Ipsum\n      - Placeholder Text\n      - Content Generation\n    serviceName: Lorem Ipsum API\n    serviceCategory: API\n  - name: Placeholder Image API\n    baseURL: https://api-snap.com/api\n    tags:\n      - Placeholder Images\n      - SVG\n      - Design Utilities\n    serviceName: Placeholder Image API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per\
  \ 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/finops/api-snap-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Utilities
- Developer Tools
- QR Codes
- Screenshots
- Image Processing
- PDF Generation
- Markdown
- URL Metadata
- Hashing
- JWT
- Base64
- UUID
- Color Conversion
- Lorem Ipsum
- Placeholder Images
- FinOps
- Cost Management
- FOCUS
---
