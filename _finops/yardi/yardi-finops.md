---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: yardi-voyager-api-openapi.yml
  format: yaml
  label: Yardi Voyager API
  slug: yardi-voyager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/yardi/refs/heads/main/openapi/yardi-voyager-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Contact Sales
description: Yardi's commercial model is sales-negotiated by portfolio and module mix, with no public price card; this artifact is a Contact Sales placeholder.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Yardi Systems, Inc.
  ProviderName: Yardi
  PublisherName: Yardi Systems, Inc.
  ServiceCategory: Property Management / PropTech
  ServiceName: Yardi
layout: finops
meters:
- aggregation: sum
  description: Module / product bundles licensed under the Yardi agreement (Voyager, Breeze, RentCafe, etc.); priced per portfolio.
  name: contracted_modules
  unit: varies
name: Yardi Finops
provider_name: Yardi
provider_slug: yardi
publisher_name: Yardi Systems, Inc.
service_category: Property Management / PropTech
slug: yardi-finops
source_filename: yardi-finops.yml
source_heading: FinOps Profile
source_url: https://www.yardi.com/products/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Yardi\nproviderId: yardi\npublisherName: Yardi Systems, Inc.\nserviceCategory: Property Management / PropTech\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Property Management\n  - Real Estate\n  - FinOps\n  - FOCUS\ndescription: Yardi's commercial model is sales-negotiated by portfolio and module mix,\n  with no public price card; this artifact is a Contact Sales placeholder.\nsources:\n  - https://www.yardi.com/products/\nnotes: |\n  Yardi does not publish per-meter pricing or invoice line items publicly. Meter and\n  FOCUS column values below are minimal placeholders pending the customer's signed\n  Yardi license\
  \ / SaaS agreement.\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Yardi\n  ServiceCategory: Property Management / PropTech\n  ProviderName: Yardi\n  PublisherName: Yardi Systems, Inc.\n  InvoiceIssuerName: Yardi Systems, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contracted_modules\n    description: Module / product bundles licensed under the Yardi agreement (Voyager,\n      Breeze, RentCafe, etc.); priced per portfolio.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Yardi invoices roll up by module and portfolio; line-item detail comes\n      from the customer's Yardi account team rather than a self-serve usage API.\n  - name: Allocation\n    description: Allocate Yardi spend by property / portfolio / business unit using the\n      cost-center fields configured in Voyager General Ledger.\n  - name:\
  \ Optimization\n    description: Optimization is module-driven — review Voyager add-ons, RentCafe seat\n      counts, and Marketplace transaction fees during annual contract renewal.\n  - name: Accountability\n    description: Spend ownership sits with the property operations / IT lead who signs the\n      Yardi master agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/yardi/refs/heads/main/finops/yardi-finops.yml
sources:
- https://www.yardi.com/products/
specification: FinOps Framework
tags:
- Property Management
- Real Estate
- FinOps
- FOCUS
---
