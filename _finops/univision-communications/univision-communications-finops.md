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
  pricingCategory: Contract
description: TelevisaUnivision does not expose a metered API billing surface. Buyer-side spend is ad inventory paid via insertion-orders or programmatic auction; partner-side access is contracted. FinOps maps to advertising and distribution spend rather than per-API-call.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: TelevisaUnivision, Inc.
  ProviderName: TelevisaUnivision
  PublisherName: TelevisaUnivision, Inc.
  ServiceCategory: Media and Advertising
  ServiceName: TelevisaUnivision
layout: finops
meters:
- aggregation: sum
  description: Ad inventory bought through insertion-orders or programmatic auction across TelevisaUnivision properties (TV, radio, ViX streaming, digital).
  dimensions:
  - property
  - format
  - daypart
  name: ad_insertion_order
  unit: varies
- aggregation: sum
  description: Distribution / partner agreement covering content syndication or platform integration.
  name: partner_agreement
  unit: varies
name: Univision Communications Finops
provider_name: TelevisaUnivision (Univision Communications)
provider_slug: univision-communications
publisher_name: TelevisaUnivision, Inc.
service_category: Media and Advertising
slug: univision-communications-finops
source_filename: univision-communications-finops.yml
source_heading: FinOps Profile
source_url: https://corporate.univision.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TelevisaUnivision (Univision Communications)\nproviderId: univision-communications\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Media\n  - Streaming\n  - Advertising\n  - FinOps\n  - FOCUS\n  - B2B\ndescription: TelevisaUnivision does not expose a metered API billing surface. Buyer-side spend is\n  ad inventory paid via insertion-orders or programmatic auction; partner-side access is contracted.\n  FinOps maps to advertising and distribution spend rather than per-API-call.\nsources:\n  - https://corporate.univision.com\nnotes: No public usage-based API billing exists. This artifact captures the contractual surface only.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: TelevisaUnivision, Inc.\nserviceCategory: Media and Advertising\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: TelevisaUnivision\n  ServiceCategory: Media and Advertising\n  ProviderName: TelevisaUnivision\n  PublisherName: TelevisaUnivision, Inc.\n  InvoiceIssuerName: TelevisaUnivision, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: ad_insertion_order\n    description: Ad inventory bought through insertion-orders or programmatic auction across TelevisaUnivision\n      properties (TV, radio, ViX streaming, digital).\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - property\n      - format\n      - daypart\n  - name: partner_agreement\n    description: Distribution / partner agreement covering content syndication or platform integration.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n\
  \    description: API consumption is not separately metered. Track ad delivery and partner integration\n      volume against insertion-order or distribution-agreement targets.\n  - name: Allocation\n    description: Allocate spend at the campaign or partnership level, typically already aligned with\n      a marketing or distribution business owner.\n  - name: Optimization\n    description: Optimization happens at the buy level - daypart selection, programmatic vs direct,\n      property mix - rather than per-API-call.\n  - name: Accountability\n    description: Assign ownership to the campaign manager (buy-side) or partnership owner (distribution-side);\n      FinOps signals are the post-campaign performance and partner-usage reports.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/univision-communications/refs/heads/main/finops/univision-communications-finops.yml
sources:
- https://corporate.univision.com
specification: FinOps Framework
tags:
- Media
- Streaming
- Advertising
- FinOps
- FOCUS
- B2B
---
