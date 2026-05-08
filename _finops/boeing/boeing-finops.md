---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Capital Purchase + Services Subscription (Negotiated)
description: 'FOCUS-aligned FinOps placeholder for Boeing: not a developer-facing platform. Spend with Boeing flows through commercial-airplane purchase contracts, defense / space programs, and services / digital subscriptions (Boeing Global Services, Jeppesen, ForeFlight, Digital Aviation Solutions). No public per-API billing surface.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: The Boeing Company
  ProviderName: Boeing
  PublisherName: The Boeing Company
  ServiceCategory: Aerospace
  ServiceName: Boeing
layout: finops
meters:
- aggregation: count
  dimensions:
  - model
  - configuration
  name: aircraft_purchases
  unit: aircraft
- aggregation: sum
  dimensions:
  - product
  - tail_number
  name: services_subscription
  unit: year
- aggregation: sum
  dimensions:
  - product
  - region
  name: jeppesen_subscriptions
  unit: year
- aggregation: max
  dimensions:
  - tier
  name: foreflight_seats
  unit: seat
name: Boeing Finops
provider_name: Boeing
provider_slug: boeing
publisher_name: The Boeing Company
service_category: Aerospace / Aviation Services
slug: boeing-finops
source_filename: boeing-finops.yml
source_heading: FinOps Profile
source_url: https://www.boeing.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Boeing\nproviderId: boeing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Aviation\n  - Aerospace\ndescription: 'FOCUS-aligned FinOps placeholder for Boeing: not a developer-facing platform. Spend\n  with Boeing flows through commercial-airplane purchase contracts, defense / space programs, and\n  services / digital subscriptions (Boeing Global Services, Jeppesen, ForeFlight, Digital Aviation\n  Solutions). No public per-API billing surface.'\nsources:\n  - https://www.boeing.com\nnotes: Boeing has no public API billing surface; reconcile against the active contract for actual\n  fee structure.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: The Boeing Company\nserviceCategory: Aerospace / Aviation Services\nbillingModel:\n  pricingCategory: Capital Purchase + Services Subscription (Negotiated)\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Boeing\n  ServiceCategory: Aerospace\n  ProviderName: Boeing\n  PublisherName: The Boeing Company\n  InvoiceIssuerName: The Boeing Company\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: aircraft_purchases\n    unit: aircraft\n    aggregation: count\n    dimensions:\n      - model\n      - configuration\n  - name: services_subscription\n    unit: year\n    aggregation: sum\n    dimensions:\n      - product\n      - tail_number\n  - name: jeppesen_subscriptions\n    unit: year\n    aggregation: sum\n    dimensions:\n      - product\n      - region\n  - name: foreflight_seats\n    unit: seat\n    aggregation: max\n    dimensions:\n\
  \      - tier\nprinciples:\n  - name: Visibility\n    description: Use Boeing customer-services portals (Toolbox / MyBoeingFleet) and Jeppesen /\n      ForeFlight admin consoles to track active subscriptions and per-tail entitlements.\n  - name: Allocation\n    description: Map services subscriptions and digital licenses to consuming fleets / pilot\n      groups for chargeback against the bundled Boeing invoice.\n  - name: Optimization\n    description: Reclaim unused Jeppesen / ForeFlight seats during annual renewal; align Digital\n      Aviation Solutions subscriptions with active fleet composition; consolidate vendors where\n      Boeing Global Services covers the same scope.\n  - name: Accountability\n    description: Designate a Boeing services contract owner per fleet; review utilization\n      quarterly with Boeing Global Services and Jeppesen account teams.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/boeing/refs/heads/main/finops/boeing-finops.yml
sources:
- https://www.boeing.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Aviation
- Aerospace
---
