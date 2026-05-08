---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: NetApp Cloud Manager API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.netapp.com/us-en/cloud-manager-automation/api/openapi.yaml
- filename: netapp-ontap-openapi.yml
  format: yaml
  label: NetApp ONTAP REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/netapp/refs/heads/main/openapi/netapp-ontap-openapi.yml
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
description: FinOps framework definition for the NetApp API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: NetApp
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: NetApp
  PublisherName: NetApp
  ServiceCategory: Developer Tools / API
  ServiceName: NetApp
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
name: Netapp Finops
provider_name: NetApp
provider_slug: netapp
publisher_name: NetApp
service_category: API
slug: netapp-finops
source_filename: netapp-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: NetApp\nproviderId: netapp\npublisherName: NetApp\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - Data Management\n  - Hybrid Cloud\n  - Infrastructure\n  - Storage\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the NetApp API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: NetApp\n  ServiceCategory: Developer Tools / API\n  ProviderName: NetApp\n  PublisherName: NetApp\n  InvoiceIssuerName: NetApp\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: NetApp Cloud Manager API\n    baseURL: https://cloudmanager.cloud.netapp.com\n    tags:\n      - Automation\n      - Cloud Management\n      - ONTAP\n    serviceName: NetApp Cloud Manager API\n    serviceCategory: API\n  - name: NetApp ONTAP REST API\n    baseURL: https://<cluster-management-ip>/api\n    tags:\n      - ONTAP\n      - REST API\n      - Storage Management\n    serviceName: NetApp ONTAP REST API\n    serviceCategory: API\n  - name: NetApp Cloud Volumes Service API\n    baseURL: https://cloudvolumesgcp-api.netapp.com\n    tags:\n      - AWS\n      - Azure\n      - Cloud Volumes\n      - GCP\n    serviceName: NetApp Cloud Volumes Service API\n    serviceCategory: API\n  - name: NetApp Astra Control API\n\
  \    baseURL: https://astra.netapp.io/accounts\n    tags:\n      - Application Management\n      - Container Storage\n      - Data Protection\n      - Kubernetes\n    serviceName: NetApp Astra Control API\n    serviceCategory: API\n  - name: NetApp StorageGRID API\n    baseURL: https://<storagegrid-endpoint>/api/v3\n    tags:\n      - Grid Management\n      - Object Storage\n      - S3\n    serviceName: NetApp StorageGRID API\n    serviceCategory: API\n  - name: NetApp Element API\n    baseURL: https://<mvip>/json-rpc\n    tags:\n      - Element\n      - HCI\n      - JSON-RPC\n      - Storage\n    serviceName: NetApp Element API\n    serviceCategory: API\n  - name: NetApp Cloud Insights API\n    baseURL: https://<tenant>.cloudinsights.netapp.com/rest/v1\n    tags:\n      - Analytics\n      - Monitoring\n      - Observability\n    serviceName: NetApp Cloud Insights API\n    serviceCategory: API\n  - name: NetApp BlueXP Automation API\n    baseURL: https://cloudmanager.cloud.netapp.com\n\
  \    tags:\n      - BlueXP\n      - Cloud Automation\n      - Hybrid Cloud\n      - Storage Management\n    serviceName: NetApp BlueXP Automation API\n    serviceCategory: API\n  - name: NetApp Active IQ Unified Manager API\n    baseURL: https://<aiqum-host>/api\n    tags:\n      - Active IQ\n      - Monitoring\n      - Storage Analytics\n      - Unified Manager\n    serviceName: NetApp Active IQ Unified Manager API\n    serviceCategory: API\n  - name: NetApp Active IQ Digital Advisor API\n    baseURL: https://api.activeiq.netapp.com\n    tags:\n      - Active IQ\n      - Digital Advisor\n      - Health\n      - Monitoring\n      - Upgrades\n    serviceName: NetApp Active IQ Digital Advisor API\n    serviceCategory: API\n  - name: NetApp SnapCenter API\n    baseURL: https://<snapcenter-host>:8146/api\n    tags:\n      - Backup\n      - Clone\n      - Data Protection\n      - Restore\n      - SnapCenter\n    serviceName: NetApp SnapCenter API\n    serviceCategory: API\n  - name: NetApp\
  \ E-Series SANtricity Web Services API\n    baseURL: https://<web-services-proxy-host>/devmgr/v2\n    tags:\n      - E-Series\n      - SANtricity\n      - Storage\n      - Web Services\n    serviceName: NetApp E-Series SANtricity Web Services API\n    serviceCategory: API\n  - name: Azure NetApp Files REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Azure\n      - Cloud Volumes\n      - Microsoft Azure\n      - Storage\n    serviceName: Azure NetApp Files REST API\n    serviceCategory: API\n  - name: NetApp ONTAP Tools for VMware vSphere API\n    baseURL: https://<ontap-tools-host>:8443\n    tags:\n      - ONTAP\n      - Virtualization\n      - VMware\n      - vSphere\n    serviceName: NetApp ONTAP Tools for VMware vSphere API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n\
  \  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/netapp/refs/heads/main/finops/netapp-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Data Management
- Hybrid Cloud
- Infrastructure
- Storage
- FinOps
- Cost Management
- FOCUS
---
