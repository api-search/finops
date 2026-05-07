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
  pricingCategory: Custom Contract
description: 'FOCUS-aligned FinOps for Umpqua Holdings: regulated banking integrations billed via treasury-management service charges and aggregator / open-banking agreements rather than a public per-API price sheet.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Umpqua Bank (Columbia Banking System)
  ProviderName: Umpqua Holdings
  PublisherName: Umpqua Bank (Columbia Banking System)
  ServiceCategory: Banking / Financial Services
  ServiceName: Umpqua Treasury Integration
layout: finops
meters:
- aggregation: sum
  description: Monthly treasury-management service charges (per-account, per-transaction, per-report)
  dimensions:
  - service
  - account
  name: treasury_service_fees
  unit: varies
- aggregation: max
  description: Open-banking / aggregator data-sharing connections
  name: aggregator_connections
  unit: connection
name: Umpqua Holdings Finops
provider_name: Umpqua Holdings
provider_slug: umpqua-holdings
publisher_name: Umpqua Bank (Columbia Banking System)
service_category: Banking / Financial Services
slug: umpqua-holdings-finops
source_filename: umpqua-holdings-finops.yml
source_heading: FinOps Profile
source_url: https://www.umpquabank.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Umpqua Holdings\nproviderId: umpqua-holdings\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Financial Services\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Umpqua Holdings: regulated banking integrations billed via treasury-management\n  service charges and aggregator / open-banking agreements rather than a public per-API price sheet.'\nnotes: Umpqua / Columbia Banking System has no public developer portal or pricing surface. Meters and\n  FOCUS columns are placeholders pending reconciliation against actual treasury-management invoices.\nsources:\n  - https://www.umpquabank.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Umpqua Bank (Columbia Banking System)\nserviceCategory: Banking / Financial Services\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Umpqua Treasury Integration\n  ServiceCategory: Banking / Financial Services\n  ProviderName: Umpqua Holdings\n  PublisherName: Umpqua Bank (Columbia Banking System)\n  InvoiceIssuerName: Umpqua Bank (Columbia Banking System)\n  BillingCurrency: USD\nmeters:\n  - name: treasury_service_fees\n    description: Monthly treasury-management service charges (per-account, per-transaction, per-report)\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - account\n  - name: aggregator_connections\n    description: Open-banking / aggregator data-sharing connections\n    unit: connection\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Reconcile spend from monthly\
  \ treasury-management analysis statements; Umpqua does not\n      expose a public usage-API surface.\n  - name: Allocation\n    description: Allocate per business account / entity using account-analysis statements and treasury\n      group hierarchy.\n  - name: Optimization\n    description: Re-negotiate treasury fees on renewal based on transaction volume; consolidate accounts\n      and rationalize aggregator connections.\n  - name: Accountability\n    description: Treasury and corporate-finance owners review the bank's account-analysis statements\n      and reconcile against forecasted activity.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/umpqua-holdings/refs/heads/main/finops/umpqua-holdings-finops.yml
sources:
- https://www.umpquabank.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Banking
- Financial Services
- FinOps
- FOCUS
---
