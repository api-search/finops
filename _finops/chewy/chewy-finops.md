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
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Chewy vendor integration: Chewy itself does not bill suppliers per API call. Cost shape is the Dsco / CommerceHub platform subscription plus normal trading-partner economics (drop-ship fees, returns, chargebacks) — not metered API usage.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: CommerceHub (Dsco platform)
  PricingCategory: Subscription
  ProviderName: Chewy
  PublisherName: Chewy, Inc.
  ServiceCategory: E-Commerce / EDI
  ServiceName: Chewy Vendor Integration (Dsco)
layout: finops
meters:
- aggregation: sum
  description: Monthly Dsco supplier-platform subscription line
  dimensions:
  - tier
  - supplier_id
  name: dsco_subscription
  unit: month
- aggregation: sum
  description: Volume of EDI documents (850, 846, 856, 810) exchanged through the Dsco connector
  dimensions:
  - document_type
  - retailer
  name: edi_transactions
  unit: transaction
- aggregation: sum
  description: Trading-partner chargebacks issued by Chewy for compliance violations
  dimensions:
  - reason
  - po_number
  name: chargebacks
  unit: event
name: Chewy Finops
provider_name: Chewy
provider_slug: chewy
publisher_name: Chewy, Inc.
service_category: E-Commerce / Vendor Integration
slug: chewy-finops
source_filename: chewy-finops.yml
source_heading: FinOps Profile
source_url: https://www.chewy.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Chewy\nproviderId: chewy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Dsco\n  - E-Commerce\n  - EDI\n  - Pet Retail\n  - Vendor Integration\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Chewy vendor integration: Chewy itself does not bill suppliers\n  per API call. Cost shape is the Dsco / CommerceHub platform subscription plus normal trading-partner\n  economics (drop-ship fees, returns, chargebacks) — not metered API usage.'\nnotes: Chewy does not publish a usage-based billing surface for its APIs. The FinOps shape below\n  reflects the Dsco supplier subscription cost.\nsources:\n  - https://www.chewy.com/\n  - https://www.dsco.io/\n  - https://www.commercehub.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Chewy, Inc.\nserviceCategory: E-Commerce / Vendor Integration\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Chewy Vendor Integration (Dsco)\n  ServiceCategory: E-Commerce / EDI\n  ProviderName: Chewy\n  PublisherName: Chewy, Inc.\n  InvoiceIssuerName: CommerceHub (Dsco platform)\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\nmeters:\n  - name: dsco_subscription\n    description: Monthly Dsco supplier-platform subscription line\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - supplier_id\n  - name: edi_transactions\n    description: Volume of EDI documents (850, 846, 856, 810) exchanged through the Dsco connector\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - document_type\n\
  \      - retailer\n  - name: chargebacks\n    description: Trading-partner chargebacks issued by Chewy for compliance violations\n    unit: event\n    aggregation: sum\n    dimensions:\n      - reason\n      - po_number\nprinciples:\n  - name: Visibility\n    description: Track Dsco subscription invoices, EDI transaction counts in the Dsco portal, and\n      Chewy chargeback statements as the three cost surfaces for the integration.\n  - name: Allocation\n    description: Tag Dsco connector cost to the channel (Chewy) and to the brand / SKU family that\n      drives the volume so e-commerce ops can see channel margin.\n  - name: Optimization\n    description: Reduce chargebacks by tightening ASN accuracy and inventory feed cadence; size the\n      Dsco tier to actual document volume rather than negotiated peaks.\n  - name: Accountability\n    description: E-commerce / channel operations owns the Chewy P&L; supply chain owns ASN compliance;\n      finance reconciles Dsco invoices and Chewy\
  \ chargeback settlements.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chewy/refs/heads/main/finops/chewy-finops.yml
sources:
- https://www.chewy.com/
- https://www.dsco.io/
- https://www.commercehub.com/
specification: FinOps Framework
tags:
- Dsco
- E-Commerce
- EDI
- Pet Retail
- Vendor Integration
- FinOps
- FOCUS
---
