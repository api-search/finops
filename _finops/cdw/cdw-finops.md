---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Order / Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Pass-Through Product Purchase (No API Fee)
description: FOCUS-aligned FinOps for CDW. CDW does not bill for API calls; the cost surface is the product purchases that flow through the Catalog / PunchOut / eProcurement integration. FinOps reporting rolls up product spend by buyer system, cost center, and category, and uses API telemetry only as a control-plane signal.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: CDW LLC
  ProviderName: CDW
  PublisherName: CDW LLC
  ServiceCategory: IT Distribution
  ServiceName: CDW Catalog / eProcurement
layout: finops
meters:
- aggregation: sum
  dimensions:
  - account
  - operation
  name: catalog_api_requests
  unit: request
- aggregation: count
  dimensions:
  - buyer_system
  - account
  name: punchout_sessions
  unit: session
- aggregation: count
  dimensions:
  - buyer_system
  - account
  name: purchase_orders_received
  unit: po
- aggregation: sum
  dimensions:
  - account
  - product_category
  - cost_center
  name: invoiced_amount
  unit: USD
- aggregation: count
  dimensions:
  - account
  name: invoices_issued
  unit: invoice
name: Cdw Finops
provider_name: CDW
provider_slug: cdw
publisher_name: CDW LLC
service_category: IT Distribution + eProcurement
slug: cdw-finops
source_filename: cdw-finops.yml
source_heading: FinOps Profile
source_url: https://www.cdw.com/content/cdw/en/services/eprocurement-and-custom-catalogs.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CDW\nproviderId: cdw\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - eProcurement\n  - IT Distribution\n  - Catalog\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for CDW. CDW does not bill for API calls; the cost surface is the\n  product purchases that flow through the Catalog / PunchOut / eProcurement integration. FinOps reporting\n  rolls up product spend by buyer system, cost center, and category, and uses API telemetry only as\n  a control-plane signal.'\nnotes: API itself is not billed; meters track product purchases and integration usage that drive the\n  product invoice.\nsources:\n  - https://www.cdw.com/content/cdw/en/services/eprocurement-and-custom-catalogs.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CDW LLC\nserviceCategory: IT Distribution + eProcurement\nbillingModel:\n  pricingCategory: Pass-Through Product Purchase (No API Fee)\n  billingFrequency: Per-Order / Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: CDW Catalog / eProcurement\n  ServiceCategory: IT Distribution\n  ProviderName: CDW\n  PublisherName: CDW LLC\n  InvoiceIssuerName: CDW LLC\n  BillingCurrency: USD\nmeters:\n  - name: catalog_api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - account\n      - operation\n  - name: punchout_sessions\n    unit: session\n    aggregation: count\n    dimensions:\n      - buyer_system\n      - account\n  - name: purchase_orders_received\n    unit: po\n    aggregation: count\n    dimensions:\n      - buyer_system\n      - account\n  - name: invoiced_amount\n    unit: USD\n    aggregation:\
  \ sum\n    dimensions:\n      - account\n      - product_category\n      - cost_center\n  - name: invoices_issued\n    unit: invoice\n    aggregation: count\n    dimensions:\n      - account\nprinciples:\n  - name: Visibility\n    description: Combine CDW invoice exports (cXML / EDI) with PunchOut session telemetry to see who\n      bought what, when, and through which buyer system.\n  - name: Allocation\n    description: Map cost centers to PunchOut sessions; carry that mapping into GL postings so CDW spend\n      is allocated at order time, not at month-end.\n  - name: Optimization\n    description: Use CDW custom catalogs to enforce approved configurations and avoid maverick spend;\n      consolidate vendors and renegotiate margins as volume grows; align order cadence to capture quarterly\n      programs.\n  - name: Accountability\n    description: Procurement owns CDW relationship spend; IT manages the integration health; finance\n      reconciles cXML invoices against PO data nightly.\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cdw/refs/heads/main/finops/cdw-finops.yml
sources:
- https://www.cdw.com/content/cdw/en/services/eprocurement-and-custom-catalogs.html
specification: FinOps Framework
tags:
- eProcurement
- IT Distribution
- Catalog
- FinOps
- FOCUS
---
