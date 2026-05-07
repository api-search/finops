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
description: FinOps framework definition for the Schema.org API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Schema.org
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Schema.org
  PublisherName: Schema.org
  ServiceCategory: Developer Tools / API
  ServiceName: Schema.org
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
name: Schema Org Finops
provider_name: Schema.org
provider_slug: schema-org
publisher_name: Schema.org
service_category: API
slug: schema-org-finops
source_filename: schema-org-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Schema.org\nproviderId: schema-org\npublisherName: Schema.org\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Schema.org\n  - Structured Data\n  - Linked Data\n  - JSON-LD\n  - Vocabulary\n  - SEO\n  - Web Standards\n  - RDF\n  - Ontology\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Schema.org API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Schema.org\n  ServiceCategory: Developer Tools / API\n  ProviderName: Schema.org\n  PublisherName: Schema.org\n  InvoiceIssuerName: Schema.org\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the\
  \ network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Schema.org Vocabulary\n    baseURL: https://schema.org\n    tags:\n      - Schema.org\n      - Vocabulary\n      - Structured Data\n      - Linked Data\n      - JSON-LD\n      - RDF\n      - Microdata\n      - RDFa\n      - SEO\n      - Web Standards\n    serviceName: Schema.org Vocabulary\n    serviceCategory: API\n  - name: Schema.org JSON-LD Context\n    baseURL: https://schema.org\n    tags:\n      - JSON-LD\n      - Linked Data\n      - Context\n      - Vocabulary\n      - Structured Data\n    serviceName: Schema.org JSON-LD Context\n    serviceCategory: API\n  - name: Schema.org Markup Validator\n    baseURL: https://validator.schema.org\n\
  \    tags:\n      - Validation\n      - Structured Data\n      - Testing\n      - Schema\n      - Markup\n    serviceName: Schema.org Markup Validator\n    serviceCategory: API\n  - name: Schema.org WebAPI Type\n    baseURL: https://schema.org\n    tags:\n      - WebAPI\n      - API Description\n      - Structured Data\n      - Linked Data\n      - Schema\n    serviceName: Schema.org WebAPI Type\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/schema-org/refs/heads/main/finops/schema-org-finops.yml
sources: []
specification: FinOps Framework
tags:
- Schema.org
- Structured Data
- Linked Data
- JSON-LD
- Vocabulary
- SEO
- Web Standards
- RDF
- Ontology
- FinOps
- Cost Management
- FOCUS
---
