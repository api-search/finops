---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: td-synnex-streamone-ion-openapi.yml
  format: yaml
  label: TD SYNNEX StreamOne Ion API
  slug: streamone-ion
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/td-synnex/refs/heads/main/openapi/td-synnex-streamone-ion-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract / Partner-Negotiated
description: FOCUS-aligned FinOps shape for TD SYNNEX is partner-contractual rather than consumption-priced. The StreamOne Ion API surface is used by resellers to operate cloud subscriptions on behalf of customers; TD SYNNEX bills under partner agreements and does not publish a public consumption price book.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: TD SYNNEX Corporation
  ProviderName: TD SYNNEX
  PublisherName: TD SYNNEX Corporation
  ServiceCategory: Technology Distribution
  ServiceName: TD SYNNEX StreamOne Ion
layout: finops
meters:
- aggregation: sum
  dimensions:
  - vendor
  - customer
  - subscription
  name: partner_resold_subscription
  unit: varies
name: Td Synnex Finops
provider_name: TD SYNNEX
provider_slug: td-synnex
publisher_name: TD SYNNEX Corporation
service_category: Technology Distribution
slug: td-synnex-finops
source_filename: td-synnex-finops.yml
source_heading: FinOps Profile
source_url: https://www.tdsynnex.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TD SYNNEX\nproviderId: td-synnex\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Technology Distribution\n  - IT Distribution\n  - Cloud\n  - Reseller\n  - StreamOne\n  - Fortune 100\n  - B2B\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for TD SYNNEX is partner-contractual rather than\n  consumption-priced. The StreamOne Ion API surface is used by resellers to operate cloud\n  subscriptions on behalf of customers; TD SYNNEX bills under partner agreements and does not\n  publish a public consumption price book.\nsources:\n  - https://www.tdsynnex.com/\n  - https://streamoneion.tdsynnex.com/\nnotes: Billing, meters, and FOCUS column values for direct API consumption could not be reconciled\n  against a public price list. Commercial terms are negotiated per partner contract. FOCUS columns\n  below capture the publisher\
  \ identity only; ChargeCategory and PricingUnit values would be set by\n  the underlying cloud subscriptions resold through StreamOne Ion.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TD SYNNEX Corporation\nserviceCategory: Technology Distribution\nbillingModel:\n  pricingCategory: Contract / Partner-Negotiated\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: TD SYNNEX StreamOne Ion\n  ServiceCategory: Technology Distribution\n  ProviderName: TD SYNNEX\n  PublisherName: TD SYNNEX Corporation\n  InvoiceIssuerName: TD SYNNEX Corporation\n  BillingCurrency: USD\nmeters:\n  - name: partner_resold_subscription\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - vendor\n      - customer\n      - subscription\nprinciples:\n\
  \  - name: Visibility\n    description: Partners observe resold-subscription consumption through the StreamOne Ion\n      reporting surface; there is no first-party usage API for the platform itself.\n  - name: Allocation\n    description: Cost is allocated by reseller partner, end customer, and the underlying cloud\n      vendor whose subscription is being resold.\n  - name: Optimization\n    description: Optimization levers live at the resold-vendor layer (e.g. AWS / Azure / Google\n      committed use) rather than at the StreamOne Ion API itself.\n  - name: Accountability\n    description: The reseller partner is the accountable owner of subscription spend transacted\n      through StreamOne Ion.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/td-synnex/refs/heads/main/finops/td-synnex-finops.yml
sources:
- https://www.tdsynnex.com/
- https://streamoneion.tdsynnex.com/
specification: FinOps Framework
tags:
- Technology Distribution
- IT Distribution
- Cloud
- Reseller
- StreamOne
- Fortune 100
- B2B
- FinOps
- FOCUS
---
