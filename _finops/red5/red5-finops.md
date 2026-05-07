---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: red5-server-api-openapi.yml
  format: yaml
  label: Red5 Pro Server API
  slug: server-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/openapi/red5-server-api-openapi.yml
- filename: red5-stream-manager-2-openapi.yml
  format: yaml
  label: Red5 Pro Stream Manager 2.0 API
  slug: stream-manager-2-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/openapi/red5-stream-manager-2-openapi.yml
- filename: red5-brew-mixer-api-openapi.yml
  format: yaml
  label: Red5 Pro Brew Mixer API
  slug: brew-mixer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/openapi/red5-brew-mixer-api-openapi.yml
- filename: red5-restreamer-api-openapi.yml
  format: yaml
  label: Red5 Pro Restreamer API
  slug: restreamer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/openapi/red5-restreamer-api-openapi.yml
- filename: red5-webrtc-streaming-asyncapi.yml
  format: yaml
  label: Red5 Pro WebRTC SDK
  slug: webrtc-sdk
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/asyncapi/red5-webrtc-streaming-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps shape for Red5 Pro. Two cost surfaces — the Red5 Pro license (subscription, contact-sales) and the customer's underlying cloud spend running the media server. Public pricing page was unavailable for automated fetch.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Infrared5, Inc.
  ProviderName: Red5
  PublisherName: Infrared5, Inc.
  ServiceCategory: Streaming Media
  ServiceName: Red5 Pro
layout: finops
meters:
- aggregation: sum
  description: Annual Red5 Pro license (sized by concurrent streams or node count)
  dimensions:
  - edition
  - concurrent_streams
  - support_level
  name: license_subscription
  unit: contract
name: Red5 Finops
provider_name: Red5
provider_slug: red5
publisher_name: Infrared5, Inc.
service_category: Streaming Media
slug: red5-finops
source_filename: red5-finops.yml
source_heading: FinOps Profile
source_url: https://www.red5.net/red5pro/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red5\nproviderId: red5\npublisherName: Infrared5, Inc.\nserviceCategory: Streaming Media\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Streaming\n  - Real-Time Video\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Red5 Pro. Two cost surfaces — the Red5 Pro license\n  (subscription, contact-sales) and the customer's underlying cloud spend running the media\n  server. Public pricing page was unavailable for automated fetch.\nsources:\n  - https://www.red5.net/red5pro/pricing/\nnotes: Red5 site returned 403 to automated fetch; meter list reflects the assumed license +\n  customer-cloud cost shape,\
  \ not a fetched billing surface.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Red5 Pro\n  ServiceCategory: Streaming Media\n  ProviderName: Red5\n  PublisherName: Infrared5, Inc.\n  InvoiceIssuerName: Infrared5, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: license_subscription\n    description: Annual Red5 Pro license (sized by concurrent streams or node count)\n    unit: contract\n    aggregation: sum\n    dimensions:\n      - edition\n      - concurrent_streams\n      - support_level\nprinciples:\n  - name: Visibility\n    description: Red5 Pro Stream Manager exposes per-stream and per-node telemetry; combine\n      with the underlying cloud bill (AWS / Azure / GCP) to see total cost-of-streaming.\n  - name: Allocation\n    description: Tag streams and nodes by application/tenant in Stream Manager so the licensed\n      capacity and the cloud spend can be attributed\
  \ to consuming products.\n  - name: Optimization\n    description: Right-size autoscaling pools, use spot/preemptible instances for non-critical\n      edges, and renegotiate Red5 license tier at renewal based on observed peak concurrency.\n  - name: Accountability\n    description: Streaming platform team owns Red5 license + cluster cost; consuming product\n      teams own their concurrency profile.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/finops/red5-finops.yml
sources:
- https://www.red5.net/red5pro/pricing/
specification: FinOps Framework
tags:
- Streaming
- Real-Time Video
- FinOps
- FOCUS
---
