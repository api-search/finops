---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ptc-thingworx-rest-openapi.yml
  format: yaml
  label: PTC ThingWorx REST API
  slug: thingworx-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ptc-thingworx/refs/heads/main/openapi/ptc-thingworx-rest-openapi.yml
- filename: ptc-thingworx-websocket-asyncapi.yml
  format: yaml
  label: PTC ThingWorx WebSocket/AlwaysOn API
  slug: thingworx-websocket-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/ptc-thingworx/refs/heads/main/asyncapi/ptc-thingworx-websocket-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps shape for PTC ThingWorx — quote-based enterprise IoT platform license, not a metered API consumption surface.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: PTC Inc.
  ProviderName: PTC
  PublisherName: PTC Inc.
  ServiceCategory: Industrial IoT Platform
  ServiceName: ThingWorx
layout: finops
meters:
- aggregation: sum
  name: platform_subscription
  unit: month
- aggregation: max
  name: connected_assets
  unit: asset
name: Ptc Thingworx Finops
provider_name: ptc-thingworx
provider_slug: ptc-thingworx
publisher_name: PTC Inc.
service_category: Industrial IoT Platform
slug: ptc-thingworx-finops
source_filename: ptc-thingworx-finops.yml
source_heading: FinOps Profile
source_url: https://www.ptc.com/en/products/thingworx
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ptc-thingworx\nproviderId: ptc-thingworx\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - IoT\n  - Industrial\n  - Manufacturing\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for PTC ThingWorx — quote-based enterprise IoT platform license,\n  not a metered API consumption surface.\nnotes: ThingWorx is licensed by deployment and connected-asset count under a contract; there is no public\n  consumption-billing API.\nsources:\n  - https://www.ptc.com/en/products/thingworx\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: PTC Inc.\nserviceCategory: Industrial IoT Platform\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency:\
  \ Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: ThingWorx\n  ServiceCategory: Industrial IoT Platform\n  ProviderName: PTC\n  PublisherName: PTC Inc.\n  InvoiceIssuerName: PTC Inc.\n  BillingCurrency: USD\nmeters:\n  - name: platform_subscription\n    unit: month\n    aggregation: sum\n  - name: connected_assets\n    unit: asset\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Cost visibility flows from the PTC subscription invoice plus the customer's own platform-sizing\n      and connected-asset telemetry inside ThingWorx.\n  - name: Allocation\n    description: Allocate by line of business, plant / site, and asset family using ThingWorx's own modeling\n      surface.\n  - name: Optimization\n    description: Right-size the deployment (CPU / memory / persistence provider), retire stale assets,\n      and renegotiate the licensed asset count at renewal.\n  - name: Accountability\n    description: Spend is owned\
  \ by the OT / digital-thread / smart-manufacturing program that signs\n      the master license agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ptc-thingworx/refs/heads/main/finops/ptc-thingworx-finops.yml
sources:
- https://www.ptc.com/en/products/thingworx
specification: FinOps Framework
tags:
- IoT
- Industrial
- Manufacturing
- FinOps
- FOCUS
---
