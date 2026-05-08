---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: adobe-pdf-services-api-openapi.yml
  format: yaml
  label: Adobe PDF Services API
  slug: adobe-pdf-services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe/refs/heads/main/openapi/adobe-pdf-services-api-openapi.yml
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
description: FinOps framework definition for the Adobe API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Adobe
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Adobe
  PublisherName: Adobe
  ServiceCategory: Developer Tools / API
  ServiceName: Adobe
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
name: Adobe Finops
provider_name: Adobe
provider_slug: adobe
publisher_name: Adobe
service_category: API
slug: adobe-finops
source_filename: adobe-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Adobe\nproviderId: adobe\npublisherName: Adobe\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Creative Cloud\n  - Digital Asset Management\n  - Document Services\n  - E-Commerce\n  - E-Signatures\n  - Experience Cloud\n  - Generative AI\n  - Marketing\n  - PDF\n  - Work Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Adobe API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance\
  \ teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Adobe\n  ServiceCategory: Developer Tools / API\n  ProviderName: Adobe\n  PublisherName: Adobe\n  InvoiceIssuerName: Adobe\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Adobe PDF Services API\n    baseURL: https://pdf-services.adobe.io\n    tags:\n      - Conversion\n      - Documents\n      - PDF\n    serviceName: Adobe PDF Services API\n    serviceCategory: API\n  - name: Adobe PDF Extract API\n    baseURL: https://pdf-services.adobe.io\n    tags:\n      - AI\n      - Extraction\n      - PDF\n    serviceName: Adobe PDF Extract API\n    serviceCategory: API\n  - name: Adobe Acrobat Sign API\n    baseURL: https://api.adobesign.com\n    tags:\n      - Documents\n      - E-Signatures\n    serviceName: Adobe Acrobat Sign API\n    serviceCategory: API\n  - name: Adobe Analytics API\n\
  \    baseURL: https://analytics.adobe.io\n    tags:\n      - Analytics\n      - Metrics\n    serviceName: Adobe Analytics API\n    serviceCategory: API\n  - name: Adobe Firefly API\n    baseURL: https://firefly-api.adobe.io\n    tags:\n      - Generative AI\n      - Image Generation\n    serviceName: Adobe Firefly API\n    serviceCategory: API\n  - name: Adobe Experience Platform API\n    baseURL: https://platform.adobe.io\n    tags:\n      - Customer Data\n      - Experience Platform\n    serviceName: Adobe Experience Platform API\n    serviceCategory: API\n  - name: Adobe Stock API\n    baseURL: https://stock.adobe.io\n    tags:\n      - Assets\n      - Stock\n    serviceName: Adobe Stock API\n    serviceCategory: API\n  - name: Adobe Commerce API\n    baseURL: ''\n    tags:\n      - E-Commerce\n      - REST\n    serviceName: Adobe Commerce API\n    serviceCategory: API\n  - name: Adobe Marketo Engage API\n    baseURL: ''\n    tags:\n      - Leads\n      - Marketing Automation\n    serviceName:\
  \ Adobe Marketo Engage API\n    serviceCategory: API\n  - name: Adobe Workfront API\n    baseURL: ''\n    tags:\n      - Projects\n      - Work Management\n    serviceName: Adobe Workfront API\n    serviceCategory: API\n  - name: Adobe User Management API\n    baseURL: https://usermanagement.adobe.io\n    tags:\n      - Identity\n      - User Management\n    serviceName: Adobe User Management API\n    serviceCategory: API\n  - name: Adobe I/O Events API\n    baseURL: https://platform.adobe.io\n    tags:\n      - Events\n      - Webhooks\n    serviceName: Adobe I/O Events API\n    serviceCategory: API\n  - name: Adobe Experience Manager API\n    baseURL: https://platform.adobe.io\n    tags:\n      - Content Management\n      - Digital Asset Management\n    serviceName: Adobe Experience Manager API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost\
  \ / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe/refs/heads/main/finops/adobe-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Creative Cloud
- Digital Asset Management
- Document Services
- E-Commerce
- E-Signatures
- Experience Cloud
- Generative AI
- Marketing
- PDF
- Work Management
- FinOps
- Cost Management
- FOCUS
---
