---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: shell-b2b-mobility-openapi.yml
  format: yaml
  label: Shell B2B Mobility Card Management API
  slug: b2b-mobility-card-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-b2b-mobility-openapi.yml
- filename: shell-b2b-mobility-openapi.yml
  format: yaml
  label: Shell B2B Mobility Card Transaction Data API
  slug: b2b-mobility-card-transaction-data
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-b2b-mobility-openapi.yml
- filename: shell-b2b-mobility-openapi.yml
  format: yaml
  label: Shell B2B Mobility Invoice API
  slug: b2b-mobility-invoice
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-b2b-mobility-openapi.yml
- filename: shell-loyalty-openapi.yml
  format: yaml
  label: Shell Loyalty Catalogue API
  slug: loyalty-catalogue
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-loyalty-openapi.yml
- filename: shell-loyalty-openapi.yml
  format: yaml
  label: Shell Loyalty Account Management API
  slug: loyalty-account-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-loyalty-openapi.yml
- filename: shell-loyalty-openapi.yml
  format: yaml
  label: Shell Loyalty Points Balance API
  slug: loyalty-points-balance
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-loyalty-openapi.yml
- filename: shell-loyalty-openapi.yml
  format: yaml
  label: Shell Loyalty Points Redemption API
  slug: loyalty-points-redemption
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-loyalty-openapi.yml
- filename: shell-lubricants-openapi.yml
  format: yaml
  label: Shell Lubricants Order Management API
  slug: lubricants-order-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-lubricants-openapi.yml
- filename: shell-b2b-mobility-openapi.yml
  format: yaml
  label: Shell B2B Mobility Sites API
  slug: b2b-mobility-sites
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-b2b-mobility-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Embedded in B2B Contract
description: FinOps shape for Shell B2B APIs — gated to existing partners with no public per-call pricing. The dominant cost line is the underlying B2B contract (fuel-card transactions, mobility services, loyalty programme); the API itself is typically a free service layer on top of that contract. Reconciliation to FOCUS columns is best-effort because Shell does not publish a meter-level rate sheet.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Shell plc
  ProviderName: Shell
  PublisherName: Shell plc
  ServiceCategory: Energy / Mobility B2B
  ServiceName: Shell B2B APIs
layout: finops
meters:
- aggregation: sum
  description: Fuel-card transactions processed under the partner's Shell agreement
  dimensions:
  - card_program
  - country
  name: card_transactions
  unit: transaction
- aggregation: max
  description: Active cards under management for a B2B partner
  dimensions:
  - card_program
  name: cards_managed
  unit: card
- aggregation: sum
  description: API requests against Shell developer endpoints (operational meter; not billed at the API layer)
  dimensions:
  - api
  name: api_requests
  unit: request
name: Shell Finops
provider_name: Shell
provider_slug: shell
publisher_name: Shell plc
service_category: Energy / Mobility B2B
slug: shell-finops
source_filename: shell-finops.yml
source_heading: FinOps Profile
source_url: https://developer.shell.com/api-catalog
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Shell\nproviderId: shell\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Mobility\n  - Fleet\n  - Fuel Cards\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Shell B2B APIs — gated to existing partners with no public per-call pricing.\n  The dominant cost line is the underlying B2B contract (fuel-card transactions, mobility services, loyalty\n  programme); the API itself is typically a free service layer on top of that contract. Reconciliation\n  to FOCUS columns is best-effort because Shell does not publish a meter-level rate sheet.\nsources:\n  - https://developer.shell.com/api-catalog\nnotes: No public per-meter pricing. Cost flows through the underlying Shell B2B agreement (fuel-card\n  fees, transaction commissions, etc.) rather than per-API metering.\nalignedWith:\n  framework: FinOps Foundation Framework\n \
  \ frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Shell plc\nserviceCategory: Energy / Mobility B2B\nbillingModel:\n  pricingCategory: Embedded in B2B Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Shell B2B APIs\n  ServiceCategory: Energy / Mobility B2B\n  ProviderName: Shell\n  PublisherName: Shell plc\n  InvoiceIssuerName: Shell plc\n  BillingCurrency: USD\nmeters:\n  - name: card_transactions\n    description: Fuel-card transactions processed under the partner's Shell agreement\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - card_program\n      - country\n  - name: cards_managed\n    description: Active cards under management for a B2B partner\n    unit: card\n    aggregation: max\n    dimensions:\n      - card_program\n  - name: api_requests\n\
  \    description: API requests against Shell developer endpoints (operational meter; not billed at the\n      API layer)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the partner's Shell B2B portal and invoice (transaction reports,\n      card-level statements). API call volume should be instrumented client-side because Shell does not\n      publish a usage API.\n  - name: Allocation\n    description: Allocate fuel-card and transaction cost by cost center / fleet / driver via card metadata;\n      align with the partner's existing fuel-card cost-allocation process rather than re-deriving it\n      from API logs.\n  - name: Optimization\n    description: Optimization happens at the Shell B2B contract level (volume rebates, network preference)\n      rather than via API tuning. On the integration side, batch transaction queries and respect partner\n      rate limits to avoid disruption.\n\
  \  - name: Accountability\n    description: Procurement / Fleet management owns the Shell partner relationship. Integration-platform\n      engineering owns API hygiene and is the contact for partner-side rate-limit issues escalated through\n      the Shell account team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/finops/shell-finops.yml
sources:
- https://developer.shell.com/api-catalog
specification: FinOps Framework
tags:
- Energy
- Mobility
- Fleet
- Fuel Cards
- FinOps
- FOCUS
---
