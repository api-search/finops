---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Order
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Sales Quote / Contract
description: AK Steel Holding was acquired by Cleveland-Cliffs in March 2020 and no longer operates as an independent entity. Cost surface for any historical AK Steel relationships is steel product invoiced by Cleveland-Cliffs (tonnage × grade × delivery), not API consumption.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Cleveland-Cliffs Inc.
  ProviderName: AK Steel Holding
  PublisherName: Cleveland-Cliffs Inc.
  ServiceCategory: Steel / Manufacturing
  ServiceName: AK Steel Products (now Cleveland-Cliffs)
layout: finops
meters:
- aggregation: sum
  description: Steel ordered, by grade and product family
  dimensions:
  - grade
  - product_family
  - mill
  name: steel_tonnage
  unit: ton
- aggregation: sum
  description: Freight, handling, and surcharge fees
  dimensions:
  - mode
  - destination
  name: delivery_charges
  unit: shipment
name: Ak Steel Holding Finops
provider_name: AK Steel Holding
provider_slug: ak-steel-holding
publisher_name: Cleveland-Cliffs Inc. (successor to AK Steel Holding)
service_category: Steel / Manufacturing
slug: ak-steel-holding-finops
source_filename: ak-steel-holding-finops.yml
source_heading: FinOps Profile
source_url: https://www.clevelandcliffs.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AK Steel Holding\nproviderId: ak-steel-holding\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cleveland-Cliffs Inc. (successor to AK Steel Holding)\nserviceCategory: Steel / Manufacturing\ntags:\n  - Steel\n  - Manufacturing\n  - Metals\n  - FinOps\n  - FOCUS\ndescription: AK Steel Holding was acquired by Cleveland-Cliffs in March 2020 and no longer operates as\n  an independent entity. Cost surface for any historical AK Steel relationships is steel product\n  invoiced by Cleveland-Cliffs (tonnage × grade × delivery), not API consumption.\nnotes: Defunct entity; meters reflect the steel-product commerce model the\
  \ successor (Cleveland-Cliffs)\n  uses.\nsources:\n  - https://www.clevelandcliffs.com/\nbillingModel:\n  pricingCategory: Sales Quote / Contract\n  billingFrequency: Per-Order\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: AK Steel Products (now Cleveland-Cliffs)\n  ServiceCategory: Steel / Manufacturing\n  ProviderName: AK Steel Holding\n  PublisherName: Cleveland-Cliffs Inc.\n  InvoiceIssuerName: Cleveland-Cliffs Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: steel_tonnage\n    description: Steel ordered, by grade and product family\n    unit: ton\n    aggregation: sum\n    dimensions:\n      - grade\n      - product_family\n      - mill\n  - name: delivery_charges\n    description: Freight, handling, and surcharge fees\n    unit: shipment\n    aggregation: sum\n    dimensions:\n      - mode\n      - destination\nprinciples:\n  - name: Visibility\n    description: Visibility comes\
  \ from purchase-order and invoice data issued by Cleveland-Cliffs;\n      AK Steel itself no longer reports independently.\n  - name: Allocation\n    description: Allocate steel cost by program, plant, and product family using the same purchase\n      order keys carried over from AK Steel relationships.\n  - name: Optimization\n    description: Optimize through grade rationalization, mill consolidation, and contract/term renegotiation\n      with Cleveland-Cliffs.\n  - name: Accountability\n    description: Procurement and operations jointly own the supplier relationship; align reviews with\n      Cleveland-Cliffs annual contract cycles.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ak-steel-holding/refs/heads/main/finops/ak-steel-holding-finops.yml
sources:
- https://www.clevelandcliffs.com/
specification: FinOps Framework
tags:
- Steel
- Manufacturing
- Metals
- FinOps
- FOCUS
---
