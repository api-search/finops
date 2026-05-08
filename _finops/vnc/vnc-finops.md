---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: vnc-cloud-openapi.yml
  format: yaml
  label: VNC Cloud API
  slug: vnc-cloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vnc/refs/heads/main/openapi/vnc-cloud-openapi.yml
billing_model:
  billingCurrency: GBP
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps view of RealVNC Connect - tiered per-active- connection annual subscription with no usage-based metering. Cost levers are tier selection (Essentials / Plus / Premium / Enterprise) and active-connection count.
focus_columns:
  BillingCurrency: GBP
  ChargeCategory: Purchase
  InvoiceIssuerName: RealVNC Limited
  ProviderName: RealVNC
  PublisherName: RealVNC Limited
  ServiceCategory: Remote Access / Remote Desktop
  ServiceName: VNC Connect
layout: finops
meters:
- aggregation: max
  description: Active concurrent VNC Connect connections licensed under the subscription, billed annually per seat.
  dimensions:
  - tier
  - region
  name: active_connection_seats
  unit: seat
- aggregation: max
  description: Devices enrolled into the RealVNC managed estate; capped per tier (3 / 50 / 150 / unlimited).
  dimensions:
  - tier
  name: managed_devices
  unit: device
name: Vnc Finops
provider_name: VNC
provider_slug: vnc
publisher_name: RealVNC Limited
service_category: Remote Access / Remote Desktop
slug: vnc-finops
source_filename: vnc-finops.yml
source_heading: FinOps Profile
source_url: https://www.realvnc.com/en/connect/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: VNC\nproviderId: vnc\npublisherName: RealVNC Limited\nserviceCategory: Remote Access / Remote Desktop\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Remote Access\n  - Remote Desktop\n  - FinOps\n  - FOCUS\n  - Subscription\ndescription: FOCUS-aligned FinOps view of RealVNC Connect - tiered per-active-\n  connection annual subscription with no usage-based metering. Cost levers are\n  tier selection (Essentials / Plus / Premium / Enterprise) and active-connection\n  count.\nsources:\n  - https://www.realvnc.com/en/connect/pricing/\n  - https://www.realvnc.com/en/developer/\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency:\
  \ GBP\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: VNC Connect\n  ServiceCategory: Remote Access / Remote Desktop\n  ProviderName: RealVNC\n  PublisherName: RealVNC Limited\n  InvoiceIssuerName: RealVNC Limited\n  BillingCurrency: GBP\n  ChargeCategory: Purchase\nmeters:\n  - name: active_connection_seats\n    description: Active concurrent VNC Connect connections licensed under the\n      subscription, billed annually per seat.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tier\n      - region\n  - name: managed_devices\n    description: Devices enrolled into the RealVNC managed estate; capped per\n      tier (3 / 50 / 150 / unlimited).\n    unit: device\n    aggregation: max\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Use the RealVNC management console to track active-connection\n      utilization vs licensed seats and the device inventory against the tier\n      cap; cross-check\
  \ against the annual RealVNC invoice.\n  - name: Allocation\n    description: Allocate Connect spend per supported team or product line by\n      tagging devices in the management console; chargeback by enrolled-device\n      count or by named-user assignment.\n  - name: Optimization\n    description: Reclaim idle active-connection seats, downgrade tier when\n      session-recording / audit-log features are unused, and consolidate\n      device enrollments to stay below the next-tier breakpoint.\n  - name: Accountability\n    description: IT or workplace-services owns the RealVNC contract; per-team\n      device counts and seat consumption are reviewed against the licensed\n      tier on a quarterly basis.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vnc/refs/heads/main/finops/vnc-finops.yml
sources:
- https://www.realvnc.com/en/connect/pricing/
- https://www.realvnc.com/en/developer/
specification: FinOps Framework
tags:
- Remote Access
- Remote Desktop
- FinOps
- FOCUS
- Subscription
---
