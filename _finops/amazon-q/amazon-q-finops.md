---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-q-business.json
  format: json
  label: Amazon Q Business API
  slug: ''
  spec_type: OpenAPI
  url: https://example.com/openapi/amazon-q-business.json
- filename: amazon-q-developer.json
  format: json
  label: Amazon Q Developer API
  slug: ''
  spec_type: OpenAPI
  url: https://example.com/openapi/amazon-q-developer.json
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
description: FinOps framework definition for the Amazon Q API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Q
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Amazon Q
  PublisherName: Amazon Q
  ServiceCategory: Developer Tools / API
  ServiceName: Amazon Q
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
name: Amazon Q Finops
provider_name: Amazon Q
provider_slug: amazon-q
publisher_name: Amazon Q
service_category: API
slug: amazon-q-finops
source_filename: amazon-q-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Amazon Q\nproviderId: amazon-q\npublisherName: Amazon Q\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Artificial Intelligence\n  - Assistant\n  - AWS\n  - Enterprise\n  - Generative AI\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Amazon Q API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Amazon Q\n  ServiceCategory: Developer Tools / API\n  ProviderName: Amazon Q\n  PublisherName: Amazon Q\n  InvoiceIssuerName: Amazon Q\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Amazon Q Business API\n    baseURL: https://qbusiness.{region}.amazonaws.com\n    tags:\n      - Business Intelligence\n      - Enterprise\n      - Generative AI\n      - Knowledge Management\n      - Q&A\n    serviceName: Amazon Q Business API\n    serviceCategory: API\n  - name: Amazon Q Business QApps API\n    baseURL: https://qbusiness.{region}.amazonaws.com\n    tags:\n      - Applications\n      - Enterprise\n      - Generative AI\n      - Low Code\n    serviceName: Amazon Q Business QApps API\n    serviceCategory: API\n  - name: Amazon Q Developer API\n    baseURL: https://q.{region}.amazonaws.com\n    tags:\n      - AI Assistant\n      - Code Generation\n      - Developer Tools\n      - IDE Integration\n\
  \      - Security Scanning\n    serviceName: Amazon Q Developer API\n    serviceCategory: API\n  - name: Amazon Q Connect API\n    baseURL: https://wisdom.{region}.amazonaws.com\n    tags:\n      - Agent Assistance\n      - Contact Center\n      - Customer Service\n      - Generative AI\n      - Real-Time\n    serviceName: Amazon Q Connect API\n    serviceCategory: API\n  - name: Amazon Q Developer in Chat Applications API\n    baseURL: https://chatbot.{region}.amazonaws.com\n    tags:\n      - Chat\n      - Developer Tools\n      - Integration\n      - Messaging\n    serviceName: Amazon Q Developer in Chat Applications API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    x-twitter: apievangelist\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-q/refs/heads/main/finops/amazon-q-finops.yml
sources: []
specification: FinOps Framework
tags:
- Artificial Intelligence
- Assistant
- Enterprise
- Generative AI
- FinOps
- Cost Management
- FOCUS
---
