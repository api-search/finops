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
description: FinOps framework definition for the Zero Trust Architecture API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Zero Trust Architecture
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Zero Trust Architecture
  PublisherName: Zero Trust Architecture
  ServiceCategory: Developer Tools / API
  ServiceName: Zero Trust Architecture
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
name: Zero Trust Architecture Finops
provider_name: Zero Trust Architecture
provider_slug: zero-trust-architecture
publisher_name: Zero Trust Architecture
service_category: API
slug: zero-trust-architecture-finops
source_filename: zero-trust-architecture-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Zero Trust Architecture\nproviderId: zero-trust-architecture\npublisherName: Zero Trust Architecture\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Access Control\n  - Authentication\n  - Authorization\n  - Cybersecurity\n  - Identity Management\n  - Least Privilege\n  - Network Security\n  - NIST\n  - Security\n  - Zero Trust\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Zero Trust Architecture API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption\
  \ costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n\
  \      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Zero Trust Architecture\n  ServiceCategory: Developer Tools / API\n  ProviderName: Zero Trust Architecture\n  PublisherName: Zero Trust Architecture\n  InvoiceIssuerName: Zero Trust Architecture\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: NIST SP 800-207 Zero Trust Architecture\n    baseURL: ''\n    tags:\n      - NIST\n      - Security Framework\n      - Zero Trust\n    serviceName: NIST SP 800-207 Zero Trust Architecture\n    serviceCategory: API\n  - name: NIST SP 800-207A ZTA for Cloud-Native Applications\n    baseURL: ''\n    tags:\n      - Cloud Security\n      - Kubernetes\n      - NIST\n      - Zero Trust\n    serviceName: NIST SP 800-207A ZTA for Cloud-Native Applications\n    serviceCategory: API\n  - name:\
  \ SPIFFE - Secure Production Identity Framework for Everyone\n    baseURL: ''\n    tags:\n      - CNCF\n      - Identity\n      - Open Source\n      - Standards\n      - Workload Identity\n      - Zero Trust\n    serviceName: SPIFFE - Secure Production Identity Framework for Everyone\n    serviceCategory: API\n  - name: SPIRE - SPIFFE Runtime Environment\n    baseURL: ''\n    tags:\n      - CNCF\n      - Identity\n      - Open Source\n      - Runtime\n      - Zero Trust\n    serviceName: SPIRE - SPIFFE Runtime Environment\n    serviceCategory: API\n  - name: Open Policy Agent (OPA)\n    baseURL: ''\n    tags:\n      - Authorization\n      - CNCF\n      - Open Source\n      - Policy Engine\n      - Zero Trust\n    serviceName: Open Policy Agent (OPA)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zero-trust-architecture/refs/heads/main/finops/zero-trust-architecture-finops.yml
sources: []
specification: FinOps Framework
tags:
- Access Control
- Authentication
- Authorization
- Cybersecurity
- Identity Management
- Least Privilege
- Network Security
- NIST
- Security
- Zero Trust
- FinOps
- Cost Management
- FOCUS
---
