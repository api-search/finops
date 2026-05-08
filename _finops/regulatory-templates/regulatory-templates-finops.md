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
description: FinOps framework definition for the Regulatory Templates API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Regulatory Templates
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Regulatory Templates
  PublisherName: Regulatory Templates
  ServiceCategory: Developer Tools / API
  ServiceName: Regulatory Templates
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
name: Regulatory Templates Finops
provider_name: Regulatory Templates
provider_slug: regulatory-templates
publisher_name: Regulatory Templates
service_category: API
slug: regulatory-templates-finops
source_filename: regulatory-templates-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Regulatory Templates\nproviderId: regulatory-templates\npublisherName: Regulatory Templates\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Compliance\n  - Governance\n  - GDPR\n  - HIPAA\n  - ISO 27001\n  - PCI DSS\n  - Policy Templates\n  - Regulatory\n  - SOC 2\n  - Templates\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Regulatory Templates API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance\
  \ teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Regulatory Templates\n  ServiceCategory: Developer Tools / API\n  ProviderName: Regulatory Templates\n  PublisherName: Regulatory Templates\n  InvoiceIssuerName: Regulatory Templates\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n\
  \      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: OneTrust API\n    baseURL: https://app.onetrust.com/api/v2\n    tags:\n      - Compliance Automation\n      - GDPR\n      - Privacy\n      - Risk Management\n    serviceName: OneTrust API\n    serviceCategory: API\n  - name: Vanta API\n    baseURL: https://api.vanta.com/v1\n    tags:\n      - Audit Automation\n      - Compliance\n      - SOC 2\n      - Security\n    serviceName: Vanta API\n    serviceCategory: API\n  - name: Drata API\n    baseURL: https://api.drata.com/v1\n    tags:\n      - Compliance\n      - Control Frameworks\n      - ISO 27001\n      -\
  \ SOC 2\n    serviceName: Drata API\n    serviceCategory: API\n  - name: Scrut Automation API\n    baseURL: https://api.scrut.io/v1\n    tags:\n      - Compliance\n      - Evidence Collection\n      - Framework Automation\n      - Security\n    serviceName: Scrut Automation API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/regulatory-templates/refs/heads/main/finops/regulatory-templates-finops.yml
sources: []
specification: FinOps Framework
tags:
- Compliance
- Governance
- GDPR
- HIPAA
- ISO 27001
- PCI DSS
- Policy Templates
- Regulatory
- SOC 2
- Templates
- FinOps
- Cost Management
- FOCUS
---
