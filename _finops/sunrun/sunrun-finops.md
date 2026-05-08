---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Per-Invoice
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Contract-Negotiated Services
description: Sunrun bills end customers under solar lease/PPA/loan/purchase contracts and any partner data exchanges under bilateral agreements. There is no public API meter. This artifact captures publisher and category surface only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Sunrun Inc.
  ProviderName: Sunrun
  PublisherName: Sunrun Inc.
  ServiceCategory: Residential Solar & Storage
  ServiceName: Sunrun
layout: finops
meters:
- aggregation: sum
  description: Negotiated solar lease/PPA/partner integration line items
  name: contract_services
  unit: varies
name: Sunrun Finops
provider_name: Sunrun
provider_slug: sunrun
publisher_name: Sunrun Inc.
service_category: Residential Solar & Storage
slug: sunrun-finops
source_filename: sunrun-finops.yml
source_heading: FinOps Profile
source_url: https://www.sunrun.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Sunrun\nproviderId: sunrun\npublisherName: Sunrun Inc.\nserviceCategory: Residential Solar & Storage\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Residential Solar\n  - Clean Energy\ndescription: Sunrun bills end customers under solar lease/PPA/loan/purchase contracts and any partner\n  data exchanges under bilateral agreements. There is no public API meter. This artifact captures publisher\n  and category surface only.\nsources:\n  - https://www.sunrun.com\nnotes: 'Reconciliation marked false: Sunrun publishes no public API billing/pricing schedule. Programmatic\n  cost is bundled into the\
  \ underlying customer or partner agreement.'\nbillingModel:\n  pricingCategory: Contract-Negotiated Services\n  billingFrequency: Monthly or Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Sunrun\n  ServiceCategory: Residential Solar & Storage\n  ProviderName: Sunrun\n  PublisherName: Sunrun Inc.\n  InvoiceIssuerName: Sunrun Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_services\n    description: Negotiated solar lease/PPA/partner integration line items\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility is via the customer-portal account view or partner-data feed defined in\n      the agreement, not a usage API.\n  - name: Allocation\n    description: Allocation is by site/system in the customer-facing case and per-program in the partner\n      case.\n  - name: Optimization\n    description: Optimization levers are operational (battery dispatch,\
  \ virtual power plant participation)\n      rather than API-tier driven.\n  - name: Accountability\n    description: Account ownership rests with the homeowner (customer) or the partner organization's\n      assigned program lead.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sunrun/refs/heads/main/finops/sunrun-finops.yml
sources:
- https://www.sunrun.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Residential Solar
- Clean Energy
---
