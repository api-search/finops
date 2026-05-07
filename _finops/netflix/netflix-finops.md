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
  - Adjustment
  pricingCategory: Partner Program (No Cost) + Enterprise Contract
description: 'FOCUS-aligned FinOps for Netflix: Netflix has no publicly billable API. Open Connect partner ISP appliances are provided at no cost in exchange for hosting / power / peering. Device Partner Program is contractual.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Netflix, Inc.
  PricingCategory: Free + Contract
  ProviderName: Netflix
  PublisherName: Netflix, Inc.
  ServiceCategory: Media
  ServiceName: Netflix Open Connect / Device Partner Program
  ServiceSubcategory: CDN + Device Certification
layout: finops
meters:
- aggregation: avg
  description: Open Connect Appliances deployed to ISP partner POPs.
  dimensions:
  - region
  - partner
  name: open_connect_appliance
  unit: appliance-month
- aggregation: sum
  description: Settlement-free peering traffic delivered through Open Connect.
  dimensions:
  - region
  - partner
  name: peering_traffic
  unit: GB
- aggregation: sum
  description: Device Partner Program contractual obligations.
  dimensions:
  - partner
  name: device_partner_contract
  unit: contract-month
name: Netflix Finops
provider_name: Netflix
provider_slug: netflix
publisher_name: Netflix, Inc.
service_category: Media + CDN
slug: netflix-finops
source_filename: netflix-finops.yml
source_heading: FinOps Profile
source_url: https://openconnect.netflix.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Netflix\nproviderId: netflix\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - CDN\n  - Streaming\n  - Open Connect\nnotes: Netflix does not sell a public developer API; there is no FinOps surface to reconcile. The artifact\n  here documents the partner-program billing shape (zero-cost Open Connect appliances to qualifying ISPs,\n  contractual Device Partner terms) for completeness.\ndescription: 'FOCUS-aligned FinOps for Netflix: Netflix has no publicly billable API. Open Connect partner\n  ISP appliances are provided at no cost in exchange for hosting / power / peering. Device Partner Program\n  is contractual.'\nsources:\n  - https://openconnect.netflix.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Netflix, Inc.\nserviceCategory: Media + CDN\nbillingModel:\n  pricingCategory: Partner Program (No Cost) + Enterprise Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\nfocusColumns:\n  ServiceName: Netflix Open Connect / Device Partner Program\n  ServiceCategory: Media\n  ServiceSubcategory: CDN + Device Certification\n  ProviderName: Netflix\n  PublisherName: Netflix, Inc.\n  InvoiceIssuerName: Netflix, Inc.\n  BillingCurrency: USD\n  PricingCategory: Free + Contract\nmeters:\n  - name: open_connect_appliance\n    description: Open Connect Appliances deployed to ISP partner POPs.\n    unit: appliance-month\n    aggregation: avg\n    dimensions:\n      - region\n      - partner\n  - name: peering_traffic\n    description: Settlement-free peering traffic delivered through Open Connect.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n\
  \      - partner\n  - name: device_partner_contract\n    description: Device Partner Program contractual obligations.\n    unit: contract-month\n    aggregation: sum\n    dimensions:\n      - partner\nprinciples:\n  - name: Visibility\n    description: Open Connect partners receive traffic and cache-fill telemetry through the Open Connect\n      partner portal; Netflix internally tracks egress savings vs. transit.\n  - name: Allocation\n    description: Netflix attributes Open Connect deployments per partner and per POP for capacity planning.\n  - name: Optimization\n    description: Netflix optimizes by deploying appliances closer to viewers (fill at off-peak, serve\n      at peak) — partners save transit costs in exchange for hosting.\n  - name: Accountability\n    description: Open Connect partner team owns appliance fleet TCO; Device Partner team owns certification\n      and contractual SLAs.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/netflix/refs/heads/main/finops/netflix-finops.yml
sources:
- https://openconnect.netflix.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- CDN
- Streaming
- Open Connect
---
