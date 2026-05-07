---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription (Cat Connect / VisionLink Bundled)
description: FOCUS-aligned FinOps scaffold for Caterpillar's Cat Digital Marketplace APIs. The dominant invoice line is the customer's Cat Connect / VisionLink subscription sold through the Cat Dealer network; API access is bundled within that. Meters track per-asset and per-API consumption to support internal allocation.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Caterpillar Cat Dealer
  ProviderName: Caterpillar
  PublisherName: Caterpillar Inc.
  ServiceCategory: Equipment Telematics
  ServiceName: Cat Digital Marketplace API
layout: finops
meters:
- aggregation: count
  dimensions:
  - product_family
  - subscription_class
  name: connected_assets
  unit: asset
- aggregation: sum
  dimensions:
  - api_product
  - subscription
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - api_product
  - asset
  name: telematics_records_delivered
  unit: record
- aggregation: count
  dimensions:
  - subscription_class
  name: subscription_seats
  unit: seat
name: Caterpillar Finops
provider_name: Caterpillar
provider_slug: caterpillar
publisher_name: Caterpillar Inc.
service_category: Equipment Telematics + Fleet Data
slug: caterpillar-finops
source_filename: caterpillar-finops.yml
source_heading: FinOps Profile
source_url: https://digital.cat.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Caterpillar\nproviderId: caterpillar\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Telematics\n  - Heavy Equipment\n  - Manufacturing\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps scaffold for Caterpillar''s Cat Digital Marketplace APIs. The dominant\n  invoice line is the customer''s Cat Connect / VisionLink subscription sold through the Cat Dealer\n  network; API access is bundled within that. Meters track per-asset and per-API consumption to support\n  internal allocation.'\nnotes: Most spend comes from the upstream Cat Connect / VisionLink subscription; API consumption is bundled.\n  Per-call invoicing not externally surfaced.\nsources:\n  - https://digital.cat.com/\n  - https://digital.cat.com/api-catalog-overview\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Caterpillar Inc.\nserviceCategory: Equipment Telematics + Fleet Data\nbillingModel:\n  pricingCategory: Subscription (Cat Connect / VisionLink Bundled)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Cat Digital Marketplace API\n  ServiceCategory: Equipment Telematics\n  ProviderName: Caterpillar\n  PublisherName: Caterpillar Inc.\n  InvoiceIssuerName: Caterpillar Cat Dealer\n  BillingCurrency: USD\nmeters:\n  - name: connected_assets\n    unit: asset\n    aggregation: count\n    dimensions:\n      - product_family\n      - subscription_class\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_product\n      - subscription\n  - name: telematics_records_delivered\n    unit: record\n    aggregation: sum\n    dimensions:\n\
  \      - api_product\n      - asset\n  - name: subscription_seats\n    unit: seat\n    aggregation: count\n    dimensions:\n      - subscription_class\nprinciples:\n  - name: Visibility\n    description: Combine Cat Digital portal usage reports with the Cat Connect / VisionLink customer dashboard\n      to see assets, subscription class, and API call volume in one view.\n  - name: Allocation\n    description: Allocate Cat Connect subscription cost to the operating unit / fleet that owns the assets;\n      attribute API integration cost to the consuming product team via subscription tag.\n  - name: Optimization\n    description: Right-size subscription class per asset (Essentials vs. Advanced); avoid polling APIs\n      faster than VisionLink's data-refresh cadence; consolidate dealer accounts to reach volume tiers.\n  - name: Accountability\n    description: Fleet manager owns the Cat Connect subscription cost; integration platform owner reconciles\n      API consumption against the negotiated\
  \ entitlement.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/caterpillar/refs/heads/main/finops/caterpillar-finops.yml
sources:
- https://digital.cat.com/
- https://digital.cat.com/api-catalog-overview
specification: FinOps Framework
tags:
- Telematics
- Heavy Equipment
- Manufacturing
- FinOps
- FOCUS
---
