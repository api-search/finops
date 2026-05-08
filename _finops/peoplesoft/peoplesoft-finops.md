---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rest-api.yml
  format: yaml
  label: PeopleSoft REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/rest-api.yml
- filename: application-services-framework.yml
  format: yaml
  label: PeopleSoft Application Services Framework API
  slug: application-services-framework-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/application-services-framework.yml
- filename: integration-broker.yml
  format: yaml
  label: PeopleSoft Integration Broker
  slug: integration-broker
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/integration-broker.yml
- filename: query.yml
  format: yaml
  label: PeopleSoft Query API
  slug: query-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/query.yml
- filename: component-interface.yml
  format: yaml
  label: PeopleSoft Component Interface API
  slug: component-interface-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/component-interface.yml
- filename: search-framework.yml
  format: yaml
  label: PeopleSoft Search Framework API
  slug: search-framework-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/search-framework.yml
- filename: notification-framework.yml
  format: yaml
  label: PeopleSoft Notification Framework API
  slug: notification-framework-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/notification-framework.yml
- filename: chatbot-integration.yml
  format: yaml
  label: PeopleSoft Chatbot Integration Framework API
  slug: chatbot-integration-framework-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/chatbot-integration.yml
- filename: approval-workflow-engine.yml
  format: yaml
  label: PeopleSoft Approval Workflow Engine API
  slug: approval-workflow-engine-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/approval-workflow-engine.yml
- filename: process-scheduler.yml
  format: yaml
  label: PeopleSoft Process Scheduler API
  slug: process-scheduler-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/process-scheduler.yml
- filename: cloud-manager.yml
  format: yaml
  label: PeopleSoft Cloud Manager API
  slug: cloud-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/cloud-manager.yml
- filename: update-manager.yml
  format: yaml
  label: PeopleSoft Update Manager API
  slug: update-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/update-manager.yml
- filename: pivot-grid.yml
  format: yaml
  label: PeopleSoft Pivot Grid API
  slug: pivot-grid-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/pivot-grid.yml
- filename: hcm.yml
  format: yaml
  label: PeopleSoft HCM API
  slug: hcm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/hcm.yml
- filename: recruiting-talent-management.yml
  format: yaml
  label: PeopleSoft Recruiting and Talent Management API
  slug: recruiting-and-talent-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/recruiting-talent-management.yml
- filename: financials.yml
  format: yaml
  label: PeopleSoft Financials API
  slug: financials-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/financials.yml
- filename: supply-chain-management.yml
  format: yaml
  label: PeopleSoft Supply Chain Management API
  slug: supply-chain-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/supply-chain-management.yml
- filename: crm.yml
  format: yaml
  label: PeopleSoft CRM API
  slug: crm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/crm.yml
- filename: campus-solutions.yml
  format: yaml
  label: PeopleSoft Campus Solutions API
  slug: campus-solutions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/campus-solutions.yml
- filename: enterprise-performance-management.yml
  format: yaml
  label: PeopleSoft Enterprise Performance Management API
  slug: enterprise-performance-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/enterprise-performance-management.yml
- filename: interaction-hub.yml
  format: yaml
  label: PeopleSoft Interaction Hub API
  slug: interaction-hub-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/interaction-hub.yml
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
description: FinOps framework definition for the PeopleSoft API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: PeopleSoft
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: PeopleSoft
  PublisherName: PeopleSoft
  ServiceCategory: Developer Tools / API
  ServiceName: PeopleSoft
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
name: Peoplesoft Finops
provider_name: PeopleSoft
provider_slug: peoplesoft
publisher_name: PeopleSoft
service_category: API
slug: peoplesoft-finops
source_filename: peoplesoft-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: PeopleSoft\nproviderId: peoplesoft\npublisherName: PeopleSoft\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Campus Solutions\n  - CRM\n  - Enterprise Software\n  - ERP\n  - Financial Management\n  - HCM\n  - Supply Chain Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the PeopleSoft API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: PeopleSoft\n  ServiceCategory: Developer Tools / API\n  ProviderName: PeopleSoft\n  PublisherName: PeopleSoft\n  InvoiceIssuerName: PeopleSoft\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the\
  \ network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: PeopleSoft REST API\n    baseURL: https://{hostname}:{port}/psft/api/v1\n    tags:\n      - Integration\n      - REST\n      - Web Services\n    serviceName: PeopleSoft REST API\n    serviceCategory: API\n  - name: PeopleSoft Application Services Framework API\n    baseURL: https://{hostname}:{port}/psft/asf/v1\n    tags:\n      - Integration\n      - Modern\n      - OpenAPI\n      - REST\n    serviceName: PeopleSoft Application Services Framework API\n    serviceCategory: API\n  - name: PeopleSoft Integration Broker\n    baseURL: https://{hostname}:{port}/PSIGW/RESTListeningConnector\n    tags:\n      - Integration\n      - Messaging\n \
  \     - REST\n      - SOAP\n    serviceName: PeopleSoft Integration Broker\n    serviceCategory: API\n  - name: PeopleSoft Query API\n    baseURL: https://{hostname}:{port}/psft/api/query/v1\n    tags:\n      - Data Access\n      - QAS\n      - Query\n      - Reporting\n    serviceName: PeopleSoft Query API\n    serviceCategory: API\n  - name: PeopleSoft Component Interface API\n    baseURL: https://{hostname}:{port}/psft/api/componentinterface/v1\n    tags:\n      - Component Interface\n      - CRUD Operations\n      - Data Access\n    serviceName: PeopleSoft Component Interface API\n    serviceCategory: API\n  - name: PeopleSoft Search Framework API\n    baseURL: https://{hostname}:{port}/psft/api/search/v1\n    tags:\n      - Analytics\n      - Insights\n      - OpenSearch\n      - Search\n    serviceName: PeopleSoft Search Framework API\n    serviceCategory: API\n  - name: PeopleSoft Data Distribution Framework API\n    baseURL: https://{hostname}:{port}/psft/api/ddf/v1\n    tags:\n\
  \      - Analytics\n      - Data Distribution\n      - Data Extraction\n      - Machine Learning\n    serviceName: PeopleSoft Data Distribution Framework API\n    serviceCategory: API\n  - name: PeopleSoft Notification Framework API\n    baseURL: https://{hostname}:{port}/psft/api/notifications/v1\n    tags:\n      - Events\n      - Messaging\n      - Notifications\n      - Push Notifications\n    serviceName: PeopleSoft Notification Framework API\n    serviceCategory: API\n  - name: PeopleSoft Chatbot Integration Framework API\n    baseURL: https://{hostname}:{port}/psft/api/chatbot/v1\n    tags:\n      - Chatbot\n      - Conversational AI\n      - Digital Assistant\n      - PICASO\n    serviceName: PeopleSoft Chatbot Integration Framework API\n    serviceCategory: API\n  - name: PeopleSoft Approval Workflow Engine API\n    baseURL: https://{hostname}:{port}/psft/api/approvals/v1\n    tags:\n      - Approvals\n      - AWE\n      - Workflow\n    serviceName: PeopleSoft Approval Workflow\
  \ Engine API\n    serviceCategory: API\n  - name: PeopleSoft Process Scheduler API\n    baseURL: https://{hostname}:{port}/psft/api/scheduler/v1\n    tags:\n      - Batch Processing\n      - Process Monitor\n      - Scheduling\n    serviceName: PeopleSoft Process Scheduler API\n    serviceCategory: API\n  - name: PeopleSoft Cloud Manager API\n    baseURL: https://{hostname}:{port}/psft/api/cloudmgr/v1\n    tags:\n      - Cloud\n      - Deployment\n      - OCI\n      - Provisioning\n    serviceName: PeopleSoft Cloud Manager API\n    serviceCategory: API\n  - name: PeopleSoft Update Manager API\n    baseURL: https://{hostname}:{port}/psft/api/pum/v1\n    tags:\n      - Lifecycle Management\n      - Patching\n      - Updates\n    serviceName: PeopleSoft Update Manager API\n    serviceCategory: API\n  - name: PeopleSoft Pivot Grid API\n    baseURL: https://{hostname}:{port}/psft/api/pivotgrid/v1\n    tags:\n      - Analytics\n      - Dashboards\n      - Pivot Grid\n      - Reporting\n    serviceName:\
  \ PeopleSoft Pivot Grid API\n    serviceCategory: API\n  - name: PeopleSoft HCM API\n    baseURL: https://{hostname}:{port}/psft/api/hcm/v1\n    tags:\n      - Benefits\n      - HCM\n      - HR\n      - Payroll\n    serviceName: PeopleSoft HCM API\n    serviceCategory: API\n  - name: PeopleSoft Employee Directory API\n    baseURL: https://{hostname}:{port}/psft/api/hcm/employeedirectory/v1\n    tags:\n      - Employee Directory\n      - HCM\n      - Workforce Data\n    serviceName: PeopleSoft Employee Directory API\n    serviceCategory: API\n  - name: PeopleSoft Absence Management API\n    baseURL: https://{hostname}:{port}/psft/api/hcm/absence/v1\n    tags:\n      - Absence Management\n      - HCM\n      - Leave\n      - Time Off\n    serviceName: PeopleSoft Absence Management API\n    serviceCategory: API\n  - name: PeopleSoft Recruiting and Talent Management API\n    baseURL: https://{hostname}:{port}/psft/api/hcm/recruiting/v1\n    tags:\n      - Candidate Gateway\n      - Job Search\n\
  \      - Recruiting\n      - Talent Management\n    serviceName: PeopleSoft Recruiting and Talent Management API\n    serviceCategory: API\n  - name: PeopleSoft Payroll for North America API\n    baseURL: https://{hostname}:{port}/psft/api/hcm/payrollbankingyearendforms/v1\n    tags:\n      - Compensation\n      - HCM\n      - North America\n      - Payroll\n    serviceName: PeopleSoft Payroll for North America API\n    serviceCategory: API\n  - name: PeopleSoft Global Payroll API\n    baseURL: https://{hostname}:{port}/psft/api/hcm/globalpayroll/v1\n    tags:\n      - Global Payroll\n      - HCM\n      - International\n      - Payroll\n    serviceName: PeopleSoft Global Payroll API\n    serviceCategory: API\n  - name: PeopleSoft HR Common Utility Services API\n    baseURL: https://{hostname}:{port}/psft/api/hcm/hcmcommonutilities/v1\n    tags:\n      - Employee Data\n      - HCM\n      - Utilities\n    serviceName: PeopleSoft HR Common Utility Services API\n    serviceCategory: API\n\
  \  - name: PeopleSoft Financials API\n    baseURL: https://{hostname}:{port}/psft/api/financials/v1\n    tags:\n      - AP\n      - AR\n      - Expenses\n      - Financials\n      - General Ledger\n    serviceName: PeopleSoft Financials API\n    serviceCategory: API\n  - name: PeopleSoft Expenses API\n    baseURL: https://{hostname}:{port}/psft/api/fscm/expenses/v1\n    tags:\n      - Expense Reports\n      - Expenses\n      - Financials\n      - Travel\n    serviceName: PeopleSoft Expenses API\n    serviceCategory: API\n  - name: PeopleSoft eSettlements API\n    baseURL: https://{hostname}:{port}/psft/api/fscm/esettlements/v1\n    tags:\n      - eSettlements\n      - Financials\n      - Invoices\n      - Payments\n    serviceName: PeopleSoft eSettlements API\n    serviceCategory: API\n  - name: PeopleSoft Supply Chain Management API\n    baseURL: https://{hostname}:{port}/psft/api/scm/v1\n    tags:\n      - Inventory\n      - Logistics\n      - Order Fulfillment\n      - Procurement\n\
  \      - Supply Chain\n    serviceName: PeopleSoft Supply Chain Management API\n    serviceCategory: API\n  - name: PeopleSoft eProcurement API\n    baseURL: https://{hostname}:{port}/psft/api/fscm/eprocurement/v1\n    tags:\n      - eProcurement\n      - Purchasing\n      - Requisitions\n      - Supply Chain\n    serviceName: PeopleSoft eProcurement API\n    serviceCategory: API\n  - name: PeopleSoft Supplier Portal API\n    baseURL: https://{hostname}:{port}/psft/api/fscm/scp/v1\n    tags:\n      - Sourcing\n      - Supplier Collaboration\n      - Supplier Portal\n      - Supply Chain\n    serviceName: PeopleSoft Supplier Portal API\n    serviceCategory: API\n  - name: PeopleSoft CRM API\n    baseURL: https://{hostname}:{port}/psft/api/crm/v1\n    tags:\n      - Case Management\n      - CRM\n      - Customer Data\n      - Marketing\n      - Sales\n    serviceName: PeopleSoft CRM API\n    serviceCategory: API\n  - name: PeopleSoft Campus Solutions API\n    baseURL: https://{hostname}:{port}/psft/api/campus/v1\n\
  \    tags:\n      - Admissions\n      - Campus Solutions\n      - Education\n      - Financial Aid\n      - Student Records\n    serviceName: PeopleSoft Campus Solutions API\n    serviceCategory: API\n  - name: PeopleSoft Enterprise Performance Management API\n    baseURL: https://{hostname}:{port}/psft/api/epm/v1\n    tags:\n      - Analytics\n      - Budgeting\n      - EPM\n      - Forecasting\n      - Planning\n    serviceName: PeopleSoft Enterprise Performance Management API\n    serviceCategory: API\n  - name: PeopleSoft Interaction Hub API\n    baseURL: https://{hostname}:{port}/psft/api/hub/v1\n    tags:\n      - Branding\n      - Content Management\n      - Interaction Hub\n      - Portal\n    serviceName: PeopleSoft Interaction Hub API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/finops/peoplesoft-finops.yml
sources: []
specification: FinOps Framework
tags:
- Campus Solutions
- CRM
- Enterprise Software
- ERP
- Financial Management
- HCM
- Supply Chain Management
- FinOps
- Cost Management
- FOCUS
---
