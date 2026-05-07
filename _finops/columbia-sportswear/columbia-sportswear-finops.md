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
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Wholesale / Purchase Order
description: 'FOCUS-aligned FinOps for Columbia Sportswear: no public API/SaaS surface — Columbia is a retailer, not a platform vendor. Meters below cover wholesale/partner data exchange invoice abstractions.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Columbia Sportswear Company
  ProviderName: Columbia Sportswear
  PublisherName: Columbia Sportswear Company
  ServiceCategory: Retail
  ServiceName: Columbia Sportswear
layout: finops
meters:
- aggregation: sum
  dimensions:
  - sku
  - season
  - region
  name: wholesale_units
  unit: unit
- aggregation: sum
  dimensions:
  - account
  - region
  name: order_value
  unit: USD
name: Columbia Sportswear Finops
provider_name: Columbia Sportswear
provider_slug: columbia-sportswear
publisher_name: Columbia Sportswear Company
service_category: Retail
slug: columbia-sportswear-finops
source_filename: columbia-sportswear-finops.yml
source_heading: FinOps Profile
source_url: https://www.columbia.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Columbia Sportswear\nproviderId: columbia-sportswear\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Retail\n  - Apparel\ndescription: 'FOCUS-aligned FinOps for Columbia Sportswear: no public API/SaaS surface — Columbia is a\n  retailer, not a platform vendor. Meters below cover wholesale/partner data exchange invoice abstractions.'\nsources:\n  - https://www.columbia.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Columbia Sportswear Company\nserviceCategory: Retail\nbillingModel:\n  pricingCategory: Wholesale / Purchase Order\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n\
  \    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Columbia Sportswear\n  ServiceCategory: Retail\n  ProviderName: Columbia Sportswear\n  PublisherName: Columbia Sportswear Company\n  InvoiceIssuerName: Columbia Sportswear Company\n  BillingCurrency: USD\nmeters:\n  - name: wholesale_units\n    unit: unit\n    aggregation: sum\n    dimensions:\n      - sku\n      - season\n      - region\n  - name: order_value\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - account\n      - region\nprinciples:\n  - name: Visibility\n    description: Reconcile Columbia invoices and EDI 810/856 documents against purchase orders and ASNs.\n  - name: Allocation\n    description: Tag wholesale POs to retail location, banner, or e-commerce channel.\n  - name: Optimization\n    description: Right-size seasonal buys; manage markdown reserves; coordinate freight terms with Columbia\n      logistics.\n  - name: Accountability\n    description: Merchandising owns buy quantities;\
  \ finance owns AP and reconciliation.\nnotes: No public API/SaaS pricing; this is a retail/wholesale relationship, not an API consumption relationship.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/columbia-sportswear/refs/heads/main/finops/columbia-sportswear-finops.yml
sources:
- https://www.columbia.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Retail
- Apparel
---
