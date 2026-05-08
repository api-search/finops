---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: docusign-openapi-original.yml
  format: yaml
  label: Docusign eSignature REST API
  slug: docusign-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-openapi-original.yml
- filename: docusign-admin-openapi-original.yml
  format: yaml
  label: Docusign Admin API
  slug: docusign-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-admin-openapi-original.yml
- filename: docusign-click-openapi-original.yml
  format: yaml
  label: Docusign Click API
  slug: docusign-click-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-click-openapi-original.yml
- filename: docusign-maestro-openapi-original.yml
  format: yaml
  label: Docusign Maestro API
  slug: docusign-maestro-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-maestro-openapi-original.yml
- filename: docusign-monitor-openapi-original.yml
  format: yaml
  label: Docusign Monitor API
  slug: docusign-monitor-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-monitor-openapi-original.yml
- filename: docusign-rooms-openapi-original.yml
  format: yaml
  label: Docusign Rooms API
  slug: docusign-rooms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-rooms-openapi-original.yml
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
description: FinOps framework definition for the Docusign API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Docusign
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Docusign
  PublisherName: Docusign
  ServiceCategory: Developer Tools / API
  ServiceName: Docusign
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
name: Docusign Finops
provider_name: Docusign
provider_slug: docusign
publisher_name: Docusign
service_category: API
slug: docusign-finops
source_filename: docusign-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Docusign\nproviderId: docusign\npublisherName: Docusign\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Agreements\n  - Contracts\n  - Digital Transaction Management\n  - Documents\n  - Electronic Signatures\n  - eSignature\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Docusign API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Docusign\n  ServiceCategory: Developer Tools / API\n  ProviderName: Docusign\n  PublisherName: Docusign\n  InvoiceIssuerName: Docusign\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n \
  \   unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Docusign eSignature REST API\n    baseURL: https://demo.docusign.net/restapi\n    tags:\n      - Documents\n      - Envelopes\n      - Signatures\n      - Templates\n    serviceName: Docusign eSignature REST API\n    serviceCategory: API\n  - name: Docusign Admin API\n    baseURL: https://api-d.docusign.net/management\n    tags:\n      - Accounts\n      - Administration\n      - Organizations\n      - Users\n    serviceName: Docusign Admin API\n    serviceCategory: API\n  - name: Docusign Click API\n    baseURL: https://demo.docusign.net/clickapi\n    tags:\n      - Clickwrap\n      - Compliance\n      - Consent\n      - Terms of Service\n    serviceName: Docusign Click\
  \ API\n    serviceCategory: API\n  - name: Docusign Maestro API\n    baseURL: https://demo.docusign.net/aow-manage\n    tags:\n      - Automation\n      - Orchestration\n      - Workflows\n    serviceName: Docusign Maestro API\n    serviceCategory: API\n  - name: Docusign Monitor API\n    baseURL: https://lens-d.docusign.net\n    tags:\n      - Audit\n      - Events\n      - Monitoring\n      - Security\n    serviceName: Docusign Monitor API\n    serviceCategory: API\n  - name: Docusign Rooms API\n    baseURL: https://demo.rooms.docusign.com/restapi\n    tags:\n      - Collaboration\n      - Mortgages\n      - Real Estate\n      - Transactions\n    serviceName: Docusign Rooms API\n    serviceCategory: API\n  - name: Docusign Web Forms API\n    baseURL: https://demo.docusign.net/webforms\n    tags:\n      - Data Collection\n      - Documents\n      - Forms\n    serviceName: Docusign Web Forms API\n    serviceCategory: API\n  - name: Docusign Notary API\n    baseURL: https://demo.docusign.net/restapi\n\
  \    tags:\n      - Legal\n      - Notarization\n      - Remote Online Notary\n    serviceName: Docusign Notary API\n    serviceCategory: API\n  - name: Docusign Navigator API\n    baseURL: https://demo.docusign.net/navigator\n    tags:\n      - Agreements\n      - AI\n      - Analytics\n      - Insights\n    serviceName: Docusign Navigator API\n    serviceCategory: API\n  - name: Docusign Workspaces API\n    baseURL: https://demo.docusign.net/restapi\n    tags:\n      - Agreements\n      - Collaboration\n      - Workspaces\n    serviceName: Docusign Workspaces API\n    serviceCategory: API\n  - name: Docusign CLM API\n    baseURL: https://api.example.com\n    tags:\n      - Contract Lifecycle Management\n      - Documents\n      - Workflows\n    serviceName: Docusign CLM API\n    serviceCategory: API\n  - name: Docusign Connected Fields API\n    baseURL: https://demo.docusign.net/restapi\n    tags:\n      - Data Verification\n      - Extensions\n      - Fields\n      - Validation\n  \
  \  serviceName: Docusign Connected Fields API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    url: http://apievangelist.com\n    email: kin@apievangelist.com\n  - name: DocuSign\n    email: devcenter@docusign.com\n    url: https://developers.docusign.com/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/finops/docusign-finops.yml
sources: []
specification: FinOps Framework
tags:
- Agreements
- Contracts
- Digital Transaction Management
- Documents
- Electronic Signatures
- eSignature
- FinOps
- Cost Management
- FOCUS
---
