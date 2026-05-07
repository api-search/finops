---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: marqeta-core-api-openapi.yml
  format: yaml
  label: Marqeta Core API
  slug: core-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/marqeta/refs/heads/main/openapi/marqeta-core-api-openapi.yml
- filename: marqeta-diva-api-openapi.yml
  format: yaml
  label: Marqeta DiVA API
  slug: diva-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/marqeta/refs/heads/main/openapi/marqeta-diva-api-openapi.yml
- filename: marqeta-webhooks-asyncapi.yml
  format: yaml
  label: Marqeta Webhooks
  slug: webhooks
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/marqeta/refs/heads/main/asyncapi/marqeta-webhooks-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Subscription + Per-Transaction (Take Rate offset by Interchange Share)
description: 'FOCUS-aligned FinOps shape for Marqeta: card-issuing platform billed as platform fee + per-active-card + per-transaction with interchange revenue share, all priced per program under MSA.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Marqeta, Inc.
  ProviderName: Marqeta
  PublisherName: Marqeta, Inc.
  ServiceCategory: Card Issuing & Processing
  ServiceName: Marqeta Card Issuing Platform
layout: finops
meters:
- aggregation: max
  description: Recurring platform fee per program / per BIN.
  dimensions:
  - program
  - bin
  name: platform_fee
  unit: month
- aggregation: avg
  description: Count of active cards in the period.
  dimensions:
  - program
  - card_product
  - state
  name: active_cards
  unit: card-month
- aggregation: sum
  description: Authorized and/or settled transactions processed.
  dimensions:
  - program
  - card_product
  - mcc
  - country
  - network
  name: card_transactions
  unit: transaction
- aggregation: sum
  description: Interchange revenue share returned to the program (a credit / negative cost).
  dimensions:
  - program
  - network
  - card_product
  name: interchange_revenue_share
  unit: USD
- aggregation: sum
  description: Optional services such as fraud management, dispute services, KYC, or accelerated wage.
  dimensions:
  - service
  - program
  name: ancillary_services
  unit: varies
name: Marqeta Finops
provider_name: marqeta
provider_slug: marqeta
publisher_name: Marqeta, Inc.
service_category: Card Issuing & Processing
slug: marqeta-finops
source_filename: marqeta-finops.yml
source_heading: FinOps Profile
source_url: https://www.marqeta.com/platform
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Marqeta\nproviderId: marqeta\npublisherName: Marqeta, Inc.\nserviceCategory: Card Issuing & Processing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Card Issuing\n  - Payments\n  - Fintech\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Marqeta: card-issuing platform billed as platform fee +\n  per-active-card + per-transaction with interchange revenue share, all priced per program under MSA.'\nnotes: |\n  Pricing is not publicly published; meter unit-prices remain unknown until quoted. Marqeta is a B2B\n  platform - costs are typically allocated by program / BIN / card product within a finance\
  \ org.\nsources:\n  - https://www.marqeta.com/platform\n  - https://www.marqeta.com/about/investor-relations\nprinciples:\n  - name: Visibility\n    description: Use the Marqeta Insights / DiVA reporting dashboard and the program's monthly invoice\n      to observe platform fees, per-card counts, transaction volumes, and interchange share. Reconcile\n      against your own authorization log via the Transactions endpoint of the Core API.\n  - name: Allocation\n    description: Allocate by program token and card product; tag transaction metadata (memo / user_token)\n      with internal tenant or product IDs at issuance to enable downstream chargeback to the consuming\n      business unit.\n  - name: Optimization\n    description: Sunset inactive cards (per-card fee dominates at low utilization), prefer virtual cards\n      where physical issuance is unnecessary, batch state-changing API calls to reduce processing overhead,\n      and renegotiate interchange share at volume thresholds.\n\
  \  - name: Accountability\n    description: Assign a program owner responsible for the monthly invoice, fraud loss, and chargeback\n      ratios; review unit economics quarterly with the Marqeta account team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Subscription + Per-Transaction (Take Rate offset by Interchange Share)\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Marqeta Card Issuing Platform\n  ServiceCategory: Card Issuing & Processing\n  ProviderName: Marqeta\n  PublisherName: Marqeta, Inc.\n  InvoiceIssuerName: Marqeta, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: platform_fee\n    description: Recurring platform fee per program / per BIN.\n    unit: month\n    aggregation: max\n    dimensions:\n      - program\n      - bin\n  - name: active_cards\n    description: Count of active cards in the period.\n    unit: card-month\n    aggregation: avg\n    dimensions:\n      - program\n      - card_product\n      - state\n  - name: card_transactions\n    description: Authorized and/or settled transactions processed.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - program\n      - card_product\n      - mcc\n      - country\n      - network\n  - name:\
  \ interchange_revenue_share\n    description: Interchange revenue share returned to the program (a credit / negative cost).\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - program\n      - network\n      - card_product\n  - name: ancillary_services\n    description: Optional services such as fraud management, dispute services, KYC, or accelerated wage.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - program\napis:\n  - name: Marqeta Core API\n    baseURL: https://sandbox-api.marqeta.com/v3\n    tags:\n      - Card Issuing\n      - Fintech\n      - Payment Processing\n      - Payments\n      - REST\n    serviceName: Marqeta Core API\n    serviceCategory: API\n  - name: Marqeta DiVA API\n    baseURL: https://diva-api.marqeta.com/data/v2\n    tags:\n      - Analytics\n      - Data\n      - Fintech\n      - Reporting\n      - REST\n    serviceName: Marqeta DiVA API\n    serviceCategory: API\n  - name: Marqeta Webhooks\n    baseURL: https://your-server.example.com/webhooks\n\
  \    tags:\n      - Events\n      - Fintech\n      - Notifications\n      - Real-Time\n      - Webhooks\n    serviceName: Marqeta Webhooks\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Active Card\n    metric: billed_cost / active_cards\n    target: TBD\n  - name: Cost per Transaction\n    metric: billed_cost / card_transactions\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/marqeta/refs/heads/main/finops/marqeta-finops.yml
sources:
- https://www.marqeta.com/platform
- https://www.marqeta.com/about/investor-relations
specification: FinOps Framework
tags:
- Card Issuing
- Payments
- Fintech
- FinOps
- FOCUS
---
