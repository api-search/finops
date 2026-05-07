---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Not Applicable (Holding Company)
description: FOCUS-aligned FinOps placeholder for Fortune Brands Innovations. FBIN as a parent holding company does not invoice for API consumption directly; any developer-FinOps concerns map to the operating brands (Moen, Yale, Master Lock).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Fortune Brands Innovations, Inc. (or operating subsidiary)
  ProviderName: Fortune Brands Innovations, Inc.
  PublisherName: Fortune Brands Innovations, Inc.
  ServiceCategory: Home Products / Holding Company
  ServiceName: Fortune Brands Innovations
layout: finops
meters:
- aggregation: max
  description: Count of active partner agreements with FBIN brands (Moen, Yale, Master Lock, etc.)
  dimensions:
  - brand
  - partner
  name: brand_partner_agreements
  unit: agreement
name: Fortune Brands Innovations Finops
provider_name: Fortune Brands Innovations
provider_slug: fortune-brands-innovations
publisher_name: Fortune Brands Innovations, Inc.
service_category: Home Products / Holding Company
slug: fortune-brands-innovations-finops
source_filename: fortune-brands-innovations-finops.yml
source_heading: FinOps Profile
source_url: https://www.fbin.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Fortune Brands Innovations\nproviderId: fortune-brands-innovations\npublisherName: Fortune Brands Innovations, Inc.\nserviceCategory: Home Products / Holding Company\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Home Products\n  - Hardware\n  - Connected Home\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Fortune Brands Innovations. FBIN as a parent holding company does not invoice for API consumption directly; any developer-FinOps concerns map to the operating brands (Moen, Yale, Master Lock).\nnotes: Parent corporation has no API revenue. Meters and FOCUS columns are placeholder umbrellas;\
  \ real consumer agreements live at the brand level.\nsources:\n  - https://www.fbin.com/\nbillingModel:\n  pricingCategory: Not Applicable (Holding Company)\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Fortune Brands Innovations\n  ServiceCategory: Home Products / Holding Company\n  ProviderName: Fortune Brands Innovations, Inc.\n  PublisherName: Fortune Brands Innovations, Inc.\n  InvoiceIssuerName: Fortune Brands Innovations, Inc. (or operating subsidiary)\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: brand_partner_agreements\n    description: Count of active partner agreements with FBIN brands (Moen, Yale, Master Lock, etc.)\n    unit: agreement\n    aggregation: max\n    dimensions:\n      - brand\n      - partner\nprinciples:\n  - name: Visibility\n    description: Aggregate developer/API spend across FBIN brands by reviewing each brand's separate partner\
  \ agreement; FBIN does not publish a consolidated API spend view.\n  - name: Allocation\n    description: Allocate any brand-level API spend to the consuming product / division.\n  - name: Optimization\n    description: Negotiate cross-brand bundles where multiple FBIN brand APIs are consumed by a single partner.\n  - name: Accountability\n    description: Each FBIN brand owns its own developer-program economics; corporate procurement may aggregate sourcing.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fortune-brands-innovations/refs/heads/main/finops/fortune-brands-innovations-finops.yml
sources:
- https://www.fbin.com/
specification: FinOps Framework
tags:
- Home Products
- Hardware
- Connected Home
- FinOps
- FOCUS
---
