---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: vantiv-cnp-openapi.yml
  format: yaml
  label: Vantiv CNP API
  slug: cnp-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vantiv/refs/heads/main/openapi/vantiv-cnp-openapi.yml
- filename: vantiv-express-openapi.yml
  format: yaml
  label: Vantiv Express API
  slug: express-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vantiv/refs/heads/main/openapi/vantiv-express-openapi.yml
- filename: vantiv-chargeback-openapi.yml
  format: yaml
  label: Vantiv Chargeback API
  slug: chargeback-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vantiv/refs/heads/main/openapi/vantiv-chargeback-openapi.yml
billing_model:
  billingCurrency: GBP
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Refund
  pricingCategory: Take Rate + Subscription
description: 'FOCUS-aligned FinOps for Vantiv (now Worldpay): per-transaction authorisation fee plus monthly recurring service/equipment fees and chargeback charges. Bespoke pricing replaces the indicative rate card based on volume, MCC, and channel.'
focus_columns:
  BillingCurrency: GBP
  ChargeCategory: Usage
  InvoiceIssuerName: Worldpay
  ProviderName: Worldpay
  PublisherName: Worldpay
  ServiceCategory: Payments
  ServiceName: Worldpay (Vantiv)
layout: finops
meters:
- aggregation: sum
  description: Card authorisation requests, billed at the flat per-transaction auth fee
  dimensions:
  - card_brand
  - channel
  - mcc
  name: card_authorisations
  unit: transaction
- aggregation: sum
  description: Active POS terminal months billed at the monthly terminal fee
  name: pos_terminal_months
  unit: terminal-month
- aggregation: sum
  description: PCI DSS service months billed at the monthly PCI fee
  name: pci_dss_months
  unit: month
- aggregation: sum
  description: Minimum monthly service charge applied when usage fees fall below the floor
  name: minimum_service
  unit: month
- aggregation: sum
  description: Chargebacks billed at the per-event fee
  dimensions:
  - reason_code
  name: chargebacks
  unit: chargeback
name: Vantiv Finops
provider_name: Vantiv
provider_slug: vantiv
publisher_name: Worldpay (Vantiv legacy brand)
service_category: Payments
slug: vantiv-finops
source_filename: vantiv-finops.yml
source_heading: FinOps Profile
source_url: https://go.worldpay.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Vantiv\nproviderId: vantiv\npublisherName: Worldpay (Vantiv legacy brand)\nserviceCategory: Payments\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Payments\n  - Payment Processing\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Vantiv (now Worldpay): per-transaction authorisation fee plus monthly recurring service/equipment fees and chargeback charges. Bespoke pricing replaces the indicative rate card based on volume, MCC, and channel.'\nsources:\n  - https://go.worldpay.com/pricing\n  - https://docs.worldpay.com/access/\nbillingModel:\n  pricingCategory: Take Rate + Subscription\n  billingFrequency:\
  \ Monthly\n  billingCurrency: GBP\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Worldpay (Vantiv)\n  ServiceCategory: Payments\n  ProviderName: Worldpay\n  PublisherName: Worldpay\n  InvoiceIssuerName: Worldpay\n  BillingCurrency: GBP\n  ChargeCategory: Usage\nmeters:\n  - name: card_authorisations\n    description: Card authorisation requests, billed at the flat per-transaction auth fee\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - card_brand\n      - channel\n      - mcc\n  - name: pos_terminal_months\n    description: Active POS terminal months billed at the monthly terminal fee\n    unit: terminal-month\n    aggregation: sum\n  - name: pci_dss_months\n    description: PCI DSS service months billed at the monthly PCI fee\n    unit: month\n    aggregation: sum\n  - name: minimum_service\n    description: Minimum monthly service charge applied when usage fees fall below the floor\n    unit: month\n\
  \    aggregation: sum\n  - name: chargebacks\n    description: Chargebacks billed at the per-event fee\n    unit: chargeback\n    aggregation: sum\n    dimensions:\n      - reason_code\nprinciples:\n  - name: Visibility\n    description: Reconcile monthly Worldpay statements against transaction logs by channel (in-person vs online/phone) and card brand; capture WP-CorrelationId for any disputed line.\n  - name: Allocation\n    description: Allocate by MID/store and by channel using Worldpay reporting; tag transactions with internal location/department identifiers in the merchant reference.\n  - name: Optimization\n    description: Lower effective cost by submitting an updated turnover/AVT questionnaire to renegotiate the bespoke rate card; reduce chargebacks via 3DS, address checks, and risk rules.\n  - name: Accountability\n    description: Owner is the merchant's payments/finance team; review monthly minimum-service and PCI DSS charges and reconcile chargeback fees against dispute resolution\
  \ outcomes.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vantiv/refs/heads/main/finops/vantiv-finops.yml
sources:
- https://go.worldpay.com/pricing
- https://docs.worldpay.com/access/
specification: FinOps Framework
tags:
- Payments
- Payment Processing
- FinOps
- FOCUS
---
