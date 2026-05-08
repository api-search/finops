---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: overview
  format: yaml
  label: SAP S/4HANA Business Partner API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_BUSINESS_PARTNER/overview
- filename: sap-s4hana-sales-order-openapi.yml
  format: yaml
  label: SAP S/4HANA Sales Order API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-s4hana/refs/heads/main/openapi/sap-s4hana-sales-order-openapi.yml
- filename: overview
  format: yaml
  label: SAP S/4HANA Purchase Order API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_PURCHASEORDER_PROCESS_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Material Document API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_MATERIAL_DOCUMENT_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Product Master API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_PRODUCT_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Journal Entry API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_JOURNALENTRY_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Billing Document API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_BILLING_DOCUMENT_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Supplier Invoice API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_SUPPLIERINVOICE_PROCESS_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Customer Return API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_CUSTOMER_RETURN_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Purchase Requisition API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_PURCHASEREQ_PROCESS_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Outbound Delivery API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_OUTBOUND_DELIVERY_SRV_0002/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Inbound Delivery API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_INBOUND_DELIVERY_SRV_0002/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Cost Center API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_COSTCENTER_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA GL Account API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_GLACCOUNTINCHARTOFACCOUNTS_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Bank Master API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_BANKDETAIL_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Production Order API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_PRODUCTION_ORDER_2_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Maintenance Order API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_MAINTENANCEORDER/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Workforce Timesheet API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_MANAGE_WORKFORCE_TIMESHEET/overview
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
description: FinOps framework definition for the SAP S/4HANA API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SAP S/4HANA
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SAP S/4HANA
  PublisherName: SAP S/4HANA
  ServiceCategory: Developer Tools / API
  ServiceName: SAP S/4HANA
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
name: Sap S4Hana Finops
provider_name: SAP S/4HANA
provider_slug: sap-s4hana
publisher_name: SAP S/4HANA
service_category: API
slug: sap-s4hana-finops
source_filename: sap-s4hana-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP S/4HANA\nproviderId: sap-s4hana\npublisherName: SAP S/4HANA\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Business Applications\n  - Cloud\n  - Enterprise Resource Planning\n  - ERP\n  - Finance\n  - Human Resources\n  - Inventory\n  - Logistics\n  - Manufacturing\n  - Plant Maintenance\n  - Procurement\n  - S/4HANA\n  - Sales\n  - SAP\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SAP S/4HANA API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption\
  \ costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n\
  \      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SAP S/4HANA\n  ServiceCategory: Developer Tools / API\n  ProviderName: SAP S/4HANA\n  PublisherName: SAP S/4HANA\n  InvoiceIssuerName: SAP S/4HANA\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SAP S/4HANA Business Partner API\n    baseURL: ''\n    tags:\n      - Business Partner\n      - Customer\n      - ERP\n      - Master Data\n      - Supplier\n    serviceName: SAP S/4HANA Business Partner API\n    serviceCategory: API\n  - name: SAP S/4HANA Sales Order API\n    baseURL: ''\n    tags:\n      - ERP\n      - Order Management\n      - Sales\n      - Sales Order\n    serviceName: SAP S/4HANA Sales Order API\n    serviceCategory: API\n  - name: SAP S/4HANA Purchase Order API\n    baseURL: ''\n    tags:\n      - ERP\n  \
  \    - Procurement\n      - Purchase Order\n      - Purchasing\n    serviceName: SAP S/4HANA Purchase Order API\n    serviceCategory: API\n  - name: SAP S/4HANA Material Document API\n    baseURL: ''\n    tags:\n      - ERP\n      - Goods Movement\n      - Inventory\n      - Material Document\n      - Warehouse\n    serviceName: SAP S/4HANA Material Document API\n    serviceCategory: API\n  - name: SAP S/4HANA Product Master API\n    baseURL: ''\n    tags:\n      - ERP\n      - Master Data\n      - Material\n      - Product\n    serviceName: SAP S/4HANA Product Master API\n    serviceCategory: API\n  - name: SAP S/4HANA Journal Entry API\n    baseURL: ''\n    tags:\n      - Accounting\n      - ERP\n      - Finance\n      - General Ledger\n      - Journal Entry\n    serviceName: SAP S/4HANA Journal Entry API\n    serviceCategory: API\n  - name: SAP S/4HANA Billing Document API\n    baseURL: ''\n    tags:\n      - Billing\n      - ERP\n      - Finance\n      - Invoice\n      - Sales\n  \
  \  serviceName: SAP S/4HANA Billing Document API\n    serviceCategory: API\n  - name: SAP S/4HANA Supplier Invoice API\n    baseURL: ''\n    tags:\n      - Accounts Payable\n      - ERP\n      - Finance\n      - Procurement\n      - Supplier Invoice\n    serviceName: SAP S/4HANA Supplier Invoice API\n    serviceCategory: API\n  - name: SAP S/4HANA Customer Return API\n    baseURL: ''\n    tags:\n      - Customer Return\n      - ERP\n      - Logistics\n      - Returns Management\n      - Sales\n    serviceName: SAP S/4HANA Customer Return API\n    serviceCategory: API\n  - name: SAP S/4HANA Purchase Requisition API\n    baseURL: ''\n    tags:\n      - ERP\n      - Procurement\n      - Purchase Requisition\n      - Purchasing\n    serviceName: SAP S/4HANA Purchase Requisition API\n    serviceCategory: API\n  - name: SAP S/4HANA Outbound Delivery API\n    baseURL: ''\n    tags:\n      - ERP\n      - Logistics\n      - Outbound Delivery\n      - Shipping\n      - Warehouse\n    serviceName:\
  \ SAP S/4HANA Outbound Delivery API\n    serviceCategory: API\n  - name: SAP S/4HANA Inbound Delivery API\n    baseURL: ''\n    tags:\n      - ERP\n      - Inbound Delivery\n      - Logistics\n      - Receiving\n      - Warehouse\n    serviceName: SAP S/4HANA Inbound Delivery API\n    serviceCategory: API\n  - name: SAP S/4HANA Cost Center API\n    baseURL: ''\n    tags:\n      - Controlling\n      - Cost Center\n      - ERP\n      - Finance\n      - Master Data\n    serviceName: SAP S/4HANA Cost Center API\n    serviceCategory: API\n  - name: SAP S/4HANA GL Account API\n    baseURL: ''\n    tags:\n      - Accounting\n      - ERP\n      - Finance\n      - General Ledger\n      - GL Account\n      - Master Data\n    serviceName: SAP S/4HANA GL Account API\n    serviceCategory: API\n  - name: SAP S/4HANA Bank Master API\n    baseURL: ''\n    tags:\n      - Bank\n      - ERP\n      - Finance\n      - Master Data\n      - Payment\n    serviceName: SAP S/4HANA Bank Master API\n    serviceCategory:\
  \ API\n  - name: SAP S/4HANA Production Order API\n    baseURL: ''\n    tags:\n      - ERP\n      - Manufacturing\n      - Production Order\n      - Production Planning\n    serviceName: SAP S/4HANA Production Order API\n    serviceCategory: API\n  - name: SAP S/4HANA Maintenance Order API\n    baseURL: ''\n    tags:\n      - Asset Management\n      - ERP\n      - Maintenance Order\n      - Plant Maintenance\n    serviceName: SAP S/4HANA Maintenance Order API\n    serviceCategory: API\n  - name: SAP S/4HANA Workforce Timesheet API\n    baseURL: ''\n    tags:\n      - ERP\n      - Human Resources\n      - Time Management\n      - Timesheet\n      - Workforce\n    serviceName: SAP S/4HANA Workforce Timesheet API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email:\
  \ kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-s4hana/refs/heads/main/finops/sap-s4hana-finops.yml
sources: []
specification: FinOps Framework
tags:
- Business Applications
- Cloud
- Enterprise Resource Planning
- ERP
- Finance
- Human Resources
- Inventory
- Logistics
- Manufacturing
- Plant Maintenance
- Procurement
- S/4HANA
- Sales
- SAP
- FinOps
- Cost Management
- FOCUS
---
