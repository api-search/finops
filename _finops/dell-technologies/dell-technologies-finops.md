---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: dell-technologies-dell-api-openapi.yml
  format: yaml
  label: Dell Technologies API
  slug: dell-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dell-technologies/refs/heads/main/openapi/dell-technologies-dell-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Hardware Entitlement + APEX Consumption Subscription
description: FOCUS-aligned FinOps for Dell Technologies APIs. Bundled-with-product economics for management APIs (iDRAC, OpenManage, PowerStore) plus APEX consumption-based subscription metering for cloud and as-a-service offerings.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Dell Technologies Inc.
  PricingCategory: Subscription + Hardware
  PricingUnit: varies
  ProviderName: Dell Technologies
  PublisherName: Dell Technologies Inc.
  ServiceCategory: Enterprise IT / Infrastructure
  ServiceName: Dell Technologies API
layout: finops
meters:
- aggregation: max
  description: APEX storage / compute capacity reserved (committed) and on-demand
  dimensions:
  - subscription
  - product
  - region
  name: apex_capacity
  unit: GB
- aggregation: sum
  description: APEX consumption-based metered usage above commitment
  dimensions:
  - subscription
  - product
  - region
  name: apex_consumption
  unit: varies
- aggregation: sum
  description: ProSupport / ProSupport Plus / Keep Your Hard Drive entitlements
  dimensions:
  - service_tag
  - service_level
  name: support_subscription
  unit: month
- aggregation: max
  description: OpenManage Enterprise advanced license seats
  dimensions:
  - product
  name: management_seat
  unit: seat
name: Dell Technologies Finops
provider_name: Dell Technologies
provider_slug: dell-technologies
publisher_name: Dell Technologies Inc.
service_category: Enterprise IT / Infrastructure
slug: dell-technologies-finops
source_filename: dell-technologies-finops.yml
source_heading: FinOps Profile
source_url: https://developer.dell.com/apis
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Dell Technologies\nproviderId: dell-technologies\npublisherName: Dell Technologies Inc.\nserviceCategory: Enterprise IT / Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: Dell APIs (Redfish / iDRAC, OpenManage, PowerStore, Premier, APEX) are billed indirectly via the\n  underlying product entitlement or APEX consumption subscription. There is no per-API-call price; FinOps\n  shape follows hardware lifecycle plus APEX consumption metering. Reconcile against APEX subscription\n  invoices when available.\ntags:\n  - Enterprise IT\n  - Infrastructure\n  - Servers\n  - Storage\n  - APEX\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Dell\
  \ Technologies APIs. Bundled-with-product economics for management\n  APIs (iDRAC, OpenManage, PowerStore) plus APEX consumption-based subscription metering for cloud and\n  as-a-service offerings.'\nsources:\n  - https://developer.dell.com/apis\n  - https://www.dell.com/en-us/dt/apex/index.htm\nprinciples:\n  - name: Visibility\n    description: For APEX consumption, use the APEX Console / APEX Cloud Services dashboards to track\n      capacity-on-demand metering (storage GB, instance-hours, data services). For on-prem product APIs,\n      observe at the device / array level via OpenManage Enterprise telemetry.\n  - name: Allocation\n    description: Allocate APEX subscription costs to the consuming workload via APEX subscription tags;\n      allocate on-prem device usage by service tag and asset record from Dell Premier inventory.\n  - name: Optimization\n    description: Right-size APEX subscriptions against actual capacity utilization; consolidate iDRAC\n      management traffic and\
  \ OpenManage automation jobs to avoid licensing extra OME instances; review\n      data services and replication add-ons.\n  - name: Accountability\n    description: Asset owners track hardware lifecycle cost; APEX subscription owners track consumption\n      drift; route invoice anomalies through Dell account team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n\
  \  pricingCategory: Hardware Entitlement + APEX Consumption Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Dell Technologies API\n  ServiceCategory: Enterprise IT / Infrastructure\n  ProviderName: Dell Technologies\n  PublisherName: Dell Technologies Inc.\n  InvoiceIssuerName: Dell Technologies Inc.\n  PricingCategory: Subscription + Hardware\n  PricingUnit: varies\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: apex_capacity\n    description: APEX storage / compute capacity reserved (committed) and on-demand\n    unit: GB\n    aggregation: max\n    dimensions:\n      - subscription\n      - product\n      - region\n  - name: apex_consumption\n    description: APEX consumption-based metered usage above commitment\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - subscription\n  \
  \    - product\n      - region\n  - name: support_subscription\n    description: ProSupport / ProSupport Plus / Keep Your Hard Drive entitlements\n    unit: month\n    aggregation: sum\n    dimensions:\n      - service_tag\n      - service_level\n  - name: management_seat\n    description: OpenManage Enterprise advanced license seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\napis:\n  - name: Dell Technologies API\n    baseURL: https://developer.dell.com/apis\n    tags:\n      - Enterprise IT\n      - Infrastructure\n      - Servers\n      - Storage\n      - PowerEdge\n      - PowerStore\n      - OpenManage\n    serviceName: Dell Technologies API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per APEX-managed TB-month\n    metric: apex_subscription_cost / managed_tb_months\n    target: TBD\n  - name: Cost per Managed Asset\n    metric: support_cost / active_service_tags\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dell-technologies/refs/heads/main/finops/dell-technologies-finops.yml
sources:
- https://developer.dell.com/apis
- https://www.dell.com/en-us/dt/apex/index.htm
specification: FinOps Framework
tags:
- Enterprise IT
- Infrastructure
- Servers
- Storage
- APEX
- FinOps
- FOCUS
---
