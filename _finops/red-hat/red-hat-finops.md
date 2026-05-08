---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi
  format: yaml
  label: Red Hat OpenShift API
  slug: ''
  spec_type: OpenAPI
  url: https://api.openshift.com/api/clusters_mgmt/v1/openapi
- filename: openapi
  format: yaml
  label: Red Hat OpenShift Cluster Manager API
  slug: ''
  spec_type: OpenAPI
  url: https://api.openshift.com/api/clusters_mgmt/v1/openapi
- filename: red-hat-ansible-automation-platform-openapi.yml
  format: yaml
  label: Red Hat Ansible Automation Platform API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/openapi/red-hat-ansible-automation-platform-openapi.yml
- filename: discovery
  format: yaml
  label: Red Hat Quay API
  slug: ''
  spec_type: OpenAPI
  url: https://quay.io/api/v1/discovery
- filename: red-hat-insights-openapi.yml
  format: yaml
  label: Red Hat Insights API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/openapi/red-hat-insights-openapi.yml
- filename: red-hat-satellite-openapi.yml
  format: yaml
  label: Red Hat Satellite API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/openapi/red-hat-satellite-openapi.yml
- filename: red-hat-keycloak-admin-openapi.yml
  format: yaml
  label: Red Hat Build of Keycloak Admin REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/openapi/red-hat-keycloak-admin-openapi.yml
- filename: red-hat-kafka-bridge-asyncapi.yml
  format: yaml
  label: Red Hat Streams for Apache Kafka Bridge API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/asyncapi/red-hat-kafka-bridge-asyncapi.yml
- filename: red-hat-notifications-webhooks-asyncapi.yml
  format: yaml
  label: Red Hat Notifications API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/asyncapi/red-hat-notifications-webhooks-asyncapi.yml
- filename: openapi
  format: yaml
  label: Red Hat Assisted Installer API
  slug: ''
  spec_type: OpenAPI
  url: https://api.openshift.com/api/assisted-install/v2/openapi
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
description: FinOps framework definition for the Red Hat API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Red Hat
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Red Hat
  PublisherName: Red Hat
  ServiceCategory: Developer Tools / API
  ServiceName: Red Hat
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
name: Red Hat Finops
provider_name: Red Hat
provider_slug: red-hat
publisher_name: Red Hat
service_category: API
slug: red-hat-finops
source_filename: red-hat-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red Hat\nproviderId: red-hat\npublisherName: Red Hat\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - Containers\n  - Enterprise\n  - Hybrid Cloud\n  - Kubernetes\n  - Linux\n  - Open Source\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Red Hat API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Red Hat\n  ServiceCategory: Developer Tools / API\n  ProviderName: Red Hat\n  PublisherName: Red Hat\n  InvoiceIssuerName: Red Hat\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Red Hat OpenShift API\n    baseURL: ''\n    tags:\n      - Cloud Native\n      - Containers\n      - Kubernetes\n      - Platform as a Service\n    serviceName: Red Hat OpenShift API\n    serviceCategory: API\n  - name: Red Hat OpenShift Cluster Manager API\n    baseURL: ''\n    tags:\n      - Cluster Management\n      - Hybrid Cloud\n      - Kubernetes\n      - Provisioning\n    serviceName: Red Hat OpenShift Cluster Manager API\n    serviceCategory: API\n  - name: Red Hat Ansible Automation Platform API\n    baseURL: ''\n    tags:\n      - Automation\n      - Configuration Management\n      - DevOps\n      - Infrastructure as Code\n    serviceName: Red Hat Ansible Automation Platform API\n  \
  \  serviceCategory: API\n  - name: Red Hat Quay API\n    baseURL: ''\n    tags:\n      - Container Registry\n      - Docker\n      - Image Management\n      - Security\n    serviceName: Red Hat Quay API\n    serviceCategory: API\n  - name: Red Hat Insights API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Compliance\n      - Monitoring\n      - Security\n    serviceName: Red Hat Insights API\n    serviceCategory: API\n  - name: Red Hat Subscription Management API\n    baseURL: ''\n    tags:\n      - Entitlements\n      - Licensing\n      - Subscriptions\n      - System Management\n    serviceName: Red Hat Subscription Management API\n    serviceCategory: API\n  - name: Red Hat Satellite API\n    baseURL: ''\n    tags:\n      - Content Management\n      - Patch Management\n      - Provisioning\n      - Systems Management\n    serviceName: Red Hat Satellite API\n    serviceCategory: API\n  - name: Red Hat Advanced Cluster Management API\n    baseURL: ''\n    tags:\n      - Cluster\
  \ Management\n      - Governance\n      - Kubernetes\n      - Multi-Cluster\n    serviceName: Red Hat Advanced Cluster Management API\n    serviceCategory: API\n  - name: Red Hat Advanced Cluster Security API\n    baseURL: ''\n    tags:\n      - Compliance\n      - Kubernetes\n      - Security\n      - Vulnerability Management\n    serviceName: Red Hat Advanced Cluster Security API\n    serviceCategory: API\n  - name: Red Hat Build of Keycloak Admin REST API\n    baseURL: ''\n    tags:\n      - Authentication\n      - Authorization\n      - Identity\n      - Single Sign-On\n    serviceName: Red Hat Build of Keycloak Admin REST API\n    serviceCategory: API\n  - name: Red Hat 3scale API Management\n    baseURL: ''\n    tags:\n      - API Gateway\n      - API Management\n      - Developer Portal\n      - Rate Limiting\n    serviceName: Red Hat 3scale API Management\n    serviceCategory: API\n  - name: Red Hat Cost Management API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Cloud\n\
  \      - Cost Management\n      - FinOps\n    serviceName: Red Hat Cost Management API\n    serviceCategory: API\n  - name: Red Hat Image Builder API\n    baseURL: ''\n    tags:\n      - Cloud\n      - Image Building\n      - Provisioning\n      - RHEL\n    serviceName: Red Hat Image Builder API\n    serviceCategory: API\n  - name: Red Hat Vulnerability Management API\n    baseURL: ''\n    tags:\n      - Compliance\n      - CVE\n      - Security\n      - Vulnerability Management\n    serviceName: Red Hat Vulnerability Management API\n    serviceCategory: API\n  - name: Red Hat Patch API\n    baseURL: ''\n    tags:\n      - Patch Management\n      - RHEL\n      - Security\n      - Updates\n    serviceName: Red Hat Patch API\n    serviceCategory: API\n  - name: Red Hat Compliance API\n    baseURL: ''\n    tags:\n      - Compliance\n      - Policy Management\n      - SCAP\n      - Security\n    serviceName: Red Hat Compliance API\n    serviceCategory: API\n  - name: Red Hat Build of Apicurio\
  \ Registry API\n    baseURL: ''\n    tags:\n      - API Design\n      - Data Governance\n      - Event-Driven\n      - Schema Registry\n    serviceName: Red Hat Build of Apicurio Registry API\n    serviceCategory: API\n  - name: Red Hat Streams for Apache Kafka Bridge API\n    baseURL: ''\n    tags:\n      - Data Integration\n      - Event Streaming\n      - Kafka\n      - Messaging\n    serviceName: Red Hat Streams for Apache Kafka Bridge API\n    serviceCategory: API\n  - name: Red Hat Ansible Lightspeed API\n    baseURL: ''\n    tags:\n      - Ansible\n      - Artificial Intelligence\n      - Automation\n      - Generative AI\n    serviceName: Red Hat Ansible Lightspeed API\n    serviceCategory: API\n  - name: Red Hat Managed Inventory API\n    baseURL: ''\n    tags:\n      - Host Management\n      - Inventory\n      - RHEL\n      - Systems Management\n    serviceName: Red Hat Managed Inventory API\n    serviceCategory: API\n  - name: Red Hat Remediations API\n    baseURL: ''\n    tags:\n\
  \      - Automation\n      - Compliance\n      - Remediation\n      - Security\n    serviceName: Red Hat Remediations API\n    serviceCategory: API\n  - name: Red Hat Notifications API\n    baseURL: ''\n    tags:\n      - Alerts\n      - Integrations\n      - Notifications\n      - Webhooks\n    serviceName: Red Hat Notifications API\n    serviceCategory: API\n  - name: Red Hat Role-Based Access Control API\n    baseURL: ''\n    tags:\n      - Access Control\n      - Authorization\n      - Identity\n      - Security\n    serviceName: Red Hat Role-Based Access Control API\n    serviceCategory: API\n  - name: Red Hat Advisor API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Monitoring\n      - Recommendations\n      - RHEL\n    serviceName: Red Hat Advisor API\n    serviceCategory: API\n  - name: Red Hat Malware Detection API\n    baseURL: ''\n    tags:\n      - Malware\n      - RHEL\n      - Security\n      - Threat Detection\n    serviceName: Red Hat Malware Detection API\n \
  \   serviceCategory: API\n  - name: Red Hat Sources API\n    baseURL: ''\n    tags:\n      - Cloud\n      - Configuration\n      - Data Sources\n      - Integrations\n    serviceName: Red Hat Sources API\n    serviceCategory: API\n  - name: Red Hat Integrations API\n    baseURL: ''\n    tags:\n      - Configuration\n      - Integrations\n      - Notifications\n      - Webhooks\n    serviceName: Red Hat Integrations API\n    serviceCategory: API\n  - name: Red Hat Resource Optimization API\n    baseURL: ''\n    tags:\n      - Analytics\n      - FinOps\n      - Resource Optimization\n      - RHEL\n    serviceName: Red Hat Resource Optimization API\n    serviceCategory: API\n  - name: Red Hat Export Service API\n    baseURL: ''\n    tags:\n      - Automation\n      - Data Export\n      - Inventory\n      - Reporting\n    serviceName: Red Hat Export Service API\n    serviceCategory: API\n  - name: Red Hat Playbook Dispatcher API\n    baseURL: ''\n    tags:\n      - Ansible\n      - Automation\n\
  \      - Playbooks\n      - Remediation\n    serviceName: Red Hat Playbook Dispatcher API\n    serviceCategory: API\n  - name: Red Hat Content Sources API\n    baseURL: ''\n    tags:\n      - Content Management\n      - Packages\n      - Repositories\n      - RHEL\n    serviceName: Red Hat Content Sources API\n    serviceCategory: API\n  - name: Red Hat Tasks API\n    baseURL: ''\n    tags:\n      - Automation\n      - RHEL\n      - Systems Management\n      - Task Management\n    serviceName: Red Hat Tasks API\n    serviceCategory: API\n  - name: Red Hat Subscriptions Usage API\n    baseURL: ''\n    tags:\n      - Compliance\n      - Reporting\n      - Subscriptions\n      - Usage\n    serviceName: Red Hat Subscriptions Usage API\n    serviceCategory: API\n  - name: Red Hat Assisted Installer API\n    baseURL: ''\n    tags:\n      - Bare Metal\n      - Cluster Provisioning\n      - Installation\n      - OpenShift\n    serviceName: Red Hat Assisted Installer API\n    serviceCategory: API\n\
  \  - name: Red Hat Account Management Service API\n    baseURL: ''\n    tags:\n      - Account Management\n      - OpenShift\n      - Organizations\n      - Subscriptions\n    serviceName: Red Hat Account Management Service API\n    serviceCategory: API\n  - name: Red Hat Authorization Service API\n    baseURL: ''\n    tags:\n      - Access Control\n      - Authorization\n      - OpenShift\n      - Security\n    serviceName: Red Hat Authorization Service API\n    serviceCategory: API\n  - name: Red Hat Service Logs API\n    baseURL: ''\n    tags:\n      - Logging\n      - Monitoring\n      - Observability\n      - OpenShift\n    serviceName: Red Hat Service Logs API\n    serviceCategory: API\n  - name: Red Hat Connector Management API\n    baseURL: ''\n    tags:\n      - Connectors\n      - Data Integration\n      - Integrations\n      - OpenShift\n    serviceName: Red Hat Connector Management API\n    serviceCategory: API\n  - name: Red Hat Upgrades Information Service API\n    baseURL:\
  \ ''\n    tags:\n      - Cluster Management\n      - OpenShift\n      - Upgrades\n      - Version Management\n    serviceName: Red Hat Upgrades Information Service API\n    serviceCategory: API\n  - name: Red Hat Automation Hub API\n    baseURL: ''\n    tags:\n      - Ansible\n      - Automation\n      - Collections\n      - Content Management\n    serviceName: Red Hat Automation Hub API\n    serviceCategory: API\n  - name: Red Hat Operator Gathering Conditions Service API\n    baseURL: ''\n    tags:\n      - Data Collection\n      - Insights\n      - OpenShift\n      - Operators\n    serviceName: Red Hat Operator Gathering Conditions Service API\n    serviceCategory: API\n  - name: Red Hat Payload Ingress Service API\n    baseURL: ''\n    tags:\n      - Data Ingestion\n      - Platform\n      - Systems Management\n      - Upload\n    serviceName: Red Hat Payload Ingress Service API\n    serviceCategory: API\n  - name: Red Hat Lightspeed Advisor for OpenShift API\n    baseURL: ''\n   \
  \ tags:\n      - Artificial Intelligence\n      - Monitoring\n      - OpenShift\n      - Recommendations\n    serviceName: Red Hat Lightspeed Advisor for OpenShift API\n    serviceCategory: API\n  - name: Red Hat OCP Vulnerability Dashboard API\n    baseURL: ''\n    tags:\n      - CVE\n      - OpenShift\n      - Security\n      - Vulnerability Management\n    serviceName: Red Hat OCP Vulnerability Dashboard API\n    serviceCategory: API\n  - name: Red Hat Web-RCA Service API\n    baseURL: ''\n    tags:\n      - Incident Management\n      - OpenShift\n      - Operations\n      - Root Cause Analysis\n    serviceName: Red Hat Web-RCA Service API\n    serviceCategory: API\n  - name: Red Hat Case Management API\n    baseURL: ''\n    tags:\n      - Case Management\n      - Customer Portal\n      - Incident Management\n      - Support\n    serviceName: Red Hat Case Management API\n    serviceCategory: API\n  - name: Red Hat Security Data API\n    baseURL: ''\n    tags:\n      - CSAF\n      -\
  \ CVE\n      - Security\n      - Vulnerability Management\n    serviceName: Red Hat Security Data API\n    serviceCategory: API\n  - name: Red Hat Edge Management API\n    baseURL: ''\n    tags:\n      - Device Management\n      - Edge Computing\n      - Fleet Management\n      - IoT\n    serviceName: Red Hat Edge Management API\n    serviceCategory: API\n  - name: Red Hat Lightspeed for RHEL Planning API\n    baseURL: ''\n    tags:\n      - Lifecycle\n      - Planning\n      - Product Roadmap\n      - RHEL\n    serviceName: Red Hat Lightspeed for RHEL Planning API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/finops/red-hat-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Containers
- Enterprise
- Hybrid Cloud
- Kubernetes
- Linux
- Open Source
- FinOps
- Cost Management
- FOCUS
---
