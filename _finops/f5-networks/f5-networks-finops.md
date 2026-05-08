---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bigip-icontrol-rest.yml
  format: yaml
  label: F5 BIG-IP iControl REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/f5-networks/refs/heads/main/openapi/bigip-icontrol-rest.yml
- filename: swagger
  format: yaml
  label: F5 Distributed Cloud API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.cloud.f5.com/docs/api/swagger
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
description: FinOps framework definition for the F5 Networks API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: F5 Networks
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: F5 Networks
  PublisherName: F5 Networks
  ServiceCategory: Developer Tools / API
  ServiceName: F5 Networks
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
name: F5 Networks Finops
provider_name: F5 Networks
provider_slug: f5-networks
publisher_name: F5 Networks
service_category: API
slug: f5-networks-finops
source_filename: f5-networks-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: F5 Networks\nproviderId: f5-networks\npublisherName: F5 Networks\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - API Gateway\n  - Application Delivery\n  - Automation\n  - Edge Computing\n  - Kubernetes\n  - Load Balancing\n  - Multi-Cloud\n  - NGINX\n  - Security\n  - WAF\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the F5 Networks API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n\
  \      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n   \
  \   - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: F5 Networks\n  ServiceCategory: Developer Tools / API\n  ProviderName: F5 Networks\n  PublisherName: F5 Networks\n  InvoiceIssuerName: F5 Networks\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: F5 BIG-IP iControl REST API\n    baseURL: https://{{bigip_host}}/mgmt/tm\n    tags:\n      - ADC\n      - Application Delivery\n      - Load Balancing\n      - Network Management\n      - Security\n    serviceName: F5 BIG-IP iControl REST API\n    serviceCategory: API\n  - name: F5 Distributed Cloud API\n    baseURL: https://{{tenant}}.console.ves.volterra.io/api\n    tags:\n      - API Security\n      - CDN\n      - Edge Computing\n      - Multi-Cloud\n      - WAF\n    serviceName: F5 Distributed Cloud API\n    serviceCategory: API\n  - name: F5 NGINX Management Suite API\n    baseURL: https://{{nms-host}}/api\n\
  \    tags:\n      - API Gateway\n      - Application Delivery\n      - Configuration Management\n      - Monitoring\n      - NGINX\n    serviceName: F5 NGINX Management Suite API\n    serviceCategory: API\n  - name: F5 Essential App Protect API\n    baseURL: https://api.f5.com/app-protect\n    tags:\n      - API Protection\n      - Bot Defense\n      - DDoS Protection\n      - Security\n      - WAF\n    serviceName: F5 Essential App Protect API\n    serviceCategory: API\n  - name: F5 BIG-IQ Centralized Management API\n    baseURL: https://{{bigiq_host}}/mgmt\n    tags:\n      - Analytics\n      - Centralized Management\n      - Device Management\n      - Licensing\n      - Monitoring\n    serviceName: F5 BIG-IQ Centralized Management API\n    serviceCategory: API\n  - name: F5 BIG-IP Application Services 3 Extension API\n    baseURL: https://{{bigip_host}}/mgmt/shared/appsvcs\n    tags:\n      - Application Delivery\n      - Application Services\n      - Automation\n      - Declarative\n\
  \      - Infrastructure as Code\n    serviceName: F5 BIG-IP Application Services 3 Extension API\n    serviceCategory: API\n  - name: F5 Declarative Onboarding API\n    baseURL: https://{{bigip_host}}/mgmt/shared/declarative-onboarding\n    tags:\n      - Automation\n      - Declarative\n      - Device Configuration\n      - Infrastructure as Code\n      - Onboarding\n    serviceName: F5 Declarative Onboarding API\n    serviceCategory: API\n  - name: F5 Telemetry Streaming API\n    baseURL: https://{{bigip_host}}/mgmt/shared/telemetry\n    tags:\n      - Analytics\n      - Monitoring\n      - Observability\n      - Streaming\n      - Telemetry\n    serviceName: F5 Telemetry Streaming API\n    serviceCategory: API\n  - name: F5 NGINX Plus API\n    baseURL: https://{{nginx_host}}/api\n    tags:\n      - Dynamic Configuration\n      - Load Balancing\n      - Monitoring\n      - NGINX\n      - Reverse Proxy\n    serviceName: F5 NGINX Plus API\n    serviceCategory: API\n  - name: F5 NGINX One\
  \ Console API\n    baseURL: https://{{nginx-one-host}}/api\n    tags:\n      - Configuration Management\n      - Fleet Management\n      - Monitoring\n      - NGINX\n      - Security\n    serviceName: F5 NGINX One Console API\n    serviceCategory: API\n  - name: F5 NGINX Ingress Controller API\n    baseURL: https://{{kubernetes_host}}\n    tags:\n      - Containers\n      - Ingress Controller\n      - Kubernetes\n      - Load Balancing\n      - NGINX\n    serviceName: F5 NGINX Ingress Controller API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/f5-networks/refs/heads/main/finops/f5-networks-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Gateway
- Application Delivery
- Automation
- Edge Computing
- Kubernetes
- Load Balancing
- Multi-Cloud
- NGINX
- Security
- WAF
- FinOps
- Cost Management
- FOCUS
---
