---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: isg-rest-api.yml
  format: yaml
  label: Oracle EBS Integrated SOA Gateway REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/openapi/isg-rest-api.yml
- filename: financial-services-api.yml
  format: yaml
  label: Oracle EBS Financial Services API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/openapi/financial-services-api.yml
- filename: supply-chain-api.yml
  format: yaml
  label: Oracle EBS Supply Chain Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/openapi/supply-chain-api.yml
- filename: human-resources-api.yml
  format: yaml
  label: Oracle EBS Human Resources API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/openapi/human-resources-api.yml
- filename: manufacturing-api.yml
  format: yaml
  label: Oracle EBS Manufacturing API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/openapi/manufacturing-api.yml
- filename: ecommerce-gateway-api.yml
  format: yaml
  label: Oracle EBS e-Commerce Gateway API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/openapi/ecommerce-gateway-api.yml
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
description: FinOps framework definition for the Oracle E-Business Suite API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle E-Business Suite
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle E-Business Suite
  PublisherName: Oracle E-Business Suite
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle E-Business Suite
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
name: Oracle E Business Suite Finops
provider_name: Oracle E-Business Suite
provider_slug: oracle-e-business-suite
publisher_name: Oracle E-Business Suite
service_category: API
slug: oracle-e-business-suite-finops
source_filename: oracle-e-business-suite-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle E-Business Suite\nproviderId: oracle-e-business-suite\npublisherName: Oracle E-Business Suite\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Business Applications\n  - E-Business Suite\n  - Enterprise\n  - ERP\n  - Oracle\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle E-Business Suite API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle E-Business Suite\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle E-Business Suite\n  PublisherName: Oracle E-Business Suite\n  InvoiceIssuerName: Oracle E-Business Suite\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle EBS Integrated SOA Gateway REST API\n    baseURL: https://{instance}.oracle.com/webservices/rest/\n    tags:\n      - Enterprise\n      - Integration\n      - Rest Services\n      - Soa Gateway\n    serviceName: Oracle EBS Integrated SOA Gateway REST API\n    serviceCategory: API\n  - name: Oracle EBS Integrated SOA Gateway SOAP Web Services\n    baseURL: https://{instance}.oracle.com/webservices/SOAProvider/\n    tags:\n      - Integration\n      - Soa Gateway\n      - Soap Services\n      - Web Services\n    serviceName: Oracle EBS Integrated SOA Gateway SOAP Web Services\n  \
  \  serviceCategory: API\n  - name: Oracle EBS Financial Services API\n    baseURL: https://{instance}.oracle.com/webservices/rest/\n    tags:\n      - Accounting\n      - Accounts Payable\n      - Financials\n      - General Ledger\n    serviceName: Oracle EBS Financial Services API\n    serviceCategory: API\n  - name: Oracle EBS Supply Chain Management API\n    baseURL: https://{instance}.oracle.com/webservices/rest/\n    tags:\n      - Inventory\n      - Order Management\n      - Purchasing\n      - Supply Chain\n    serviceName: Oracle EBS Supply Chain Management API\n    serviceCategory: API\n  - name: Oracle EBS Human Resources API\n    baseURL: https://{instance}.oracle.com/webservices/rest/\n    tags:\n      - Human Capital\n      - Human Resources\n      - Payroll\n      - Workforce Management\n    serviceName: Oracle EBS Human Resources API\n    serviceCategory: API\n  - name: Oracle EBS Manufacturing API\n    baseURL: https://{instance}.oracle.com/webservices/rest/\n    tags:\n\
  \      - Bills of Material\n      - Manufacturing\n      - Production\n      - Work Orders\n    serviceName: Oracle EBS Manufacturing API\n    serviceCategory: API\n  - name: Oracle EBS e-Commerce Gateway API\n    baseURL: https://{instance}.oracle.com/\n    tags:\n      - Data Interchange\n      - E-Commerce\n      - Edi\n      - Trading Partners\n    serviceName: Oracle EBS e-Commerce Gateway API\n    serviceCategory: API\n  - name: Oracle EBS PL/SQL API Framework\n    baseURL: https://{instance}.oracle.com/\n    tags:\n      - Database Api\n      - Development Framework\n      - Pl/Sql\n      - Stored Procedures\n    serviceName: Oracle EBS PL/SQL API Framework\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/finops/oracle-e-business-suite-finops.yml
sources: []
specification: FinOps Framework
tags:
- Business Applications
- E-Business Suite
- Enterprise
- ERP
- Oracle
- FinOps
- Cost Management
- FOCUS
---
