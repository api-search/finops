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
  pricingCategory: Contract-Negotiated Services
description: Stifel Financial bills under client agreements (advisory fees, brokerage commissions, deal fees), not under a public API meter. This artifact captures publisher and category surface only; meters are placeholders.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Stifel, Nicolaus & Company, Incorporated
  ProviderName: Stifel Financial
  PublisherName: Stifel, Nicolaus & Company, Incorporated
  ServiceCategory: Financial Services
  ServiceName: Stifel Financial
layout: finops
meters:
- aggregation: sum
  description: Negotiated advisory, brokerage, and integration fees on the underlying client agreement
  name: contract_services
  unit: varies
name: Stifel Financial Finops
provider_name: Stifel Financial
provider_slug: stifel-financial
publisher_name: Stifel, Nicolaus & Company, Incorporated
service_category: Financial Services
slug: stifel-financial-finops
source_filename: stifel-financial-finops.yml
source_heading: FinOps Profile
source_url: https://www.stifel.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Stifel Financial\nproviderId: stifel-financial\npublisherName: Stifel, Nicolaus & Company, Incorporated\nserviceCategory: Financial Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Finance\n  - Wealth Management\n  - Investment Banking\ndescription: Stifel Financial bills under client agreements (advisory fees, brokerage commissions, deal\n  fees), not under a public API meter. This artifact captures publisher and category surface only; meters\n  are placeholders.\nsources:\n  - https://www.stifel.com\nnotes: 'Reconciliation marked false: Stifel Financial does not publish a public billing/pricing\
  \ schedule\n  for programmatic access. All commercial terms are private to the client agreement.'\nbillingModel:\n  pricingCategory: Contract-Negotiated Services\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Stifel Financial\n  ServiceCategory: Financial Services\n  ProviderName: Stifel Financial\n  PublisherName: Stifel, Nicolaus & Company, Incorporated\n  InvoiceIssuerName: Stifel, Nicolaus & Company, Incorporated\n  BillingCurrency: USD\nmeters:\n  - name: contract_services\n    description: Negotiated advisory, brokerage, and integration fees on the underlying client agreement\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility into Stifel-related spend is via client statements and the relationship\n      manager, not a usage API.\n  - name: Allocation\n    description: Allocation is by account or trading desk per the client\
  \ agreement.\n  - name: Optimization\n    description: Optimization levers are commercial (renegotiating fee schedules, rebalancing AUM tiers)\n      rather than technical.\n  - name: Accountability\n    description: Account ownership rests with the contracting institution's treasury or operations team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stifel-financial/refs/heads/main/finops/stifel-financial-finops.yml
sources:
- https://www.stifel.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Finance
- Wealth Management
- Investment Banking
---
