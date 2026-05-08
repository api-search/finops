---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: api_docs
  format: yaml
  label: Coupa Core API
  slug: ''
  spec_type: OpenAPI
  url: https://compass.coupa.com/en-us/api_docs
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
description: FinOps framework definition for the Coupa API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Coupa
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Coupa
  PublisherName: Coupa
  ServiceCategory: Developer Tools / API
  ServiceName: Coupa
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
name: Coupa Finops
provider_name: Coupa
provider_slug: coupa
publisher_name: Coupa
service_category: API
slug: coupa-finops
source_filename: coupa-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Coupa\nproviderId: coupa\npublisherName: Coupa\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - BSM\n  - Business Spend Management\n  - Cloud Platform\n  - Enterprise\n  - Financial Management\n  - Invoicing\n  - Procurement\n  - Supply Chain\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Coupa API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Coupa\n  ServiceCategory: Developer Tools / API\n  ProviderName: Coupa\n  PublisherName: Coupa\n  InvoiceIssuerName: Coupa\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Coupa Core API\n    baseURL: https://instance.coupahost.com/api\n    tags:\n      - Invoices\n      - Procurement\n      - Purchase Orders\n      - Requisitions\n      - REST\n    serviceName: Coupa Core API\n    serviceCategory: API\n  - name: Coupa Integration API\n    baseURL: https://instance.coupahost.com/api\n    tags:\n      - Enterprise\n      - ERP\n      - Integration\n      - Webhooks\n    serviceName: Coupa Integration API\n    serviceCategory: API\n  - name: Coupa Supplier API\n    baseURL: https://instance.coupahost.com/api/suppliers\n    tags:\n      - Catalogs\n      - Suppliers\n      - Vendor Management\n    serviceName: Coupa Supplier API\n    serviceCategory:\
  \ API\n  - name: Coupa Analytics API\n    baseURL: https://instance.coupahost.com/api/analytics\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Data Export\n      - Reporting\n    serviceName: Coupa Analytics API\n    serviceCategory: API\n  - name: Coupa CCW API\n    baseURL: https://instance.coupahost.com/api\n    tags:\n      - Candidates\n      - Contingent Workforce\n      - REST\n      - Staffing\n      - Workers\n    serviceName: Coupa CCW API\n    serviceCategory: API\n  - name: Coupa CSO API\n    baseURL: https://instance.cso.coupahost.com/api\n    tags:\n      - Fact Sheets\n      - Markets\n      - Optimization\n      - REST\n      - Sourcing\n    serviceName: Coupa CSO API\n    serviceCategory: API\n  - name: Coupa Treasury API\n    baseURL: https://instance.ctm.coupahost.com/v1\n    tags:\n      - Account Balances\n      - Cash Management\n      - Payments\n      - REST\n      - Treasury\n    serviceName: Coupa Treasury API\n    serviceCategory: API\n\
  \  - name: Coupa Open Buy API\n    baseURL: https://instance.coupahost.com\n    tags:\n      - Catalog\n      - eCommerce\n      - Open Buy\n      - REST\n      - Search\n      - Suppliers\n    serviceName: Coupa Open Buy API\n    serviceCategory: API\n  - name: Coupa Payments API\n    baseURL: https://instance.coupahost.com/api/coupa_pay/payments\n    tags:\n      - Coupa Pay\n      - Expense Payments\n      - Invoice Payments\n      - Payments\n      - REST\n    serviceName: Coupa Payments API\n    serviceCategory: API\n  - name: Coupa Procurement API\n    baseURL: https://instance.coupahost.com/api\n    tags:\n      - Contracts\n      - Procurement\n      - Purchase Orders\n      - Requisitions\n      - REST\n      - Sourcing\n    serviceName: Coupa Procurement API\n    serviceCategory: API\n  - name: Coupa Invoicing API\n    baseURL: https://instance.coupahost.com/api/invoices\n    tags:\n      - Accounts Payable\n      - Charge Allocations\n      - Invoices\n      - Invoicing\n  \
  \    - REST\n    serviceName: Coupa Invoicing API\n    serviceCategory: API\n  - name: Coupa Expenses API\n    baseURL: https://instance.coupahost.com/api/expense_reports\n    tags:\n      - Expense Lines\n      - Expense Reports\n      - Expenses\n      - Per Diem\n      - REST\n    serviceName: Coupa Expenses API\n    serviceCategory: API\n  - name: Coupa Inventory and Receipts API\n    baseURL: https://instance.coupahost.com/api\n    tags:\n      - Advance Ship Notices\n      - Fulfillment\n      - Inventory\n      - Receipts\n      - REST\n      - Warehouse\n    serviceName: Coupa Inventory and Receipts API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coupa/refs/heads/main/finops/coupa-finops.yml
sources: []
specification: FinOps Framework
tags:
- BSM
- Business Spend Management
- Cloud Platform
- Enterprise
- Financial Management
- Invoicing
- Procurement
- Supply Chain
- FinOps
- Cost Management
- FOCUS
---
