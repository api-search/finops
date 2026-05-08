---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Shipment / Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Carrier Tariff (No Direct API Pricing)
description: 'FOCUS-aligned FinOps placeholder for Saia: API access is bundled with the underlying carrier relationship rather than priced per call. The financial unit of consumption is the freight shipment, not the API request.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Saia, Inc.
  ProviderName: Saia Inc
  PublisherName: Saia, Inc.
  ServiceCategory: Freight / LTL Carrier
  ServiceName: Saia
layout: finops
meters:
- aggregation: sum
  dimensions:
  - origin
  - destination
  - service_level
  name: shipments
  unit: shipment
- aggregation: sum
  dimensions:
  - api_family
  name: api_calls
  unit: request
name: Saia Finops
provider_name: Saia Inc
provider_slug: saia
publisher_name: Saia, Inc.
service_category: Freight / LTL Carrier
slug: saia-finops
source_filename: saia-finops.yml
source_heading: FinOps Profile
source_url: https://www.saia.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Saia Inc\nproviderId: saia\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Freight\n  - LTL\n  - B2B\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Saia: API access is bundled with the underlying carrier\n  relationship rather than priced per call. The financial unit of consumption is the freight shipment,\n  not the API request.'\nsources:\n  - https://www.saia.com/\nnotes: Saia does not publish per-call API prices. Cost optimization for Saia consumers is dominated by\n  shipment-level economics (rating accuracy, tracking-driven OTIF, document automation), not API metering.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Saia, Inc.\nserviceCategory: Freight / LTL Carrier\nbillingModel:\n  pricingCategory: Carrier Tariff (No Direct API Pricing)\n  billingFrequency: Per-Shipment / Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Saia\n  ServiceCategory: Freight / LTL Carrier\n  ProviderName: Saia Inc\n  PublisherName: Saia, Inc.\n  InvoiceIssuerName: Saia, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: shipments\n    unit: shipment\n    aggregation: sum\n    dimensions:\n      - origin\n      - destination\n      - service_level\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_family\nprinciples:\n  - name: Visibility\n    description: Visibility is shipment-centric — pull data from Saia's invoicing, EDI 210 freight invoice\n      feeds, and tracking API to reconcile expected vs actual freight charges.\n  - name: Allocation\n    description: Allocate by shipping origin, business unit, and SKU / order so\
  \ freight cost can be attributed\n      to the customer or product driving it.\n  - name: Optimization\n    description: Optimize lane selection, consolidation, and accessorial avoidance via accurate rating\n      API use; reduce reweigh / reclass exposure with better dimensioning data.\n  - name: Accountability\n    description: Logistics ops owns carrier reconciliation. Exception management and dispute filing should\n      be tied to specific PRO numbers via the documents API.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/saia/refs/heads/main/finops/saia-finops.yml
sources:
- https://www.saia.com/
specification: FinOps Framework
tags:
- Freight
- LTL
- B2B
- FinOps
- FOCUS
---
