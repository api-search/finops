---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Varies
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Varies by Vendor
description: RFID is a multi-vendor technology category, not a single billable service. FinOps treatment must be applied per underlying vendor. This artifact carries a placeholder shape.
focus_columns:
  BillingCurrency: USD
  ProviderName: Multiple Vendors
  PublisherName: Multiple Vendors
  ServiceCategory: IoT / RFID
  ServiceName: RFID (multi-vendor)
layout: finops
meters:
- aggregation: sum
  description: Aggregate of vendor-specific RFID service charges
  dimensions:
  - vendor
  - product
  name: vendor_charges
  unit: varies
name: Rfid Finops
provider_name: RFID
provider_slug: rfid
publisher_name: Multiple Vendors
service_category: IoT / RFID
slug: rfid-finops
source_filename: rfid-finops.yml
source_heading: FinOps Profile
source_url: https://www.zebra.com/us/en/services/data-services.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: RFID\nproviderId: rfid\npublisherName: Multiple Vendors\nserviceCategory: IoT / RFID\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - RFID\n  - IoT\n  - FinOps\n  - FOCUS\ndescription: >-\n  RFID is a multi-vendor technology category, not a single billable service. FinOps treatment\n  must be applied per underlying vendor. This artifact carries a placeholder shape.\nnotes: >-\n  No unified billing model exists across the RFID ecosystem. Allocate cost per underlying\n  vendor invoice (Zebra, Impinj, GS1, ClearStream, etc.).\nsources:\n  - https://www.zebra.com/us/en/services/data-services.html\n  - https://www.impinj.com/products/platform/itemsense\n\
  billingModel:\n  pricingCategory: Varies by Vendor\n  billingFrequency: Varies\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: RFID (multi-vendor)\n  ServiceCategory: IoT / RFID\n  ProviderName: Multiple Vendors\n  PublisherName: Multiple Vendors\n  BillingCurrency: USD\nmeters:\n  - name: vendor_charges\n    description: Aggregate of vendor-specific RFID service charges\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - vendor\n      - product\nprinciples:\n  - name: Visibility\n    description: >-\n      Consolidate RFID vendor invoices into a single line of sight per program (Zebra, Impinj,\n      GS1, ClearStream).\n  - name: Allocation\n    description: >-\n      Tag RFID hardware and API spend to the originating warehouse, store, or supply-chain lane\n      rather than to a generic IT bucket.\n  - name: Optimization\n    description: >-\n      Negotiate volume discounts per vendor; consolidate readers and tag\
  \ SKUs to reduce\n      vendor sprawl.\n  - name: Accountability\n    description: >-\n      Assign supply-chain or operations owners to each RFID vendor relationship; review tag\n      and reader unit economics quarterly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rfid/refs/heads/main/finops/rfid-finops.yml
sources:
- https://www.zebra.com/us/en/services/data-services.html
- https://www.impinj.com/products/platform/itemsense
specification: FinOps Framework
tags:
- RFID
- IoT
- FinOps
- FOCUS
---
