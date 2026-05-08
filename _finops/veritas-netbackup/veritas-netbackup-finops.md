---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: veritas-netbackup-rest-api-openapi.yml
  format: yaml
  label: Veritas NetBackup REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veritas-netbackup/refs/heads/main/openapi/veritas-netbackup-rest-api-openapi.yml
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
description: FinOps framework definition for the Veritas NetBackup API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Veritas NetBackup
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Veritas NetBackup
  PublisherName: Veritas NetBackup
  ServiceCategory: Developer Tools / API
  ServiceName: Veritas NetBackup
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
name: Veritas Netbackup Finops
provider_name: Veritas NetBackup
provider_slug: veritas-netbackup
publisher_name: Veritas NetBackup
service_category: API
slug: veritas-netbackup-finops
source_filename: veritas-netbackup-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Veritas NetBackup\nproviderId: veritas-netbackup\npublisherName: Veritas NetBackup\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Backup\n  - Data Protection\n  - Disaster Recovery\n  - Enterprise\n  - Recovery\n  - Storage\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Veritas NetBackup API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Veritas NetBackup\n  ServiceCategory: Developer Tools / API\n  ProviderName: Veritas NetBackup\n  PublisherName: Veritas NetBackup\n  InvoiceIssuerName: Veritas NetBackup\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Veritas NetBackup REST API\n    baseURL: https://netbackup-primary-server:1556/netbackup\n    tags:\n      - Backup\n      - Catalog\n      - Jobs\n      - Policies\n      - Restore\n    serviceName: Veritas NetBackup REST API\n    serviceCategory: API\n  - name: NetBackup Administration API\n    baseURL: https://netbackup-primary-server:1556/netbackup/admin\n    tags:\n      - Administration\n      - Jobs\n      - Management\n      - Monitoring\n    serviceName: NetBackup Administration API\n    serviceCategory: API\n  - name: NetBackup Asset Management API\n    baseURL: https://netbackup-primary-server:1556/netbackup/assets\n\
  \    tags:\n      - Assets\n      - Clients\n      - Inventory\n      - Servers\n    serviceName: NetBackup Asset Management API\n    serviceCategory: API\n  - name: NetBackup Security API\n    baseURL: https://netbackup-primary-server:1556/netbackup/security\n    tags:\n      - Audit\n      - Authentication\n      - Authorization\n      - Certificates\n      - Credentials\n      - Security\n    serviceName: NetBackup Security API\n    serviceCategory: API\n  - name: NetBackup Image Management API\n    baseURL: https://netbackup-primary-server:1556/netbackup/catalog\n    tags:\n      - Catalog\n      - Images\n      - Media\n      - Retention\n    serviceName: NetBackup Image Management API\n    serviceCategory: API\n  - name: NetBackup Configuration API\n    baseURL: https://netbackup-primary-server:1556/netbackup/config\n    tags:\n      - Configuration\n      - Hosts\n      - Policies\n      - Servers\n      - Storage\n    serviceName: NetBackup Configuration API\n    serviceCategory:\
  \ API\n  - name: NetBackup Storage API\n    baseURL: https://netbackup-primary-server:1556/netbackup/storage\n    tags:\n      - Capacity\n      - Consumption\n      - Reporting\n      - Storage\n    serviceName: NetBackup Storage API\n    serviceCategory: API\n  - name: NetBackup Recovery API\n    baseURL: https://netbackup-primary-server:1556/netbackup/recovery\n    tags:\n      - Cloud\n      - Instant-Access\n      - Recovery\n      - Restore\n      - Vmware\n    serviceName: NetBackup Recovery API\n    serviceCategory: API\n  - name: NetBackup RBAC Administration API\n    baseURL: https://netbackup-primary-server:1556/netbackup/rbac\n    tags:\n      - Access-Control\n      - Permissions\n      - Rbac\n      - Roles\n    serviceName: NetBackup RBAC Administration API\n    serviceCategory: API\n  - name: NetBackup Licensing API\n    baseURL: https://netbackup-primary-server:1556/netbackup/licensing\n    tags:\n      - Consumption\n      - Entitlements\n      - Licensing\n    serviceName:\
  \ NetBackup Licensing API\n    serviceCategory: API\n  - name: NetBackup Service Catalog API\n    baseURL: https://netbackup-primary-server:1556/netbackup/servicecatalog\n    tags:\n      - Protection-Plans\n      - Service-Catalog\n      - Slo\n      - Subscriptions\n    serviceName: NetBackup Service Catalog API\n    serviceCategory: API\n  - name: NetBackup Manage API\n    baseURL: https://netbackup-primary-server:1556/netbackup/manage\n    tags:\n      - Alerts\n      - Management\n      - Notifications\n    serviceName: NetBackup Manage API\n    serviceCategory: API\n  - name: NetBackup Troubleshooting API\n    baseURL: https://netbackup-primary-server:1556/netbackup/troubleshooting\n    tags:\n      - Diagnostics\n      - Errors\n      - Status-Codes\n      - Troubleshooting\n    serviceName: NetBackup Troubleshooting API\n    serviceCategory: API\n  - name: NetBackup IT Analytics REST API\n    baseURL: https://portal-server/api/v1\n    tags:\n      - Analytics\n      - Dashboards\n\
  \      - Monitoring\n      - Reporting\n    serviceName: NetBackup IT Analytics REST API\n    serviceCategory: API\n  - name: NetBackup Self Service REST API\n    baseURL: https://self-service-server/NetbackupAdapterPanels/Api\n    tags:\n      - Portal\n      - Self-Service\n      - Tenants\n      - Utilization\n    serviceName: NetBackup Self Service REST API\n    serviceCategory: API\n  - name: NetBackup Flex Scale REST API\n    baseURL: https://management-server:14161/swagger/infra/v1.0\n    tags:\n      - Appliance\n      - Cluster\n      - Flex-Scale\n      - Infrastructure\n      - Node-Management\n    serviceName: NetBackup Flex Scale REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veritas-netbackup/refs/heads/main/finops/veritas-netbackup-finops.yml
sources: []
specification: FinOps Framework
tags:
- Backup
- Data Protection
- Disaster Recovery
- Enterprise
- Recovery
- Storage
- FinOps
- Cost Management
- FOCUS
---
