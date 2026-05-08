---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: citrix-netscaler-nitro-openapi.yml
  format: yaml
  label: Citrix ADC (NetScaler) NITRO API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citrix-netscaler/refs/heads/main/openapi/citrix-netscaler-nitro-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription + Perpetual License
description: FOCUS-aligned FinOps shape for NetScaler. Cost is driven by NetScaler edition (Standard / Advanced / Premium), throughput tier, and form factor (MPX / VPX / SDX / CPX), increasingly delivered via pooled-capacity subscriptions managed by NetScaler Console. Underlying compute / network for VPX / CPX instances is billed by the hosting hyperscaler or on-prem hypervisor.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Cloud Software Group, Inc.
  ProviderName: NetScaler
  PublisherName: Cloud Software Group, Inc.
  ServiceCategory: Application Delivery
  ServiceName: Citrix NetScaler
layout: finops
meters:
- aggregation: max
  description: Per-instance NetScaler edition + throughput-tier license.
  dimensions:
  - edition
  - throughput_tier
  - form_factor
  - region
  name: netscaler_instance_license
  unit: instance-month
- aggregation: max
  description: Pooled bandwidth allocated across NetScaler instances under Pooled Capacity.
  dimensions:
  - region
  name: netscaler_pooled_bandwidth
  unit: Mbps-month
- aggregation: max
  description: Pooled SSL transactions-per-second under Pooled Capacity.
  dimensions:
  - region
  name: netscaler_pooled_ssl_tps
  unit: TPS-month
- aggregation: max
  description: NetScaler Console (ADM) management capacity (managed instances / agents).
  dimensions:
  - tier
  - region
  name: netscaler_console_management
  unit: instance-month
- aggregation: sum
  description: Underlying VM / container compute for VPX / CPX deployments.
  dimensions:
  - cloud
  - instance_type
  - region
  name: hyperscaler_compute
  unit: instance-hour
name: Citrix Netscaler Finops
provider_name: Citrix NetScaler
provider_slug: citrix-netscaler
publisher_name: Cloud Software Group, Inc.
service_category: Application Delivery
slug: citrix-netscaler-finops
source_filename: citrix-netscaler-finops.yml
source_heading: FinOps Profile
source_url: https://www.netscaler.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Citrix NetScaler\nproviderId: citrix-netscaler\npublisherName: Cloud Software Group, Inc.\nserviceCategory: Application Delivery\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Application Delivery Controller\n  - Load Balancing\n  - Web Application Firewall\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps shape for NetScaler. Cost is driven by NetScaler edition (Standard / Advanced\n  / Premium), throughput tier, and form factor (MPX / VPX / SDX / CPX), increasingly delivered via\n  pooled-capacity subscriptions managed by NetScaler Console. Underlying compute / network for VPX /\n  CPX instances is billed\
  \ by the hosting hyperscaler or on-prem hypervisor.\nnotes: Underlying compute / network for virtual NetScaler instances on AWS / Azure / GCP / on-prem\n  is billed separately by those providers and tracked through their FinOps surfaces.\nsources:\n  - https://www.netscaler.com\n  - https://docs.netscaler.com\nbillingModel:\n  pricingCategory: Subscription + Perpetual License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Citrix NetScaler\n  ServiceCategory: Application Delivery\n  ProviderName: NetScaler\n  PublisherName: Cloud Software Group, Inc.\n  InvoiceIssuerName: Cloud Software Group, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: netscaler_instance_license\n    description: Per-instance NetScaler edition + throughput-tier license.\n    unit: instance-month\n    aggregation: max\n    dimensions:\n      - edition\n      - throughput_tier\n\
  \      - form_factor\n      - region\n  - name: netscaler_pooled_bandwidth\n    description: Pooled bandwidth allocated across NetScaler instances under Pooled Capacity.\n    unit: Mbps-month\n    aggregation: max\n    dimensions:\n      - region\n  - name: netscaler_pooled_ssl_tps\n    description: Pooled SSL transactions-per-second under Pooled Capacity.\n    unit: TPS-month\n    aggregation: max\n    dimensions:\n      - region\n  - name: netscaler_console_management\n    description: NetScaler Console (ADM) management capacity (managed instances / agents).\n    unit: instance-month\n    aggregation: max\n    dimensions:\n      - tier\n      - region\n  - name: hyperscaler_compute\n    description: Underlying VM / container compute for VPX / CPX deployments.\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cloud\n      - instance_type\n      - region\nprinciples:\n  - name: Visibility\n    description: Use NetScaler Console (ADM) for license-pool consumption,\
  \ throughput, and SSL TPS\n      utilization; pair with hyperscaler cost reports for VPX / CPX compute.\n  - name: Allocation\n    description: Allocate appliance license cost to platform / network team budgets; chargeback by\n      virtual server / tenant using ADM analytics tags.\n  - name: Optimization\n    description: Move to Pooled Capacity to share bandwidth across MPX / VPX / SDX / CPX, retire\n      under-utilized appliances, choose the right edition (Standard vs Premium), and prefer reserved\n      / savings-plan commitments for hyperscaler compute hosting VPX.\n  - name: Accountability\n    description: Network / platform owner is accountable for NetScaler license-pool sizing,\n      term-renewal cadence, and coordination with cloud platform teams on the underlying compute.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/citrix-netscaler/refs/heads/main/finops/citrix-netscaler-finops.yml
sources:
- https://www.netscaler.com
- https://docs.netscaler.com
specification: FinOps Framework
tags:
- Application Delivery Controller
- Load Balancing
- Web Application Firewall
- FinOps
- FOCUS
---
