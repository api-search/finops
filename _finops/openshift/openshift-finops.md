---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.json
  format: json
  label: OpenShift REST API
  slug: openshift-rest-api
  spec_type: OpenAPI
  url: https://api.openshift.com/api/swagger.json
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
description: FinOps framework definition for the OpenShift API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: OpenShift
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: OpenShift
  PublisherName: OpenShift
  ServiceCategory: Developer Tools / API
  ServiceName: OpenShift
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
name: Openshift Finops
provider_name: OpenShift
provider_slug: openshift
publisher_name: OpenShift
service_category: API
slug: openshift-finops
source_filename: openshift-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: OpenShift\nproviderId: openshift\npublisherName: OpenShift\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - CI/CD\n  - Cloud Native\n  - Containers\n  - DevOps\n  - Enterprise\n  - Kubernetes\n  - PaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the OpenShift API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: OpenShift\n  ServiceCategory: Developer Tools / API\n  ProviderName: OpenShift\n  PublisherName: OpenShift\n  InvoiceIssuerName: OpenShift\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n  \
  \  aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: OpenShift REST API\n    baseURL: https://api.openshift.com\n    tags:\n      - Cloud\n      - Containers\n      - Kubernetes\n      - Platform\n    serviceName: OpenShift REST API\n    serviceCategory: API\n  - name: OpenShift OAuth API\n    baseURL: https://oauth-openshift.apps.openshift.com\n    tags:\n      - Authentication\n      - OAuth\n      - Security\n    serviceName: OpenShift OAuth API\n    serviceCategory: API\n  - name: OpenShift Routes API\n    baseURL: https://api.openshift.com/apis/route.openshift.io/v1\n    tags:\n      - Ingress\n      - Networking\n      - Routing\n    serviceName: OpenShift Routes API\n    serviceCategory: API\n  - name: OpenShift Build API\n \
  \   baseURL: https://api.openshift.com/apis/build.openshift.io/v1\n    tags:\n      - Builds\n      - CI/CD\n      - Source-To-Image\n    serviceName: OpenShift Build API\n    serviceCategory: API\n  - name: OpenShift Image API\n    baseURL: https://api.openshift.com/apis/image.openshift.io/v1\n    tags:\n      - Containers\n      - Images\n      - Registry\n    serviceName: OpenShift Image API\n    serviceCategory: API\n  - name: OpenShift Project API\n    baseURL: https://api.openshift.com/apis/project.openshift.io/v1\n    tags:\n      - Multi-Tenancy\n      - Namespaces\n      - Projects\n    serviceName: OpenShift Project API\n    serviceCategory: API\n  - name: OpenShift Workloads API\n    baseURL: https://api.openshift.com/apis/apps/v1\n    tags:\n      - Deployments\n      - Jobs\n      - Pods\n      - StatefulSets\n      - Workloads\n    serviceName: OpenShift Workloads API\n    serviceCategory: API\n  - name: OpenShift Network API\n    baseURL: https://api.openshift.com/apis/network.openshift.io/v1\n\
  \    tags:\n      - Ingress\n      - Networking\n      - NetworkPolicy\n    serviceName: OpenShift Network API\n    serviceCategory: API\n  - name: OpenShift Storage API\n    baseURL: https://api.openshift.com/api/v1\n    tags:\n      - CSI\n      - PersistentVolumes\n      - Storage\n      - StorageClasses\n    serviceName: OpenShift Storage API\n    serviceCategory: API\n  - name: OpenShift Authorization API\n    baseURL: https://api.openshift.com/apis/authorization.k8s.io/v1\n    tags:\n      - Access Control\n      - Authorization\n      - Security\n    serviceName: OpenShift Authorization API\n    serviceCategory: API\n  - name: OpenShift Autoscale API\n    baseURL: https://api.openshift.com/apis/autoscaling/v2\n    tags:\n      - Autoscaling\n      - ClusterAutoscaler\n      - HPA\n    serviceName: OpenShift Autoscale API\n    serviceCategory: API\n  - name: OpenShift Config API\n    baseURL: https://api.openshift.com/apis/config.openshift.io/v1\n    tags:\n      - Cluster Settings\n\
  \      - Configuration\n      - Infrastructure\n    serviceName: OpenShift Config API\n    serviceCategory: API\n  - name: OpenShift Console API\n    baseURL: https://api.openshift.com/apis/console.openshift.io/v1\n    tags:\n      - Console\n      - Extensions\n      - Plugins\n      - Web UI\n    serviceName: OpenShift Console API\n    serviceCategory: API\n  - name: OpenShift Cluster API\n    baseURL: https://api.openshift.com/apis/config.openshift.io/v1\n    tags:\n      - Cluster\n      - ClusterVersion\n      - Infrastructure\n    serviceName: OpenShift Cluster API\n    serviceCategory: API\n  - name: OpenShift Machine API\n    baseURL: https://api.openshift.com/apis/machine.openshift.io/v1beta1\n    tags:\n      - Autoscaling\n      - Infrastructure\n      - Machines\n      - Nodes\n    serviceName: OpenShift Machine API\n    serviceCategory: API\n  - name: OpenShift Operator API\n    baseURL: https://api.openshift.com/apis/operator.openshift.io/v1\n    tags:\n      - Cluster Services\n\
  \      - Lifecycle Management\n      - Operators\n    serviceName: OpenShift Operator API\n    serviceCategory: API\n  - name: OpenShift OperatorHub API\n    baseURL: https://api.openshift.com/apis/operators.coreos.com/v1alpha1\n    tags:\n      - Catalog\n      - OLM\n      - OperatorHub\n      - Subscriptions\n    serviceName: OpenShift OperatorHub API\n    serviceCategory: API\n  - name: OpenShift Template API\n    baseURL: https://api.openshift.com/apis/template.openshift.io/v1\n    tags:\n      - Application Deployment\n      - Parameterization\n      - Templates\n    serviceName: OpenShift Template API\n    serviceCategory: API\n  - name: OpenShift Security API\n    baseURL: https://api.openshift.com/apis/security.openshift.io/v1\n    tags:\n      - Access Control\n      - Pod Security\n      - SCC\n      - Security\n    serviceName: OpenShift Security API\n    serviceCategory: API\n  - name: OpenShift RBAC API\n    baseURL: https://api.openshift.com/apis/rbac.authorization.k8s.io/v1\n\
  \    tags:\n      - Access Control\n      - Authorization\n      - RBAC\n      - Roles\n    serviceName: OpenShift RBAC API\n    serviceCategory: API\n  - name: OpenShift Node API\n    baseURL: https://api.openshift.com/api/v1\n    tags:\n      - Infrastructure\n      - Nodes\n      - Runtime\n    serviceName: OpenShift Node API\n    serviceCategory: API\n  - name: OpenShift Monitoring API\n    baseURL: https://api.openshift.com/apis/monitoring.coreos.com/v1\n    tags:\n      - Alerting\n      - Monitoring\n      - Observability\n      - Prometheus\n    serviceName: OpenShift Monitoring API\n    serviceCategory: API\n  - name: OpenShift Provisioning API\n    baseURL: https://api.openshift.com/apis/metal3.io/v1alpha1\n    tags:\n      - Bare Metal\n      - Hardware\n      - Infrastructure\n      - Provisioning\n    serviceName: OpenShift Provisioning API\n    serviceCategory: API\n  - name: OpenShift Schedule and Quota API\n    baseURL: https://api.openshift.com/api/v1\n    tags:\n    \
  \  - LimitRanges\n      - Quotas\n      - Resource Management\n      - Scheduling\n    serviceName: OpenShift Schedule and Quota API\n    serviceCategory: API\n  - name: OpenShift Metadata API\n    baseURL: https://api.openshift.com/api/v1\n    tags:\n      - ConfigMaps\n      - Events\n      - Metadata\n      - Secrets\n    serviceName: OpenShift Metadata API\n    serviceCategory: API\n  - name: OpenShift Cluster Manager API\n    baseURL: https://api.openshift.com/api/clusters_mgmt/v1\n    tags:\n      - Cluster Management\n      - Managed Service\n      - Multi-Cloud\n      - ROSA\n    serviceName: OpenShift Cluster Manager API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openshift/refs/heads/main/finops/openshift-finops.yml
sources: []
specification: FinOps Framework
tags:
- CI/CD
- Cloud Native
- Containers
- DevOps
- Enterprise
- Kubernetes
- PaaS
- FinOps
- Cost Management
- FOCUS
---
