---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: apple-keynote-icloud-openapi.yaml
  format: yaml
  label: Keynote iCloud API
  slug: keynote-icloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apple-keynote/refs/heads/main/openapi/apple-keynote-icloud-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  pricingCategory: Subscription (Storage Tier)
description: 'FOCUS-aligned FinOps view for Apple Keynote: the Keynote app itself is free; the only direct charge associated with Keynote workflows is the iCloud+ storage tier that holds the .key files. Allocation should track per-user iCloud+ tier cost and (where applicable) Apple Business Manager / Apple Education device-bundled licensing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Apple Inc.
  PricingCategory: Subscription
  ProviderName: Apple
  PublisherName: Apple Inc.
  ServiceCategory: Productivity / Presentations
  ServiceName: Apple Keynote / iCloud+
layout: finops
meters:
- aggregation: sum
  description: Per-user monthly iCloud+ storage tier covering Keynote document sync (50GB / 200GB / 2TB / 6TB / 12TB)
  dimensions:
  - tier
  - apple_id
  name: icloud_plus_subscription
  unit: month
- aggregation: max
  description: Actual iCloud storage consumed by Keynote documents (telemetry, not directly billed)
  dimensions:
  - apple_id
  - app
  name: icloud_storage_used
  unit: GB
- aggregation: max
  description: Count of Keynote documents stored in iCloud Drive (for chargeback)
  dimensions:
  - apple_id
  name: keynote_documents
  unit: document
name: Apple Keynote Finops
provider_name: Apple Keynote
provider_slug: apple-keynote
publisher_name: Apple Inc.
service_category: Productivity / Presentations
slug: apple-keynote-finops
source_filename: apple-keynote-finops.yml
source_heading: FinOps Profile
source_url: https://www.apple.com/keynote/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Apple Keynote\nproviderId: apple-keynote\npublisherName: Apple Inc.\nserviceCategory: Productivity / Presentations\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Apple\n  - iWork\n  - iCloud\ndescription: 'FOCUS-aligned FinOps view for Apple Keynote: the Keynote app itself is free; the only direct\n  charge associated with Keynote workflows is the iCloud+ storage tier that holds the .key files. Allocation\n  should track per-user iCloud+ tier cost and (where applicable) Apple Business Manager / Apple Education\n  device-bundled licensing.'\nsources:\n  - https://www.apple.com/keynote/\n  - https://www.apple.com/icloud/\n\
  billingModel:\n  pricingCategory: Subscription (Storage Tier)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\nfocusColumns:\n  ServiceName: Apple Keynote / iCloud+\n  ServiceCategory: Productivity / Presentations\n  ProviderName: Apple\n  PublisherName: Apple Inc.\n  InvoiceIssuerName: Apple Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\nmeters:\n  - name: icloud_plus_subscription\n    description: Per-user monthly iCloud+ storage tier covering Keynote document sync (50GB / 200GB /\n      2TB / 6TB / 12TB)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - apple_id\n  - name: icloud_storage_used\n    description: Actual iCloud storage consumed by Keynote documents (telemetry, not directly billed)\n    unit: GB\n    aggregation: max\n    dimensions:\n      - apple_id\n      - app\n  - name: keynote_documents\n    description: Count of Keynote documents stored in\
  \ iCloud Drive (for chargeback)\n    unit: document\n    aggregation: max\n    dimensions:\n      - apple_id\nprinciples:\n  - name: Visibility\n    description: Use Apple Business Manager (where managed) or per-user Apple ID storage views to track\n      iCloud+ tier and storage utilization.\n  - name: Allocation\n    description: Allocate iCloud+ subscription cost per managed Apple ID; tag by department or cost center\n      via Apple Business Manager metadata.\n  - name: Optimization\n    description: Right-size iCloud+ tier per user; consolidate via Family Sharing where licensing permits;\n      archive large legacy .key files locally.\n  - name: Accountability\n    description: IT / Workplace team owns the Apple Business Manager contract and per-seat iCloud+ assignment;\n      individual users accountable for keeping storage within tier.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apple-keynote/refs/heads/main/finops/apple-keynote-finops.yml
sources:
- https://www.apple.com/keynote/
- https://www.apple.com/icloud/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Apple
- iWork
- iCloud
---
