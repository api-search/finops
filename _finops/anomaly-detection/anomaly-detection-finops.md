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
description: FinOps framework definition for the Anomaly Detection API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Anomaly Detection
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Anomaly Detection
  PublisherName: Anomaly Detection
  ServiceCategory: Developer Tools / API
  ServiceName: Anomaly Detection
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
name: Anomaly Detection Finops
provider_name: Anomaly Detection
provider_slug: anomaly-detection
publisher_name: Anomaly Detection
service_category: API
slug: anomaly-detection-finops
source_filename: anomaly-detection-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Anomaly Detection\nproviderId: anomaly-detection\npublisherName: Anomaly Detection\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Anomaly Detection\n  - Artificial Intelligence\n  - Data Science\n  - Fraud Detection\n  - Machine Learning\n  - Monitoring\n  - Observability\n  - Outlier Detection\n  - Pattern Recognition\n  - Security\n  - Time Series\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Anomaly Detection API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description:\
  \ Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n   \
  \   - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Anomaly Detection\n  ServiceCategory: Developer Tools / API\n  ProviderName: Anomaly Detection\n  PublisherName: Anomaly Detection\n  InvoiceIssuerName: Anomaly Detection\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure AI Anomaly Detector\n    baseURL: https://api.cognitive.microsoft.com\n    tags:\n      - Anomaly Detection\n      - Azure\n      - Machine Learning\n      - Microsoft\n      - Multivariate\n      - Time Series\n      - Univariate\n    serviceName: Azure AI Anomaly Detector\n    serviceCategory: API\n  - name: Elasticsearch Anomaly Detection API\n    baseURL: https://your-elasticsearch-host:9200\n    tags:\n      - Anomaly Detection\n      - Elasticsearch\n      - Machine Learning\n\
  \      - Monitoring\n      - Time Series\n    serviceName: Elasticsearch Anomaly Detection API\n    serviceCategory: API\n  - name: Datadog Anomaly Monitor API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Anomaly Detection\n      - Datadog\n      - Monitoring\n      - Observability\n      - Time Series\n    serviceName: Datadog Anomaly Monitor API\n    serviceCategory: API\n  - name: AWS Lookout for Metrics\n    baseURL: https://lookoutmetrics.us-east-1.amazonaws.com\n    tags:\n      - Amazon Web Services\n      - Anomaly Detection\n      - AWS\n      - Business Metrics\n      - Machine Learning\n    serviceName: AWS Lookout for Metrics\n    serviceCategory: API\n  - name: PyOD (Python Outlier Detection)\n    baseURL: https://pypi.org/project/pyod/\n    tags:\n      - Anomaly Detection\n      - Data Science\n      - Machine Learning\n      - Open Source\n      - Outlier Detection\n      - Python\n    serviceName: PyOD (Python Outlier Detection)\n    serviceCategory: API\n\
  unitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n    X: apievangelist\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/anomaly-detection/refs/heads/main/finops/anomaly-detection-finops.yml
sources: []
specification: FinOps Framework
tags:
- Anomaly Detection
- Artificial Intelligence
- Data Science
- Fraud Detection
- Machine Learning
- Monitoring
- Observability
- Outlier Detection
- Pattern Recognition
- Security
- Time Series
- FinOps
- Cost Management
- FOCUS
---
