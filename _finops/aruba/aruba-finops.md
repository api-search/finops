---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: aruba-central-api.yml
  format: yaml
  label: Aruba Central API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aruba/refs/heads/main/openapi/aruba-central-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription + Perpetual License
description: FOCUS-aligned FinOps shape for HPE Aruba Networking APIs — APIs are bundled with subscription licenses (Aruba Central Foundation/Advanced, ClearPass), perpetual hardware purchases (AOS-CX, EdgeConnect), and support contracts. There is no per-API metered billing line.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Hewlett Packard Enterprise
  PricingCategory: Subscription + Perpetual License
  ProviderName: HPE Aruba Networking
  PublisherName: Hewlett Packard Enterprise
  ServiceCategory: Networking
  ServiceName: HPE Aruba Networking
  ServiceSubcategory: Network Management & Security
layout: finops
meters:
- aggregation: max
  description: Aruba Central Foundation/Advanced/Premium device-month subscription
  dimensions:
  - tier
  - device_type
  - region
  name: aruba_central_subscription
  unit: device-month
- aggregation: max
  description: ClearPass policy manager licenses (endpoint counts)
  dimensions:
  - product
  - region
  name: clearpass_license
  unit: endpoint
- aggregation: max
  description: EdgeConnect SD-WAN appliance/site subscription
  dimensions:
  - bandwidth_tier
  - region
  name: edgeconnect_subscription
  unit: site-month
- aggregation: sum
  description: API call activity — not separately billed; tracked for capacity planning only
  dimensions:
  - product
  - cluster
  name: api_calls
  unit: request
name: Aruba Finops
provider_name: Aruba
provider_slug: aruba
publisher_name: Hewlett Packard Enterprise (HPE Aruba Networking)
service_category: Networking
slug: aruba-finops
source_filename: aruba-finops.yml
source_heading: FinOps Profile
source_url: https://www.arubanetworks.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Aruba\nproviderId: aruba\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Network Management\n  - Networking\n  - SD-WAN\n  - Security\n  - Wireless\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for HPE Aruba Networking APIs — APIs are bundled with subscription\n  licenses (Aruba Central Foundation/Advanced, ClearPass), perpetual hardware purchases (AOS-CX, EdgeConnect),\n  and support contracts. There is no per-API metered billing line.\nsources:\n  - https://www.arubanetworks.com/\n  - https://www.hpe.com/us/en/aruba-networking.html\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: APIs are not separately metered or invoiced. Cost is allocated via the parent device/subscription\n  SKU. Treat the meters below as proxies for activity tracking rather than billing inputs.\nalignedWith:\n  framework: FinOps\
  \ Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Hewlett Packard Enterprise (HPE Aruba Networking)\nserviceCategory: Networking\nbillingModel:\n  pricingCategory: Subscription + Perpetual License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: HPE Aruba Networking\n  ServiceCategory: Networking\n  ServiceSubcategory: Network Management & Security\n  ProviderName: HPE Aruba Networking\n  PublisherName: Hewlett Packard Enterprise\n  InvoiceIssuerName: Hewlett Packard Enterprise\n  BillingCurrency: USD\n  PricingCategory: Subscription + Perpetual License\n  ChargeCategory: Purchase\nmeters:\n  - name: aruba_central_subscription\n    description: Aruba Central Foundation/Advanced/Premium device-month subscription\n    unit: device-month\n\
  \    aggregation: max\n    dimensions:\n      - tier\n      - device_type\n      - region\n  - name: clearpass_license\n    description: ClearPass policy manager licenses (endpoint counts)\n    unit: endpoint\n    aggregation: max\n    dimensions:\n      - product\n      - region\n  - name: edgeconnect_subscription\n    description: EdgeConnect SD-WAN appliance/site subscription\n    unit: site-month\n    aggregation: max\n    dimensions:\n      - bandwidth_tier\n      - region\n  - name: api_calls\n    description: API call activity — not separately billed; tracked for capacity planning only\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\n      - cluster\nprinciples:\n  - name: Visibility\n    description: Use HPE GreenLake / Aruba Central usage reports and the per-product invoice line items\n      from HPE to surface the underlying device/subscription costs that fund API access.\n  - name: Allocation\n    description: Allocate Aruba spend by site, business\
  \ unit, and device group using Aruba Central labels\n      and HPE GreenLake tagging; APIs themselves carry no separate cost line.\n  - name: Optimization\n    description: Right-size Central tiers (Foundation vs Advanced), retire shelfware ClearPass endpoint\n      licenses, and consolidate AirWave instances. API access does not drive cost — device counts and\n      subscription tiers do.\n  - name: Accountability\n    description: Network architects and IT ops own Aruba spend; review device subscriptions quarterly\n      against actual deployed counts in Central inventory.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aruba/refs/heads/main/finops/aruba-finops.yml
sources:
- https://www.arubanetworks.com/
- https://www.hpe.com/us/en/aruba-networking.html
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Network Management
- Networking
- SD-WAN
- Security
- Wireless
- FinOps
- FOCUS
---
