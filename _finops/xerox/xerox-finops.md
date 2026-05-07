---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: xerox-public-print-openapi.yml
  format: yaml
  label: Xerox Public Print API
  slug: xerox-public-print-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xerox/refs/heads/main/openapi/xerox-public-print-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription + Usage (click-charge)
description: FinOps shape for Xerox is opaque. The Xerox Developer Program APIs are bundled with Xerox device, MPS, and print-service contracts, not sold as a separate metered API. Spend is recorded against MPS contracts (typically click-charges for printed pages) rather than per-API-call meters.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Xerox Holdings Corporation
  ProviderName: Xerox
  PublisherName: Xerox Holdings Corporation
  ServiceCategory: Managed Print Services
  ServiceName: Xerox
layout: finops
meters:
- aggregation: sum
  dimensions:
  - device_model
  - contract
  name: device_subscription
  unit: device-month
- aggregation: sum
  dimensions:
  - device
  - color_mode
  - contract
  name: pages_printed
  unit: page
name: Xerox Finops
provider_name: Xerox
provider_slug: xerox
publisher_name: Xerox Holdings Corporation
service_category: Managed Print Services
slug: xerox-finops
source_filename: xerox-finops.yml
source_heading: FinOps Profile
source_url: https://www.xerox.com/en-us/services/managed-print-services
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Xerox\nproviderId: xerox\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Print Services\n  - Managed Print Services\n  - Document Management\ndescription: FinOps shape for Xerox is opaque. The Xerox Developer Program APIs are bundled with\n  Xerox device, MPS, and print-service contracts, not sold as a separate metered API. Spend is\n  recorded against MPS contracts (typically click-charges for printed pages) rather than\n  per-API-call meters.\nsources:\n  - https://www.xerox.com/en-us/services/managed-print-services\n  - https://publicprintapi.services.xerox.com/\nnotes: Xerox publishes no public API price list and no usage-billing API or FOCUS-aligned cost\n  export. Meters reflect the underlying print-services billing model (per page / per device)\n  rather than per-request API charges.\nalignedWith:\n  framework:\
  \ FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Xerox Holdings Corporation\nserviceCategory: Managed Print Services\nbillingModel:\n  pricingCategory: Subscription + Usage (click-charge)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Xerox\n  ServiceCategory: Managed Print Services\n  ProviderName: Xerox\n  PublisherName: Xerox Holdings Corporation\n  InvoiceIssuerName: Xerox Holdings Corporation\n  BillingCurrency: USD\nmeters:\n  - name: device_subscription\n    unit: device-month\n    aggregation: sum\n    dimensions:\n      - device_model\n      - contract\n  - name: pages_printed\n    unit: page\n    aggregation: sum\n    dimensions:\n      - device\n      - color_mode\n      - contract\nprinciples:\n  - name: Visibility\n    description:\
  \ Xerox MPS reporting (typically delivered through the customer's Xerox account\n      manager and the MPS portal) shows per-device click counts; there is no separate per-API\n      usage feed.\n  - name: Allocation\n    description: Costs allocate by device, location, and contract line; per-application\n      attribution requires capturing the calling appid in client-side telemetry.\n  - name: Optimization\n    description: Levers are device fleet right-sizing, color-vs-mono routing, ConnectKey\n      workflow consolidation, and renegotiating click-rates at renewal rather than API-side\n      tuning.\n  - name: Accountability\n    description: Print services contract is owned by IT / facilities procurement; integration\n      teams own the Developer Program appid and the printer-side workflows that drive volume.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/xerox/refs/heads/main/finops/xerox-finops.yml
sources:
- https://www.xerox.com/en-us/services/managed-print-services
- https://publicprintapi.services.xerox.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Print Services
- Managed Print Services
- Document Management
---
