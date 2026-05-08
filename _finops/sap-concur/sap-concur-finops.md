---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: expense-report.json
  format: json
  label: Concur Expense API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.concur.com/api-reference/expense/expense-report/expense-report.json
- filename: itinerary.json
  format: json
  label: Concur Travel API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.concur.com/api-reference/travel/itinerary/itinerary.json
- filename: v3.invoice.json
  format: json
  label: Concur Invoice API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.concur.com/api-reference/invoice/v3.invoice.json
- filename: v4.request.json
  format: json
  label: Concur Request API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.concur.com/api-reference/request/v4.request.json
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
name: Sap Concur Finops
provider_name: SAP Concur
provider_slug: sap-concur
publisher_name: SAP Concur
service_category: API
slug: sap-concur-finops
source_filename: sap-concur-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP Concur\nproviderId: sap-concur\npublisherName: SAP Concur\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Business Travel\n  - Expense Management\n  - Financial Services\n  - Invoice Management\n  - Travel Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SAP Concur API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SAP Concur\n  ServiceCategory: Developer Tools / API\n  ProviderName: SAP Concur\n  PublisherName: SAP Concur\n  InvoiceIssuerName: SAP Concur\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Concur Expense API\n    baseURL: https://www.concursolutions.com/api/v3.0\n    tags:\n      - Expenses\n      - Receipts\n      - Reports\n    serviceName: Concur Expense API\n    serviceCategory: API\n  - name: Concur Travel API\n    baseURL: https://www.concursolutions.com/api/v3.0\n    tags:\n      - Bookings\n      - Itineraries\n      - Travel\n    serviceName: Concur Travel API\n    serviceCategory: API\n  - name: Concur Invoice API\n    baseURL: https://www.concursolutions.com/api/v3.0\n    tags:\n      - Invoices\n      - Payments\n      - Purchase Requests\n    serviceName: Concur Invoice API\n    serviceCategory: API\n  - name: Concur Request API\n    baseURL:\
  \ https://www.concursolutions.com/api/v4.0\n    tags:\n      - Approvals\n      - Travel Requests\n      - Workflows\n    serviceName: Concur Request API\n    serviceCategory: API\n  - name: Concur User Provisioning API\n    baseURL: https://www.concursolutions.com/api/user/v1.0\n    tags:\n      - Identity Management\n      - Provisioning\n      - Users\n    serviceName: Concur User Provisioning API\n    serviceCategory: API\n  - name: Concur Receipt API\n    baseURL: https://www.concursolutions.com/api/v3.0\n    tags:\n      - Documents\n      - Images\n      - Receipts\n    serviceName: Concur Receipt API\n    serviceCategory: API\n  - name: Concur Budget API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Budgets\n      - Financial Planning\n      - Fiscal Years\n    serviceName: Concur Budget API\n    serviceCategory: API\n  - name: Concur Cards API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Credit Cards\n      - Financial\
  \ Data\n      - Transactions\n    serviceName: Concur Cards API\n    serviceCategory: API\n  - name: Concur Quick Expense API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Expenses\n      - Quick Entry\n      - Receipts\n    serviceName: Concur Quick Expense API\n    serviceCategory: API\n  - name: Concur Exchange Rate API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Currency\n      - Exchange Rates\n      - Financial Data\n    serviceName: Concur Exchange Rate API\n    serviceCategory: API\n  - name: Concur Financial Integration API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - ERP\n      - Financial Integration\n      - Posting\n    serviceName: Concur Financial Integration API\n    serviceCategory: API\n  - name: Concur Identity API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Identity\n      - SCIM\n      - User Profiles\n    serviceName: Concur Identity API\n    serviceCategory:\
  \ API\n  - name: Concur Event Subscription Service API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Events\n      - Subscriptions\n      - Webhooks\n    serviceName: Concur Event Subscription Service API\n    serviceCategory: API\n  - name: Concur Callouts API\n    baseURL: https://www.concursolutions.com/api/v1.0\n    tags:\n      - Callouts\n      - Connectors\n      - Integrations\n    serviceName: Concur Callouts API\n    serviceCategory: API\n  - name: Concur Direct Connect Hotel Service API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Booking\n      - Direct Connect\n      - Hotels\n    serviceName: Concur Direct Connect Hotel Service API\n    serviceCategory: API\n  - name: Concur Direct Connect Ground Transportation API\n    baseURL: https://www.concursolutions.com/api/v1.0\n    tags:\n      - Booking\n      - Direct Connect\n      - Ground Transportation\n    serviceName: Concur Direct Connect Ground Transportation API\n\
  \    serviceCategory: API\n  - name: Concur Spend Documents API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Documents\n      - Receipts\n      - Spend Management\n    serviceName: Concur Spend Documents API\n    serviceCategory: API\n  - name: Concur List Item API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Configuration\n      - List Items\n      - Lists\n    serviceName: Concur List Item API\n    serviceCategory: API\n  - name: Concur Lists API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Configuration\n      - Lists\n      - Shared Resources\n    serviceName: Concur Lists API\n    serviceCategory: API\n  - name: Concur Travel Profile API\n    baseURL: https://www.concursolutions.com/api/v2.0\n    tags:\n      - Loyalty Programs\n      - Travel Profiles\n      - User Profiles\n    serviceName: Concur Travel Profile API\n    serviceCategory: API\n  - name: Concur Travel Allowance API\n    baseURL:\
  \ https://www.concursolutions.com/api/v4.0\n    tags:\n      - Expenses\n      - Per Diem\n      - Travel Allowance\n    serviceName: Concur Travel Allowance API\n    serviceCategory: API\n  - name: Concur Cash Advance API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Cash Advances\n      - Expenses\n      - Reimbursements\n    serviceName: Concur Cash Advance API\n    serviceCategory: API\n  - name: Concur Purchase Order API\n    baseURL: https://www.concursolutions.com/api/v3.0\n    tags:\n      - Invoices\n      - Procurement\n      - Purchase Orders\n    serviceName: Concur Purchase Order API\n    serviceCategory: API\n  - name: Concur Purchase Request API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Approvals\n      - Procurement\n      - Purchase Requests\n    serviceName: Concur Purchase Request API\n    serviceCategory: API\n  - name: Concur Vendor API\n    baseURL: https://www.concursolutions.com/api/v3.0\n    tags:\n\
  \      - Invoices\n      - Supplier Management\n      - Vendors\n    serviceName: Concur Vendor API\n    serviceCategory: API\n  - name: Concur Sales Tax Validation API\n    baseURL: https://www.concursolutions.com/api/v3.0\n    tags:\n      - Invoices\n      - Tax Compliance\n      - Tax Validation\n    serviceName: Concur Sales Tax Validation API\n    serviceCategory: API\n  - name: Concur Document Compliance Gateway API\n    baseURL: https://www.concursolutions.com/api/v4.0\n    tags:\n      - Compliance\n      - Document Validation\n      - Tax Documents\n    serviceName: Concur Document Compliance Gateway API\n    serviceCategory: API\n  - name: Concur Image API\n    baseURL: https://www.concursolutions.com/api/image/v1.0\n    tags:\n      - Documents\n      - Images\n      - Receipts\n    serviceName: Concur Image API\n    serviceCategory: API\n  - name: Concur Travel Receipts API\n    baseURL: https://us.api.concursolutions.com/travelreceipts/v1\n    tags:\n      - E-Receipts\n\
  \      - Travel\n      - Travel Receipts\n    serviceName: Concur Travel Receipts API\n    serviceCategory: API\n  - name: Concur Locations API\n    baseURL: https://www.concursolutions.com/api/v3.0\n    tags:\n      - Common Resources\n      - Geography\n      - Locations\n    serviceName: Concur Locations API\n    serviceCategory: API\n  - name: Concur Expense Attendee Types API\n    baseURL: https://www.concursolutions.com/api/v3.0\n    tags:\n      - Attendees\n      - Configuration\n      - Expenses\n    serviceName: Concur Expense Attendee Types API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://developer.concur.com/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-concur/refs/heads/main/finops/sap-concur-finops.yml
sources: []
specification: FinOps Framework
tags:
- Business Travel
- Expense Management
- Financial Services
- Invoice Management
- Travel Management
- FinOps
- Cost Management
- FOCUS
---
