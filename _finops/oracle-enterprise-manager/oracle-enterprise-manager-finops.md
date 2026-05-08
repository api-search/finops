---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: oracle-enterprise-manager-cloud-control-openapi.yml
  format: yaml
  label: Oracle Enterprise Manager Cloud Control REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-enterprise-manager/refs/heads/main/openapi/oracle-enterprise-manager-cloud-control-openapi.yml
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
description: FinOps framework definition for the Oracle Enterprise Manager API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle Enterprise Manager
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle Enterprise Manager
  PublisherName: Oracle Enterprise Manager
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle Enterprise Manager
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
name: Oracle Enterprise Manager Finops
provider_name: Oracle Enterprise Manager
provider_slug: oracle-enterprise-manager
publisher_name: Oracle Enterprise Manager
service_category: API
slug: oracle-enterprise-manager-finops
source_filename: oracle-enterprise-manager-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Enterprise Manager\nproviderId: oracle-enterprise-manager\npublisherName: Oracle Enterprise Manager\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Management\n  - Database Management\n  - Enterprise Management\n  - Infrastructure Management\n  - Monitoring\n  - Oracle\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle Enterprise Manager API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle Enterprise Manager\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle Enterprise Manager\n  PublisherName: Oracle Enterprise Manager\n  InvoiceIssuerName: Oracle Enterprise Manager\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      -\
  \ endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle Enterprise Manager Cloud Control REST API\n    baseURL: https://<em-host>:<port>/em/api\n    tags:\n      - Administration\n      - Cloud Control\n      - Monitoring\n      - REST API\n    serviceName: Oracle Enterprise Manager Cloud Control REST API\n    serviceCategory: API\n  - name: Enterprise Manager Command Line Interface (EM CLI)\n    baseURL: https://<em-host>:<port>/em\n    tags:\n      - Automation\n      - CLI\n      - Command Line\n      - Scripting\n    serviceName: Enterprise Manager Command Line Interface\
  \ (EM CLI)\n    serviceCategory: API\n  - name: Enterprise Manager Job System API\n    baseURL: https://<em-host>:<port>/em/websvcs/restful/emws/job\n    tags:\n      - Automation\n      - Jobs\n      - Scheduling\n      - Task Management\n    serviceName: Enterprise Manager Job System API\n    serviceCategory: API\n  - name: Enterprise Manager Metric and Monitoring API\n    baseURL: https://<em-host>:<port>/em/websvcs/restful/emws/metric\n    tags:\n      - Alerts\n      - Metrics\n      - Monitoring\n      - Performance\n    serviceName: Enterprise Manager Metric and Monitoring API\n    serviceCategory: API\n  - name: Enterprise Manager Target Management API\n    baseURL: https://<em-host>:<port>/em/websvcs/restful/emws/target\n    tags:\n      - Configuration\n      - Discovery\n      - Lifecycle\n      - Target Management\n    serviceName: Enterprise Manager Target Management API\n    serviceCategory: API\n  - name: Enterprise Manager Incidents and Events API\n    baseURL: https://<em-host>:<port>/em/api/incidents\n\
  \    tags:\n      - Alerting\n      - Events\n      - Incidents\n      - Troubleshooting\n    serviceName: Enterprise Manager Incidents and Events API\n    serviceCategory: API\n  - name: Enterprise Manager Blackout Management API\n    baseURL: https://<em-host>:<port>/em/api/blackouts\n    tags:\n      - Blackouts\n      - Maintenance Windows\n      - Scheduling\n    serviceName: Enterprise Manager Blackout Management API\n    serviceCategory: API\n  - name: Enterprise Manager Credentials Management API\n    baseURL: https://<em-host>:<port>/em/api/credentials\n    tags:\n      - Authentication\n      - Credentials\n      - Security\n    serviceName: Enterprise Manager Credentials Management API\n    serviceCategory: API\n  - name: Enterprise Manager User Management API\n    baseURL: https://<em-host>:<port>/em/api/users\n    tags:\n      - Permissions\n      - Roles\n      - Security\n      - User Management\n    serviceName: Enterprise Manager User Management API\n    serviceCategory:\
  \ API\n  - name: Enterprise Manager Database Patching and Maintenance API\n    baseURL: https://<em-host>:<port>/em/api/dblm\n    tags:\n      - Database Maintenance\n      - Fleet Maintenance\n      - Gold Images\n      - Lifecycle Management\n      - Patching\n    serviceName: Enterprise Manager Database Patching and Maintenance API\n    serviceCategory: API\n  - name: Enterprise Manager Deployment Procedure API\n    baseURL: https://<em-host>:<port>/em/api/deploymentProcedures\n    tags:\n      - Automation\n      - Deployment\n      - Procedures\n      - Provisioning\n    serviceName: Enterprise Manager Deployment Procedure API\n    serviceCategory: API\n  - name: Enterprise Manager Database Backup Management API\n    baseURL: https://<em-host>:<port>/em/api/databaseBackup\n    tags:\n      - Backup Management\n      - Database Backup\n      - Recovery\n    serviceName: Enterprise Manager Database Backup Management API\n    serviceCategory: API\n  - name: Enterprise Manager ZDLRA Management\
  \ API\n    baseURL: https://<em-host>:<port>/em/api/zdlra\n    tags:\n      - Data Protection\n      - Recovery Appliance\n      - ZDLRA\n      - Zero Data Loss\n    serviceName: Enterprise Manager ZDLRA Management API\n    serviceCategory: API\n  - name: Enterprise Manager SQL Execution REST API\n    baseURL: https://<em-host>:<port>/em/api/db/sql\n    tags:\n      - Data Extraction\n      - Database Queries\n      - Reporting\n      - SQL Execution\n    serviceName: Enterprise Manager SQL Execution REST API\n    serviceCategory: API\n  - name: Enterprise Manager Data Guard Administration REST API\n    baseURL: https://<em-host>:<port>/em/api/dataguard\n    tags:\n      - Data Guard\n      - Disaster Recovery\n      - High Availability\n      - Standby Database\n    serviceName: Enterprise Manager Data Guard Administration REST API\n    serviceCategory: API\n  - name: Enterprise Manager Cloud APIs (DBaaS)\n    baseURL: https://<em-host>:<port>/em/cloud\n    tags:\n      - Cloud\n    \
  \  - Database as a Service\n      - DBaaS\n      - Provisioning\n      - Self-Service\n    serviceName: Enterprise Manager Cloud APIs (DBaaS)\n    serviceCategory: API\n  - name: Enterprise Manager Extensibility Development Kit (EDK) API\n    baseURL: https://<em-host>:<port>/em\n    tags:\n      - Custom Monitoring\n      - Extensibility\n      - Plugin Development\n      - SDK\n    serviceName: Enterprise Manager Extensibility Development Kit (EDK) API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-enterprise-manager/refs/heads/main/finops/oracle-enterprise-manager-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Management
- Database Management
- Enterprise Management
- Infrastructure Management
- Monitoring
- Oracle
- FinOps
- Cost Management
- FOCUS
---
