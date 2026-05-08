---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: apideck-accounting-openapi.yml
  format: yaml
  label: Apideck Accounting API
  slug: accounting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apideck/refs/heads/main/openapi/apideck-accounting-openapi.yml
- filename: apideck-crm-openapi.yml
  format: yaml
  label: Apideck CRM API
  slug: crm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apideck/refs/heads/main/openapi/apideck-crm-openapi.yml
- filename: apideck-hris-openapi.yml
  format: yaml
  label: Apideck HRIS API
  slug: hris-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apideck/refs/heads/main/openapi/apideck-hris-openapi.yml
- filename: ats.yml
  format: yaml
  label: Apideck ATS API
  slug: ats-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/ats.yml
- filename: apideck-file-storage-openapi.yml
  format: yaml
  label: Apideck File Storage API
  slug: file-storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apideck/refs/heads/main/openapi/apideck-file-storage-openapi.yml
- filename: ecommerce.yml
  format: yaml
  label: Apideck Ecommerce API
  slug: ecommerce-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/ecommerce.yml
- filename: pos.yml
  format: yaml
  label: Apideck POS API
  slug: pos-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/pos.yml
- filename: issue-tracking.yml
  format: yaml
  label: Apideck Issue Tracking API
  slug: issue-tracking-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/issue-tracking.yml
- filename: lead.yml
  format: yaml
  label: Apideck Lead API
  slug: lead-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/lead.yml
- filename: sms.yml
  format: yaml
  label: Apideck SMS API
  slug: sms-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/sms.yml
- filename: vault.yml
  format: yaml
  label: Apideck Vault API
  slug: vault-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/vault.yml
- filename: webhook.yml
  format: yaml
  label: Apideck Webhook API
  slug: webhook-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/webhook.yml
- filename: connector.yml
  format: yaml
  label: Apideck Connector API
  slug: connector-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/connector.yml
- filename: proxy.yml
  format: yaml
  label: Apideck Proxy API
  slug: proxy-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/proxy.yml
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
description: FinOps framework definition for the Apideck API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Apideck
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Apideck
  PublisherName: Apideck
  ServiceCategory: Developer Tools / API
  ServiceName: Apideck
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
name: Apideck Finops
provider_name: Apideck
provider_slug: apideck
publisher_name: Apideck
service_category: API
slug: apideck-finops
source_filename: apideck-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Apideck\nproviderId: apideck\npublisherName: Apideck\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Integrations\n  - Unified API\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Apideck API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n \
  \     feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and\
  \ Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Apideck\n  ServiceCategory: Developer Tools / API\n  ProviderName: Apideck\n  PublisherName: Apideck\n  InvoiceIssuerName: Apideck\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      -\
  \ consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Apideck\n    baseURL: https://unify.apideck.com\n    tags:\n      - Integrations\n      - Unified API\n    serviceName: Apideck\n    serviceCategory: API\n  - name: Apideck Accounting API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Accounting\n      - Invoices\n      - Payments\n      - Unified API\n    serviceName: Apideck Accounting API\n    serviceCategory: API\n  - name: Apideck CRM API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Contacts\n      - CRM\n      - Leads\n      - Unified API\n    serviceName: Apideck CRM API\n    serviceCategory: API\n  - name: Apideck HRIS API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Employees\n      - HRIS\n      - Human Resources\n      - Unified API\n    serviceName:\
  \ Apideck HRIS API\n    serviceCategory: API\n  - name: Apideck ATS API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Applicant Tracking\n      - ATS\n      - Recruitment\n      - Unified API\n    serviceName: Apideck ATS API\n    serviceCategory: API\n  - name: Apideck File Storage API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Cloud Storage\n      - File Storage\n      - Files\n      - Unified API\n    serviceName: Apideck File Storage API\n    serviceCategory: API\n  - name: Apideck Ecommerce API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Ecommerce\n      - Orders\n      - Products\n      - Unified API\n    serviceName: Apideck Ecommerce API\n    serviceCategory: API\n  - name: Apideck POS API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Payments\n      - Point of Sale\n      - POS\n      - Unified API\n    serviceName: Apideck POS API\n    serviceCategory: API\n  - name: Apideck Issue Tracking API\n    baseURL: https://unify.apideck.com\n\
  \    tags:\n      - Issue Tracking\n      - Project Management\n      - Tickets\n      - Unified API\n    serviceName: Apideck Issue Tracking API\n    serviceCategory: API\n  - name: Apideck Lead API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Leads\n      - Marketing\n      - Sales\n      - Unified API\n    serviceName: Apideck Lead API\n    serviceCategory: API\n  - name: Apideck SMS API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Messaging\n      - SMS\n      - Unified API\n    serviceName: Apideck SMS API\n    serviceCategory: API\n  - name: Apideck Vault API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Authentication\n      - Credentials\n      - OAuth\n      - Unified API\n    serviceName: Apideck Vault API\n    serviceCategory: API\n  - name: Apideck Webhook API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Events\n      - Unified API\n      - Webhooks\n    serviceName: Apideck Webhook API\n    serviceCategory: API\n \
  \ - name: Apideck Connector API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Connectors\n      - Integrations\n      - Unified API\n    serviceName: Apideck Connector API\n    serviceCategory: API\n  - name: Apideck Proxy API\n    baseURL: https://unify.apideck.com\n    tags:\n      - Monitoring\n      - Proxy\n      - Unified API\n    serviceName: Apideck Proxy API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apideck/refs/heads/main/finops/apideck-finops.yml
sources: []
specification: FinOps Framework
tags:
- Integrations
- Unified API
- FinOps
- Cost Management
- FOCUS
---
