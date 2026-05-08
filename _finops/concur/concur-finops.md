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
description: FinOps framework definition for the SAP Concur API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SAP Concur
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SAP Concur
  PublisherName: SAP Concur
  ServiceCategory: Developer Tools / API
  ServiceName: SAP Concur
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
name: Concur Finops
provider_name: SAP Concur
provider_slug: concur
publisher_name: SAP Concur
service_category: API
slug: concur-finops
source_filename: concur-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP Concur\nproviderId: concur\npublisherName: SAP Concur\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Expense Management\n  - Finance\n  - Invoice\n  - SAP\n  - Travel\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SAP Concur API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SAP Concur\n  ServiceCategory: Developer Tools / API\n  ProviderName: SAP Concur\n  PublisherName: SAP Concur\n  InvoiceIssuerName: SAP Concur\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SAP Concur Expense API\n    baseURL: https://us.api.concursolutions.com/expensereports/v4/\n    tags:\n      - Expense Reports\n      - Expense Tracking\n      - REST\n      - Spend Management\n    serviceName: SAP Concur Expense API\n    serviceCategory: API\n  - name: SAP Concur Travel API\n    baseURL: https://us.api.concursolutions.com/travel/\n    tags:\n      - Bookings\n      - Itineraries\n      - REST\n      - Travel\n    serviceName: SAP Concur Travel API\n    serviceCategory: API\n  - name: SAP Concur Invoice API\n    baseURL: https://us.api.concursolutions.com/invoice/\n    tags:\n      - Accounts Payable\n      - Invoices\n      - Payments\n      - REST\n    serviceName: SAP Concur Invoice\
  \ API\n    serviceCategory: API\n  - name: SAP Concur Receipts API\n    baseURL: https://us.api.concursolutions.com/receipts/v4/\n    tags:\n      - Digital Receipts\n      - E-Receipts\n      - REST\n    serviceName: SAP Concur Receipts API\n    serviceCategory: API\n  - name: SAP Concur Request API\n    baseURL: https://us.api.concursolutions.com/travelrequest/v4/\n    tags:\n      - Approvals\n      - REST\n      - Travel Requests\n    serviceName: SAP Concur Request API\n    serviceCategory: API\n  - name: SAP Concur User Provisioning API\n    baseURL: https://us.api.concursolutions.com/provisioning/v4/\n    tags:\n      - Provisioning\n      - REST\n      - SCIM\n      - Users\n    serviceName: SAP Concur User Provisioning API\n    serviceCategory: API\n  - name: SAP Concur Events API\n    baseURL: https://us.api.concursolutions.com/events/v4/\n    tags:\n      - Events\n      - REST\n      - Subscriptions\n      - Webhooks\n    serviceName: SAP Concur Events API\n    serviceCategory:\
  \ API\n  - name: SAP Concur Lists API\n    baseURL: https://us.api.concursolutions.com/list/v4/\n    tags:\n      - Configuration\n      - Lists\n      - REST\n    serviceName: SAP Concur Lists API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/concur/refs/heads/main/finops/concur-finops.yml
sources: []
specification: FinOps Framework
tags:
- Expense Management
- Finance
- Invoice
- SAP
- Travel
- FinOps
- Cost Management
- FOCUS
---
