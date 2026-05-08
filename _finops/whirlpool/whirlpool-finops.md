---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Partner-Negotiated
description: FinOps shape for Whirlpool's connected-appliance APIs is partner-driven rather than billed per-call. There is no public price list; integrations live inside ecosystem partner relationships, so meters and FOCUS columns are minimum placeholders.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Whirlpool Corporation
  ProviderName: Whirlpool Corporation
  PublisherName: Whirlpool Corporation
  ServiceCategory: Connected Appliances
  ServiceName: Whirlpool Connected Appliances
layout: finops
meters:
- aggregation: sum
  dimensions:
  - partner_program
  - device_class
  name: partner_integration
  unit: varies
name: Whirlpool Finops
provider_name: Whirlpool Corporation
provider_slug: whirlpool
publisher_name: Whirlpool Corporation
service_category: Connected Appliances
slug: whirlpool-finops
source_filename: whirlpool-finops.yml
source_heading: FinOps Profile
source_url: https://www.whirlpoolcorp.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Whirlpool Corporation\nproviderId: whirlpool\npublisherName: Whirlpool Corporation\nserviceCategory: Connected Appliances\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Appliances\n  - Smart Home\n  - IoT\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps shape for Whirlpool's connected-appliance APIs is partner-driven rather than billed per-call. There is no public price list; integrations live inside ecosystem partner relationships, so meters and FOCUS columns are minimum placeholders.\nsources:\n  - https://www.whirlpoolcorp.com\nnotes: No public pricing or billing surface. Populate meters and FOCUS columns\
  \ from an actual partner integration agreement when one exists.\nbillingModel:\n  pricingCategory: Partner-Negotiated\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Whirlpool Connected Appliances\n  ServiceCategory: Connected Appliances\n  ProviderName: Whirlpool Corporation\n  PublisherName: Whirlpool Corporation\n  InvoiceIssuerName: Whirlpool Corporation\n  BillingCurrency: USD\nmeters:\n  - name: partner_integration\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - partner_program\n      - device_class\nprinciples:\n  - name: Visibility\n    description: Telemetry comes from each ecosystem partner's own usage / device-event reporting (Alexa skill metrics, Dash Replenishment reports, etc.) - not a Whirlpool billing API.\n  - name: Allocation\n    description: Allocate by partner program (Alexa, Google, Dash) and device class (washer, dryer, oven, refrigerator).\n  - name: Optimization\n\
  \    description: Optimization is event-shape - reduce unnecessary device polling and consolidate webhooks per partner spec.\n  - name: Accountability\n    description: Owned by the integrating ecosystem team (smart-home / consumer-IoT product owner); finance has no separate API line item.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/whirlpool/refs/heads/main/finops/whirlpool-finops.yml
sources:
- https://www.whirlpoolcorp.com
specification: FinOps Framework
tags:
- Appliances
- Smart Home
- IoT
- FinOps
- FOCUS
- Contact Sales
---
