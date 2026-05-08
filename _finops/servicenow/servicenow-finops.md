---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: servicenow-table-api-openapi.yml
  format: yaml
  label: ServiceNow Table API
  slug: servicenow-table-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-table-api-openapi.yml
- filename: servicenow-aggregate-api-openapi.yml
  format: yaml
  label: ServiceNow Aggregate API
  slug: servicenow-aggregate-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-aggregate-api-openapi.yml
- filename: servicenow-attachment-api-openapi.yml
  format: yaml
  label: ServiceNow Attachment API
  slug: servicenow-attachment-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-attachment-api-openapi.yml
- filename: servicenow-import-set-api-openapi.yml
  format: yaml
  label: ServiceNow Import Set API
  slug: servicenow-import-set-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-import-set-api-openapi.yml
- filename: servicenow-change-management-api-openapi.yml
  format: yaml
  label: ServiceNow Change Management API
  slug: servicenow-change-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-change-management-api-openapi.yml
- filename: servicenow-service-catalog-api-openapi.yml
  format: yaml
  label: ServiceNow Service Catalog API
  slug: servicenow-service-catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-service-catalog-api-openapi.yml
- filename: servicenow-cmdb-instance-api-openapi.yml
  format: yaml
  label: ServiceNow CMDB Instance API
  slug: servicenow-cmdb-instance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-cmdb-instance-api-openapi.yml
- filename: contact-api-openapi.yaml
  format: yaml
  label: ServiceNow Contact API
  slug: servicenow-contact-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/contact-api-openapi.yaml
- filename: trouble-ticket-openapi.yaml
  format: yaml
  label: ServiceNow Trouble Ticket Open API
  slug: servicenow-trouble-ticket-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/trouble-ticket-openapi.yaml
- filename: servicenow-events-asyncapi.yml
  format: yaml
  label: ServiceNow Event Management Topic Open API
  slug: servicenow-event-management-topic-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/asyncapi/servicenow-events-asyncapi.yml
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
description: FinOps framework definition for the ServiceNow API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: ServiceNow
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: ServiceNow
  PublisherName: ServiceNow
  ServiceCategory: Developer Tools / API
  ServiceName: ServiceNow
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
name: Servicenow Finops
provider_name: ServiceNow
provider_slug: servicenow
publisher_name: ServiceNow
service_category: API
slug: servicenow-finops
source_filename: servicenow-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: ServiceNow\nproviderId: servicenow\npublisherName: ServiceNow\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Automation\n  - Cloud Services\n  - Digital Workflows\n  - Enterprise Platform\n  - IT Service Management\n  - ITSM\n  - Processes\n  - T1\n  - Workflow Automation\n  - Workflows\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the ServiceNow API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance\
  \ teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: ServiceNow\n  ServiceCategory: Developer Tools / API\n  ProviderName: ServiceNow\n  PublisherName: ServiceNow\n  InvoiceIssuerName: ServiceNow\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: ServiceNow Table API\n    baseURL: https://{instance}.service-now.com/api/now/table\n    tags:\n      - CRUD\n      - Data\n      - ITSM\n      - Records\n      - Tables\n    serviceName: ServiceNow Table API\n    serviceCategory: API\n  - name: ServiceNow Aggregate API\n    baseURL: https://{instance}.service-now.com/api/now/stats\n    tags:\n      - Aggregation\n      - Analytics\n      - Reporting\n      - Statistics\n      - Tables\n    serviceName: ServiceNow Aggregate API\n    serviceCategory: API\n  - name: ServiceNow Attachment API\n    baseURL: https://{instance}.service-now.com/api/now/attachment\n\
  \    tags:\n      - Attachments\n      - Files\n      - Records\n      - Upload\n    serviceName: ServiceNow Attachment API\n    serviceCategory: API\n  - name: ServiceNow Import Set API\n    baseURL: https://{instance}.service-now.com/api/now/import\n    tags:\n      - Data Loading\n      - ETL\n      - Import\n      - Integration\n    serviceName: ServiceNow Import Set API\n    serviceCategory: API\n  - name: ServiceNow Batch API\n    baseURL: https://{instance}.service-now.com/api/now/v1/batch\n    tags:\n      - Batch\n      - Integration\n      - Performance\n      - REST\n    serviceName: ServiceNow Batch API\n    serviceCategory: API\n  - name: ServiceNow Change Management API\n    baseURL: https://{instance}.service-now.com/api/sn_chg_rest/v1/change\n    tags:\n      - Change Management\n      - IT Operations\n      - ITSM\n      - Workflows\n    serviceName: ServiceNow Change Management API\n    serviceCategory: API\n  - name: ServiceNow Knowledge Management API\n    baseURL:\
  \ https://{instance}.service-now.com/api/sn_km_api/knowledge\n    tags:\n      - Articles\n      - Knowledge Base\n      - Knowledge Management\n      - Self-Service\n    serviceName: ServiceNow Knowledge Management API\n    serviceCategory: API\n  - name: ServiceNow Service Catalog API\n    baseURL: https://{instance}.service-now.com/api/sn_sc/servicecatalog\n    tags:\n      - ITSM\n      - Requests\n      - Self-Service\n      - Service Catalog\n    serviceName: ServiceNow Service Catalog API\n    serviceCategory: API\n  - name: ServiceNow CMDB Instance API\n    baseURL: https://{instance}.service-now.com/api/now/cmdb/instance\n    tags:\n      - Assets\n      - CMDB\n      - Configuration Management\n      - IT Operations\n    serviceName: ServiceNow CMDB Instance API\n    serviceCategory: API\n  - name: ServiceNow Identification and Reconciliation API\n    baseURL: https://{instance}.service-now.com/api/now/identifyreconcile\n    tags:\n      - CMDB\n      - Configuration Management\n\
  \      - Discovery\n      - Reconciliation\n    serviceName: ServiceNow Identification and Reconciliation API\n    serviceCategory: API\n  - name: ServiceNow Performance Analytics API\n    baseURL: https://{instance}.service-now.com/api/now/pa\n    tags:\n      - Analytics\n      - Dashboards\n      - Performance\n      - Reporting\n    serviceName: ServiceNow Performance Analytics API\n    serviceCategory: API\n  - name: ServiceNow Contact API\n    baseURL: https://{instance}.service-now.com/api/now/contact\n    tags:\n      - Contacts\n      - CSM\n      - Customer Service\n      - Records\n    serviceName: ServiceNow Contact API\n    serviceCategory: API\n  - name: ServiceNow Trouble Ticket Open API\n    baseURL: https://{instance}.service-now.com/api/now/troubleticket\n    tags:\n      - Customer Service\n      - Incidents\n      - TM Forum\n      - Trouble Tickets\n    serviceName: ServiceNow Trouble Ticket Open API\n    serviceCategory: API\n  - name: ServiceNow Scripted REST APIs\n\
  \    baseURL: https://{instance}.service-now.com/api/{namespace}/{api_id}\n    tags:\n      - Custom APIs\n      - Integration\n      - Platform\n      - Scripting\n    serviceName: ServiceNow Scripted REST APIs\n    serviceCategory: API\n  - name: ServiceNow GraphQL API\n    baseURL: https://{instance}.service-now.com/api/now/graphql\n    tags:\n      - Custom APIs\n      - GraphQL\n      - Integration\n      - Platform\n    serviceName: ServiceNow GraphQL API\n    serviceCategory: API\n  - name: ServiceNow Application Service API\n    baseURL: https://{instance}.service-now.com/api/now/cmdb/app_service\n    tags:\n      - Application Services\n      - CMDB\n      - IT Operations\n      - Service Mapping\n    serviceName: ServiceNow Application Service API\n    serviceCategory: API\n  - name: ServiceNow Case API\n    baseURL: https://{instance}.service-now.com/api/sn_customerservice/case\n    tags:\n      - Cases\n      - CSM\n      - Customer Service\n      - Support\n    serviceName:\
  \ ServiceNow Case API\n    serviceCategory: API\n  - name: ServiceNow Account API\n    baseURL: https://{instance}.service-now.com/api/now/account\n    tags:\n      - Accounts\n      - CSM\n      - Customer Service\n      - Records\n    serviceName: ServiceNow Account API\n    serviceCategory: API\n  - name: ServiceNow Consumer API\n    baseURL: https://{instance}.service-now.com/api/now/consumer\n    tags:\n      - Consumers\n      - CSM\n      - Customer Service\n      - Self-Service\n    serviceName: ServiceNow Consumer API\n    serviceCategory: API\n  - name: ServiceNow CSM Attachment API\n    baseURL: https://{instance}.service-now.com/api/sn_customerservice/attachment\n    tags:\n      - Attachments\n      - CSM\n      - Customer Service\n      - Files\n    serviceName: ServiceNow CSM Attachment API\n    serviceCategory: API\n  - name: ServiceNow Email API\n    baseURL: https://{instance}.service-now.com/api/now/email\n    tags:\n      - Email\n      - Messaging\n      - Notifications\n\
  \      - Platform\n    serviceName: ServiceNow Email API\n    serviceCategory: API\n  - name: ServiceNow CI/CD API\n    baseURL: https://{instance}.service-now.com/api/sn_cicd\n    tags:\n      - Automation\n      - CI/CD\n      - Deployment\n      - DevOps\n    serviceName: ServiceNow CI/CD API\n    serviceCategory: API\n  - name: ServiceNow CI/CD Update Set API\n    baseURL: https://{instance}.service-now.com/api/sn_cicd/update_set\n    tags:\n      - CI/CD\n      - Deployment\n      - DevOps\n      - Update Sets\n    serviceName: ServiceNow CI/CD Update Set API\n    serviceCategory: API\n  - name: ServiceNow DevOps API\n    baseURL: https://{instance}.service-now.com/api/sn_devops\n    tags:\n      - Change Velocity\n      - CI/CD\n      - DevOps\n      - Pipelines\n    serviceName: ServiceNow DevOps API\n    serviceCategory: API\n  - name: ServiceNow DevOps Config API\n    baseURL: https://{instance}.service-now.com/api/sn_devops_config\n    tags:\n      - Automation\n      - Change\
  \ Management\n      - Configuration\n      - DevOps\n    serviceName: ServiceNow DevOps Config API\n    serviceCategory: API\n  - name: ServiceNow CMDB Meta API\n    baseURL: https://{instance}.service-now.com/api/now/cmdb/meta\n    tags:\n      - CMDB\n      - Configuration Management\n      - Metadata\n      - Schema\n    serviceName: ServiceNow CMDB Meta API\n    serviceCategory: API\n  - name: ServiceNow CMDB Data Ingestion API\n    baseURL: https://{instance}.service-now.com/api/now/cmdb/ingest\n    tags:\n      - CMDB\n      - Configuration Management\n      - Data Ingestion\n      - Integration\n    serviceName: ServiceNow CMDB Data Ingestion API\n    serviceCategory: API\n  - name: ServiceNow MetricBase Time Series API\n    baseURL: https://{instance}.service-now.com/api/now/clotho\n    tags:\n      - ITOM\n      - Metrics\n      - Monitoring\n      - Time Series\n    serviceName: ServiceNow MetricBase Time Series API\n    serviceCategory: API\n  - name: ServiceNow Interaction\
  \ Management API\n    baseURL: https://{instance}.service-now.com/api/interaction\n    tags:\n      - Agent Workspace\n      - Customer Service\n      - Interactions\n      - Omnichannel\n    serviceName: ServiceNow Interaction Management API\n    serviceCategory: API\n  - name: ServiceNow Voice Interaction Resource API\n    baseURL: https://{instance}.service-now.com/api/now/voice\n    tags:\n      - Contact Center\n      - Interactions\n      - Telephony\n      - Voice\n    serviceName: ServiceNow Voice Interaction Resource API\n    serviceCategory: API\n  - name: ServiceNow User Role Inheritance API\n    baseURL: https://{instance}.service-now.com/api/now/user_role_inheritance\n    tags:\n      - Access Control\n      - Roles\n      - Security\n      - Users\n    serviceName: ServiceNow User Role Inheritance API\n    serviceCategory: API\n  - name: ServiceNow HR API\n    baseURL: https://{instance}.service-now.com/api/sn_hr_core\n    tags:\n      - Employee Services\n      - HR Service\
  \ Delivery\n      - HRSD\n      - Human Resources\n    serviceName: ServiceNow HR API\n    serviceCategory: API\n  - name: ServiceNow Event Management Topic Open API\n    baseURL: https://{instance}.service-now.com/api/em/topic\n    tags:\n      - Alerts\n      - Event Management\n      - ITOM\n      - Monitoring\n    serviceName: ServiceNow Event Management Topic Open API\n    serviceCategory: API\n  - name: ServiceNow Predictive Intelligence API\n    baseURL: https://{instance}.service-now.com/api/now/agent_intelligence\n    tags:\n      - AI\n      - Classification\n      - Machine Learning\n      - Predictions\n    serviceName: ServiceNow Predictive Intelligence API\n    serviceCategory: API\n  - name: ServiceNow AWA Agent API\n    baseURL: https://{instance}.service-now.com/api/now/awa/agent\n    tags:\n      - Agent Workspace\n      - Queues\n      - Routing\n      - Workforce Management\n    serviceName: ServiceNow AWA Agent API\n    serviceCategory: API\n  - name: ServiceNow AWA\
  \ Offer Work API\n    baseURL: https://{instance}.service-now.com/api/now/awa/offerwork\n    tags:\n      - Agent Workspace\n      - Queues\n      - Routing\n      - Work Assignment\n    serviceName: ServiceNow AWA Offer Work API\n    serviceCategory: API\n  - name: ServiceNow Virtual Agent Bot Integration API\n    baseURL: https://{instance}.service-now.com/api/sn_va_as_service\n    tags:\n      - Chatbot\n      - Conversational AI\n      - Self-Service\n      - Virtual Agent\n    serviceName: ServiceNow Virtual Agent Bot Integration API\n    serviceCategory: API\n  - name: ServiceNow Openframe API\n    baseURL: https://{instance}.service-now.com/api/now/openframe\n    tags:\n      - CCaaS\n      - Contact Center\n      - Integration\n      - Telephony\n    serviceName: ServiceNow Openframe API\n    serviceCategory: API\n  - name: ServiceNow AI Assets API\n    baseURL: https://{instance}.service-now.com/api/now/ai/assets\n    tags:\n      - AI Governance\n      - Artificial Intelligence\n\
  \      - Machine Learning\n      - Platform\n    serviceName: ServiceNow AI Assets API\n    serviceCategory: API\n  - name: ServiceNow Lead API\n    baseURL: https://{instance}.service-now.com/api/sn_lead\n    tags:\n      - CRM\n      - Leads\n      - Marketing\n      - Sales\n    serviceName: ServiceNow Lead API\n    serviceCategory: API\n  - name: ServiceNow Sales Agreement API\n    baseURL: https://{instance}.service-now.com/api/sn_sales_agreement\n    tags:\n      - Agreements\n      - Contracts\n      - CRM\n      - Sales\n    serviceName: ServiceNow Sales Agreement API\n    serviceCategory: API\n  - name: ServiceNow Agent Client Collector API\n    baseURL: https://{instance}.service-now.com/api/now/acc\n    tags:\n      - Agents\n      - Discovery\n      - ITOM\n      - Monitoring\n    serviceName: ServiceNow Agent Client Collector API\n    serviceCategory: API\n  - name: ServiceNow Agent Mapping API\n    baseURL: https://{instance}.service-now.com/api/now/agent_mapping\n    tags:\n\
  \      - Agent Workspace\n      - Integration\n      - Mapping\n      - Routing\n    serviceName: ServiceNow Agent Mapping API\n    serviceCategory: API\n  - name: ServiceNow Automation Center API\n    baseURL: https://{instance}.service-now.com/api/sn_automation_center\n    tags:\n      - Automation\n      - Orchestration\n      - Platform\n      - Workflows\n    serviceName: ServiceNow Automation Center API\n    serviceCategory: API\n  - name: ServiceNow AP Invoice API\n    baseURL: https://{instance}.service-now.com/api/now/ap/invoice\n    tags:\n      - Accounts Payable\n      - Finance\n      - Invoices\n      - Procurement\n    serviceName: ServiceNow AP Invoice API\n    serviceCategory: API\n  - name: ServiceNow CSM Order API\n    baseURL: https://{instance}.service-now.com/api/sn_customerservice/order\n    tags:\n      - Commerce\n      - CSM\n      - Customer Service\n      - Orders\n    serviceName: ServiceNow CSM Order API\n    serviceCategory: API\n  - name: ServiceNow CI Lifecycle\
  \ Management API\n    baseURL: https://{instance}.service-now.com/api/now/cmdb/ci_lifecycle\n    tags:\n      - CMDB\n      - Configuration Management\n      - IT Operations\n      - Lifecycle\n    serviceName: ServiceNow CI Lifecycle Management API\n    serviceCategory: API\n  - name: ServiceNow Alarm Management Open API\n    baseURL: https://{instance}.service-now.com/api/now/alarm\n    tags:\n      - Alerts\n      - Event Management\n      - ITOM\n      - Monitoring\n    serviceName: ServiceNow Alarm Management Open API\n    serviceCategory: API\n  - name: ServiceNow SAM Software Usage Data Integration API\n    baseURL: https://{instance}.service-now.com/api/sam/software_usage\n    tags:\n      - ITAM\n      - Licensing\n      - Software Asset Management\n      - Usage Tracking\n    serviceName: ServiceNow SAM Software Usage Data Integration API\n    serviceCategory: API\n  - name: ServiceNow Product Catalog Open API\n    baseURL: https://{instance}.service-now.com/api/sn_ind_tmt_orm/catalogManagement/v4\n\
  \    tags:\n      - Commerce\n      - Product Catalog\n      - Telecommunications\n      - TMF\n    serviceName: ServiceNow Product Catalog Open API\n    serviceCategory: API\n  - name: ServiceNow Service Catalog Open API\n    baseURL: https://{instance}.service-now.com/api/sn_ind_tmt_orm/serviceCatalogManagement/v4\n    tags:\n      - Commerce\n      - Service Catalog\n      - Telecommunications\n      - TMF\n    serviceName: ServiceNow Service Catalog Open API\n    serviceCategory: API\n  - name: ServiceNow Product Order Open API\n    baseURL: https://{instance}.service-now.com/api/sn_ind_tmt_orm/productOrderingManagement/v4\n    tags:\n      - Commerce\n      - Product Ordering\n      - Telecommunications\n      - TMF\n    serviceName: ServiceNow Product Order Open API\n    serviceCategory: API\n  - name: ServiceNow Service Order Open API\n    baseURL: https://{instance}.service-now.com/api/sn_ind_tmt_orm/serviceOrderingManagement/v4\n    tags:\n      - Commerce\n      - Service Ordering\n\
  \      - Telecommunications\n      - TMF\n    serviceName: ServiceNow Service Order Open API\n    serviceCategory: API\n  - name: ServiceNow Resource Inventory Open API\n    baseURL: https://{instance}.service-now.com/api/sn_ind_tmt_orm/resourceInventoryManagement/v4\n    tags:\n      - Inventory\n      - Resources\n      - Telecommunications\n      - TMF\n    serviceName: ServiceNow Resource Inventory Open API\n    serviceCategory: API\n  - name: ServiceNow Product Inventory Open API\n    baseURL: https://{instance}.service-now.com/api/sn_ind_tmt_orm/productInventoryManagement/v4\n    tags:\n      - Inventory\n      - Products\n      - Telecommunications\n      - TMF\n    serviceName: ServiceNow Product Inventory Open API\n    serviceCategory: API\n  - name: ServiceNow Service Test Management Open API\n    baseURL: https://{instance}.service-now.com/api/sn_ind_tmt_orm/serviceTestManagement/v4\n    tags:\n      - Quality\n      - Service Testing\n      - Telecommunications\n      - TMF\n\
  \    serviceName: ServiceNow Service Test Management Open API\n    serviceCategory: API\n  - name: ServiceNow Project Portfolio Management API\n    baseURL: https://{instance}.service-now.com/api/now/ppm\n    tags:\n      - Governance\n      - PPM\n      - Project Management\n      - Strategic Portfolio Management\n    serviceName: ServiceNow Project Portfolio Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/finops/servicenow-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automation
- Cloud Services
- Digital Workflows
- Enterprise Platform
- IT Service Management
- ITSM
- Processes
- T1
- Workflow Automation
- Workflows
- FinOps
- Cost Management
- FOCUS
---
