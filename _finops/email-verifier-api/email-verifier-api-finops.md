---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: email-verifier-api-openapi.yml
  format: yaml
  label: Email Verifier API Verification
  slug: verification
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/email-verifier-api/refs/heads/main/openapi/email-verifier-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: OnDemand
  chargeCategories:
  - Purchase
  pricingCategory: PayAsYouGo
description: 'FOCUS-aligned FinOps scaffold for Email Verifier API. The vendor uses a single,

  transparent commercial model: pay-as-you-go credit packs that never expire. Spend is

  driven by the count of "Paid" verification events (mailbox-level outcomes that require

  an SMTP probe). Free events (syntax, DNS, MX, catch-all, greylisting, transient

  failures) do not consume credits, so the effective unit cost per deliverable result is

  a function of list quality.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Email Verifier API
  ProviderName: Email Verifier API
  PublisherName: Email Verifier API
  ServiceCategory: Email Verification
  ServiceName: Email Verifier API
layout: finops
meters:
- aggregation: sum
  description: 'Paid event consuming one credit. Issued for mailboxExists, mailboxDoesNotExist,

    and mailboxIsFull outcomes that required an SMTP probe.'
  dimensions:
  - api_key
  - event
  - status
  name: paid_verification
  unit: verification
- aggregation: sum
  description: 'Free event that did not consume credits. Issued for invalidSyntax,

    domainDoesNotExist, mxServerDoesNotExist, isCatchall, isGreylisting, and

    transientError outcomes.'
  dimensions:
  - api_key
  - event
  - status
  name: free_verification
  unit: verification
- aggregation: sum
  description: One-time purchase of a credit pack that never expires.
  dimensions:
  - pack_size
  - unit_price
  name: credit_pack_purchase
  unit: pack
name: Email Verifier Api Finops
provider_name: Email Verifier API
provider_slug: email-verifier-api
publisher_name: Email Verifier API
service_category: Email Verification
slug: email-verifier-api-finops
source_filename: email-verifier-api-finops.yml
source_heading: FinOps Profile
source_url: https://emailverifierapi.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Email Verifier API\nproviderId: email-verifier-api\npublisherName: Email Verifier API\nserviceCategory: Email Verification\ncreated: '2026-05-06'\nmodified: '2026-05-06'\nreconciled: true\ntags:\n  - Email Verification\n  - Deliverability\n  - SMTP Check\n  - FinOps\n  - FOCUS\ndescription: |-\n  FOCUS-aligned FinOps scaffold for Email Verifier API. The vendor uses a single,\n  transparent commercial model: pay-as-you-go credit packs that never expire. Spend is\n  driven by the count of \"Paid\" verification events (mailbox-level outcomes that require\n  an SMTP probe). Free events (syntax, DNS, MX, catch-all, greylisting, transient\n  failures)\
  \ do not consume credits, so the effective unit cost per deliverable result is\n  a function of list quality.\nsources:\n  - https://emailverifierapi.com/pricing/\n  - https://emailverifierapi.com/api-docs/\nnotes: |-\n  Reconciled prices are the public credit-pack list prices in USD. Per-email price\n  declines from $0.0080 at 1,000 credits to $0.0013 at 10,000,000 credits. Since\n  credits are one-time purchases that never expire, the FOCUS ChargeCategory is\n  Purchase rather than Usage; the customer \"burns down\" the purchased asset over time.\nbillingModel:\n  pricingCategory: PayAsYouGo\n  billingFrequency: OnDemand\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Email Verifier API\n  ServiceCategory: Email Verification\n  ProviderName: Email Verifier API\n  PublisherName: Email Verifier API\n  InvoiceIssuerName: Email Verifier API\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: paid_verification\n    description:\
  \ |-\n      Paid event consuming one credit. Issued for mailboxExists, mailboxDoesNotExist,\n      and mailboxIsFull outcomes that required an SMTP probe.\n    unit: verification\n    aggregation: sum\n    dimensions:\n      - api_key\n      - event\n      - status\n  - name: free_verification\n    description: |-\n      Free event that did not consume credits. Issued for invalidSyntax,\n      domainDoesNotExist, mxServerDoesNotExist, isCatchall, isGreylisting, and\n      transientError outcomes.\n    unit: verification\n    aggregation: sum\n    dimensions:\n      - api_key\n      - event\n      - status\n  - name: credit_pack_purchase\n    description: One-time purchase of a credit pack that never expires.\n    unit: pack\n    aggregation: sum\n    dimensions:\n      - pack_size\n      - unit_price\nprinciples:\n  - name: Visibility\n    description: |-\n      Every API response includes the `remaining` field with the up-to-date credit\n      balance and the `event`/`status` pair that\
  \ determines whether the request was\n      Paid or Free. Capture both into the customer's metering store to attribute\n      verification spend per environment, tenant, or feature.\n  - name: Allocation\n    description: |-\n      Allocate credit-pack purchases to the team that owns the address-quality program\n      (typically growth / marketing-ops or auth / signup). Tag the API key per cost\n      center so that distinct environments and tenants do not co-mingle spend.\n  - name: Optimization\n    description: |-\n      Pre-filter input lists for syntax and disposable-domain matches before calling\n      the API; treat catch-all and greylisting as deferred outcomes rather than\n      retrying immediately. Buying larger credit packs unlocks materially lower\n      per-email pricing (down to $0.0013/email at 10M).\n  - name: Accountability\n    description: |-\n      Engineering signup / list-hygiene leads own per-event verification spend; finance\n      owns credit-pack purchase cadence\
  \ and approves enterprise volume contracts.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/email-verifier-api/refs/heads/main/finops/email-verifier-api-finops.yml
sources:
- https://emailverifierapi.com/pricing/
- https://emailverifierapi.com/api-docs/
specification: FinOps Framework
tags:
- Email Verification
- Deliverability
- SMTP Check
- FinOps
- FOCUS
---
