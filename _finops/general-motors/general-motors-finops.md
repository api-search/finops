---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Partner / Subscription
description: General Motors monetizes connected-vehicle and OnStar services to consumers via subscription, and to partners/fleets via commercial agreement. There is no public per-API billing surface; FinOps applies to subscription mix and partner-fee allocation.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: General Motors LLC
  ProviderName: General Motors
  PublisherName: General Motors LLC
  ServiceCategory: Automotive & Connected Services
  ServiceName: General Motors
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api_product
  - vin
  - partner_id
  name: api_calls
  unit: request
- aggregation: max
  dimensions:
  - service_plan
  name: vehicles_under_service
  unit: vehicle-month
- aggregation: sum
  dimensions:
  - api_product
  name: data_transferred
  unit: GB
name: General Motors Finops
provider_name: General Motors
provider_slug: general-motors
publisher_name: General Motors LLC
service_category: Automotive & Connected Services
slug: general-motors-finops
source_filename: general-motors-finops.yml
source_heading: FinOps Profile
source_url: https://developer.gm.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: General Motors\nproviderId: general-motors\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Automotive\n  - Connected Vehicle\ndescription: General Motors monetizes connected-vehicle and OnStar services to consumers via\n  subscription, and to partners/fleets via commercial agreement. There is no public per-API\n  billing surface; FinOps applies to subscription mix and partner-fee allocation.\nnotes: No public API pricing surface; FinOps shape inferred from a vehicle-OEM connected-services\n  / partner-program model.\nsources:\n  - https://developer.gm.com/\n  - https://www.gm.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ General Motors LLC\nserviceCategory: Automotive & Connected Services\nbillingModel:\n  pricingCategory: Partner / Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: General Motors\n  ServiceCategory: Automotive & Connected Services\n  ProviderName: General Motors\n  PublisherName: General Motors LLC\n  InvoiceIssuerName: General Motors LLC\n  BillingCurrency: USD\nmeters:\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_product\n      - vin\n      - partner_id\n  - name: vehicles_under_service\n    unit: vehicle-month\n    aggregation: max\n    dimensions:\n      - service_plan\n  - name: data_transferred\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api_product\nprinciples:\n  - name: Visibility\n    description: For partners, reconcile GM invoices against per-VIN service activations and API\n      call\
  \ volumes recorded in the partner portal.\n  - name: Allocation\n    description: Tag VINs / fleet groups to cost centers; segregate partner credentials per\n      consuming application.\n  - name: Optimization\n    description: Right-size telematics polling intervals; use event-driven (push) channels where\n      available rather than polling; consolidate fleet plans by usage tier.\n  - name: Accountability\n    description: Fleet manager / mobility-product owner owns spend; review service-plan mix and\n      data-transfer growth quarterly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/general-motors/refs/heads/main/finops/general-motors-finops.yml
sources:
- https://developer.gm.com/
- https://www.gm.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Automotive
- Connected Vehicle
---
