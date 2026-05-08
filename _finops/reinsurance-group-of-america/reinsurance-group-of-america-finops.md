---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: FinOps shape for RGA. Pricing is governed by reinsurance treaties and service contracts rather than by metered API consumption.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Reinsurance Group of America, Incorporated
  ProviderName: Reinsurance Group of America
  PublisherName: Reinsurance Group of America, Incorporated
  ServiceCategory: Reinsurance
  ServiceName: RGA
layout: finops
meters:
- aggregation: sum
  name: treaty_term
  unit: month
name: Reinsurance Group Of America Finops
provider_name: Reinsurance Group of America
provider_slug: reinsurance-group-of-america
publisher_name: Reinsurance Group of America, Incorporated
service_category: Reinsurance
slug: reinsurance-group-of-america-finops
source_filename: reinsurance-group-of-america-finops.yml
source_heading: FinOps Profile
source_url: https://www.rgare.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Reinsurance Group of America\nproviderId: reinsurance-group-of-america\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Reinsurance\n  - Insurance\ndescription: FinOps shape for RGA. Pricing is governed by reinsurance treaties and service contracts\n  rather than by metered API consumption.\nsources:\n  - https://www.rgare.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Reinsurance Group of America, Incorporated\nserviceCategory: Reinsurance\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName:\
  \ RGA\n  ServiceCategory: Reinsurance\n  ProviderName: Reinsurance Group of America\n  PublisherName: Reinsurance Group of America, Incorporated\n  InvoiceIssuerName: Reinsurance Group of America, Incorporated\n  BillingCurrency: USD\nmeters:\n  - name: treaty_term\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility comes from treaty statements and cedant-portal reports; no programmatic API\n      usage feed.\n  - name: Allocation\n    description: Allocate to the ceding insurer / product line covered by the treaty; portal access\n      is not separately metered.\n  - name: Optimization\n    description: Optimization is treaty-level — adjust retention, scope, and structure at renewal rather\n      than tuning request volume.\n  - name: Accountability\n    description: Owner is the cedant's reinsurance / treaty-management function.\nnotes: Treaty- and contract-driven; no metered API surface. Generic FOCUS per-call meters removed.\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/reinsurance-group-of-america/refs/heads/main/finops/reinsurance-group-of-america-finops.yml
sources:
- https://www.rgare.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Reinsurance
- Insurance
---
