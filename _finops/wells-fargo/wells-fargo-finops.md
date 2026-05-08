---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: wells-fargo-gateway-api-openapi.yml
  format: yaml
  label: Wells Fargo Gateway API
  slug: gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wells-fargo/refs/heads/main/openapi/wells-fargo-gateway-api-openapi.yml
- filename: wells-fargo-account-transactions-api-openapi.yml
  format: yaml
  label: Wells Fargo Account Transactions API
  slug: account-transactions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wells-fargo/refs/heads/main/openapi/wells-fargo-account-transactions-api-openapi.yml
- filename: wells-fargo-ach-payments-api-openapi.yml
  format: yaml
  label: Wells Fargo ACH Payments API
  slug: ach-payments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wells-fargo/refs/heads/main/openapi/wells-fargo-ach-payments-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Bank Fees / Partner Agreement
description: FinOps placement for Wells Fargo Open Banking APIs. Cost is bundled into the treasury / commercial-banking relationship rather than published as per-call API pricing; FOCUS mapping reflects bank-fee billing.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Wells Fargo Bank, N.A.
  ProviderName: Wells Fargo
  PublisherName: Wells Fargo Bank, N.A.
  ServiceCategory: Banking / Open Banking
  ServiceName: Wells Fargo Open Banking APIs
layout: finops
meters:
- aggregation: sum
  description: Count of payment-initiation / wire / ACH calls executed via the Open Banking Payments APIs; priced through the treasury services schedule.
  dimensions:
  - rail
  - account
  name: payment_transactions
  unit: transaction
- aggregation: sum
  description: Count of account-information / balance / transaction-history calls via the Open Banking Data APIs; pricing depends on the partner agreement.
  dimensions:
  - product
  - account
  name: data_calls
  unit: request
name: Wells Fargo Finops
provider_name: wells-fargo
provider_slug: wells-fargo
publisher_name: Wells Fargo Bank, N.A.
service_category: Banking / Open Banking
slug: wells-fargo-finops
source_filename: wells-fargo-finops.yml
source_heading: FinOps Profile
source_url: https://developer.wellsfargo.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: wells-fargo\nproviderId: wells-fargo\npublisherName: Wells Fargo Bank, N.A.\nserviceCategory: Banking / Open Banking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Open Banking\n  - Payments\n  - Treasury\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps placement for Wells Fargo Open Banking APIs. Cost is bundled into the treasury /\n  commercial-banking relationship rather than published as per-call API pricing; FOCUS mapping\n  reflects bank-fee billing.\nnotes: No public per-call price list. FOCUS columns reflect the treasury / commercial-banking invoice\n  shape only.\nsources:\n  - https://developer.wellsfargo.com/\n\
  billingModel:\n  pricingCategory: Bank Fees / Partner Agreement\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Wells Fargo Open Banking APIs\n  ServiceCategory: Banking / Open Banking\n  ProviderName: Wells Fargo\n  PublisherName: Wells Fargo Bank, N.A.\n  InvoiceIssuerName: Wells Fargo Bank, N.A.\n  BillingCurrency: USD\nmeters:\n  - name: payment_transactions\n    description: Count of payment-initiation / wire / ACH calls executed via the Open Banking\n      Payments APIs; priced through the treasury services schedule.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - rail\n      - account\n  - name: data_calls\n    description: Count of account-information / balance / transaction-history calls via the Open\n      Banking Data APIs; pricing depends on the partner agreement.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\n      - account\nprinciples:\n\
  \  - name: Visibility\n    description: Spend visibility is via the Wells Fargo Commercial Electronic Office (CEO) account\n      analysis statement and any partner-portal reporting provisioned at onboarding.\n  - name: Allocation\n    description: Allocate API-driven banking spend by account, legal entity, or product line using\n      the Wells Fargo account hierarchy and your internal cost-center tags on the integrating\n      application.\n  - name: Optimization\n    description: Cost levers are payment-rail selection (ACH vs wire vs RTP), batching, and renegotiation\n      of the treasury services schedule; idempotency on payments avoids duplicate-charge incidents.\n  - name: Accountability\n    description: Treasury operations and the bank's relationship manager hold accountability;\n      engineering owns idempotency, retry, and reconciliation hygiene.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wells-fargo/refs/heads/main/finops/wells-fargo-finops.yml
sources:
- https://developer.wellsfargo.com/
specification: FinOps Framework
tags:
- Banking
- Open Banking
- Payments
- Treasury
- FinOps
- FOCUS
- Contact Sales
---
