---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: lane-api-openapi.yml
  format: yaml
  label: Lane API
  slug: lane-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lane-api/refs/heads/main/openapi/lane-api-openapi.yml
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
description: FinOps framework definition for the Lane API API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Lane API
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Lane API
  PublisherName: Lane API
  ServiceCategory: Developer Tools / API
  ServiceName: Lane API
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
name: Lane Api Finops
provider_name: Lane API
provider_slug: lane-api
publisher_name: Lane API
service_category: API
slug: lane-api-finops
source_filename: lane-api-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Lane API\nproviderId: lane-api\npublisherName: Lane API\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Asset Leasing\n  - Credit\n  - Loans\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Lane API API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application,\
  \ and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education\
  \ and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Lane API\n  ServiceCategory: Developer Tools / API\n  ProviderName: Lane API\n  PublisherName: Lane API\n  InvoiceIssuerName: Lane API\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n\
  \      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Lane API\n    baseURL: ''\n    tags:\n      - Accord\n      - Add\n      - Additional\n      - Address\n      - Affordability\n      - Agreement\n      - Allowed\n      - An\n      - Analytics\n      - Appointment\n      - Appointment  Management\n      - Approve\n      - Assets\n      - Associated\n      - Bookmarks\n      - Builder\n      - Calculate\n      - Calculations\n      - Changes\n      - Checks\n      - Code\n      - Comments\n      - Company\n      - Configuration\n      - Configure\n      - Consents\n      - Contract\n      - Contracts\n      - Countries\n      - Create_application\n      - Credit\n      - Currencies\n      - Customer\n      - Customer  Consent\n      - Customer  Document\n      - Customer_reference_id\n      - Customers\n\
  \      - Dashboard\n      - Data\n      - Deal\n      - Dealer\n      - Dealer  Management\n      - Dealer_code\n      - Dealer_id\n      - Dealers\n      - Decisions\n      - Disclaimer\n      - Disclaimer  Management\n      - Disclaimers\n      - Distance\n      - Dms\n      - Document\n      - Document  Generation\n      - Document  Package  Management\n      - Document_id\n      - Document_identifier\n      - Documents\n      - Downloads\n      - Due\n      - Dynamic\n      - Email\n      - Employment\n      - Event_analytic\n      - Event_name\n      - Expiry\n      - External\n      - Fee\n      - Fees\n      - Filter\n      - Finance\n      - Financial\n      - Find\n      - Flags\n      - Fraud\n      - Fulfillment\n      - Generate\n      - Get  a N  Signed  U R L\n      - Get_event_associated_checklist\n      - Health\n      - History\n      - Identifiers\n      - Impact\n      - Index  Wrapper\n      - Indicators\n      - Information\n      - Inspection\n      - Insurance\n\
  \      - Integration_type\n      - Integrations\n      - Inventory\n      - Is_payment_updated\n      - Keys\n      - Lead\n      - Lead- Management\n      - Lender\n      - Lender_id\n      - Licenses\n      - Links\n      - Make\n      - Metadata\n      - Methods\n      - Mileage\n      - Model\n      - Multi\n      - Name\n      - Notifications\n      - Numbers\n      - Options\n      - Order\n      - Order  Calculations\n      - Order  Management\n      - Order  Stakeholder  Management\n      - Orders\n      - Packages\n      - Party\n      - Past\n      - Payment\n      - Payments\n      - Personal\n      - Plaid\n      - Pre\n      - Preferences\n      - Profiles\n      - Programs\n      - Proposals\n      - Provider_name\n      - Quantity\n      - Quotation\n      - Quote\n      - Ratings\n      - Reference\n      - Reference_number\n      - References\n      - Removes\n      - Request\n      - Response\n      - Reviews\n      - Role\n      - Root\n      - Save\n      - Search\n\
  \      - Send\n      - Send  Email  Notification\n      - Set\n      - Setup\n      - Signature\n      - Signatures\n      - Signed\n      - Signer_role\n      - State\n      - Status\n      - Statuses\n      - Stipulation\n      - Stream\n      - Submission_id\n      - Submit\n      - Tenant\n      - Term\n      - Theme\n      - Theme  Builder\n      - Trade\n      - Trade- In\n      - Trade_in_history\n      - Tradein\n      - Trim\n      - Uploading\n      - Uploads\n      - Usage\n      - Vehicle\n      - Vendor\n      - Verifications\n      - Verify\n      - Version\n      - Vin\n      - Webhooks\n      - Workqueue  Management\n      - Year\n    serviceName: Lane API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lane-api/refs/heads/main/finops/lane-api-finops.yml
sources: []
specification: FinOps Framework
tags:
- Asset Leasing
- Credit
- Loans
- FinOps
- Cost Management
- FOCUS
---
