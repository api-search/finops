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
  - Adjustment
  pricingCategory: Custom Contract
description: FinOps view of Walgreens Boots Alliance at the holding-company level. WBA does not bill API consumption directly; API-related cost flows are reported by the operating subsidiaries (Walgreens, Boots) under their respective partnership agreements. This artifact records that mapping rather than a direct WBA invoice surface.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Walgreens Boots Alliance, Inc.
  ProviderName: Walgreens Boots Alliance
  PublisherName: Walgreens Boots Alliance, Inc.
  ServiceCategory: Pharmacy / Healthcare Holding Company
  ServiceName: Walgreens Boots Alliance Partnerships
layout: finops
meters:
- aggregation: sum
  description: Negotiated settlement under the bilateral partnership agreement, attributed to the relevant operating company.
  dimensions:
  - operating_company
  - region
  name: partnership_settlement
  unit: varies
name: Walgreens Boots Alliance Finops
provider_name: Walgreens Boots Alliance
provider_slug: walgreens-boots-alliance
publisher_name: Walgreens Boots Alliance, Inc.
service_category: Pharmacy / Healthcare Holding Company
slug: walgreens-boots-alliance-finops
source_filename: walgreens-boots-alliance-finops.yml
source_heading: FinOps Profile
source_url: https://www.walgreensbootsalliance.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Walgreens Boots Alliance\nproviderId: walgreens-boots-alliance\npublisherName: Walgreens Boots Alliance, Inc.\nserviceCategory: Pharmacy / Healthcare Holding Company\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Pharmacy\n  - Healthcare\n  - Retail\n  - FinOps\n  - FOCUS\ndescription: FinOps view of Walgreens Boots Alliance at the holding-company\n  level. WBA does not bill API consumption directly; API-related cost flows\n  are reported by the operating subsidiaries (Walgreens, Boots) under their\n  respective partnership agreements. This artifact records that mapping\n  rather than a direct WBA invoice surface.\nsources:\n  - https://www.walgreensbootsalliance.com/\n\
  \  - https://corporate.walgreens.com/\nnotes: No corporate-level API invoice; FOCUS attribution flows through the\n  operating-company billing entity (Walgreen Co., Boots UK Limited).\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Walgreens Boots Alliance Partnerships\n  ServiceCategory: Pharmacy / Healthcare Holding Company\n  ProviderName: Walgreens Boots Alliance\n  PublisherName: Walgreens Boots Alliance, Inc.\n  InvoiceIssuerName: Walgreens Boots Alliance, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: partnership_settlement\n    description: Negotiated settlement under the bilateral partnership\n      agreement, attributed to the relevant operating company.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - operating_company\n      - region\nprinciples:\n  - name: Visibility\n    description:\
  \ Track partnership-level settlements at the WBA holding\n      level; drill into operating-company telemetry (Walgreens, Boots) for\n      per-API observability.\n  - name: Allocation\n    description: Allocate partnership cost / revenue to the operating-company\n      P&L (Walgreens vs Boots) based on the contract's settlement entity.\n  - name: Optimization\n    description: Optimization happens at the operating-company API surface\n      (request volume, conversion); WBA-level levers are renegotiation of\n      the partnership agreement at renewal.\n  - name: Accountability\n    description: Corporate development / partnerships at WBA owns the\n      bilateral agreement; operating-company finance teams own the\n      partnership P&L.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/walgreens-boots-alliance/refs/heads/main/finops/walgreens-boots-alliance-finops.yml
sources:
- https://www.walgreensbootsalliance.com/
- https://corporate.walgreens.com/
specification: FinOps Framework
tags:
- Pharmacy
- Healthcare
- Retail
- FinOps
- FOCUS
---
