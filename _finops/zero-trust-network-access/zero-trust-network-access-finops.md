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
description: FinOps framework definition for the Zero Trust Network Access API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Zero Trust Network Access
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Zero Trust Network Access
  PublisherName: Zero Trust Network Access
  ServiceCategory: Developer Tools / API
  ServiceName: Zero Trust Network Access
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
name: Zero Trust Network Access Finops
provider_name: Zero Trust Network Access
provider_slug: zero-trust-network-access
publisher_name: Zero Trust Network Access
service_category: API
slug: zero-trust-network-access-finops
source_filename: zero-trust-network-access-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Zero Trust Network Access\nproviderId: zero-trust-network-access\npublisherName: Zero Trust Network Access\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Access Control\n  - Cloud Security\n  - Cybersecurity\n  - Identity Management\n  - Network Access\n  - Network Security\n  - Security\n  - VPN Replacement\n  - Zero Trust\n  - ZTNA\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Zero Trust Network Access API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API\
  \ consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate\
  \ Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Zero Trust Network Access\n  ServiceCategory: Developer Tools / API\n  ProviderName: Zero Trust Network Access\n  PublisherName: Zero Trust Network Access\n  InvoiceIssuerName: Zero Trust Network Access\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Cloudflare Zero Trust API\n    baseURL: ''\n    tags:\n      - Cloudflare\n      - SASE\n      - ZTNA\n    serviceName: Cloudflare Zero Trust API\n    serviceCategory: API\n  - name: Zscaler Private Access (ZPA) API\n    baseURL: ''\n    tags:\n      - SASE\n      - Zscaler\n      - ZTNA\n    serviceName: Zscaler Private Access (ZPA) API\n    serviceCategory: API\n  - name: Netskope Private Access API\n    baseURL: ''\n    tags:\n      - Netskope\n      - SASE\n\
  \      - ZTNA\n    serviceName: Netskope Private Access API\n    serviceCategory: API\n  - name: Palo Alto Prisma Access (Prisma SASE) API\n    baseURL: ''\n    tags:\n      - Palo Alto\n      - SASE\n      - ZTNA\n    serviceName: Palo Alto Prisma Access (Prisma SASE) API\n    serviceCategory: API\n  - name: Tailscale API\n    baseURL: ''\n    tags:\n      - Mesh VPN\n      - Tailscale\n      - WireGuard\n      - ZTNA\n    serviceName: Tailscale API\n    serviceCategory: API\n  - name: Twingate API\n    baseURL: ''\n    tags:\n      - Twingate\n      - ZTNA\n    serviceName: Twingate API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zero-trust-network-access/refs/heads/main/finops/zero-trust-network-access-finops.yml
sources: []
specification: FinOps Framework
tags:
- Access Control
- Cloud Security
- Cybersecurity
- Identity Management
- Network Access
- Network Security
- Security
- VPN Replacement
- Zero Trust
- ZTNA
- FinOps
- Cost Management
- FOCUS
---
