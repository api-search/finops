---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: vmware-vsphere-api-openapi.yml
  format: yaml
  label: vSphere API
  slug: vsphere-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vmware/refs/heads/main/openapi/vmware-vsphere-api-openapi.yml
- filename: openapi.yaml
  format: yaml
  label: vCloud Director API
  slug: vcloud-director-api
  spec_type: OpenAPI
  url: https://developer.vmware.com/apis/vmware-cloud-director/latest/openapi/
- filename: openapi.yaml
  format: yaml
  label: NSX-T Data Center API
  slug: nsx-t-data-center-api
  spec_type: OpenAPI
  url: https://developer.vmware.com/apis/nsx-t/latest/openapi/
- filename: openapi.yaml
  format: yaml
  label: vRealize Automation API
  slug: vrealize-automation-api
  spec_type: OpenAPI
  url: https://developer.vmware.com/apis/vrealize-automation/latest/openapi/
- filename: openapi.yaml
  format: yaml
  label: VMware Cloud on AWS API
  slug: vmware-cloud-on-aws-api
  spec_type: OpenAPI
  url: https://developer.vmware.com/apis/vmc/latest/openapi/
- filename: openapi.yaml
  format: yaml
  label: vRealize Operations API
  slug: vrealize-operations-api
  spec_type: OpenAPI
  url: https://developer.vmware.com/apis/vrealize-operations/latest/openapi/
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
description: FinOps framework definition for the VMware API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: VMware
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: VMware
  PublisherName: VMware
  ServiceCategory: Developer Tools / API
  ServiceName: VMware
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
name: Vmware Finops
provider_name: VMware
provider_slug: vmware
publisher_name: VMware
service_category: API
slug: vmware-finops
source_filename: vmware-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: VMware\nproviderId: vmware\npublisherName: VMware\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Computing\n  - Container Management\n  - Hybrid Cloud\n  - Infrastructure\n  - Virtualization\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the VMware API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API\
  \ call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: VMware\n  ServiceCategory: Developer Tools / API\n  ProviderName: VMware\n  PublisherName: VMware\n  InvoiceIssuerName: VMware\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: vSphere API\n    baseURL: https://{{vcenter}}/api\n    tags:\n      - Data Center\n      - Hypervisor\n      - Virtualization\n      - VM Management\n    serviceName: vSphere API\n    serviceCategory: API\n  - name: vSphere Web Services API\n    baseURL: https://{{vcenter}}/sdk\n    tags:\n      - Data Center\n      - SOAP\n      - Virtualization\n      - VM Management\n    serviceName: vSphere Web Services API\n    serviceCategory: API\n  - name: Virtual Infrastructure JSON API\n    baseURL: https://{{vcenter}}/sdk/vim25/8.0.1.0\n    tags:\n      - JSON\n      - REST\n      - vCenter\n      - Virtualization\n    serviceName: Virtual Infrastructure JSON API\n    serviceCategory: API\n  - name:\
  \ vCloud Director API\n    baseURL: https://{{vcd-host}}/api\n    tags:\n      - Cloud Management\n      - Multi-Tenancy\n      - Service Provider\n    serviceName: vCloud Director API\n    serviceCategory: API\n  - name: NSX-T Data Center API\n    baseURL: https://{{nsx-manager}}/api/v1\n    tags:\n      - Load Balancing\n      - Micro-Segmentation\n      - Network Virtualization\n      - Security\n    serviceName: NSX-T Data Center API\n    serviceCategory: API\n  - name: NSX-T Global Manager API\n    baseURL: https://{{global-manager}}/global-manager/api/v1\n    tags:\n      - Federation\n      - Multi-Site\n      - Network Virtualization\n      - Security\n    serviceName: NSX-T Global Manager API\n    serviceCategory: API\n  - name: NSX Intelligence API\n    baseURL: https://{{nsx-manager}}/napp/api/v1\n    tags:\n      - Network Intelligence\n      - Security Analytics\n      - Traffic Analysis\n    serviceName: NSX Intelligence API\n    serviceCategory: API\n  - name: NSX Autonomous\
  \ Edge API\n    baseURL: https://{{nsx-edge}}/api/v1\n    tags:\n      - Edge Computing\n      - Network Virtualization\n      - SD-WAN\n    serviceName: NSX Autonomous Edge API\n    serviceCategory: API\n  - name: vRealize Automation API\n    baseURL: https://{{vra-host}}/automation-api\n    tags:\n      - Automation\n      - Infrastructure as Code\n      - Orchestration\n      - Self-Service\n    serviceName: vRealize Automation API\n    serviceCategory: API\n  - name: VMware Cloud on AWS API\n    baseURL: https://vmc.vmware.com/vmc/api\n    tags:\n      - AWS\n      - Cloud Services\n      - Hybrid Cloud\n      - SDDC\n    serviceName: VMware Cloud on AWS API\n    serviceCategory: API\n  - name: Tanzu Kubernetes Grid API\n    baseURL: https://{{tkg-endpoint}}/api\n    tags:\n      - Cloud Native\n      - Containers\n      - DevOps\n      - Kubernetes\n    serviceName: Tanzu Kubernetes Grid API\n    serviceCategory: API\n  - name: vRealize Operations API\n    baseURL: https://{{vrops-host}}/suite-api/api\n\
  \    tags:\n      - Analytics\n      - Monitoring\n      - Operations\n      - Performance\n    serviceName: vRealize Operations API\n    serviceCategory: API\n  - name: Workspace ONE API\n    baseURL: https://{{ws1-host}}/api\n    tags:\n      - Endpoint Management\n      - Enterprise Mobility\n      - Identity\n      - Mobile Device Management\n    serviceName: Workspace ONE API\n    serviceCategory: API\n  - name: VMware Cloud Foundation API\n    baseURL: https://{{sddc-manager}}/v1\n    tags:\n      - Cloud Foundation\n      - Hyperconverged Infrastructure\n      - Lifecycle Management\n      - SDDC\n    serviceName: VMware Cloud Foundation API\n    serviceCategory: API\n  - name: VMware Horizon Server API\n    baseURL: https://{{horizon-server}}/rest\n    tags:\n      - Desktop Virtualization\n      - Remote Access\n      - VDI\n      - Virtual Desktop\n    serviceName: VMware Horizon Server API\n    serviceCategory: API\n  - name: vSAN Management API\n    baseURL: https://{{vcenter}}/vsanHealth\n\
  \    tags:\n      - Data Management\n      - Hyper-Converged\n      - Storage\n      - vSAN\n    serviceName: vSAN Management API\n    serviceCategory: API\n  - name: VMware Aria Operations for Logs API\n    baseURL: https://{{log-insight-host}}:9543/api/v2\n    tags:\n      - Analytics\n      - Log Management\n      - Monitoring\n      - Observability\n    serviceName: VMware Aria Operations for Logs API\n    serviceCategory: API\n  - name: VMware Aria Operations for Networks API\n    baseURL: https://{{vrni-host}}/api/ni\n    tags:\n      - Microsegmentation\n      - Network Analytics\n      - Network Monitoring\n      - Troubleshooting\n    serviceName: VMware Aria Operations for Networks API\n    serviceCategory: API\n  - name: VMware Aria Suite Lifecycle API\n    baseURL: https://{{lcm-host}}/lcm/api\n    tags:\n      - Automation\n      - Configuration Management\n      - Deployment\n      - Lifecycle Management\n    serviceName: VMware Aria Suite Lifecycle API\n    serviceCategory:\
  \ API\n  - name: VMware Site Recovery Manager API\n    baseURL: https://{{srm-host}}/api\n    tags:\n      - Business Continuity\n      - Disaster Recovery\n      - Replication\n      - Site Recovery\n    serviceName: VMware Site Recovery Manager API\n    serviceCategory: API\n  - name: VMware Live Cyber Recovery API\n    baseURL: https://{{vcdr-orchestrator}}/api\n    tags:\n      - Cloud Recovery\n      - Cyber Recovery\n      - Data Protection\n      - Ransomware Protection\n    serviceName: VMware Live Cyber Recovery API\n    serviceCategory: API\n  - name: VMware Live Site Recovery API\n    baseURL: https://{{vcdr-host}}/api/vcdr/v1\n    tags:\n      - Business Continuity\n      - Disaster Recovery\n      - DRaaS\n      - Site Recovery\n    serviceName: VMware Live Site Recovery API\n    serviceCategory: API\n  - name: VMware vDefend API\n    baseURL: https://{{nsx-manager}}/api/v1\n    tags:\n      - Firewall\n      - Micro-Segmentation\n      - Network Security\n      - Threat Detection\n\
  \    serviceName: VMware vDefend API\n    serviceCategory: API\n  - name: VCF Operations API\n    baseURL: https://{{vrops-host}}/suite-api/api\n    tags:\n      - Analytics\n      - Cloud Foundation\n      - Monitoring\n      - Operations Management\n    serviceName: VCF Operations API\n    serviceCategory: API\n  - name: VMware View API\n    baseURL: https://{{horizon-server}}/view-vlsi/rest\n    tags:\n      - Desktop Management\n      - Horizon View\n      - VDI\n      - Virtual Desktop\n    serviceName: VMware View API\n    serviceCategory: API\n  - name: VMware Cloud on AWS API Reference\n    baseURL: https://vmc.vmware.com/vmc/api\n    tags:\n      - AWS\n      - Cloud Infrastructure\n      - Hybrid Cloud\n      - SDDC\n    serviceName: VMware Cloud on AWS API Reference\n    serviceCategory: API\n  - name: NSX VMC Policy API\n    baseURL: https://{{nsx-manager}}/policy/api/v1\n    tags:\n      - AWS\n      - Network Virtualization\n      - Security Policy\n      - VMware Cloud\n\
  \    serviceName: NSX VMC Policy API\n    serviceCategory: API\n  - name: VMware Cloud Disaster Recovery API\n    baseURL: https://{{vcdr-host}}/api\n    tags:\n      - Business Continuity\n      - Cloud Recovery\n      - Data Protection\n      - Disaster Recovery\n    serviceName: VMware Cloud Disaster Recovery API\n    serviceCategory: API\n  - name: VMware Aria Automation Orchestrator API\n    baseURL: https://{{vro-host}}/vco/api\n    tags:\n      - IT Automation\n      - Orchestration\n      - Plug-Ins\n      - Workflow Automation\n    serviceName: VMware Aria Automation Orchestrator API\n    serviceCategory: API\n  - name: VMware Aria Operations for Networks SaaS API\n    baseURL: https://{{vrni-saas-host}}/api/ni\n    tags:\n      - Microsegmentation\n      - Network Analytics\n      - Network Monitoring\n      - SaaS\n    serviceName: VMware Aria Operations for Networks SaaS API\n    serviceCategory: API\n  - name: VCF Operations for Networks API\n    baseURL: https://{{vrni-host}}/api/ni\n\
  \    tags:\n      - Cloud Foundation\n      - Network Analytics\n      - Network Monitoring\n      - Troubleshooting\n    serviceName: VCF Operations for Networks API\n    serviceCategory: API\n  - name: VMware Avi Load Balancer API\n    baseURL: https://{{avi-controller}}/api\n    tags:\n      - Analytics\n      - Application Delivery\n      - Load Balancing\n      - Traffic Management\n    serviceName: VMware Avi Load Balancer API\n    serviceCategory: API\n  - name: VMware Data Services Manager API\n    baseURL: https://{{dsm-host}}/api\n    tags:\n      - Data Services\n      - Database Management\n      - MySQL\n      - PostgreSQL\n    serviceName: VMware Data Services Manager API\n    serviceCategory: API\n  - name: VMware Data Services Manager Kubernetes API\n    baseURL: https://{{k8s-api}}/apis\n    tags:\n      - Data Services\n      - Database Management\n      - Kubernetes\n      - Self-Service\n    serviceName: VMware Data Services Manager Kubernetes API\n    serviceCategory:\
  \ API\n  - name: App Volumes API\n    baseURL: https://{{app-volumes-manager}}/api\n    tags:\n      - Application Delivery\n      - Application Management\n      - Desktop Virtualization\n      - VDI\n    serviceName: App Volumes API\n    serviceCategory: API\n  - name: VMware vSphere Kubernetes Service API\n    baseURL: https://{{vcenter}}/api\n    tags:\n      - Container Management\n      - Kubernetes\n      - Tanzu\n      - vSphere\n    serviceName: VMware vSphere Kubernetes Service API\n    serviceCategory: API\n  - name: SDDC Manager API\n    baseURL: https://{{sddc-manager}}/v1\n    tags:\n      - Cloud Foundation\n      - Infrastructure\n      - Lifecycle Management\n      - SDDC\n    serviceName: SDDC Manager API\n    serviceCategory: API\n  - name: VCF Installer API\n    baseURL: https://{{cloud-builder}}/v1\n    tags:\n      - Automation\n      - Cloud Foundation\n      - Deployment\n      - Installation\n    serviceName: VCF Installer API\n    serviceCategory: API\n  - name:\
  \ VCF Operations Orchestrator API\n    baseURL: https://{{vro-host}}/vco/api\n    tags:\n      - Cloud Foundation\n      - Operations\n      - Orchestration\n      - Workflow Automation\n    serviceName: VCF Operations Orchestrator API\n    serviceCategory: API\n  - name: VMware Cloud Director OpenAPI\n    baseURL: https://{{vcd-host}}/cloudapi\n    tags:\n      - Cloud Management\n      - Multi-Tenancy\n      - OpenAPI\n      - Service Provider\n    serviceName: VMware Cloud Director OpenAPI\n    serviceCategory: API\n  - name: VMware Cloud Director API\n    baseURL: https://{{vcd-host}}/api\n    tags:\n      - Cloud Management\n      - Multi-Tenancy\n      - Service Provider\n      - XML\n    serviceName: VMware Cloud Director API\n    serviceCategory: API\n  - name: VMware Identity Manager API\n    baseURL: https://{{idm-host}}/SAAS/jersey/manager/api\n    tags:\n      - Access Management\n      - Authentication\n      - Identity Management\n      - Single Sign-On\n    serviceName:\
  \ VMware Identity Manager API\n    serviceCategory: API\n  - name: Operations for Applications REST API\n    baseURL: https://{{wavefront-host}}/api/v2\n    tags:\n      - Dashboards\n      - Metrics\n      - Monitoring\n      - Observability\n    serviceName: Operations for Applications REST API\n    serviceCategory: API\n  - name: Data Management for VMware Tanzu REST API\n    baseURL: https://{{tanzu-data-host}}/api\n    tags:\n      - Data Management\n      - Database\n      - Kubernetes\n      - Tanzu\n    serviceName: Data Management for VMware Tanzu REST API\n    serviceCategory: API\n  - name: VMware Cloud Foundation for VxRail API\n    baseURL: https://{{sddc-manager}}/v1\n    tags:\n      - Cloud Foundation\n      - Dell\n      - Hyperconverged Infrastructure\n      - VxRail\n    serviceName: VMware Cloud Foundation for VxRail API\n    serviceCategory: API\n  - name: VCF Usage Meter API\n    baseURL: https://{{usage-meter}}/api\n    tags:\n      - Billing\n      - Reporting\n\
  \      - Service Provider\n      - Usage Metering\n    serviceName: VCF Usage Meter API\n    serviceCategory: API\n  - name: Virtual Storage Lifecycle Management API\n    baseURL: https://{{vcenter}}/api\n    tags:\n      - Lifecycle Management\n      - Storage\n      - Storage Policy\n      - Virtual Disk\n    serviceName: Virtual Storage Lifecycle Management API\n    serviceCategory: API\n  - name: VMware Private AI Service API\n    baseURL: https://{{pai-host}}/api\n    tags:\n      - Artificial Intelligence\n      - Infrastructure\n      - Machine Learning\n      - Private AI\n    serviceName: VMware Private AI Service API\n    serviceCategory: API\n  - name: VMware HCX API\n    baseURL: https://{{hcx-manager}}/hybridity/api\n    tags:\n      - Disaster Recovery\n      - Hybrid Cloud\n      - Network Extension\n      - Workload Migration\n    serviceName: VMware HCX API\n    serviceCategory: API\n  - name: VMware Cloud Provider Lifecycle Manager API\n    baseURL: https://{{vclm-host}}/api\n\
  \    tags:\n      - Cloud Provider\n      - Deployment\n      - Lifecycle Management\n      - Service Provider\n    serviceName: VMware Cloud Provider Lifecycle Manager API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vmware/refs/heads/main/finops/vmware-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Computing
- Container Management
- Hybrid Cloud
- Infrastructure
- Virtualization
- FinOps
- Cost Management
- FOCUS
---
