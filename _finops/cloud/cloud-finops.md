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
description: FinOps framework definition for the Cloud API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cloud
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cloud
  PublisherName: Cloud
  ServiceCategory: Developer Tools / API
  ServiceName: Cloud
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
name: Cloud Finops
provider_name: Cloud
provider_slug: cloud
publisher_name: Cloud
service_category: API
slug: cloud-finops
source_filename: cloud-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cloud\nproviderId: cloud\npublisherName: Cloud\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Cloud\n  - Cloud Computing\n  - Compute\n  - Hyperscaler\n  - IaaS\n  - Infrastructure\n  - PaaS\n  - Public Cloud\n  - SaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cloud API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cloud\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cloud\n  PublisherName: Cloud\n  InvoiceIssuerName: Cloud\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Amazon Web Services\n    baseURL: ''\n    tags:\n      - AWS\n      - Hyperscaler\n      - IaaS\n      - PaaS\n    serviceName: Amazon Web Services\n    serviceCategory: API\n  - name: Microsoft Azure\n    baseURL: ''\n    tags:\n      - Azure\n      - Hyperscaler\n      - IaaS\n      - PaaS\n    serviceName: Microsoft Azure\n    serviceCategory: API\n  - name: Google Cloud\n    baseURL: ''\n    tags:\n      - GCP\n      - Google\n      - Hyperscaler\n      - IaaS\n      - PaaS\n    serviceName: Google Cloud\n    serviceCategory: API\n  - name: Oracle Cloud Infrastructure\n    baseURL: ''\n    tags:\n      - Oracle\n      - OCI\n    serviceName: Oracle Cloud Infrastructure\n   \
  \ serviceCategory: API\n  - name: IBM Cloud\n    baseURL: ''\n    tags:\n      - IBM\n    serviceName: IBM Cloud\n    serviceCategory: API\n  - name: Alibaba Cloud\n    baseURL: ''\n    tags:\n      - Alibaba\n      - Asia\n      - Hyperscaler\n    serviceName: Alibaba Cloud\n    serviceCategory: API\n  - name: DigitalOcean\n    baseURL: ''\n    tags:\n      - DigitalOcean\n      - Developer Cloud\n    serviceName: DigitalOcean\n    serviceCategory: API\n  - name: Linode (Akamai Cloud)\n    baseURL: ''\n    tags:\n      - Akamai\n      - Linode\n    serviceName: Linode (Akamai Cloud)\n    serviceCategory: API\n  - name: Vultr\n    baseURL: ''\n    tags:\n      - Vultr\n    serviceName: Vultr\n    serviceCategory: API\n  - name: Hetzner Cloud\n    baseURL: ''\n    tags:\n      - Europe\n      - Hetzner\n    serviceName: Hetzner Cloud\n    serviceCategory: API\n  - name: Scaleway\n    baseURL: ''\n    tags:\n      - Europe\n      - Scaleway\n    serviceName: Scaleway\n    serviceCategory:\
  \ API\n  - name: Cloudflare\n    baseURL: ''\n    tags:\n      - Cloudflare\n      - Edge\n      - Network\n    serviceName: Cloudflare\n    serviceCategory: API\n  - name: Fastly Compute\n    baseURL: ''\n    tags:\n      - Edge\n      - Fastly\n      - WebAssembly\n    serviceName: Fastly Compute\n    serviceCategory: API\n  - name: CoreWeave\n    baseURL: ''\n    tags:\n      - AI\n      - CoreWeave\n      - GPU\n    serviceName: CoreWeave\n    serviceCategory: API\n  - name: Crusoe Cloud\n    baseURL: ''\n    tags:\n      - AI\n      - Crusoe\n      - GPU\n      - Sustainable\n    serviceName: Crusoe Cloud\n    serviceCategory: API\n  - name: Lambda Labs Cloud\n    baseURL: ''\n    tags:\n      - AI\n      - GPU\n      - Lambda\n    serviceName: Lambda Labs Cloud\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n\
  \    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kinlane@gmail.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloud/refs/heads/main/finops/cloud-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Cloud Computing
- Compute
- Hyperscaler
- IaaS
- Infrastructure
- PaaS
- Public Cloud
- SaaS
- FinOps
- Cost Management
- FOCUS
---
