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
description: FinOps framework definition for the Zero-Trust Security Model API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Zero-Trust Security Model
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Zero-Trust Security Model
  PublisherName: Zero-Trust Security Model
  ServiceCategory: Developer Tools / API
  ServiceName: Zero-Trust Security Model
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
name: Zero Trust Security Model Finops
provider_name: Zero-Trust Security Model
provider_slug: zero-trust-security-model
publisher_name: Zero-Trust Security Model
service_category: API
slug: zero-trust-security-model-finops
source_filename: zero-trust-security-model-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Zero-Trust Security Model\nproviderId: zero-trust-security-model\npublisherName: Zero-Trust Security Model\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Access Control\n  - Cybersecurity\n  - Federal\n  - Identity Management\n  - Network Security\n  - NIST\n  - Security\n  - Security Framework\n  - Zero Trust\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Zero-Trust Security Model API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible\
  \ to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload\
  \ Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Zero-Trust Security Model\n  ServiceCategory: Developer Tools / API\n  ProviderName: Zero-Trust Security Model\n  PublisherName: Zero-Trust Security Model\n  InvoiceIssuerName: Zero-Trust Security Model\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: NIST SP 800-207 Zero Trust Architecture\n    baseURL: ''\n    tags:\n      - NIST\n      - Specification\n      - Zero Trust\n    serviceName: NIST SP 800-207 Zero Trust Architecture\n    serviceCategory: API\n  - name: CISA Zero Trust Maturity Model\n    baseURL: ''\n    tags:\n      - CISA\n      - Federal\n      - Maturity Model\n    serviceName: CISA Zero Trust Maturity Model\n    serviceCategory: API\n  - name: DoD Zero Trust Reference Architecture\n    baseURL: ''\n    tags:\n      - DoD\n   \
  \   - Federal\n      - Reference Architecture\n    serviceName: DoD Zero Trust Reference Architecture\n    serviceCategory: API\n  - name: NSA Zero Trust Guidance\n    baseURL: ''\n    tags:\n      - Federal\n      - Guidance\n      - NSA\n    serviceName: NSA Zero Trust Guidance\n    serviceCategory: API\n  - name: UK NCSC Zero Trust Architecture Design Principles\n    baseURL: ''\n    tags:\n      - Guidance\n      - NCSC\n      - UK\n    serviceName: UK NCSC Zero Trust Architecture Design Principles\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zero-trust-security-model/refs/heads/main/finops/zero-trust-security-model-finops.yml
sources: []
specification: FinOps Framework
tags:
- Access Control
- Cybersecurity
- Federal
- Identity Management
- Network Security
- NIST
- Security
- Security Framework
- Zero Trust
- FinOps
- Cost Management
- FOCUS
---
