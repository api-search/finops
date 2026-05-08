---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sap-sd-sales-order-openapi.yml
  format: yaml
  label: Sales Order API
  slug: sales-order
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-sales-order-openapi.yml
- filename: sap-sd-customer-master-data-openapi.yml
  format: yaml
  label: Customer Master Data API
  slug: customer-master-data
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-customer-master-data-openapi.yml
- filename: sap-sd-outbound-delivery-openapi.yml
  format: yaml
  label: Outbound Delivery API
  slug: outbound-delivery
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-outbound-delivery-openapi.yml
- filename: sap-sd-billing-document-openapi.yml
  format: yaml
  label: Billing Document API
  slug: billing-document
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-billing-document-openapi.yml
- filename: sap-sd-pricing-openapi.yml
  format: yaml
  label: Pricing API
  slug: pricing
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-pricing-openapi.yml
- filename: sap-sd-sales-quotation-openapi.yml
  format: yaml
  label: Sales Quotation API
  slug: sales-quotation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-sales-quotation-openapi.yml
- filename: sap-sd-credit-management-openapi.yml
  format: yaml
  label: Credit Management API
  slug: credit-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-credit-management-openapi.yml
- filename: sap-sd-material-master-openapi.yml
  format: yaml
  label: Material Master API
  slug: material-master
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-material-master-openapi.yml
- filename: sap-sd-credit-memo-request-openapi.yml
  format: yaml
  label: Credit Memo Request API
  slug: credit-memo-request
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-credit-memo-request-openapi.yml
- filename: sap-sd-debit-memo-request-openapi.yml
  format: yaml
  label: Debit Memo Request API
  slug: debit-memo-request
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-debit-memo-request-openapi.yml
- filename: sap-sd-sales-contract-openapi.yml
  format: yaml
  label: Sales Contract API
  slug: sales-contract
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-sales-contract-openapi.yml
- filename: sap-sd-sales-inquiry-openapi.yml
  format: yaml
  label: Sales Inquiry API
  slug: sales-inquiry
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-sales-inquiry-openapi.yml
- filename: sap-sd-sales-scheduling-agreement-openapi.yml
  format: yaml
  label: Sales Scheduling Agreement API
  slug: sales-scheduling-agreement
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-sales-scheduling-agreement-openapi.yml
- filename: sap-sd-customer-return-openapi.yml
  format: yaml
  label: Customer Return API
  slug: customer-return
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-customer-return-openapi.yml
- filename: sap-sd-customer-returns-delivery-openapi.yml
  format: yaml
  label: Customer Returns Delivery API
  slug: customer-returns-delivery
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-customer-returns-delivery-openapi.yml
- filename: sap-sd-customer-material-openapi.yml
  format: yaml
  label: Customer Material API
  slug: customer-material
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-customer-material-openapi.yml
- filename: sap-sd-inbound-delivery-openapi.yml
  format: yaml
  label: Inbound Delivery API
  slug: inbound-delivery
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-inbound-delivery-openapi.yml
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
description: FinOps framework definition for the SAP Sales and Distribution (SD) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SAP Sales and Distribution (SD)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SAP Sales and Distribution (SD)
  PublisherName: SAP Sales and Distribution (SD)
  ServiceCategory: Developer Tools / API
  ServiceName: SAP Sales and Distribution (SD)
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
name: Sap Sales And Distribution Sd Finops
provider_name: SAP Sales and Distribution (SD)
provider_slug: sap-sales-and-distribution-sd
publisher_name: SAP Sales and Distribution (SD)
service_category: API
slug: sap-sales-and-distribution-sd-finops
source_filename: sap-sales-and-distribution-sd-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP Sales and Distribution (SD)\nproviderId: sap-sales-and-distribution-sd\npublisherName: SAP Sales and Distribution (SD)\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Distribution\n  - ERP\n  - OData\n  - S/4HANA\n  - Sales\n  - SAP\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SAP Sales and Distribution (SD) API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SAP Sales and Distribution (SD)\n  ServiceCategory: Developer Tools / API\n  ProviderName: SAP Sales and Distribution (SD)\n  PublisherName: SAP Sales and Distribution (SD)\n  InvoiceIssuerName: SAP Sales and Distribution (SD)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n  \
  \    - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Sales Order API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_SALES_ORDER_SRV\n    tags:\n      - OData\n      - Order Management\n      - S/4HANA\n      - Sales Orders\n    serviceName: Sales Order API\n    serviceCategory: API\n  - name: Customer Master Data API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER\n    tags:\n      - Business Partner\n      - Customer Data\n      - Master Data\n      - OData\n    serviceName: Customer Master Data API\n    serviceCategory:\
  \ API\n  - name: Outbound Delivery API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_OUTBOUND_DELIVERY_SRV\n    tags:\n      - Delivery\n      - Logistics\n      - OData\n      - Shipping\n    serviceName: Outbound Delivery API\n    serviceCategory: API\n  - name: Billing Document API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BILLING_DOCUMENT_SRV\n    tags:\n      - Billing\n      - Credit Memo\n      - Invoice\n      - OData\n    serviceName: Billing Document API\n    serviceCategory: API\n  - name: Pricing API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_SLSPRCGCONDITIONRECORD_SRV\n    tags:\n      - Conditions\n      - Discount\n      - OData\n      - Pricing\n    serviceName: Pricing API\n    serviceCategory: API\n  - name: Sales Quotation API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_SALES_QUOTATION_SRV\n    tags:\n      - OData\n      - Pre-Sales\n    \
  \  - Quotation\n      - Sales Document\n    serviceName: Sales Quotation API\n    serviceCategory: API\n  - name: Credit Management API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_CREDIT_MANAGEMENT\n    tags:\n      - Credit\n      - Finance\n      - OData\n      - Risk Management\n    serviceName: Credit Management API\n    serviceCategory: API\n  - name: Material Master API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_PRODUCT_SRV\n    tags:\n      - Master Data\n      - Material\n      - OData\n      - Product\n    serviceName: Material Master API\n    serviceCategory: API\n  - name: Credit Memo Request API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_CREDIT_MEMO_REQUEST_SRV\n    tags:\n      - Billing\n      - Credit Memo\n      - OData\n      - Sales Document\n    serviceName: Credit Memo Request API\n    serviceCategory: API\n  - name: Debit Memo Request API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_DEBIT_MEMO_REQUEST_SRV\n\
  \    tags:\n      - Billing\n      - Debit Memo\n      - OData\n      - Sales Document\n    serviceName: Debit Memo Request API\n    serviceCategory: API\n  - name: Sales Contract API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_SALES_CONTRACT_SRV\n    tags:\n      - Agreement\n      - OData\n      - S/4HANA\n      - Sales Contract\n    serviceName: Sales Contract API\n    serviceCategory: API\n  - name: Sales Inquiry API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_SALES_INQUIRY_SRV\n    tags:\n      - OData\n      - Pre-Sales\n      - S/4HANA\n      - Sales Inquiry\n    serviceName: Sales Inquiry API\n    serviceCategory: API\n  - name: Sales Scheduling Agreement API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_SALES_SCHEDULING_AGREEMENT\n    tags:\n      - Logistics\n      - OData\n      - Sales Contract\n      - Scheduling Agreement\n    serviceName: Sales Scheduling Agreement API\n    serviceCategory:\
  \ API\n  - name: Customer Return API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_CUSTOMER_RETURN_SRV\n    tags:\n      - Customer Returns\n      - OData\n      - Reverse Logistics\n      - S/4HANA\n    serviceName: Customer Return API\n    serviceCategory: API\n  - name: Customer Returns Delivery API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_CUSTOMER_RETURN_DELIVERY_SRV_0002\n    tags:\n      - OData\n      - Returns Delivery\n      - Reverse Logistics\n      - Shipping\n    serviceName: Customer Returns Delivery API\n    serviceCategory: API\n  - name: Customer Material API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_CUSTOMER_MATERIAL_SRV\n    tags:\n      - Customer Material\n      - Master Data\n      - OData\n      - Sales\n    serviceName: Customer Material API\n    serviceCategory: API\n  - name: Inbound Delivery API\n    baseURL: https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_INBOUND_DELIVERY_SRV_0002\n\
  \    tags:\n      - Inbound Delivery\n      - Logistics\n      - OData\n      - Warehouse\n    serviceName: Inbound Delivery API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/finops/sap-sales-and-distribution-sd-finops.yml
sources: []
specification: FinOps Framework
tags:
- Distribution
- ERP
- OData
- S/4HANA
- Sales
- SAP
- FinOps
- Cost Management
- FOCUS
---
