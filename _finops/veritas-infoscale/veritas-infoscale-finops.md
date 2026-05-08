---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: veritas-infoscale-rest-api.yaml
  format: yaml
  label: Veritas InfoScale REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/openapi/veritas-infoscale-rest-api.yaml
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
description: FinOps framework definition for the Veritas InfoScale API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Veritas InfoScale
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Veritas InfoScale
  PublisherName: Veritas InfoScale
  ServiceCategory: Developer Tools / API
  ServiceName: Veritas InfoScale
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
name: Veritas Infoscale Finops
provider_name: Veritas InfoScale
provider_slug: veritas-infoscale
publisher_name: Veritas InfoScale
service_category: API
slug: veritas-infoscale-finops
source_filename: veritas-infoscale-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Veritas InfoScale\nproviderId: veritas-infoscale\npublisherName: Veritas InfoScale\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Clustering\n  - Data Management\n  - Disaster Recovery\n  - High Availability\n  - Storage Management\n  - Virtualization\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Veritas InfoScale API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Veritas InfoScale\n  ServiceCategory: Developer Tools / API\n  ProviderName: Veritas InfoScale\n  PublisherName: Veritas InfoScale\n  InvoiceIssuerName: Veritas InfoScale\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Veritas InfoScale REST API\n    baseURL: https://{infoscale-server}:14149/api/v1\n    tags:\n      - Availability\n      - Clustering\n      - Storage\n    serviceName: Veritas InfoScale REST API\n    serviceCategory: API\n  - name: Veritas InfoScale Operations Manager API\n    baseURL: https://{isom-server}:14161/vom/api\n    tags:\n      - Management\n      - Monitoring\n      - Operations\n    serviceName: Veritas InfoScale Operations Manager API\n    serviceCategory: API\n  - name: Veritas Cluster Server API\n    baseURL: https://{vcs-server}:14149/vcs/api\n    tags:\n      - Clustering\n      -\
  \ Failover\n      - High Availability\n    serviceName: Veritas Cluster Server API\n    serviceCategory: API\n  - name: Veritas Volume Manager API\n    baseURL: https://{server}:14149/vxvm/api\n    tags:\n      - Snapshots\n      - Storage\n      - Volumes\n    serviceName: Veritas Volume Manager API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/finops/veritas-infoscale-finops.yml
sources: []
specification: FinOps Framework
tags:
- Clustering
- Data Management
- Disaster Recovery
- High Availability
- Storage Management
- Virtualization
- FinOps
- Cost Management
- FOCUS
---
