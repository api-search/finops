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
description: FinOps framework definition for the Configuration Language API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Configuration Language
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Configuration Language
  PublisherName: Configuration Language
  ServiceCategory: Developer Tools / API
  ServiceName: Configuration Language
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
name: Configuration Language Finops
provider_name: Configuration Language
provider_slug: configuration-language
publisher_name: Configuration Language
service_category: API
slug: configuration-language-finops
source_filename: configuration-language-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Configuration Language\nproviderId: configuration-language\npublisherName: Configuration Language\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Configuration\n  - DSL\n  - Infrastructure as Code\n  - Schemas\n  - Serialization\n  - Templating\n  - YAML\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Configuration Language API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n     \
  \ real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing\
  \ and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Configuration Language\n  ServiceCategory: Developer Tools / API\n  ProviderName: Configuration Language\n  PublisherName: Configuration Language\n  InvoiceIssuerName: Configuration Language\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n    \
  \  - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: YAML\n    baseURL: https://yaml.org\n    tags:\n      - Human Readable\n      - Serialization\n      - Standards\n      - YAML\n    serviceName: YAML\n    serviceCategory: API\n  - name: JSON\n    baseURL: https://www.json.org\n    tags:\n      - ECMA\n      - IETF\n      - Interchange\n      - JSON\n    serviceName: JSON\n    serviceCategory: API\n  - name: TOML\n    baseURL: https://toml.io\n    tags:\n      - Configuration\n      - Human Readable\n      - TOML\n    serviceName: TOML\n    serviceCategory: API\n  - name: HCL\n    baseURL: https://github.com\n  \
  \  tags:\n      - HCL\n      - HashiCorp\n      - Infrastructure as Code\n      - Terraform\n    serviceName: HCL\n    serviceCategory: API\n  - name: Cue\n    baseURL: https://cuelang.org\n    tags:\n      - Cue\n      - Schema\n      - Type System\n      - Validation\n    serviceName: Cue\n    serviceCategory: API\n  - name: Dhall\n    baseURL: https://dhall-lang.org\n    tags:\n      - Dhall\n      - Functional\n      - Total\n      - Type Safe\n    serviceName: Dhall\n    serviceCategory: API\n  - name: Pkl\n    baseURL: https://pkl-lang.org\n    tags:\n      - Apple\n      - Pkl\n      - Templating\n      - Type Safe\n    serviceName: Pkl\n    serviceCategory: API\n  - name: Jsonnet\n    baseURL: https://jsonnet.org\n    tags:\n      - Generation\n      - Jsonnet\n      - Templating\n    serviceName: Jsonnet\n    serviceCategory: API\n  - name: KDL\n    baseURL: https://kdl.dev\n    tags:\n      - KDL\n      - Tree\n    serviceName: KDL\n    serviceCategory: API\nunitEconomics:\n\
  \  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/configuration-language/refs/heads/main/finops/configuration-language-finops.yml
sources: []
specification: FinOps Framework
tags:
- Configuration
- DSL
- Infrastructure as Code
- Schemas
- Serialization
- Templating
- YAML
- FinOps
- Cost Management
- FOCUS
---
