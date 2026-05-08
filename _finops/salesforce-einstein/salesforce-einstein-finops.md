---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Einstein Vision API
  slug: ''
  spec_type: OpenAPI
  url: https://api.einstein.ai/v2/vision/openapi.json
- filename: openapi.json
  format: json
  label: Einstein Language API
  slug: ''
  spec_type: OpenAPI
  url: https://api.einstein.ai/v2/language/openapi.json
- filename: salesforce-einstein-prediction-builder-openapi.yml
  format: yaml
  label: Einstein Prediction Builder API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-einstein/refs/heads/main/openapi/salesforce-einstein-prediction-builder-openapi.yml
- filename: salesforce-einstein-discovery-openapi.yml
  format: yaml
  label: Einstein Discovery API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-einstein/refs/heads/main/openapi/salesforce-einstein-discovery-openapi.yml
- filename: salesforce-einstein-bots-openapi.yml
  format: yaml
  label: Einstein Bots API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-einstein/refs/heads/main/openapi/salesforce-einstein-bots-openapi.yml
- filename: salesforce-einstein-gpt-openapi.yml
  format: yaml
  label: Einstein GPT API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-einstein/refs/heads/main/openapi/salesforce-einstein-gpt-openapi.yml
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
description: FinOps framework definition for the Salesforce Einstein API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Salesforce Einstein
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Salesforce Einstein
  PublisherName: Salesforce Einstein
  ServiceCategory: Developer Tools / API
  ServiceName: Salesforce Einstein
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
name: Salesforce Einstein Finops
provider_name: Salesforce Einstein
provider_slug: salesforce-einstein
publisher_name: Salesforce Einstein
service_category: API
slug: salesforce-einstein-finops
source_filename: salesforce-einstein-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Salesforce Einstein\nproviderId: salesforce-einstein\npublisherName: Salesforce Einstein\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Artificial Intelligence\n  - Computer Vision\n  - CRM\n  - Machine Learning\n  - Natural Language Processing\n  - Predictive Analytics\n  - Salesforce\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Salesforce Einstein API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Salesforce Einstein\n  ServiceCategory: Developer Tools / API\n  ProviderName: Salesforce Einstein\n  PublisherName: Salesforce Einstein\n  InvoiceIssuerName: Salesforce Einstein\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n\
  \      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Einstein Vision API\n    baseURL: https://api.einstein.ai/v2/vision\n    tags:\n      - Computer Vision\n      - Image Recognition\n      - Machine Learning\n    serviceName: Einstein Vision API\n    serviceCategory: API\n  - name: Einstein Language API\n    baseURL: https://api.einstein.ai/v2/language\n    tags:\n      - Machine Learning\n      - Natural Language Processing\n      - Sentiment Analysis\n      - Text Classification\n    serviceName: Einstein Language API\n    serviceCategory: API\n  - name: Einstein Prediction Builder API\n   \
  \ baseURL: https://[instance].salesforce.com/services/data/v58.0/einstein/\n    tags:\n      - CRM\n      - Machine Learning\n      - No-Code\n      - Predictive Analytics\n    serviceName: Einstein Prediction Builder API\n    serviceCategory: API\n  - name: Einstein Discovery API\n    baseURL: https://[instance].salesforce.com/services/data/v58.0/analytics/\n    tags:\n      - Automated Insights\n      - Business Intelligence\n      - Machine Learning\n      - Predictive Analytics\n    serviceName: Einstein Discovery API\n    serviceCategory: API\n  - name: Einstein Bots API\n    baseURL: https://[instance].salesforce.com/services/data/v58.0/einstein/\n    tags:\n      - Chatbots\n      - Conversational AI\n      - Customer Service\n      - Natural Language Processing\n    serviceName: Einstein Bots API\n    serviceCategory: API\n  - name: Einstein GPT API\n    baseURL: https://[instance].salesforce.com/services/data/v58.0/einstein/\n    tags:\n      - Content Generation\n      - Generative\
  \ AI\n      - GPT\n      - Large Language Models\n    serviceName: Einstein GPT API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce-einstein/refs/heads/main/finops/salesforce-einstein-finops.yml
sources: []
specification: FinOps Framework
tags:
- Artificial Intelligence
- Computer Vision
- CRM
- Machine Learning
- Natural Language Processing
- Predictive Analytics
- Salesforce
- FinOps
- Cost Management
- FOCUS
---
