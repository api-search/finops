---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Ariba Network API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/network/openapi.json
- filename: openapi.json
  format: json
  label: Ariba Procurement API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/procurement/openapi.json
- filename: openapi.json
  format: json
  label: Ariba Sourcing API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/sourcing/openapi.json
- filename: openapi.json
  format: json
  label: Ariba Contracts API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/contracts/openapi.json
- filename: openapi.json
  format: json
  label: Ariba Supplier API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/supplier/openapi.json
- filename: openapi.json
  format: json
  label: Ariba Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/analytics/openapi.json
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
description: FinOps framework definition for the Ariba API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Ariba
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Ariba
  PublisherName: Ariba
  ServiceCategory: Developer Tools / API
  ServiceName: Ariba
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
name: Ariba Finops
provider_name: Ariba
provider_slug: ariba
publisher_name: Ariba
service_category: API
slug: ariba-finops
source_filename: ariba-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Ariba\nproviderId: ariba\npublisherName: Ariba\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - B2B\n  - Catalog Management\n  - Compliance\n  - Contracts\n  - Enterprise\n  - Integration\n  - Invoicing\n  - Procurement\n  - Risk Management\n  - SAP\n  - Sourcing\n  - Spend Analysis\n  - Supplier Lifecycle\n  - Suppliers\n  - Supply Chain\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Ariba API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs\
  \ visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n   \
  \   - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Ariba\n  ServiceCategory: Developer Tools / API\n  ProviderName: Ariba\n  PublisherName: Ariba\n  InvoiceIssuerName: Ariba\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n\
  \      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Ariba Network API\n    baseURL: https://api.ariba.com/v2/network\n    tags:\n      - B2B\n      - EDI\n      - Invoicing\n      - Procurement\n      - Supply Chain\n    serviceName: Ariba Network API\n    serviceCategory: API\n  - name: Ariba Procurement API\n    baseURL: https://api.ariba.com/v2/procurement\n    tags:\n      - Procurement\n      - Purchase Orders\n      - Requisitions\n      - Spend Management\n    serviceName: Ariba Procurement API\n    serviceCategory: API\n  - name: Ariba Sourcing API\n    baseURL: https://api.ariba.com/v2/sourcing\n    tags:\n\
  \      - Auctions\n      - RFx\n      - Sourcing\n      - Supplier Management\n    serviceName: Ariba Sourcing API\n    serviceCategory: API\n  - name: Ariba Contracts API\n    baseURL: https://api.ariba.com/v2/contracts\n    tags:\n      - CLM\n      - Compliance\n      - Contract Management\n      - Contracts\n    serviceName: Ariba Contracts API\n    serviceCategory: API\n  - name: Ariba Supplier API\n    baseURL: https://api.ariba.com/v2/supplier\n    tags:\n      - Performance\n      - Risk Management\n      - Supplier Information\n      - Supplier Management\n    serviceName: Ariba Supplier API\n    serviceCategory: API\n  - name: Ariba Analytics API\n    baseURL: https://api.ariba.com/v2/analytics\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Reporting\n      - Spend Analysis\n    serviceName: Ariba Analytics API\n    serviceCategory: API\n  - name: Operational Reporting API for Procurement\n    baseURL: ''\n    tags:\n      - Operational Data\n      - Procurement\n\
  \      - Purchase Orders\n      - Reporting\n      - Requisitions\n    serviceName: Operational Reporting API for Procurement\n    serviceCategory: API\n  - name: Operational Reporting API for Strategic Sourcing\n    baseURL: ''\n    tags:\n      - Bids\n      - Events\n      - Operational Data\n      - Reporting\n      - Strategic Sourcing\n    serviceName: Operational Reporting API for Strategic Sourcing\n    serviceCategory: API\n  - name: Analytical Reporting API for Strategic and Operational Procurement\n    baseURL: ''\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Operational Procurement\n      - Reporting\n      - Strategic Procurement\n    serviceName: Analytical Reporting API for Strategic and Operational Procurement\n    serviceCategory: API\n  - name: Supplier Data API with Pagination\n    baseURL: ''\n    tags:\n      - Pagination\n      - Performance\n      - Supplier Data\n      - Supplier Lifecycle\n      - Suppliers\n    serviceName: Supplier Data\
  \ API with Pagination\n    serviceCategory: API\n  - name: Supplier Data API\n    baseURL: ''\n    tags:\n      - Supplier Data\n      - Supplier Lifecycle\n      - Suppliers\n    serviceName: Supplier Data API\n    serviceCategory: API\n  - name: Supplier Data Extraction API\n    baseURL: ''\n    tags:\n      - Data Extraction\n      - Integration\n      - Suppliers\n    serviceName: Supplier Data Extraction API\n    serviceCategory: API\n  - name: Supplier Information API\n    baseURL: ''\n    tags:\n      - Profiles\n      - Supplier Information\n      - Suppliers\n    serviceName: Supplier Information API\n    serviceCategory: API\n  - name: Supplier Invite API\n    baseURL: ''\n    tags:\n      - Invitations\n      - Onboarding\n      - Suppliers\n    serviceName: Supplier Invite API\n    serviceCategory: API\n  - name: Ariba Network Supplier Profile API\n    baseURL: ''\n    tags:\n      - Ariba Network\n      - Certifications\n      - Profiles\n      - Suppliers\n    serviceName:\
  \ Ariba Network Supplier Profile API\n    serviceCategory: API\n  - name: Contract Workspace Management APIs\n    baseURL: ''\n    tags:\n      - Contract Requests\n      - Contract Terms\n      - Contract Workspaces\n      - Contracts\n    serviceName: Contract Workspace Management APIs\n    serviceCategory: API\n  - name: Contract Workspace Retrieval API\n    baseURL: ''\n    tags:\n      - Contract Workspaces\n      - Contracts\n      - Data Retrieval\n    serviceName: Contract Workspace Retrieval API\n    serviceCategory: API\n  - name: Contract Terms Management API\n    baseURL: ''\n    tags:\n      - Contract Terms\n      - Contracts\n      - Management\n    serviceName: Contract Terms Management API\n    serviceCategory: API\n  - name: Contract Compliance API\n    baseURL: ''\n    tags:\n      - Compliance\n      - Contracts\n      - Monitoring\n    serviceName: Contract Compliance API\n    serviceCategory: API\n  - name: Document Approval API\n    baseURL: ''\n    tags:\n     \
  \ - Approvals\n      - Invoices\n      - Requisitions\n      - Workflow\n    serviceName: Document Approval API\n    serviceCategory: API\n  - name: Ariba Network Purchase Orders API\n    baseURL: ''\n    tags:\n      - Ariba Network\n      - Buyers\n      - Purchase Orders\n      - Suppliers\n    serviceName: Ariba Network Purchase Orders API\n    serviceCategory: API\n  - name: Purchase Orders Supplier API\n    baseURL: ''\n    tags:\n      - Order Management\n      - Purchase Orders\n      - Suppliers\n    serviceName: Purchase Orders Supplier API\n    serviceCategory: API\n  - name: Order Change Requests API for Buyers\n    baseURL: ''\n    tags:\n      - Buyers\n      - Change Requests\n      - Purchase Orders\n    serviceName: Order Change Requests API for Buyers\n    serviceCategory: API\n  - name: Order Change Requests API for Suppliers\n    baseURL: ''\n    tags:\n      - Change Requests\n      - Purchase Orders\n      - Suppliers\n    serviceName: Order Change Requests API for\
  \ Suppliers\n    serviceCategory: API\n  - name: Ariba Network Invoice Header Data Extraction API\n    baseURL: ''\n    tags:\n      - Ariba Network\n      - Data Extraction\n      - Finance\n      - Invoices\n    serviceName: Ariba Network Invoice Header Data Extraction API\n    serviceCategory: API\n  - name: Ship Notice API for Buyers\n    baseURL: ''\n    tags:\n      - ASN\n      - Buyers\n      - Logistics\n      - Ship Notices\n    serviceName: Ship Notice API for Buyers\n    serviceCategory: API\n  - name: Ship Notice API for Suppliers\n    baseURL: ''\n    tags:\n      - ASN\n      - Logistics\n      - Ship Notices\n      - Suppliers\n    serviceName: Ship Notice API for Suppliers\n    serviceCategory: API\n  - name: Sourcing Project Management API\n    baseURL: ''\n    tags:\n      - Events\n      - Project Management\n      - Sourcing\n    serviceName: Sourcing Project Management API\n    serviceCategory: API\n  - name: Surrogate Bid API\n    baseURL: ''\n    tags:\n      -\
  \ Bidding\n      - Sourcing\n      - Suppliers\n    serviceName: Surrogate Bid API\n    serviceCategory: API\n  - name: Discovery RFx Publication TO External Marketplace API\n    baseURL: ''\n    tags:\n      - Discovery\n      - Marketplace\n      - RFx\n      - Supplier Participation\n    serviceName: Discovery RFx Publication TO External Marketplace API\n    serviceCategory: API\n  - name: Discovery RFx Publication FROM External Marketplace API\n    baseURL: ''\n    tags:\n      - Discovery\n      - Marketplace\n      - RFx\n      - Sourcing\n    serviceName: Discovery RFx Publication FROM External Marketplace API\n    serviceCategory: API\n  - name: External Approval API for Sourcing and Supplier Management\n    baseURL: ''\n    tags:\n      - Approvals\n      - Sourcing\n      - Supplier Management\n      - Workflow\n    serviceName: External Approval API for Sourcing and Supplier Management\n    serviceCategory: API\n  - name: Flow Extension API\n    baseURL: ''\n    tags:\n    \
  \  - Ariba Network\n      - Extensions\n      - Integration\n      - Workflow\n    serviceName: Flow Extension API\n    serviceCategory: API\n  - name: SAP Ariba Catalog Content API\n    baseURL: ''\n    tags:\n      - Catalogs\n      - Content Management\n      - Products\n    serviceName: SAP Ariba Catalog Content API\n    serviceCategory: API\n  - name: Catalog Connectivity Service API\n    baseURL: ''\n    tags:\n      - Catalogs\n      - Integration\n      - Punchout\n    serviceName: Catalog Connectivity Service API\n    serviceCategory: API\n  - name: Internal Catalogs Shop API\n    baseURL: ''\n    tags:\n      - Catalogs\n      - Procurement\n      - Shopping\n    serviceName: Internal Catalogs Shop API\n    serviceCategory: API\n  - name: Public Catalogs Shop API\n    baseURL: ''\n    tags:\n      - Catalogs\n      - Public Catalogs\n      - Shopping\n    serviceName: Public Catalogs Shop API\n    serviceCategory: API\n  - name: Network Catalog Management API\n    baseURL: ''\n\
  \    tags:\n      - Ariba Network\n      - Catalog Management\n      - Catalogs\n    serviceName: Network Catalog Management API\n    serviceCategory: API\n  - name: Content Lookup API\n    baseURL: ''\n    tags:\n      - Content\n      - Integration\n      - Lookup\n    serviceName: Content Lookup API\n    serviceCategory: API\n  - name: Create Procurement Workspace API\n    baseURL: ''\n    tags:\n      - Procurement\n      - Project Management\n      - Workspaces\n    serviceName: Create Procurement Workspace API\n    serviceCategory: API\n  - name: Dynamic Lookup Table API\n    baseURL: ''\n    tags:\n      - Configuration\n      - Data Management\n      - Lookup Tables\n    serviceName: Dynamic Lookup Table API\n    serviceCategory: API\n  - name: Risk Exposure API\n    baseURL: ''\n    tags:\n      - Risk Exposure\n      - Risk Management\n      - Suppliers\n    serviceName: Risk Exposure API\n    serviceCategory: API\n  - name: Risk Category Information API for Supplier Risk Exposure\n\
  \    baseURL: ''\n    tags:\n      - Risk Categories\n      - Risk Management\n      - Suppliers\n    serviceName: Risk Category Information API for Supplier Risk Exposure\n    serviceCategory: API\n  - name: Supplier Risk Engagements API\n    baseURL: ''\n    tags:\n      - Engagements\n      - Risk Management\n      - Suppliers\n    serviceName: Supplier Risk Engagements API\n    serviceCategory: API\n  - name: Engagement Risk Assessment External Response Import API\n    baseURL: ''\n    tags:\n      - Assessments\n      - External Data\n      - Risk Management\n    serviceName: Engagement Risk Assessment External Response Import API\n    serviceCategory: API\n  - name: Finding and Event Collaboration Integration API for Supplier Risk\n    baseURL: ''\n    tags:\n      - Collaboration\n      - Events\n      - Risk Management\n      - Suppliers\n    serviceName: Finding and Event Collaboration Integration API for Supplier Risk\n    serviceCategory: API\n  - name: Pricing API for Product\
  \ Sourcing Price Information\n    baseURL: ''\n    tags:\n      - Pricing\n      - Products\n      - Sourcing\n    serviceName: Pricing API for Product Sourcing Price Information\n    serviceCategory: API\n  - name: Audit Search API\n    baseURL: ''\n    tags:\n      - Audit\n      - Compliance\n      - Tracking\n    serviceName: Audit Search API\n    serviceCategory: API\n  - name: Master Data Retrieval API for Procurement\n    baseURL: ''\n    tags:\n      - Data Retrieval\n      - Master Data\n      - Procurement\n    serviceName: Master Data Retrieval API for Procurement\n    serviceCategory: API\n  - name: Master Data Retrieval API for Sourcing\n    baseURL: ''\n    tags:\n      - Data Retrieval\n      - Master Data\n      - Sourcing\n    serviceName: Master Data Retrieval API for Sourcing\n    serviceCategory: API\n  - name: Master Data Integration Job Status API for Operational Procurement\n    baseURL: ''\n    tags:\n      - Integration\n      - Job Status\n      - Master Data\n\
  \      - Procurement\n    serviceName: Master Data Integration Job Status API for Operational Procurement\n    serviceCategory: API\n  - name: Proof of Service API for Buyers\n    baseURL: ''\n    tags:\n      - Buyers\n      - Proof of Service\n      - Receipts\n    serviceName: Proof of Service API for Buyers\n    serviceCategory: API\n  - name: Proof of Service API for Suppliers\n    baseURL: ''\n    tags:\n      - Delivery\n      - Proof of Service\n      - Suppliers\n    serviceName: Proof of Service API for Suppliers\n    serviceCategory: API\n  - name: Asset Management API\n    baseURL: ''\n    tags:\n      - Assets\n      - Management\n      - Procurement\n    serviceName: Asset Management API\n    serviceCategory: API\n  - name: Bill of Materials Import API\n    baseURL: ''\n    tags:\n      - Bill of Materials\n      - Import\n      - Sourcing\n    serviceName: Bill of Materials Import API\n    serviceCategory: API\n  - name: Materials and BOM Tag Management API\n    baseURL:\
  \ ''\n    tags:\n      - Bill of Materials\n      - Classification\n      - Materials\n    serviceName: Materials and BOM Tag Management API\n    serviceCategory: API\n  - name: Item Volume Import API\n    baseURL: ''\n    tags:\n      - Import\n      - Items\n      - Sourcing\n      - Volume\n    serviceName: Item Volume Import API\n    serviceCategory: API\n  - name: Product Hierarchy Management API\n    baseURL: ''\n    tags:\n      - Categories\n      - Classification\n      - Hierarchy\n      - Products\n    serviceName: Product Hierarchy Management API\n    serviceCategory: API\n  - name: User Qualification API\n    baseURL: ''\n    tags:\n      - Access Control\n      - Qualifications\n      - Users\n    serviceName: User Qualification API\n    serviceCategory: API\n  - name: SAP Ariba Custom Forms API\n    baseURL: ''\n    tags:\n      - Custom Forms\n      - Extensions\n      - Procurement\n    serviceName: SAP Ariba Custom Forms API\n    serviceCategory: API\n  - name: SAP Ariba\
  \ SCIM API\n    baseURL: ''\n    tags:\n      - Identity Management\n      - SCIM\n      - User Provisioning\n    serviceName: SAP Ariba SCIM API\n    serviceCategory: API\n  - name: Event Management API\n    baseURL: ''\n    tags:\n      - Events\n      - Management\n      - Tracking\n    serviceName: Event Management API\n    serviceCategory: API\n  - name: Integration Event Monitoring Query API for Procurement\n    baseURL: ''\n    tags:\n      - Events\n      - Integration\n      - Monitoring\n      - Procurement\n    serviceName: Integration Event Monitoring Query API for Procurement\n    serviceCategory: API\n  - name: Integration Monitoring API for Procurement\n    baseURL: ''\n    tags:\n      - Integration\n      - Monitoring\n      - Procurement\n    serviceName: Integration Monitoring API for Procurement\n    serviceCategory: API\n  - name: Integration Monitoring API for Strategic Sourcing\n    baseURL: ''\n    tags:\n      - Integration\n      - Monitoring\n      - Strategic\
  \ Sourcing\n    serviceName: Integration Monitoring API for Strategic Sourcing\n    serviceCategory: API\n  - name: Transaction Monitoring API\n    baseURL: ''\n    tags:\n      - Monitoring\n      - Transactions\n      - Workflow\n    serviceName: Transaction Monitoring API\n    serviceCategory: API\n  - name: Asynchronous Requests Management API\n    baseURL: ''\n    tags:\n      - Asynchronous\n      - Integration\n      - Job Management\n    serviceName: Asynchronous Requests Management API\n    serviceCategory: API\n  - name: Configuration Parameter Review API\n    baseURL: ''\n    tags:\n      - Administration\n      - Configuration\n      - Parameters\n    serviceName: Configuration Parameter Review API\n    serviceCategory: API\n  - name: Data Replication Status for Multi-ERP Configurations\n    baseURL: ''\n    tags:\n      - Data Replication\n      - Integration\n      - Monitoring\n      - Multi-ERP\n    serviceName: Data Replication Status for Multi-ERP Configurations\n   \
  \ serviceCategory: API\n  - name: Trading Partner Profile Certification API\n    baseURL: ''\n    tags:\n      - Ariba Network\n      - Certification\n      - Compliance\n      - Trading Partners\n    serviceName: Trading Partner Profile Certification API\n    serviceCategory: API\n  - name: Cost Breakdown Data Extraction API\n    baseURL: ''\n    tags:\n      - Cost Analysis\n      - Data Extraction\n      - Sourcing\n      - Spend\n    serviceName: Cost Breakdown Data Extraction API\n    serviceCategory: API\n  - name: NDA Data Export API\n    baseURL: ''\n    tags:\n      - Compliance\n      - Data Export\n      - Legal\n      - NDA\n    serviceName: NDA Data Export API\n    serviceCategory: API\n  - name: Public Procurement Notices Export API\n    baseURL: ''\n    tags:\n      - Export\n      - Notices\n      - Public Procurement\n      - Tenders\n    serviceName: Public Procurement Notices Export API\n    serviceCategory: API\n  - name: Guided Buying Functional Documents API\n   \
  \ baseURL: ''\n    tags:\n      - Documents\n      - Guided Buying\n      - Procurement\n    serviceName: Guided Buying Functional Documents API\n    serviceCategory: API\n  - name: Planning Collaboration Buyer API\n    baseURL: ''\n    tags:\n      - Buyers\n      - Collaboration\n      - Planning\n      - Supply Chain\n    serviceName: Planning Collaboration Buyer API\n    serviceCategory: API\n  - name: Planning Collaboration Supplier API\n    baseURL: ''\n    tags:\n      - Collaboration\n      - Planning\n      - Suppliers\n      - Supply Chain\n    serviceName: Planning Collaboration Supplier API\n    serviceCategory: API\n  - name: Project Document Management API\n    baseURL: ''\n    tags:\n      - Documents\n      - Project Management\n      - Version Control\n    serviceName: Project Document Management API\n    serviceCategory: API\n  - name: ETendering Notice Management API\n    baseURL: ''\n    tags:\n      - eTendering\n      - Notices\n      - Procurement\n      - Public\
  \ Sector\n    serviceName: ETendering Notice Management API\n    serviceCategory: API\n  - name: SAP Build Work Zone CDM Content API for Sourcing\n    baseURL: ''\n    tags:\n      - Content\n      - Integration\n      - SAP Build Work Zone\n      - Sourcing\n    serviceName: SAP Build Work Zone CDM Content API for Sourcing\n    serviceCategory: API\n  - name: SAP Build Work Zone CDM Content API for Procurement\n    baseURL: ''\n    tags:\n      - Content\n      - Integration\n      - Procurement\n      - SAP Build Work Zone\n    serviceName: SAP Build Work Zone CDM Content API for Procurement\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ariba/refs/heads/main/finops/ariba-finops.yml
sources: []
specification: FinOps Framework
tags:
- B2B
- Catalog Management
- Compliance
- Contracts
- Enterprise
- Integration
- Invoicing
- Procurement
- Risk Management
- SAP
- Sourcing
- Spend Analysis
- Supplier Lifecycle
- Suppliers
- Supply Chain
- FinOps
- Cost Management
- FOCUS
---
