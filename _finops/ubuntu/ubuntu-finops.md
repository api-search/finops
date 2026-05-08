---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ubuntu-launchpad-openapi.yml
  format: yaml
  label: Launchpad API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ubuntu/refs/heads/main/openapi/ubuntu-launchpad-openapi.yml
- filename: ubuntu-snap-store-openapi.yml
  format: yaml
  label: Snap Store API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ubuntu/refs/heads/main/openapi/ubuntu-snap-store-openapi.yml
- filename: ubuntu-cve-openapi.yml
  format: yaml
  label: Ubuntu CVE API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ubuntu/refs/heads/main/openapi/ubuntu-cve-openapi.yml
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
description: FinOps framework definition for the Ubuntu API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Ubuntu
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Ubuntu
  PublisherName: Ubuntu
  ServiceCategory: Developer Tools / API
  ServiceName: Ubuntu
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
name: Ubuntu Finops
provider_name: Ubuntu
provider_slug: ubuntu
publisher_name: Ubuntu
service_category: API
slug: ubuntu-finops
source_filename: ubuntu-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Ubuntu\nproviderId: ubuntu\npublisherName: Ubuntu\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - Containers\n  - Devops\n  - Enterprise\n  - Linux\n  - Security\n  - Ubuntu\n  - Package Management\n  - Open Source\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Ubuntu API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Ubuntu\n  ServiceCategory: Developer Tools / API\n  ProviderName: Ubuntu\n  PublisherName: Ubuntu\n  InvoiceIssuerName: Ubuntu\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Launchpad API\n    baseURL: https://api.launchpad.net/1.0\n    tags:\n      - Bugs\n      - Collaboration\n      - Distributions\n      - Packages\n      - Projects\n      - Open Source\n    serviceName: Launchpad API\n    serviceCategory: API\n  - name: Ubuntu Pro API\n    baseURL: https://contracts.canonical.com/\n    tags:\n      - Enterprise\n      - Security\n      - Subscriptions\n      - Support\n    serviceName: Ubuntu Pro API\n    serviceCategory: API\n  - name: Snap Store API\n    baseURL: https://api.snapcraft.io\n    tags:\n      - Applications\n      - Distribution\n      - Packages\n      - Snaps\n      - Package Management\n    serviceName: Snap Store API\n \
  \   serviceCategory: API\n  - name: Ubuntu Archive API\n    baseURL: https://api.launchpad.net/devel/ubuntu\n    tags:\n      - Archives\n      - Packages\n      - Releases\n      - Repositories\n    serviceName: Ubuntu Archive API\n    serviceCategory: API\n  - name: Landscape API\n    baseURL: https://landscape.canonical.com/api/\n    tags:\n      - Automation\n      - Management\n      - Monitoring\n      - Servers\n    serviceName: Landscape API\n    serviceCategory: API\n  - name: MAAS API\n    baseURL: https://maas.io/docs/api\n    tags:\n      - Bare-Metal\n      - Cloud\n      - Infrastructure\n      - Provisioning\n    serviceName: MAAS API\n    serviceCategory: API\n  - name: Juju API\n    baseURL: wss://[controller-address]:17070/api\n    tags:\n      - Automation\n      - Deployment\n      - Devops\n      - Orchestration\n    serviceName: Juju API\n    serviceCategory: API\n  - name: Ubuntu CVE API\n    baseURL: https://ubuntu.com/security\n    tags:\n      - Cve\n      - Patches\n\
  \      - Security\n      - Vulnerabilities\n    serviceName: Ubuntu CVE API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ubuntu/refs/heads/main/finops/ubuntu-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Containers
- Devops
- Enterprise
- Linux
- Security
- Ubuntu
- Package Management
- Open Source
- FinOps
- Cost Management
- FOCUS
---
