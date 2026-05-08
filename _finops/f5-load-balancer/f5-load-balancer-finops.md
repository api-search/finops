---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: f5-load-balancer-icontrol-rest-openapi.yml
  format: yaml
  label: F5 BIG-IP iControl REST API
  slug: f5-bigip-icontrol-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/f5-load-balancer/refs/heads/main/openapi/f5-load-balancer-icontrol-rest-openapi.yml
- filename: f5-load-balancer-as3-openapi.yml
  format: yaml
  label: F5 BIG-IP AS3 API
  slug: f5-bigip-as3-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/f5-load-balancer/refs/heads/main/openapi/f5-load-balancer-as3-openapi.yml
- filename: f5-load-balancer-declarative-onboarding-openapi.yml
  format: yaml
  label: F5 BIG-IP Declarative Onboarding API
  slug: f5-bigip-declarative-onboarding-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/f5-load-balancer/refs/heads/main/openapi/f5-load-balancer-declarative-onboarding-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (Subscription/FCP), One-Time (Perpetual)
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  chargeFrequency: Recurring (Subscription/FCP) or One-Time (Perpetual)
  pricingCategory: Subscription / Perpetual / Flex Consumption
description: FOCUS-aligned FinOps for F5 BIG-IP load balancer products. Cost is driven by license model (Subscription / Perpetual / Flex Consumption Program) negotiated through F5 sales or a reseller; there is no per-API-call charge. FinOps levers focus on instance-count, term length, and FCP true-up.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: F5, Inc.
  PricingCategory: Subscription / Perpetual / Flex
  PricingUnit: instance
  ProviderName: F5
  PublisherName: F5, Inc.
  ServiceCategory: Application Delivery / Networking
  ServiceName: F5 BIG-IP
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
- aggregation: sum
  description: Annual FCP commitment $; trues up to actual usage.
  dimensions:
  - year
  - service
  name: fcp_commitment
  unit: USD
- aggregation: max
  description: Active support contract coverage by service module.
  dimensions:
  - service
  name: support_entitlement
  unit: month
name: F5 Load Balancer Finops
provider_name: F5 Load Balancer
provider_slug: f5-load-balancer
publisher_name: F5, Inc.
service_category: Application Delivery / Networking
slug: f5-load-balancer-finops
source_filename: f5-load-balancer-finops.yml
source_heading: FinOps Profile
source_url: https://www.f5.com/products/get-f5
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: F5 Load Balancer\nproviderId: f5-load-balancer\npublisherName: F5, Inc.\nserviceCategory: Application Delivery / Networking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Application Delivery\n  - BIG-IP\n  - Load Balancer\n  - Networking\n  - Traffic Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for F5 BIG-IP load balancer products. Cost is driven by license model\n  (Subscription / Perpetual / Flex Consumption Program) negotiated through F5 sales or a reseller; there\n  is no per-API-call charge. FinOps levers focus on instance-count, term length, and FCP true-up.'\nnotes: F5 publishes no list prices; this artifact\
  \ describes the FinOps shape. Reconcile cost values against\n  an active quote.\nsources:\n  - https://www.f5.com/products/get-f5\n  - https://www.f5.com/products/big-ip-services\nprinciples:\n  - name: Visibility\n    description: Track BIG-IP instance counts (hardware models and VE sizes) per environment; pull FCP\n      activity reports quarterly; reconcile against support entitlement records.\n  - name: Allocation\n    description: Allocate license cost by tenant/business unit via partition/route-domain on BIG-IP, or\n      by VE deployment in cloud accounts. Tag VE instances in the cloud provider with team/product.\n  - name: Optimization\n    description: Right-size BIG-IP VE flavors before renewal; consolidate workloads onto larger appliances\n      where TMOS capacity allows; choose FCP for variable demand and Perpetual+Support for steady workloads;\n      negotiate longer terms (3-yr) for better unit cost.\n  - name: Accountability\n    description: Network/platform team owns\
  \ BIG-IP entitlement; product teams own per-VS configuration\n      cost. Annual review of license vs. utilized capacity; quarterly FCP true-up.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Subscription / Perpetual / Flex Consumption\n  billingFrequency: Annual (Subscription/FCP), One-Time (Perpetual)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n\
  \    - Usage\n    - Adjustment\n    - Tax\n  chargeFrequency: Recurring (Subscription/FCP) or One-Time (Perpetual)\nfocusColumns:\n  ServiceName: F5 BIG-IP\n  ServiceCategory: Application Delivery / Networking\n  ProviderName: F5\n  PublisherName: F5, Inc.\n  InvoiceIssuerName: F5, Inc.\n  PricingCategory: Subscription / Perpetual / Flex\n  PricingUnit: instance\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: bigip_instances\n    description: Count of licensed BIG-IP instances (hardware or VE).\n    unit: instance\n    aggregation: max\n    dimensions:\n      - environment\n      - region\n      - form_factor\n  - name: fcp_commitment\n    description: Annual FCP commitment $; trues up to actual usage.\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - year\n      - service\n  - name: support_entitlement\n    description: Active support contract coverage by service module.\n    unit: month\n    aggregation: max\n    dimensions:\n      - service\napis:\n\
  \  - name: F5 BIG-IP iControl REST API\n    baseURL: https://bigip-host/mgmt/tm\n    serviceName: F5 BIG-IP iControl REST API\n    serviceCategory: API\n  - name: F5 BIG-IP AS3 API\n    baseURL: https://bigip-host/mgmt/shared/appsvcs\n    serviceName: F5 BIG-IP AS3 API\n    serviceCategory: API\n  - name: F5 BIG-IP Declarative Onboarding API\n    baseURL: https://bigip-host/mgmt/shared/declarative-onboarding\n    serviceName: F5 BIG-IP Declarative Onboarding API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per BIG-IP instance / year\n    metric: total_license_cost / bigip_instances\n    target: model-dependent (set per platform)\n  - name: FCP true-up variance\n    metric: (actual_usage - committed) / committed\n    target: minimize positive variance\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/f5-load-balancer/refs/heads/main/finops/f5-load-balancer-finops.yml
sources:
- https://www.f5.com/products/get-f5
- https://www.f5.com/products/big-ip-services
specification: FinOps Framework
tags:
- Application Delivery
- BIG-IP
- Load Balancer
- Networking
- Traffic Management
- FinOps
- Cost Management
- FOCUS
---
