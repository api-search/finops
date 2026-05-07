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
  pricingCategory: Bilateral Contract
description: AutoZone does not publish a public API or developer pricing. There is no FinOps surface to align with; commercial integrations are billed at the parts-purchase level via the customer's AutoZone Commercial account.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: AutoZone, Inc.
  ProviderName: AutoZone
  PublisherName: AutoZone, Inc.
  ServiceCategory: Automotive Parts Retail
  ServiceName: AutoZone
layout: finops
meters:
- aggregation: count
  dimensions:
  - account
  - location
  name: parts_orders
  unit: order
- aggregation: sum
  name: parts_lines
  unit: line
name: Autozone Finops
provider_name: AutoZone
provider_slug: autozone
publisher_name: AutoZone, Inc.
service_category: Automotive Parts Retail
slug: autozone-finops
source_filename: autozone-finops.yml
source_heading: FinOps Profile
source_url: https://www.autozone.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AutoZone\nproviderId: autozone\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: AutoZone has no public API and no published developer pricing. This artifact captures the\n  absence of a public FinOps surface.\ntags:\n  - FinOps\n  - FOCUS\n  - Automotive Parts\n  - Retail\ndescription: AutoZone does not publish a public API or developer pricing. There is no FinOps surface\n  to align with; commercial integrations are billed at the parts-purchase level via the customer's\n  AutoZone Commercial account.\nsources:\n  - https://www.autozone.com/\n  - https://www.autozonepro.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: AutoZone, Inc.\nserviceCategory:\
  \ Automotive Parts Retail\nbillingModel:\n  pricingCategory: Bilateral Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: AutoZone\n  ServiceCategory: Automotive Parts Retail\n  ProviderName: AutoZone\n  PublisherName: AutoZone, Inc.\n  InvoiceIssuerName: AutoZone, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: parts_orders\n    unit: order\n    aggregation: count\n    dimensions:\n      - account\n      - location\n  - name: parts_lines\n    unit: line\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: There is no public AutoZone API for usage telemetry. Reporting is via AutoZonePro\n      account statements.\n  - name: Allocation\n    description: Allocate by AutoZone Commercial account number / shop location.\n  - name: Optimization\n    description: Optimize via commercial-account terms negotiated with AutoZone Commercial sales.\n  - name: Accountability\n    description: Owned\
  \ by the procurement / shop-operations team that holds the AutoZone Commercial\n      account.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/autozone/refs/heads/main/finops/autozone-finops.yml
sources:
- https://www.autozone.com/
- https://www.autozonepro.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Automotive Parts
- Retail
---
