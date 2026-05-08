---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract / Bilateral
description: 'FOCUS-aligned FinOps placeholder for TIAA-CREF: legacy brand of TIAA, with B2B partner-only programmatic access and no public rate card.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Teachers Insurance and Annuity Association of America
  ProviderName: TIAA-CREF
  PublisherName: Teachers Insurance and Annuity Association of America
  ServiceCategory: Financial Services
  ServiceName: TIAA-CREF
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - partner
  name: contracted_partner_access
  unit: varies
name: Tiaa Cref Finops
provider_name: TIAA-CREF
provider_slug: tiaa-cref
publisher_name: Teachers Insurance and Annuity Association of America
service_category: Financial Services
slug: tiaa-cref-finops
source_filename: tiaa-cref-finops.yml
source_heading: FinOps Profile
source_url: https://www.tiaa.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TIAA-CREF\nproviderId: tiaa-cref\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Finance\n  - Retirement\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for TIAA-CREF: legacy brand of TIAA, with B2B partner-only\n  programmatic access and no public rate card.'\nsources:\n  - https://www.tiaa.org/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: TIAA-CREF is the legacy brand for TIAA; FinOps shape mirrors the TIAA partner-contract model.\n  No public usage-based rate card.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Teachers Insurance and Annuity Association of America\nserviceCategory: Financial Services\n\
  billingModel:\n  pricingCategory: Contract / Bilateral\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: TIAA-CREF\n  ServiceCategory: Financial Services\n  ProviderName: TIAA-CREF\n  PublisherName: Teachers Insurance and Annuity Association of America\n  InvoiceIssuerName: Teachers Insurance and Annuity Association of America\n  BillingCurrency: USD\nmeters:\n  - name: contracted_partner_access\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - api\n      - partner\nprinciples:\n  - name: Visibility\n    description: Rely on partner-portal usage statements TIAA issues under the contract; no public usage\n      API.\n  - name: Allocation\n    description: Allocate the contract cost to the retirement-services or recordkeeping team that owns\n      the TIAA-CREF integration.\n  - name: Optimization\n    description: Tune at integration design — batch participant data calls, cache static reference data,\n\
  \      avoid duplicate plan submissions.\n  - name: Accountability\n    description: A named partnership owner is accountable for the TIAA-CREF agreement, scope, and renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tiaa-cref/refs/heads/main/finops/tiaa-cref-finops.yml
sources:
- https://www.tiaa.org/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Finance
- Retirement
- FinOps
- FOCUS
---
