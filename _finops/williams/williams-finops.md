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
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Tariff-Based
description: FinOps shape for Williams is tariff-driven - pipeline transportation rates filed with FERC and invoiced under the shipper's transportation service agreement. The 1Line / EBB system itself is not separately metered as an API; it is the access channel for the underlying tariff service.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Williams Companies, Inc.
  ProviderName: Williams Companies
  PublisherName: The Williams Companies, Inc.
  ServiceCategory: Energy Infrastructure
  ServiceName: Williams 1Line Pipeline Service
layout: finops
meters:
- aggregation: max
  dimensions:
  - pipeline
  - rate_schedule
  - receipt_point
  - delivery_point
  name: reserved_capacity
  unit: Dth_per_day
- aggregation: sum
  dimensions:
  - pipeline
  - rate_schedule
  - cycle
  name: transported_volume
  unit: Dth
- aggregation: sum
  dimensions:
  - pipeline
  - rate_schedule
  name: capacity_release
  unit: Dth_per_day
name: Williams Finops
provider_name: Williams Companies
provider_slug: williams
publisher_name: The Williams Companies, Inc.
service_category: Energy Infrastructure
slug: williams-finops
source_filename: williams-finops.yml
source_heading: FinOps Profile
source_url: https://www.williams.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Williams Companies\nproviderId: williams\npublisherName: The Williams Companies, Inc.\nserviceCategory: Energy Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Natural Gas\n  - Pipeline\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps shape for Williams is tariff-driven - pipeline transportation rates filed with FERC and invoiced under the shipper's transportation service agreement. The 1Line / EBB system itself is not separately metered as an API; it is the access channel for the underlying tariff service.\nsources:\n  - https://www.williams.com\n  - https://www.1line.williams.com\n\
  notes: There is no API price list; cost is the pipeline tariff. Meters describe the actual tariff line items (reserved capacity, transported volume) rather than synthetic API meters.\nbillingModel:\n  pricingCategory: Tariff-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Williams 1Line Pipeline Service\n  ServiceCategory: Energy Infrastructure\n  ProviderName: Williams Companies\n  PublisherName: The Williams Companies, Inc.\n  InvoiceIssuerName: The Williams Companies, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: reserved_capacity\n    unit: Dth_per_day\n    aggregation: max\n    dimensions:\n      - pipeline\n      - rate_schedule\n      - receipt_point\n      - delivery_point\n  - name: transported_volume\n    unit: Dth\n    aggregation: sum\n    dimensions:\n      - pipeline\n      - rate_schedule\n      - cycle\n  - name: capacity_release\n    unit: Dth_per_day\n    aggregation:\
  \ sum\n    dimensions:\n      - pipeline\n      - rate_schedule\nprinciples:\n  - name: Visibility\n    description: Reconcile against 1Line nomination, scheduling, and confirmation reports plus the shipper's monthly transportation invoice; FERC-filed tariffs publish the rate schedules.\n  - name: Allocation\n    description: Allocate by pipeline (Transco / Northwest), rate schedule, and receipt / delivery point pair, matching the tariff's billing keys.\n  - name: Optimization\n    description: Optimization is contractual - capacity-release auctions, alternate path selection, and cycle timing - not API-call reduction.\n  - name: Accountability\n    description: Owned by gas-supply / scheduling and treasury; the technical 1Line integration team owns reliability of nominations, not the underlying tariff cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/williams/refs/heads/main/finops/williams-finops.yml
sources:
- https://www.williams.com
- https://www.1line.williams.com
specification: FinOps Framework
tags:
- Energy
- Natural Gas
- Pipeline
- FinOps
- FOCUS
- Contact Sales
---
