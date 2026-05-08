---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: splunk-enterprise-rest-api.yml
  format: yaml
  label: Splunk Enterprise REST API
  slug: splunk-enterprise-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/splunk/refs/heads/main/openapi/splunk-enterprise-rest-api.yml
- filename: openapi.json
  format: json
  label: Splunk Cloud ACS OpenAPI Specification
  slug: splunk-cloud-admin-config-service-openapi
  spec_type: OpenAPI
  url: https://admin.splunk.com/service/info/specs/v2/openapi.json
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
description: FinOps framework definition for the Splunk API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Splunk
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Splunk
  PublisherName: Splunk
  ServiceCategory: Developer Tools / API
  ServiceName: Splunk
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
name: Splunk Finops
provider_name: Splunk
provider_slug: splunk
publisher_name: Splunk
service_category: API
slug: splunk-finops
source_filename: splunk-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Splunk\nproviderId: splunk\npublisherName: Splunk\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Data Analysis\n  - Logging\n  - Machine Data\n  - Monitoring\n  - Observability\n  - Platform\n  - Security\n  - SIEM\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Splunk API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Splunk\n  ServiceCategory: Developer Tools / API\n  ProviderName: Splunk\n  PublisherName: Splunk\n  InvoiceIssuerName: Splunk\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Splunk\n    baseURL: ''\n    tags: []\n    serviceName: Splunk\n    serviceCategory: API\n  - name: Splunk Enterprise REST API\n    baseURL: ''\n    tags:\n      - Data\n      - Enterprise\n      - Management\n      - REST\n      - Search\n    serviceName: Splunk Enterprise REST API\n    serviceCategory: API\n  - name: Splunk Cloud Platform REST API\n    baseURL: ''\n    tags:\n      - Cloud\n      - Data\n      - Management\n      - REST\n      - Search\n    serviceName: Splunk Cloud Platform REST API\n    serviceCategory: API\n  - name: Splunk Cloud Admin Config Service (ACS) API\n    baseURL: ''\n    tags:\n      - Administration\n      - Cloud\n      - Configuration\n \
  \     - Management\n    serviceName: Splunk Cloud Admin Config Service (ACS) API\n    serviceCategory: API\n  - name: Splunk Cloud ACS OpenAPI Specification\n    baseURL: ''\n    tags:\n      - Administration\n      - Cloud\n      - OpenAPI\n    serviceName: Splunk Cloud ACS OpenAPI Specification\n    serviceCategory: API\n  - name: Splunk Observability Cloud API\n    baseURL: ''\n    tags:\n      - APM\n      - Metrics\n      - Monitoring\n      - Observability\n      - Traces\n    serviceName: Splunk Observability Cloud API\n    serviceCategory: API\n  - name: Splunk SOAR REST API\n    baseURL: ''\n    tags:\n      - Automation\n      - Orchestration\n      - Playbooks\n      - Security\n      - SOAR\n    serviceName: Splunk SOAR REST API\n    serviceCategory: API\n  - name: Splunk Enterprise Security API\n    baseURL: ''\n    tags:\n      - Enterprise Security\n      - Findings\n      - Investigations\n      - Security\n      - SIEM\n    serviceName: Splunk Enterprise Security API\n\
  \    serviceCategory: API\n  - name: Splunk IT Service Intelligence (ITSI) REST API\n    baseURL: ''\n    tags:\n      - AIOps\n      - IT Service Intelligence\n      - ITSI\n      - Monitoring\n    serviceName: Splunk IT Service Intelligence (ITSI) REST API\n    serviceCategory: API\n  - name: Splunk HTTP Event Collector (HEC) API\n    baseURL: ''\n    tags:\n      - Data Ingestion\n      - Events\n      - HEC\n      - Logging\n      - REST\n    serviceName: Splunk HTTP Event Collector (HEC) API\n    serviceCategory: API\n  - name: Splunk Intelligence Management API\n    baseURL: ''\n    tags:\n      - Indicators\n      - Security\n      - STIX\n      - TAXII\n      - Threat Intelligence\n    serviceName: Splunk Intelligence Management API\n    serviceCategory: API\n  - name: Splunk SOAR Playbook Automation API\n    baseURL: ''\n    tags:\n      - Automation\n      - Orchestration\n      - Playbooks\n      - Security\n      - SOAR\n    serviceName: Splunk SOAR Playbook Automation API\n\
  \    serviceCategory: API\n  - name: Splunk AppInspect API\n    baseURL: ''\n    tags:\n      - Apps\n      - Cloud\n      - Splunkbase\n      - Validation\n    serviceName: Splunk AppInspect API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n  - name: Splunk Inc.\n    email: devinfo@splunk.com\n    url: https://www.splunk.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/splunk/refs/heads/main/finops/splunk-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Data Analysis
- Logging
- Machine Data
- Monitoring
- Observability
- Platform
- Security
- SIEM
- FinOps
- Cost Management
- FOCUS
---
