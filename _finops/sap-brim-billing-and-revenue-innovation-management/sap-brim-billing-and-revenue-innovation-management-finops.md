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
  label: SAP Convergent Charging API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/convergent_charging/overview
- filename: overview
  format: yaml
  label: SAP Convergent Invoicing API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/convergent_invoicing/overview
- filename: overview
  format: yaml
  label: SAP Subscription Billing API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/subscription_billing/overview
- filename: overview
  format: yaml
  label: SAP Contract Accounts Receivable and Payable API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/fica/overview
- filename: overview
  format: yaml
  label: SAP BRIM Usage Data Intake API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/usage_data_intake/overview
- filename: overview
  format: yaml
  label: SAP Revenue Accounting and Reporting API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/revenue_accounting/overview
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
description: FinOps framework definition for the SAP BRIM (Billing and Revenue Innovation Management) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SAP BRIM (Billing and Revenue Innovation Management)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SAP BRIM (Billing and Revenue Innovation Management)
  PublisherName: SAP BRIM (Billing and Revenue Innovation Management)
  ServiceCategory: Developer Tools / API
  ServiceName: SAP BRIM (Billing and Revenue Innovation Management)
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
name: Sap Brim Billing And Revenue Innovation Management Finops
provider_name: SAP BRIM (Billing and Revenue Innovation Management)
provider_slug: sap-brim-billing-and-revenue-innovation-management
publisher_name: SAP BRIM (Billing and Revenue Innovation Management)
service_category: API
slug: sap-brim-billing-and-revenue-innovation-management-finops
source_filename: sap-brim-billing-and-revenue-innovation-management-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP BRIM (Billing and Revenue Innovation Management)\nproviderId: sap-brim-billing-and-revenue-innovation-management\npublisherName: SAP BRIM (Billing and Revenue Innovation Management)\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Billing\n  - Enterprise\n  - Order to Cash\n  - Revenue Management\n  - SAP\n  - Subscription Management\n  - Usage-Based Pricing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SAP BRIM (Billing and Revenue Innovation Management)\n  API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics\n  reporting across the provider's APIs.\nprinciples:\n\
  \  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n\
  \      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SAP BRIM (Billing and Revenue Innovation Management)\n  ServiceCategory: Developer Tools / API\n  ProviderName: SAP BRIM (Billing and Revenue Innovation Management)\n  PublisherName: SAP BRIM (Billing and Revenue Innovation Management)\n  InvoiceIssuerName: SAP BRIM (Billing and Revenue Innovation Management)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n\
  \  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SAP Convergent Charging API\n    baseURL: https://api.sap.com/convergent-charging\n    tags:\n      - Charging\n      - Rating\n      - Real-Time\n      - Usage-Based Pricing\n    serviceName: SAP Convergent Charging API\n    serviceCategory: API\n  - name: SAP Convergent Invoicing API\n    baseURL: https://api.sap.com/convergent-invoicing\n\
  \    tags:\n      - Billing\n      - Invoice Management\n      - Invoicing\n    serviceName: SAP Convergent Invoicing API\n    serviceCategory: API\n  - name: SAP Subscription Billing API\n    baseURL: https://api.sap.com/subscription-billing\n    tags:\n      - Lifecycle Management\n      - Recurring Billing\n      - Subscriptions\n    serviceName: SAP Subscription Billing API\n    serviceCategory: API\n  - name: SAP Contract Accounts Receivable and Payable API\n    baseURL: https://api.sap.com/fica\n    tags:\n      - Accounts Receivable\n      - Dunning\n      - Financial Accounting\n      - Payments\n    serviceName: SAP Contract Accounts Receivable and Payable API\n    serviceCategory: API\n  - name: SAP BRIM Usage Data Intake API\n    baseURL: https://api.sap.com/usage-data-intake\n    tags:\n      - Data Ingestion\n      - Mediation\n      - Usage Data\n    serviceName: SAP BRIM Usage Data Intake API\n    serviceCategory: API\n  - name: SAP Revenue Accounting and Reporting API\n\
  \    baseURL: https://api.sap.com/revenue-accounting\n    tags:\n      - ASC 606\n      - Compliance\n      - IFRS 15\n      - Revenue Recognition\n    serviceName: SAP Revenue Accounting and Reporting API\n    serviceCategory: API\n  - name: SAP Subscription Order Management API\n    baseURL: https://api.sap.com/subscription-order-management\n    tags:\n      - Lifecycle Management\n      - Order Management\n      - Subscription Orders\n    serviceName: SAP Subscription Order Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-brim-billing-and-revenue-innovation-management/refs/heads/main/finops/sap-brim-billing-and-revenue-innovation-management-finops.yml
sources: []
specification: FinOps Framework
tags:
- Billing
- Enterprise
- Order to Cash
- Revenue Management
- SAP
- Subscription Management
- Usage-Based Pricing
- FinOps
- Cost Management
- FOCUS
---
