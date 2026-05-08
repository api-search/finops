---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: availity-eligibility-openapi.yml
  format: yaml
  label: Availity Eligibility & Benefits API
  slug: availity-eligibility-benefits-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/availity/refs/heads/main/openapi/availity-eligibility-openapi.yml
- filename: availity-claim-status-openapi.yml
  format: yaml
  label: Availity Claim Status API
  slug: availity-claims-status-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/availity/refs/heads/main/openapi/availity-claim-status-openapi.yml
- filename: availity-claim-attachments-openapi.yml
  format: yaml
  label: Availity Claim Attachments API
  slug: availity-claim-attachments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/availity/refs/heads/main/openapi/availity-claim-attachments-openapi.yml
- filename: availity-service-reviews-openapi.yml
  format: yaml
  label: Availity Service Reviews (Prior Authorization) API
  slug: availity-service-reviews-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/availity/refs/heads/main/openapi/availity-service-reviews-openapi.yml
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
description: FinOps framework definition for the availity API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: availity
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: availity
  PublisherName: availity
  ServiceCategory: Developer Tools / API
  ServiceName: availity
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
name: Availity Finops
provider_name: availity
provider_slug: availity
publisher_name: availity
service_category: API
slug: availity-finops
source_filename: availity-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: availity\nproviderId: availity\npublisherName: availity\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the availity API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n\
  \  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n\
  \      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: availity\n  ServiceCategory: Developer Tools / API\n  ProviderName: availity\n  PublisherName: availity\n  InvoiceIssuerName: availity\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description:\
  \ Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Availity Eligibility & Benefits API\n    baseURL: https://api.availity.com\n    tags:\n      - Benefits\n      - EDI\n      - Eligibility\n      - Healthcare\n      - X12 270/271\n    serviceName: Availity Eligibility & Benefits API\n    serviceCategory: API\n  - name: Availity Claim Status API\n    baseURL: https://api.availity.com\n    tags:\n      - Claims\n      - Clearinghouse\n      - EDI\n      - Healthcare\n      - X12 276/277\n    serviceName: Availity Claim Status API\n    serviceCategory: API\n  - name: Availity Claim Attachments API\n    baseURL: https://api.availity.com\n    tags:\n      - Attachments\n      - Claims\n      - Clearinghouse\n      - EDI\n      - Healthcare\n    serviceName: Availity Claim Attachments API\n    serviceCategory: API\n  - name: Availity Service Reviews (Prior Authorization)\
  \ API\n    baseURL: https://api.availity.com\n    tags:\n      - EDI\n      - Healthcare\n      - Prior Authorization\n      - Service Reviews\n      - X12 278\n    serviceName: Availity Service Reviews (Prior Authorization) API\n    serviceCategory: API\n  - name: Availity Healthcare HIPAA Transactions API\n    baseURL: https://api.availity.com\n    tags:\n      - Clearinghouse\n      - EDI\n      - Healthcare\n      - HIPAA\n    serviceName: Availity Healthcare HIPAA Transactions API\n    serviceCategory: API\n  - name: Availity Patient Cost Estimator API\n    baseURL: https://api.availity.com\n    tags:\n      - Cost Estimation\n      - Healthcare\n      - Patient Financial Responsibility\n      - Price Transparency\n    serviceName: Availity Patient Cost Estimator API\n    serviceCategory: API\n  - name: Availity Eligibility & Benefits Value-Add APIs\n    baseURL: https://api.availity.com\n    tags:\n      - Care Reminders\n      - EDI\n      - Eligibility\n      - Healthcare\n   \
  \   - Member ID Card\n    serviceName: Availity Eligibility & Benefits Value-Add APIs\n    serviceCategory: API\n  - name: Availity Payer List API\n    baseURL: https://api.availity.com\n    tags:\n      - Clearinghouse\n      - Healthcare\n      - Payer Network\n      - Reference Data\n    serviceName: Availity Payer List API\n    serviceCategory: API\n  - name: Availity Configurations API\n    baseURL: https://api.availity.com\n    tags:\n      - Configuration\n      - Healthcare\n      - Payer Requirements\n      - Provider Validation\n    serviceName: Availity Configurations API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/availity/refs/heads/main/finops/availity-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
