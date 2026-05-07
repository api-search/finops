---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: doordash-drive-openapi.yml
  format: yaml
  label: DoorDash Drive API
  slug: drive-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/doordash/refs/heads/main/openapi/doordash-drive-openapi.yml
- filename: doordash-drive-classic-openapi.yml
  format: yaml
  label: DoorDash Drive Classic API
  slug: drive-classic-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/doordash/refs/heads/main/openapi/doordash-drive-classic-openapi.yml
- filename: doordash-marketplace-openapi.yml
  format: yaml
  label: DoorDash Marketplace API
  slug: marketplace-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/doordash/refs/heads/main/openapi/doordash-marketplace-openapi.yml
- filename: doordash-item-management-openapi.yml
  format: yaml
  label: DoorDash Item Management API
  slug: marketplace-item-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/doordash/refs/heads/main/openapi/doordash-item-management-openapi.yml
- filename: doordash-reporting-openapi.yml
  format: yaml
  label: DoorDash Reporting API
  slug: reporting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/doordash/refs/heads/main/openapi/doordash-reporting-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Continuous Settlement
  chargeCategories:
  - Usage
  - Refund
  - Tax
  pricingCategory: Pay-As-You-Go
description: FOCUS-aligned FinOps shape for DoorDash Drive. Per-delivery billing (distance-based base fee plus optional per-mile surcharge for the current Drive API; flat fee for Drive classic). Settlement is via Stripe credit-card by default; monthly invoicing with ACH/check is available on request.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: DoorDash, Inc.
  ProviderName: DoorDash
  PublisherName: DoorDash, Inc.
  ServiceCategory: Last-Mile Delivery
  ServiceName: DoorDash Drive
layout: finops
meters:
- aggregation: count
  description: Count of created deliveries (billable at request time)
  dimensions:
  - api_version
  - market
  - distance_band
  name: deliveries
  unit: delivery
- aggregation: sum
  description: Pickup-to-dropoff miles used for the per-mile surcharge
  dimensions:
  - api_version
  name: distance_miles
  unit: mile
- aggregation: sum
  description: End-user tips passed through to the Dasher
  dimensions:
  - api_version
  name: tips_passed_through
  unit: USD
- aggregation: count
  description: Return-to-pickup deliveries (billed at 60% of original fee)
  dimensions:
  - api_version
  name: returns
  unit: delivery
name: Doordash Finops
provider_name: doordash
provider_slug: doordash
publisher_name: DoorDash, Inc.
service_category: Last-Mile Delivery
slug: doordash-finops
source_filename: doordash-finops.yml
source_heading: FinOps Profile
source_url: https://developer.doordash.com/en-US/docs/drive/overview/pricing_payment/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: doordash\nproviderId: doordash\npublisherName: DoorDash, Inc.\nserviceCategory: Last-Mile Delivery\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Delivery\n  - Logistics\n  - Last Mile\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for DoorDash Drive. Per-delivery billing (distance-based base\n  fee plus optional per-mile surcharge for the current Drive API; flat fee for Drive classic). Settlement\n  is via Stripe credit-card by default; monthly invoicing with ACH/check is available on request.\nsources:\n  - https://developer.doordash.com/en-US/docs/drive/overview/pricing_payment/\n  - https://developer.doordash.com/en-US/docs/drive/overview/faqs/\n\
  billingModel:\n  pricingCategory: Pay-As-You-Go\n  billingFrequency: Continuous Settlement\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Refund\n    - Tax\nfocusColumns:\n  ServiceName: DoorDash Drive\n  ServiceCategory: Last-Mile Delivery\n  ProviderName: DoorDash\n  PublisherName: DoorDash, Inc.\n  InvoiceIssuerName: DoorDash, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: deliveries\n    description: Count of created deliveries (billable at request time)\n    unit: delivery\n    aggregation: count\n    dimensions:\n      - api_version\n      - market\n      - distance_band\n  - name: distance_miles\n    description: Pickup-to-dropoff miles used for the per-mile surcharge\n    unit: mile\n    aggregation: sum\n    dimensions:\n      - api_version\n  - name: tips_passed_through\n    description: End-user tips passed through to the Dasher\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - api_version\n  - name: returns\n    description:\
  \ Return-to-pickup deliveries (billed at 60% of original fee)\n    unit: delivery\n    aggregation: count\n    dimensions:\n      - api_version\nprinciples:\n  - name: Visibility\n    description: Each delivery request triggers a Stripe charge; reconcile against the credit-card statement\n      or the monthly invoice when ACH terms are in place.\n  - name: Allocation\n    description: Tag deliveries by store/storefront and order channel so cost can be attributed to the\n      revenue-generating order.\n  - name: Optimization\n    description: Keep deliveries under 5 miles where possible to avoid the per-mile surcharge; pass through\n      end-user tips to capture the $2.75 base-rate discount; minimise returns.\n  - name: Accountability\n    description: Operations / fulfilment owner reconciles delivery cost against AOV and runs SLA reviews\n      with DoorDash support.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/doordash/refs/heads/main/finops/doordash-finops.yml
sources:
- https://developer.doordash.com/en-US/docs/drive/overview/pricing_payment/
- https://developer.doordash.com/en-US/docs/drive/overview/faqs/
specification: FinOps Framework
tags:
- Delivery
- Logistics
- Last Mile
- FinOps
- FOCUS
---
