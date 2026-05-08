---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sap-ariba-procurement-api.yml
  format: yaml
  label: SAP Ariba Procurement API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-ariba/refs/heads/main/openapi/sap-ariba-procurement-api.yml
- filename: openapi.json
  format: json
  label: SAP Ariba Sourcing API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/sourcing/openapi.json
- filename: openapi.json
  format: json
  label: SAP Ariba Supplier Management API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/supplier/openapi.json
- filename: openapi.json
  format: json
  label: SAP Ariba Contract Management API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/contracts/openapi.json
- filename: openapi.json
  format: json
  label: SAP Ariba Analytical Reporting API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/analytics/openapi.json
- filename: openapi.json
  format: json
  label: SAP Ariba Invoice Management API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/invoices/openapi.json
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
description: FinOps framework definition for the SAP Ariba API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SAP Ariba
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SAP Ariba
  PublisherName: SAP Ariba
  ServiceCategory: Developer Tools / API
  ServiceName: SAP Ariba
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
name: Sap Ariba Finops
provider_name: SAP Ariba
provider_slug: sap-ariba
publisher_name: SAP Ariba
service_category: API
slug: sap-ariba-finops
source_filename: sap-ariba-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP Ariba\nproviderId: sap-ariba\npublisherName: SAP Ariba\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - B2B\n  - Contract Management\n  - Procurement\n  - Sourcing\n  - Spend Analysis\n  - Supplier Management\n  - Supply Chain\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SAP Ariba API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n   \
  \ description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the\
  \ FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SAP Ariba\n  ServiceCategory: Developer Tools / API\n  ProviderName: SAP Ariba\n  PublisherName: SAP Ariba\n  InvoiceIssuerName: SAP Ariba\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SAP Ariba Procurement API\n    baseURL: https://openapi.ariba.com/api/procurement\n    tags:\n      - Invoices\n      - Procurement\n      - Purchase Orders\n      - Requisitions\n      - Suppliers\n    serviceName: SAP Ariba Procurement API\n    serviceCategory: API\n  - name: SAP Ariba Sourcing API\n    baseURL: https://openapi.ariba.com/api/sourcing\n    tags:\n      - Auctions\n      - Bidding\n      - RFx\n      - Sourcing\n    serviceName: SAP Ariba Sourcing API\n    serviceCategory: API\n  - name: SAP Ariba Supplier Management API\n    baseURL: https://openapi.ariba.com/api/supplier\n    tags:\n      - Onboarding\n      - Performance\n   \
  \   - Risk Management\n      - Suppliers\n    serviceName: SAP Ariba Supplier Management API\n    serviceCategory: API\n  - name: SAP Ariba Contract Management API\n    baseURL: https://openapi.ariba.com/api/contracts\n    tags:\n      - CLM\n      - Compliance\n      - Contracts\n    serviceName: SAP Ariba Contract Management API\n    serviceCategory: API\n  - name: SAP Ariba Analytical Reporting API\n    baseURL: https://openapi.ariba.com/api/analytics\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Reporting\n      - Spend Analysis\n    serviceName: SAP Ariba Analytical Reporting API\n    serviceCategory: API\n  - name: SAP Ariba Invoice Management API\n    baseURL: https://openapi.ariba.com/api/invoices\n    tags:\n      - AP Automation\n      - Invoices\n      - Payments\n    serviceName: SAP Ariba Invoice Management API\n    serviceCategory: API\n  - name: Ariba Network Purchase Orders Buyer API\n    baseURL: https://openapi.ariba.com/api/purchase-orders-buyer\n\
  \    tags:\n      - Ariba Network\n      - Buyers\n      - Purchase Orders\n    serviceName: Ariba Network Purchase Orders Buyer API\n    serviceCategory: API\n  - name: Ariba Network Purchase Orders Supplier API\n    baseURL: https://openapi.ariba.com/api/purchase-orders-supplier\n    tags:\n      - Ariba Network\n      - Purchase Orders\n      - Suppliers\n    serviceName: Ariba Network Purchase Orders Supplier API\n    serviceCategory: API\n  - name: Ariba Network Supplier Profile API\n    baseURL: https://openapi.ariba.com/api/supplier-profile\n    tags:\n      - Ariba Network\n      - Profiles\n      - Suppliers\n    serviceName: Ariba Network Supplier Profile API\n    serviceCategory: API\n  - name: Ariba Network Invoice Header Data Extraction API\n    baseURL: https://openapi.ariba.com/api/invoice-extraction\n    tags:\n      - Ariba Network\n      - Data Extraction\n      - Invoices\n    serviceName: Ariba Network Invoice Header Data Extraction API\n    serviceCategory: API\n \
  \ - name: SAP Ariba Contract Compliance API\n    baseURL: https://openapi.ariba.com/api/contract-compliance\n    tags:\n      - Compliance\n      - Contracts\n      - Procurement\n    serviceName: SAP Ariba Contract Compliance API\n    serviceCategory: API\n  - name: SAP Ariba Supplier Data API\n    baseURL: https://openapi.ariba.com/api/supplier-data\n    tags:\n      - Data\n      - Master Data\n      - Suppliers\n    serviceName: SAP Ariba Supplier Data API\n    serviceCategory: API\n  - name: SAP Ariba Supplier Data API with Pagination\n    baseURL: https://openapi.ariba.com/api/supplier-data-paginated\n    tags:\n      - Data\n      - Pagination\n      - Suppliers\n    serviceName: SAP Ariba Supplier Data API with Pagination\n    serviceCategory: API\n  - name: SAP Ariba Supplier Data Extraction API\n    baseURL: https://openapi.ariba.com/api/supplier-data-extraction\n    tags:\n      - Data Extraction\n      - Integration\n      - Suppliers\n    serviceName: SAP Ariba Supplier Data\
  \ Extraction API\n    serviceCategory: API\n  - name: SAP Ariba Supplier Information API\n    baseURL: https://openapi.ariba.com/api/supplier-information\n    tags:\n      - Lifecycle\n      - Profiles\n      - Suppliers\n    serviceName: SAP Ariba Supplier Information API\n    serviceCategory: API\n  - name: SAP Ariba Supplier Invite API\n    baseURL: https://openapi.ariba.com/api/supplier-invite\n    tags:\n      - Invitations\n      - Onboarding\n      - Suppliers\n    serviceName: SAP Ariba Supplier Invite API\n    serviceCategory: API\n  - name: SAP Ariba Risk Exposure API\n    baseURL: https://openapi.ariba.com/api/risk-exposure\n    tags:\n      - Risk Management\n      - Suppliers\n      - Supply Chain\n    serviceName: SAP Ariba Risk Exposure API\n    serviceCategory: API\n  - name: SAP Ariba Supplier Risk Engagements API\n    baseURL: https://openapi.ariba.com/api/supplier-risk-engagements\n    tags:\n      - Assessments\n      - Risk Management\n      - Suppliers\n    serviceName:\
  \ SAP Ariba Supplier Risk Engagements API\n    serviceCategory: API\n  - name: SAP Ariba Risk Category Information API\n    baseURL: https://openapi.ariba.com/api/risk-category\n    tags:\n      - Categories\n      - Classification\n      - Risk Management\n    serviceName: SAP Ariba Risk Category Information API\n    serviceCategory: API\n  - name: SAP Ariba Document Approval API\n    baseURL: https://openapi.ariba.com/api/document-approval\n    tags:\n      - Approvals\n      - Documents\n      - Workflows\n    serviceName: SAP Ariba Document Approval API\n    serviceCategory: API\n  - name: SAP Ariba External Approval API for Sourcing and Supplier Management\n    baseURL: https://openapi.ariba.com/api/external-approval\n    tags:\n      - Approvals\n      - Sourcing\n      - Supplier Management\n    serviceName: SAP Ariba External Approval API for Sourcing and Supplier Management\n    serviceCategory: API\n  - name: SAP Ariba Catalog Content API\n    baseURL: https://openapi.ariba.com/api/catalog-content\n\
  \    tags:\n      - Catalogs\n      - Content Management\n      - Products\n    serviceName: SAP Ariba Catalog Content API\n    serviceCategory: API\n  - name: SAP Ariba Network Catalog Management API\n    baseURL: https://openapi.ariba.com/api/network-catalog\n    tags:\n      - Catalogs\n      - Network\n      - Publishing\n    serviceName: SAP Ariba Network Catalog Management API\n    serviceCategory: API\n  - name: SAP Ariba Internal Catalogs Shop API\n    baseURL: https://openapi.ariba.com/api/internal-catalogs\n    tags:\n      - Catalogs\n      - Internal\n      - Shopping\n    serviceName: SAP Ariba Internal Catalogs Shop API\n    serviceCategory: API\n  - name: SAP Ariba Public Catalogs Shop API\n    baseURL: https://openapi.ariba.com/api/public-catalogs\n    tags:\n      - Catalogs\n      - Marketplace\n      - Shopping\n    serviceName: SAP Ariba Public Catalogs Shop API\n    serviceCategory: API\n  - name: SAP Ariba Contract Workspace Retrieval API\n    baseURL: https://openapi.ariba.com/api/contract-workspace-retrieval\n\
  \    tags:\n      - CLM\n      - Contracts\n      - Workspaces\n    serviceName: SAP Ariba Contract Workspace Retrieval API\n    serviceCategory: API\n  - name: SAP Ariba Contract Workspace Management API\n    baseURL: https://openapi.ariba.com/api/contract-workspace-management\n    tags:\n      - Contracts\n      - Management\n      - Workspaces\n    serviceName: SAP Ariba Contract Workspace Management API\n    serviceCategory: API\n  - name: SAP Ariba Contract Terms Management API\n    baseURL: https://openapi.ariba.com/api/contract-terms\n    tags:\n      - Clauses\n      - Contracts\n      - Terms\n    serviceName: SAP Ariba Contract Terms Management API\n    serviceCategory: API\n  - name: SAP Ariba Operational Reporting API for Procurement\n    baseURL: https://openapi.ariba.com/api/operational-reporting-procurement\n    tags:\n      - Operations\n      - Procurement\n      - Reporting\n    serviceName: SAP Ariba Operational Reporting API for Procurement\n    serviceCategory: API\n\
  \  - name: SAP Ariba Operational Reporting API for Strategic Sourcing\n    baseURL: https://openapi.ariba.com/api/operational-reporting-sourcing\n    tags:\n      - Operations\n      - Reporting\n      - Sourcing\n    serviceName: SAP Ariba Operational Reporting API for Strategic Sourcing\n    serviceCategory: API\n  - name: SAP Ariba Analytical Reporting API for Strategic and Operational Procurement\n    baseURL: https://openapi.ariba.com/api/analytical-reporting\n    tags:\n      - Analytics\n      - Operational Procurement\n      - Reporting\n      - Strategic Procurement\n    serviceName: SAP Ariba Analytical Reporting API for Strategic and Operational Procurement\n    serviceCategory: API\n  - name: SAP Ariba Master Data Retrieval API for Sourcing\n    baseURL: https://openapi.ariba.com/api/master-data-sourcing\n    tags:\n      - Master Data\n      - Reference Data\n      - Sourcing\n    serviceName: SAP Ariba Master Data Retrieval API for Sourcing\n    serviceCategory: API\n  -\
  \ name: SAP Ariba Master Data Retrieval API for Procurement\n    baseURL: https://openapi.ariba.com/api/master-data-procurement\n    tags:\n      - Master Data\n      - Procurement\n      - Reference Data\n    serviceName: SAP Ariba Master Data Retrieval API for Procurement\n    serviceCategory: API\n  - name: SAP Ariba Sourcing Project Management API\n    baseURL: https://openapi.ariba.com/api/sourcing-project\n    tags:\n      - Events\n      - Projects\n      - Sourcing\n    serviceName: SAP Ariba Sourcing Project Management API\n    serviceCategory: API\n  - name: SAP Ariba Event Management API\n    baseURL: https://openapi.ariba.com/api/event-management\n    tags:\n      - Auctions\n      - Events\n      - RFx\n      - Sourcing\n    serviceName: SAP Ariba Event Management API\n    serviceCategory: API\n  - name: SAP Ariba Surrogate Bid API\n    baseURL: https://openapi.ariba.com/api/surrogate-bid\n    tags:\n      - Bidding\n      - Proxy\n      - Sourcing\n    serviceName: SAP Ariba\
  \ Surrogate Bid API\n    serviceCategory: API\n  - name: SAP Ariba Order Change Requests API for Buyers\n    baseURL: https://openapi.ariba.com/api/order-change-buyer\n    tags:\n      - Buyers\n      - Change Requests\n      - Purchase Orders\n    serviceName: SAP Ariba Order Change Requests API for Buyers\n    serviceCategory: API\n  - name: SAP Ariba Order Change Requests API for Suppliers\n    baseURL: https://openapi.ariba.com/api/order-change-supplier\n    tags:\n      - Change Requests\n      - Purchase Orders\n      - Suppliers\n    serviceName: SAP Ariba Order Change Requests API for Suppliers\n    serviceCategory: API\n  - name: SAP Ariba Ship Notice API for Buyers\n    baseURL: https://openapi.ariba.com/api/ship-notice-buyer\n    tags:\n      - Buyers\n      - Notifications\n      - Shipping\n    serviceName: SAP Ariba Ship Notice API for Buyers\n    serviceCategory: API\n  - name: SAP Ariba Ship Notice API for Suppliers\n    baseURL: https://openapi.ariba.com/api/ship-notice-supplier\n\
  \    tags:\n      - Notifications\n      - Shipping\n      - Suppliers\n    serviceName: SAP Ariba Ship Notice API for Suppliers\n    serviceCategory: API\n  - name: SAP Ariba Proof of Service API for Buyers\n    baseURL: https://openapi.ariba.com/api/proof-of-service-buyer\n    tags:\n      - Buyers\n      - Proof of Service\n    serviceName: SAP Ariba Proof of Service API for Buyers\n    serviceCategory: API\n  - name: SAP Ariba Proof of Service API for Suppliers\n    baseURL: https://openapi.ariba.com/api/proof-of-service-supplier\n    tags:\n      - Proof of Service\n      - Suppliers\n    serviceName: SAP Ariba Proof of Service API for Suppliers\n    serviceCategory: API\n  - name: SAP Ariba Planning Collaboration Buyer API\n    baseURL: https://openapi.ariba.com/api/planning-collaboration-buyer\n    tags:\n      - Buyers\n      - Collaboration\n      - Forecasting\n      - Planning\n    serviceName: SAP Ariba Planning Collaboration Buyer API\n    serviceCategory: API\n  - name: SAP\
  \ Ariba Planning Collaboration Supplier API\n    baseURL: https://openapi.ariba.com/api/planning-collaboration-supplier\n    tags:\n      - Collaboration\n      - Forecasting\n      - Planning\n      - Suppliers\n    serviceName: SAP Ariba Planning Collaboration Supplier API\n    serviceCategory: API\n  - name: SAP Ariba Item Volume Import API\n    baseURL: https://openapi.ariba.com/api/item-volume-import\n    tags:\n      - Import\n      - Planning\n      - Volume\n    serviceName: SAP Ariba Item Volume Import API\n    serviceCategory: API\n  - name: SAP Ariba Bill of Materials Import API\n    baseURL: https://openapi.ariba.com/api/bom-import\n    tags:\n      - BOM\n      - Import\n      - Materials\n    serviceName: SAP Ariba Bill of Materials Import API\n    serviceCategory: API\n  - name: SAP Ariba Product Hierarchy Management API\n    baseURL: https://openapi.ariba.com/api/product-hierarchy\n    tags:\n      - Classification\n      - Hierarchy\n      - Products\n    serviceName:\
  \ SAP Ariba Product Hierarchy Management API\n    serviceCategory: API\n  - name: SAP Ariba Pricing API for Product Sourcing\n    baseURL: https://openapi.ariba.com/api/pricing\n    tags:\n      - Pricing\n      - Products\n      - Sourcing\n    serviceName: SAP Ariba Pricing API for Product Sourcing\n    serviceCategory: API\n  - name: SAP Ariba Cost Breakdown Data Extraction API\n    baseURL: https://openapi.ariba.com/api/cost-breakdown\n    tags:\n      - Cost Analysis\n      - Data Extraction\n      - Sourcing\n    serviceName: SAP Ariba Cost Breakdown Data Extraction API\n    serviceCategory: API\n  - name: SAP Ariba Content Lookup API\n    baseURL: https://openapi.ariba.com/api/content-lookup\n    tags:\n      - Content\n      - Lookup\n      - Search\n    serviceName: SAP Ariba Content Lookup API\n    serviceCategory: API\n  - name: SAP Ariba Audit Search API\n    baseURL: https://openapi.ariba.com/api/audit-search\n    tags:\n      - Audit\n      - Compliance\n      - Search\n\
  \    serviceName: SAP Ariba Audit Search API\n    serviceCategory: API\n  - name: SAP Ariba Create Procurement Workspace API\n    baseURL: https://openapi.ariba.com/api/procurement-workspace\n    tags:\n      - Collaboration\n      - Procurement\n      - Workspaces\n    serviceName: SAP Ariba Create Procurement Workspace API\n    serviceCategory: API\n  - name: SAP Ariba Flow Extension API\n    baseURL: https://openapi.ariba.com/api/flow-extension\n    tags:\n      - Customization\n      - Extensions\n      - Workflows\n    serviceName: SAP Ariba Flow Extension API\n    serviceCategory: API\n  - name: SAP Ariba Asynchronous Requests Management API\n    baseURL: https://openapi.ariba.com/api/async-requests\n    tags:\n      - Async\n      - Management\n      - Operations\n    serviceName: SAP Ariba Asynchronous Requests Management API\n    serviceCategory: API\n  - name: SAP Ariba Integration Event Monitoring Query API for Procurement\n    baseURL: https://openapi.ariba.com/api/integration-event-monitoring\n\
  \    tags:\n      - Events\n      - Integration\n      - Monitoring\n      - Procurement\n    serviceName: SAP Ariba Integration Event Monitoring Query API for Procurement\n    serviceCategory: API\n  - name: SAP Ariba Integration Monitoring API for Procurement\n    baseURL: https://openapi.ariba.com/api/integration-monitoring-procurement\n    tags:\n      - Integration\n      - Monitoring\n      - Procurement\n    serviceName: SAP Ariba Integration Monitoring API for Procurement\n    serviceCategory: API\n  - name: SAP Ariba Integration Monitoring API for Strategic Sourcing\n    baseURL: https://openapi.ariba.com/api/integration-monitoring-sourcing\n    tags:\n      - Integration\n      - Monitoring\n      - Sourcing\n    serviceName: SAP Ariba Integration Monitoring API for Strategic Sourcing\n    serviceCategory: API\n  - name: SAP Ariba Transaction Monitoring API\n    baseURL: https://openapi.ariba.com/api/transaction-monitoring\n    tags:\n      - Monitoring\n      - Operations\n\
  \      - Transactions\n    serviceName: SAP Ariba Transaction Monitoring API\n    serviceCategory: API\n  - name: SAP Ariba NDA Data Export API\n    baseURL: https://openapi.ariba.com/api/nda-export\n    tags:\n      - Compliance\n      - Export\n      - NDA\n    serviceName: SAP Ariba NDA Data Export API\n    serviceCategory: API\n  - name: SAP Ariba Catalog Connectivity Service API\n    baseURL: https://openapi.ariba.com/api/catalog-connectivity\n    tags:\n      - Catalogs\n      - Integration\n      - Punchout\n    serviceName: SAP Ariba Catalog Connectivity Service API\n    serviceCategory: API\n  - name: SAP Ariba Trading Partner Profile Certification API\n    baseURL: https://openapi.ariba.com/api/trading-partner-certification\n    tags:\n      - Certification\n      - Compliance\n      - Trading Partners\n    serviceName: SAP Ariba Trading Partner Profile Certification API\n    serviceCategory: API\n  - name: SAP Ariba User Qualification API\n    baseURL: https://openapi.ariba.com/api/user-qualification\n\
  \    tags:\n      - Access\n      - Qualifications\n      - Users\n    serviceName: SAP Ariba User Qualification API\n    serviceCategory: API\n  - name: SAP Ariba SCIM API\n    baseURL: https://openapi.ariba.com/api/scim\n    tags:\n      - Identity\n      - Provisioning\n      - SCIM\n      - User Management\n    serviceName: SAP Ariba SCIM API\n    serviceCategory: API\n  - name: SAP Ariba Custom Forms API\n    baseURL: https://openapi.ariba.com/api/custom-forms\n    tags:\n      - Customization\n      - Forms\n      - Workflows\n    serviceName: SAP Ariba Custom Forms API\n    serviceCategory: API\n  - name: SAP Ariba Dynamic Lookup Table API\n    baseURL: https://openapi.ariba.com/api/dynamic-lookup-table\n    tags:\n      - Configuration\n      - Lookup Tables\n      - Reference Data\n    serviceName: SAP Ariba Dynamic Lookup Table API\n    serviceCategory: API\n  - name: SAP Ariba Guided Buying Functional Documents API\n    baseURL: https://openapi.ariba.com/api/guided-buying\n\
  \    tags:\n      - Documents\n      - Guided Buying\n      - Procurement\n    serviceName: SAP Ariba Guided Buying Functional Documents API\n    serviceCategory: API\n  - name: SAP Ariba Asset Management API\n    baseURL: https://openapi.ariba.com/api/asset-management\n    tags:\n      - Assets\n      - Inventory\n      - Lifecycle\n    serviceName: SAP Ariba Asset Management API\n    serviceCategory: API\n  - name: SAP Ariba Configuration Parameter Review API\n    baseURL: https://openapi.ariba.com/api/configuration-review\n    tags:\n      - Administration\n      - Configuration\n      - Parameters\n    serviceName: SAP Ariba Configuration Parameter Review API\n    serviceCategory: API\n  - name: SAP Ariba Project Document Management API\n    baseURL: https://openapi.ariba.com/api/project-documents\n    tags:\n      - Documents\n      - Management\n      - Projects\n    serviceName: SAP Ariba Project Document Management API\n    serviceCategory: API\n  - name: SAP Ariba Public Procurement\
  \ Notices Export API\n    baseURL: https://openapi.ariba.com/api/public-procurement-notices\n    tags:\n      - Notices\n      - Public Procurement\n      - Tenders\n    serviceName: SAP Ariba Public Procurement Notices Export API\n    serviceCategory: API\n  - name: SAP Ariba ETendering Notice Management API\n    baseURL: https://openapi.ariba.com/api/etendering\n    tags:\n      - eTendering\n      - Notices\n      - Public Procurement\n    serviceName: SAP Ariba ETendering Notice Management API\n    serviceCategory: API\n  - name: SAP Ariba Discovery RFx Publication TO External Marketplace API\n    baseURL: https://openapi.ariba.com/api/discovery-rfx-to-external\n    tags:\n      - Discovery\n      - Marketplace\n      - RFx\n    serviceName: SAP Ariba Discovery RFx Publication TO External Marketplace API\n    serviceCategory: API\n  - name: SAP Ariba Discovery RFx Publication FROM External Marketplace API\n    baseURL: https://openapi.ariba.com/api/discovery-rfx-from-external\n   \
  \ tags:\n      - Discovery\n      - Marketplace\n      - RFx\n    serviceName: SAP Ariba Discovery RFx Publication FROM External Marketplace API\n    serviceCategory: API\n  - name: SAP Ariba Materials and BOM Tag Management API\n    baseURL: https://openapi.ariba.com/api/materials-bom-tags\n    tags:\n      - BOM\n      - Classification\n      - Materials\n    serviceName: SAP Ariba Materials and BOM Tag Management API\n    serviceCategory: API\n  - name: SAP Ariba Data Replication Status API\n    baseURL: https://openapi.ariba.com/api/data-replication-status\n    tags:\n      - Integration\n      - Multi-ERP\n      - Replication\n    serviceName: SAP Ariba Data Replication Status API\n    serviceCategory: API\n  - name: SAP Ariba Master Data Integration Job Status API\n    baseURL: https://openapi.ariba.com/api/master-data-job-status\n    tags:\n      - Integration\n      - Jobs\n      - Master Data\n    serviceName: SAP Ariba Master Data Integration Job Status API\n    serviceCategory:\
  \ API\n  - name: SAP Ariba Engagement Risk Assessment External Response Import API\n    baseURL: https://openapi.ariba.com/api/risk-assessment-import\n    tags:\n      - Assessments\n      - Import\n      - Risk Management\n    serviceName: SAP Ariba Engagement Risk Assessment External Response Import API\n    serviceCategory: API\n  - name: SAP Ariba Finding and Event Collaboration Integration API for Supplier Risk\n    baseURL: https://openapi.ariba.com/api/risk-collaboration\n    tags:\n      - Collaboration\n      - Findings\n      - Risk Management\n    serviceName: SAP Ariba Finding and Event Collaboration Integration API for Supplier Risk\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-ariba/refs/heads/main/finops/sap-ariba-finops.yml
sources: []
specification: FinOps Framework
tags:
- B2B
- Contract Management
- Procurement
- Sourcing
- Spend Analysis
- Supplier Management
- Supply Chain
- FinOps
- Cost Management
- FOCUS
---
