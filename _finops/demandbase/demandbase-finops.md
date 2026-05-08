---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: demandbase-api-openapi.yml
  format: yaml
  label: Demandbase API
  slug: demandbase-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-api-openapi.yml
- filename: demandbase-real-time-identification-openapi.yml
  format: yaml
  label: Demandbase Real-Time Identification API
  slug: demandbase-real-time-identification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-real-time-identification-openapi.yml
- filename: demandbase-advertising-openapi.yml
  format: yaml
  label: Demandbase Advertising API
  slug: demandbase-advertising-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-advertising-openapi.yml
- filename: demandbase-engagement-openapi.yml
  format: yaml
  label: Demandbase Engagement API
  slug: demandbase-engagement-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-engagement-openapi.yml
- filename: demandbase-account-list-openapi.yml
  format: yaml
  label: Demandbase Account List API
  slug: demandbase-account-list-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-account-list-openapi.yml
- filename: demandbase-b2b-data-openapi.yml
  format: yaml
  label: Demandbase B2B Data API
  slug: demandbase-b2b-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-b2b-data-openapi.yml
- filename: demandbase-ip-openapi.yml
  format: yaml
  label: Demandbase IP API
  slug: demandbase-ip-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-ip-openapi.yml
- filename: demandbase-admin-openapi.yml
  format: yaml
  label: Demandbase Admin API
  slug: demandbase-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-admin-openapi.yml
- filename: demandbase-data-export-openapi.yml
  format: yaml
  label: Demandbase Data Export API
  slug: demandbase-data-export-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-data-export-openapi.yml
- filename: demandbase-data-import-openapi.yml
  format: yaml
  label: Demandbase Data Import API
  slug: demandbase-data-import-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-data-import-openapi.yml
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
description: FinOps framework definition for the Demandbase API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Demandbase
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Demandbase
  PublisherName: Demandbase
  ServiceCategory: Developer Tools / API
  ServiceName: Demandbase
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
name: Demandbase Finops
provider_name: Demandbase
provider_slug: demandbase
publisher_name: Demandbase
service_category: API
slug: demandbase-finops
source_filename: demandbase-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Demandbase\nproviderId: demandbase\npublisherName: Demandbase\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Account-Based Marketing\n  - Advertising\n  - AI Agents\n  - B2B Marketing\n  - Data Enrichment\n  - Intent Data\n  - Personalization\n  - Sales Intelligence\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Demandbase API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n    \
  \  real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      -\
  \ Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Demandbase\n  ServiceCategory: Developer Tools / API\n  ProviderName: Demandbase\n  PublisherName: Demandbase\n  InvoiceIssuerName: Demandbase\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n \
  \   description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Demandbase API\n    baseURL: https://api.demandbase.com\n    tags:\n      - Accounts\n      - B2B Data\n      - Firmographics\n      - Identification\n    serviceName: Demandbase API\n    serviceCategory: API\n  - name: Demandbase Real-Time Identification API\n    baseURL: https://api.company-target.com\n    tags:\n      - Identification\n      - IP Intelligence\n      - Real-Time\n      - Visitor Tracking\n    serviceName: Demandbase Real-Time Identification API\n    serviceCategory: API\n  - name: Demandbase Advertising API\n    baseURL: https://api.demandbase.com/advertising\n    tags:\n      - ABM\n\
  \      - Advertising\n      - Audiences\n      - Campaigns\n    serviceName: Demandbase Advertising API\n    serviceCategory: API\n  - name: Demandbase Engagement API\n    baseURL: https://api.demandbase.com/engagement\n    tags:\n      - Account Insights\n      - Activity Tracking\n      - Analytics\n      - Engagement\n    serviceName: Demandbase Engagement API\n    serviceCategory: API\n  - name: Demandbase Account List API\n    baseURL: https://api.demandbase.com/accounts\n    tags:\n      - Account Lists\n      - CRM Sync\n      - List Management\n      - Target Accounts\n    serviceName: Demandbase Account List API\n    serviceCategory: API\n  - name: Demandbase B2B Data API\n    baseURL: https://api.demandbase.com\n    tags:\n      - B2B Data\n      - Company Search\n      - Contact Discovery\n      - Data Enrichment\n      - Firmographics\n    serviceName: Demandbase B2B Data API\n    serviceCategory: API\n  - name: Demandbase IP API\n    baseURL: https://api.demandbase.com\n \
  \   tags:\n      - Company Identification\n      - Firmographics\n      - IP Intelligence\n      - Real-Time\n      - Visitor Identification\n    serviceName: Demandbase IP API\n    serviceCategory: API\n  - name: Demandbase Admin API\n    baseURL: https://api.demandbase.com\n    tags:\n      - Administration\n      - API Keys\n      - Platform Management\n      - User Management\n    serviceName: Demandbase Admin API\n    serviceCategory: API\n  - name: Demandbase Data Export API\n    baseURL: https://api.demandbase.com\n    tags:\n      - Accounts\n      - Analytics\n      - Bulk Export\n      - Data Export\n      - Reporting\n    serviceName: Demandbase Data Export API\n    serviceCategory: API\n  - name: Demandbase Data Import API\n    baseURL: https://api.demandbase.com\n    tags:\n      - Accounts\n      - Bulk Import\n      - CSV\n      - Data Import\n      - Data Ingestion\n    serviceName: Demandbase Data Import API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per\
  \ 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://www.demandbase.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/finops/demandbase-finops.yml
sources: []
specification: FinOps Framework
tags:
- Account-Based Marketing
- Advertising
- AI Agents
- B2B Marketing
- Data Enrichment
- Intent Data
- Personalization
- Sales Intelligence
- FinOps
- Cost Management
- FOCUS
---
