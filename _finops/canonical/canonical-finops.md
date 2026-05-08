---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rest-api.yaml
  format: yaml
  label: LXD REST API
  slug: lxd-api
  spec_type: OpenAPI
  url: https://github.com/canonical/lxd/blob/main/doc/rest-api.yaml
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
description: FinOps framework definition for the Canonical API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Canonical
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Canonical
  PublisherName: Canonical
  ServiceCategory: Developer Tools / API
  ServiceName: Canonical
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
name: Canonical Finops
provider_name: Canonical
provider_slug: canonical
publisher_name: Canonical
service_category: API
slug: canonical-finops
source_filename: canonical-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Canonical\nproviderId: canonical\npublisherName: Canonical\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - Linux\n  - Open Source\n  - Ubuntu\n  - Containers\n  - Bare Metal\n  - Charms\n  - Identity\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Canonical API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Canonical\n  ServiceCategory: Developer Tools / API\n  ProviderName: Canonical\n  PublisherName: Canonical\n  InvoiceIssuerName: Canonical\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Snap Store API\n    baseURL: https://api.snapcraft.io\n    tags:\n      - Snaps\n      - Store\n      - Packaging\n    serviceName: Snap Store API\n    serviceCategory: API\n  - name: Charmhub API\n    baseURL: https://api.charmhub.io\n    tags:\n      - Charms\n      - Operators\n      - Kubernetes\n    serviceName: Charmhub API\n    serviceCategory: API\n  - name: snapd REST API\n    baseURL: ''\n    tags:\n      - Local\n      - System\n      - Snaps\n    serviceName: snapd REST API\n    serviceCategory: API\n  - name: LXD REST API\n    baseURL: https://<host>:8443/1.0\n    tags:\n      - Containers\n      - Virtualisation\n      - OpenAPI\n    serviceName: LXD\
  \ REST API\n    serviceCategory: API\n  - name: MAAS API\n    baseURL: https://<maas-host>/MAAS/api/2.0\n    tags:\n      - Bare Metal\n      - Provisioning\n      - Infrastructure\n    serviceName: MAAS API\n    serviceCategory: API\n  - name: Juju Client / Controller API\n    baseURL: ''\n    tags:\n      - Orchestration\n      - DevOps\n      - Charms\n    serviceName: Juju Client / Controller API\n    serviceCategory: API\n  - name: Launchpad Web Services API\n    baseURL: https://api.launchpad.net/\n    tags:\n      - OAuth\n      - Open Source\n      - Project Hosting\n    serviceName: Launchpad Web Services API\n    serviceCategory: API\n  - name: Ubuntu Pro Client API\n    baseURL: ''\n    tags:\n      - ESM\n      - Livepatch\n      - FIPS\n      - Compliance\n      - Subscription\n    serviceName: Ubuntu Pro Client API\n    serviceCategory: API\n  - name: Landscape API\n    baseURL: ''\n    tags:\n      - Systems Management\n      - Patch Management\n      - Fleet\n    serviceName:\
  \ Landscape API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/canonical/refs/heads/main/finops/canonical-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Linux
- Open Source
- Ubuntu
- Containers
- Bare Metal
- Charms
- Identity
- FinOps
- Cost Management
- FOCUS
---
