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
  pricingCategory: Contact Sales
description: FinOps shape for Regal Rexnord industrial integrations. Spend is invoiced under hardware purchase or service contracts rather than as metered API usage.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Regal Rexnord Corporation
  ProviderName: Regal Rexnord
  PublisherName: Regal Rexnord Corporation
  ServiceCategory: Industrial
  ServiceName: Regal Rexnord
layout: finops
meters:
- aggregation: sum
  name: contract_term
  unit: month
name: Regal Rexnord Finops
provider_name: Regal Rexnord
provider_slug: regal-rexnord
publisher_name: Regal Rexnord Corporation
service_category: Industrial
slug: regal-rexnord-finops
source_filename: regal-rexnord-finops.yml
source_heading: FinOps Profile
source_url: https://www.regalrexnord.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Regal Rexnord\nproviderId: regal-rexnord\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Industrial\n  - Manufacturing\ndescription: FinOps shape for Regal Rexnord industrial integrations. Spend is invoiced under hardware\n  purchase or service contracts rather than as metered API usage.\nsources:\n  - https://www.regalrexnord.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Regal Rexnord Corporation\nserviceCategory: Industrial\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Regal Rexnord\n  ServiceCategory:\
  \ Industrial\n  ProviderName: Regal Rexnord\n  PublisherName: Regal Rexnord Corporation\n  InvoiceIssuerName: Regal Rexnord Corporation\n  BillingCurrency: USD\nmeters:\n  - name: contract_term\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the Regal Rexnord PO / service-contract invoice; there is no programmatic\n      usage feed.\n  - name: Allocation\n    description: Allocate to the plant, business unit, or product line consuming the motors / drives /\n      services covered by the contract.\n  - name: Optimization\n    description: Optimization happens in procurement — consolidate suppliers, negotiate volume, and\n      align spec with application need at PO time.\n  - name: Accountability\n    description: Owner is the procurement / engineering function that signed the Regal Rexnord agreement.\nnotes: Industrial-product spend rather than API usage. Generic per-request meters and FOCUS columns\n  removed.\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/regal-rexnord/refs/heads/main/finops/regal-rexnord-finops.yml
sources:
- https://www.regalrexnord.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Industrial
- Manufacturing
---
