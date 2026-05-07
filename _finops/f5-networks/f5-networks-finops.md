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
  billingFrequency: Annual (Subscription/FCP), One-Time (Perpetual), Monthly (Distributed Cloud usage)
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  chargeFrequency: Recurring (Subscription/FCP/Distributed Cloud) or One-Time (Perpetual)
  pricingCategory: Subscription / Perpetual / Flex Consumption + SaaS Usage
description: 'FOCUS-aligned FinOps for F5 Networks: cost is dominated by the BIG-IP / NGINX Plus / App Protect license model (Subscription, Perpetual, FCP) plus consumption against F5 Distributed Cloud services (CDN, WAF, Bot Defense, API Security). API access itself has no per-call charge.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: F5, Inc.
  PricingCategory: Subscription / Perpetual / FCP / Usage
  PricingUnit: instance | request | GB | transaction
  ProviderName: F5
  PublisherName: F5, Inc.
  ServiceCategory: Application Delivery / Multi-Cloud Security
  ServiceName: F5 Networks
layout: finops
meters:
- aggregation: max
  description: Count of licensed BIG-IP instances (hardware or VE).
  dimensions:
  - environment
  - region
  - form_factor
  name: bigip_instances
  unit: instance
- aggregation: max
  description: Count of licensed NGINX Plus instances.
  dimensions:
  - environment
  - region
  name: nginx_plus_instances
  unit: instance
- aggregation: max
  description: App Protect / Advanced WAF entitled instances.
  dimensions:
  - product
  name: app_protect_instances
  unit: instance
- aggregation: sum
  description: F5 Distributed Cloud HTTP/L7 requests (CDN, WAF, API Security, Bot Defense).
  dimensions:
  - service
  - tenant
  - namespace
  - region
  name: distributed_cloud_requests
  unit: request
- aggregation: sum
  description: F5 Distributed Cloud egress data.
  dimensions:
  - service
  - tenant
  - region
  name: distributed_cloud_egress
  unit: GB
- aggregation: sum
  description: Annual FCP commitment $; trues up to actual usage.
  dimensions:
  - year
  - service
  name: fcp_commitment
  unit: USD
name: F5 Networks Finops
provider_name: F5 Networks
provider_slug: f5-networks
publisher_name: F5, Inc.
service_category: Application Delivery / Multi-Cloud Security
slug: f5-networks-finops
source_filename: f5-networks-finops.yml
source_heading: FinOps Profile
source_url: https://www.f5.com/products/get-f5
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: F5 Networks\nproviderId: f5-networks\npublisherName: F5, Inc.\nserviceCategory: Application Delivery / Multi-Cloud Security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - API Gateway\n  - Application Delivery\n  - Automation\n  - Edge Computing\n  - Kubernetes\n  - Load Balancing\n  - Multi-Cloud\n  - NGINX\n  - Security\n  - WAF\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for F5 Networks: cost is dominated by the BIG-IP / NGINX Plus / App\n  Protect license model (Subscription, Perpetual, FCP) plus consumption against F5 Distributed Cloud\n  services (CDN, WAF, Bot Defense, API Security). API access itself has no per-call\
  \ charge.'\nnotes: F5 publishes no list prices for the full portfolio. Reconcile against active quotes and Distributed\n  Cloud consumption reports.\nsources:\n  - https://www.f5.com/products/get-f5\n  - https://www.f5.com/cloud\n  - https://docs.cloud.f5.com/docs/\nprinciples:\n  - name: Visibility\n    description: Track BIG-IP / NGINX Plus / BIG-IQ instance entitlement; pull Distributed Cloud usage\n      reports from the F5 Customer 360 portal; reconcile FCP true-up reports each quarter.\n  - name: Allocation\n    description: Allocate license cost by environment / business unit (BIG-IP partitions, NGINX Plus per-instance,\n      Distributed Cloud per-tenant/per-namespace). Tag VE instances and Distributed Cloud sites with team/product.\n  - name: Optimization\n    description: Right-size BIG-IP VE flavors; consolidate NGINX Plus instances onto NGINX One Console\n      for fleet management; choose FCP for variable demand workloads; cache aggressively at Distributed\n      Cloud edge\
  \ to lower egress and request meters; tune App Protect policies to avoid false-positive\n      bot challenges that drive bot-management volume.\n  - name: Accountability\n    description: Network/platform team owns BIG-IP and NGINX entitlement; security team owns App Protect\n      / Distributed Cloud Bot Defense; product teams own per-VS / per-namespace consumption. Annual license\n      review; quarterly FCP true-up; monthly Distributed Cloud usage review.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Subscription / Perpetual / Flex Consumption + SaaS Usage\n  billingFrequency: Annual (Subscription/FCP), One-Time (Perpetual), Monthly (Distributed Cloud usage)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Tax\n  chargeFrequency: Recurring (Subscription/FCP/Distributed Cloud) or One-Time (Perpetual)\nfocusColumns:\n  ServiceName: F5 Networks\n  ServiceCategory: Application Delivery / Multi-Cloud Security\n  ProviderName: F5\n  PublisherName: F5, Inc.\n  InvoiceIssuerName: F5, Inc.\n  PricingCategory: Subscription / Perpetual / FCP / Usage\n  PricingUnit: instance | request | GB | transaction\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: bigip_instances\n    description: Count of licensed BIG-IP instances (hardware or VE).\n    unit: instance\n    aggregation:\
  \ max\n    dimensions:\n      - environment\n      - region\n      - form_factor\n  - name: nginx_plus_instances\n    description: Count of licensed NGINX Plus instances.\n    unit: instance\n    aggregation: max\n    dimensions:\n      - environment\n      - region\n  - name: app_protect_instances\n    description: App Protect / Advanced WAF entitled instances.\n    unit: instance\n    aggregation: max\n    dimensions:\n      - product\n  - name: distributed_cloud_requests\n    description: F5 Distributed Cloud HTTP/L7 requests (CDN, WAF, API Security, Bot Defense).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - tenant\n      - namespace\n      - region\n  - name: distributed_cloud_egress\n    description: F5 Distributed Cloud egress data.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - service\n      - tenant\n      - region\n  - name: fcp_commitment\n    description: Annual FCP commitment $; trues up to actual usage.\n    unit: USD\n\
  \    aggregation: sum\n    dimensions:\n      - year\n      - service\napis:\n  - name: F5 BIG-IP iControl REST API\n    baseURL: https://{{bigip_host}}/mgmt/tm\n    serviceName: F5 BIG-IP iControl REST API\n    serviceCategory: API\n  - name: F5 Distributed Cloud API\n    baseURL: https://{{tenant}}.console.ves.volterra.io/api\n    serviceName: F5 Distributed Cloud API\n    serviceCategory: API\n  - name: F5 NGINX Management Suite API\n    baseURL: https://{{nms-host}}/api\n    serviceName: F5 NGINX Management Suite API\n    serviceCategory: API\n  - name: F5 Essential App Protect API\n    baseURL: https://api.f5.com/app-protect\n    serviceName: F5 Essential App Protect API\n    serviceCategory: API\n  - name: F5 BIG-IQ Centralized Management API\n    baseURL: https://{{bigiq_host}}/mgmt\n    serviceName: F5 BIG-IQ Centralized Management API\n    serviceCategory: API\n  - name: F5 BIG-IP Application Services 3 Extension API\n    baseURL: https://{{bigip_host}}/mgmt/shared/appsvcs\n \
  \   serviceName: F5 BIG-IP Application Services 3 Extension API\n    serviceCategory: API\n  - name: F5 Declarative Onboarding API\n    baseURL: https://{{bigip_host}}/mgmt/shared/declarative-onboarding\n    serviceName: F5 Declarative Onboarding API\n    serviceCategory: API\n  - name: F5 Telemetry Streaming API\n    baseURL: https://{{bigip_host}}/mgmt/shared/telemetry\n    serviceName: F5 Telemetry Streaming API\n    serviceCategory: API\n  - name: F5 NGINX Plus API\n    baseURL: https://{{nginx_host}}/api\n    serviceName: F5 NGINX Plus API\n    serviceCategory: API\n  - name: F5 NGINX One Console API\n    baseURL: https://{{nginx-one-host}}/api\n    serviceName: F5 NGINX One Console API\n    serviceCategory: API\n  - name: F5 NGINX Ingress Controller API\n    baseURL: https://{{kubernetes_host}}\n    serviceName: F5 NGINX Ingress Controller API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per BIG-IP instance / year\n    metric: total_license_cost / bigip_instances\n \
  \   target: model-dependent\n  - name: Cost per 1M Distributed Cloud requests\n    metric: distributed_cloud_cost / (distributed_cloud_requests / 1000000)\n    target: tier-dependent\n  - name: FCP true-up variance\n    metric: (actual_usage - committed) / committed\n    target: minimize positive variance\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/f5-networks/refs/heads/main/finops/f5-networks-finops.yml
sources:
- https://www.f5.com/products/get-f5
- https://www.f5.com/cloud
- https://docs.cloud.f5.com/docs/
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
