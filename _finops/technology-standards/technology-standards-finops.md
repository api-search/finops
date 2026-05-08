---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: technology-standards-openapi.yml
  format: yaml
  label: IETF Internet Standards
  slug: ietf-standards
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/technology-standards/refs/heads/main/openapi/technology-standards-openapi.yml
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
description: FinOps framework definition for the Technology Standards API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Technology Standards
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Technology Standards
  PublisherName: Technology Standards
  ServiceCategory: Developer Tools / API
  ServiceName: Technology Standards
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
name: Technology Standards Finops
provider_name: Technology Standards
provider_slug: technology-standards
publisher_name: Technology Standards
service_category: API
slug: technology-standards-finops
source_filename: technology-standards-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Technology Standards\nproviderId: technology-standards\npublisherName: Technology Standards\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - IEEE\n  - IETF\n  - ISO\n  - Protocols\n  - Standards\n  - Technology Standards\n  - W3C\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Technology Standards API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Technology Standards\n  ServiceCategory: Developer Tools / API\n  ProviderName: Technology Standards\n  PublisherName: Technology Standards\n  InvoiceIssuerName: Technology Standards\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: IETF Internet Standards\n    baseURL: https://datatracker.ietf.org/api/v1\n    tags:\n      - HTTP\n      - IETF\n      - Internet Standards\n      - OAuth\n      - Protocols\n      - RFC\n      - TLS\n    serviceName: IETF Internet Standards\n    serviceCategory: API\n  - name: W3C Web Standards\n    baseURL: https://www.w3.org\n    tags:\n      - CORS\n      - Linked Data\n      - Semantic Web\n      - W3C\n      - Web Standards\n    serviceName: W3C Web Standards\n    serviceCategory: API\n  - name: IEEE Standards\n    baseURL: https://standards.ieee.org\n    tags:\n      - Computer Science\n   \
  \   - Electrical Engineering\n      - IEEE\n      - Networking\n    serviceName: IEEE Standards\n    serviceCategory: API\n  - name: OASIS Open Standards\n    baseURL: https://www.oasis-open.org\n    tags:\n      - AMQP\n      - MQTT\n      - OData\n      - OASIS\n      - SAML\n    serviceName: OASIS Open Standards\n    serviceCategory: API\n  - name: OAuth and OpenID Connect\n    baseURL: https://oauth.net\n    tags:\n      - Authentication\n      - Authorization\n      - Identity\n      - OAuth\n      - OpenID Connect\n      - Security\n    serviceName: OAuth and OpenID Connect\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/technology-standards/refs/heads/main/finops/technology-standards-finops.yml
sources: []
specification: FinOps Framework
tags:
- IEEE
- IETF
- ISO
- Protocols
- Standards
- Technology Standards
- W3C
- FinOps
- Cost Management
- FOCUS
---
