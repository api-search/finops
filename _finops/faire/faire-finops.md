---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per Transaction
  chargeCategories:
  - Usage
  - Adjustment
  pricingCategory: Commission
description: FOCUS-aligned FinOps profile. Brands pay commission on order value; retailers do not pay subscription.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Faire
  ProviderName: Faire
  PublisherName: Faire
  ServiceCategory: Marketplace
  ServiceName: Faire
layout: finops
meters:
- aggregation: sum
  description: Commission on first orders from new retailers.
  dimensions:
  - brand
  - retailer
  name: first_order_commission
  unit: USD
- aggregation: sum
  description: Commission on retailer reorders.
  dimensions:
  - brand
  - retailer
  name: reorder_commission
  unit: USD
name: Faire Finops
provider_name: Faire
provider_slug: faire
publisher_name: Faire
service_category: Marketplace
slug: faire-finops
source_filename: faire-finops.yml
source_heading: FinOps Profile
source_url: https://www.faire.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Faire\nproviderId: faire\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Marketplace\n- Wholesale\n- Retail\n- Ecommerce\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Brands pay commission on order value; retailers do not pay\n  subscription.\nnotes: Commission-based model; cost dimension is GMV.\nsources:\n- https://www.faire.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Faire\nserviceCategory: Marketplace\nbillingModel:\n  pricingCategory: Commission\n  billingFrequency: Per Transaction\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Adjustment\n\
  focusColumns:\n  ServiceName: Faire\n  ServiceCategory: Marketplace\n  ProviderName: Faire\n  PublisherName: Faire\n  InvoiceIssuerName: Faire\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: first_order_commission\n  description: Commission on first orders from new retailers.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - brand\n  - retailer\n- name: reorder_commission\n  description: Commission on retailer reorders.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - brand\n  - retailer\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n\
  - FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/faire/refs/heads/main/finops/faire-finops.yml
sources:
- https://www.faire.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Marketplace
- Wholesale
- Retail
- Ecommerce
- FinOps
- Cost Management
- FOCUS
---
