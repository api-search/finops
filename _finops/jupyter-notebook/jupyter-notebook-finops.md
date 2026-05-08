---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: jupyter-notebook-rest-api-openapi.yml
  format: yaml
  label: Jupyter Notebook REST API
  slug: jupyter-notebook-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jupyter-notebook/refs/heads/main/openapi/jupyter-notebook-rest-api-openapi.yml
- filename: jupyter-kernel-gateway-api-openapi.yml
  format: yaml
  label: Jupyter Kernel Gateway API
  slug: jupyter-kernel-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jupyter-notebook/refs/heads/main/openapi/jupyter-kernel-gateway-api-openapi.yml
- filename: jupyterhub-rest-api-openapi.yml
  format: yaml
  label: JupyterHub REST API
  slug: jupyterhub-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jupyter-notebook/refs/heads/main/openapi/jupyterhub-rest-api-openapi.yml
- filename: jupyter-kernel-messaging-asyncapi.yml
  format: yaml
  label: Jupyter Kernel Messaging Protocol
  slug: jupyter-kernel-messaging
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/jupyter-notebook/refs/heads/main/asyncapi/jupyter-kernel-messaging-asyncapi.yml
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
description: FinOps framework definition for the Jupyter Notebook API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Jupyter Notebook
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Jupyter Notebook
  PublisherName: Jupyter Notebook
  ServiceCategory: Developer Tools / API
  ServiceName: Jupyter Notebook
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
name: Jupyter Notebook Finops
provider_name: Jupyter Notebook
provider_slug: jupyter-notebook
publisher_name: Jupyter Notebook
service_category: API
slug: jupyter-notebook-finops
source_filename: jupyter-notebook-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Jupyter Notebook\nproviderId: jupyter-notebook\npublisherName: Jupyter Notebook\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Data Science\n  - Interactive Computing\n  - Jupyter\n  - Machine Learning\n  - Notebooks\n  - Python\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Jupyter Notebook API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Jupyter Notebook\n  ServiceCategory: Developer Tools / API\n  ProviderName: Jupyter Notebook\n  PublisherName: Jupyter Notebook\n  InvoiceIssuerName: Jupyter Notebook\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Jupyter Notebook REST API\n    baseURL: http://localhost:8888/api\n    tags:\n      - Contents\n      - Files\n      - Kernels\n      - Notebooks\n      - REST API\n      - Sessions\n    serviceName: Jupyter Notebook REST API\n    serviceCategory: API\n  - name: Jupyter Kernel Gateway API\n    baseURL: http://localhost:8888\n    tags:\n      - Execution\n      - Gateway\n      - Headless\n      - Kernels\n    serviceName: Jupyter Kernel Gateway API\n    serviceCategory: API\n  - name: JupyterHub REST API\n    baseURL: http://localhost:8000/hub/api\n    tags:\n      - Authentication\n      - Hub\n      - Multi-User\n\
  \      - REST API\n    serviceName: JupyterHub REST API\n    serviceCategory: API\n  - name: Jupyter Kernel Messaging Protocol\n    baseURL: ws://localhost:8888\n    tags:\n      - Kernels\n      - Messaging\n      - Real-Time\n      - WebSocket\n    serviceName: Jupyter Kernel Messaging Protocol\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jupyter-notebook/refs/heads/main/finops/jupyter-notebook-finops.yml
sources: []
specification: FinOps Framework
tags:
- Data Science
- Interactive Computing
- Jupyter
- Machine Learning
- Notebooks
- Python
- FinOps
- Cost Management
- FOCUS
---
