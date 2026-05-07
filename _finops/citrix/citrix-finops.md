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
  label: Citrix Virtual Apps and Desktops REST API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.citrix.com/citrix-virtual-apps-and-desktops/citrix-cvad-rest-apis/docs/openapi
- filename: citrix-adc-nitro-openapi.yml
  format: yaml
  label: Citrix ADC (NetScaler) NITRO API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citrix/refs/heads/main/openapi/citrix-adc-nitro-openapi.yml
- filename: openapi
  format: yaml
  label: Citrix DaaS REST API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.citrix.com/citrix-daas/citrix-daas-rest-apis/docs/openapi
- filename: citrix-cloud-openapi.yml
  format: yaml
  label: Citrix Cloud API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citrix/refs/heads/main/openapi/citrix-cloud-openapi.yml
- filename: citrix-storefront-web-openapi.yml
  format: yaml
  label: Citrix StoreFront Web API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citrix/refs/heads/main/openapi/citrix-storefront-web-openapi.yml
- filename: citrix-endpoint-management-openapi.yml
  format: yaml
  label: Citrix Endpoint Management REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citrix/refs/heads/main/openapi/citrix-endpoint-management-openapi.yml
- filename: citrix-secure-private-access-openapi.yml
  format: yaml
  label: Citrix Secure Private Access API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citrix/refs/heads/main/openapi/citrix-secure-private-access-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps shape for Citrix. Cost is driven by per-user / per-device subscriptions (Citrix Platform License, Citrix DaaS tiers) and per-instance NetScaler / App Delivery licenses, plus underlying cloud compute / storage in customer-owned hyperscaler subscriptions when DaaS resource locations run in AWS, Azure, or GCP.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Cloud Software Group, Inc.
  ProviderName: Citrix
  PublisherName: Cloud Software Group, Inc.
  ServiceCategory: End-User Computing
  ServiceName: Citrix
layout: finops
meters:
- aggregation: max
  description: Per-user / per-device subscription to Citrix Platform License or DaaS tiers.
  dimensions:
  - tier
  - sku
  - region
  name: citrix_user_subscription
  unit: user-month
- aggregation: max
  description: NetScaler ADC throughput tier or vCPU entitlement.
  dimensions:
  - tier
  - form_factor
  - region
  name: netscaler_throughput
  unit: instance-month
- aggregation: sum
  description: Underlying VM compute hours used by Citrix DaaS resource locations on AWS / Azure / GCP.
  dimensions:
  - cloud
  - instance_type
  - region
  name: hyperscaler_compute
  unit: instance-hour
- aggregation: max
  description: Persistent disk / image storage in DaaS resource locations.
  dimensions:
  - cloud
  - storage_class
  - region
  name: hyperscaler_storage
  unit: GB-month
name: Citrix Finops
provider_name: Citrix
provider_slug: citrix
publisher_name: Cloud Software Group, Inc.
service_category: End-User Computing
slug: citrix-finops
source_filename: citrix-finops.yml
source_heading: FinOps Profile
source_url: https://www.citrix.com/products/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Citrix\nproviderId: citrix\npublisherName: Cloud Software Group, Inc.\nserviceCategory: End-User Computing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Application Delivery\n  - Desktop-As-A-Service\n  - Workspace\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps shape for Citrix. Cost is driven by per-user / per-device subscriptions\n  (Citrix Platform License, Citrix DaaS tiers) and per-instance NetScaler / App Delivery licenses,\n  plus underlying cloud compute / storage in customer-owned hyperscaler subscriptions when DaaS\n  resource locations run in AWS, Azure, or GCP.\nnotes: Underlying hyperscaler\
  \ compute / storage / egress for DaaS resource locations is billed\n  separately by AWS / Azure / GCP and should be tracked through those providers' FinOps surfaces.\nsources:\n  - https://www.citrix.com/products/\n  - https://docs.citrix.com/en-us/citrix-daas/\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Citrix\n  ServiceCategory: End-User Computing\n  ProviderName: Citrix\n  PublisherName: Cloud Software Group, Inc.\n  InvoiceIssuerName: Cloud Software Group, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: citrix_user_subscription\n    description: Per-user / per-device subscription to Citrix Platform License or DaaS tiers.\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - tier\n      - sku\n      - region\n  - name: netscaler_throughput\n    description: NetScaler ADC\
  \ throughput tier or vCPU entitlement.\n    unit: instance-month\n    aggregation: max\n    dimensions:\n      - tier\n      - form_factor\n      - region\n  - name: hyperscaler_compute\n    description: Underlying VM compute hours used by Citrix DaaS resource locations on AWS / Azure /\n      GCP.\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cloud\n      - instance_type\n      - region\n  - name: hyperscaler_storage\n    description: Persistent disk / image storage in DaaS resource locations.\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - cloud\n      - storage_class\n      - region\nprinciples:\n  - name: Visibility\n    description: Use Citrix Cloud Licensing dashboards plus Citrix Analytics for Performance to\n      observe license activation and session utilization; pair with hyperscaler cost reports for the\n      underlying DaaS compute footprint.\n  - name: Allocation\n    description: Tag Citrix users to cost centers via Active\
  \ Directory / Citrix Cloud user groups and\n      tag DaaS resource-location resources in the underlying cloud account for chargeback.\n  - name: Optimization\n    description: Right-size DaaS machine catalogs using autoscale, schedule power management, choose\n      the appropriate Citrix tier (Standard vs Premium), and use hyperscaler reserved or savings-\n      plan commitments for steady-state DaaS workloads.\n  - name: Accountability\n    description: End-user computing platform owner is accountable for Citrix license forecasting,\n      term-renewal cadence, and DaaS resource-location FinOps coordination with cloud platform teams.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/citrix/refs/heads/main/finops/citrix-finops.yml
sources:
- https://www.citrix.com/products/
- https://docs.citrix.com/en-us/citrix-daas/
specification: FinOps Framework
tags:
- Application Delivery
- Desktop-As-A-Service
- Workspace
- FinOps
- FOCUS
---
