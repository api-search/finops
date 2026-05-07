---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swift-swiftref-api-openapi.yml
  format: yaml
  label: SwiftRef API
  slug: swiftref-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/swift/refs/heads/main/openapi/swift-swiftref-api-openapi.yml
billing_model:
  billingCurrency: EUR
  billingFrequency: Annual + Per-Message Settlement
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Member-Tiered Cooperative Pricing
description: SWIFT bills members under the cooperative's published-but-member-only pricing schedule (annual support charges, traffic charges by message class, service-specific fees). This artifact captures publisher and category surface only; meters are placeholders pending member-only pricing access.
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: S.W.I.F.T. SC
  ProviderName: SWIFT
  PublisherName: S.W.I.F.T. SC
  ServiceCategory: Financial Messaging
  ServiceName: SWIFT
layout: finops
meters:
- aggregation: sum
  description: SWIFT message traffic billed by tier and message type (FIN, MX, ISO 20022); rates per member's traffic band
  dimensions:
  - message_type
  - service
  - member_tier
  name: messaging_traffic
  unit: message
- aggregation: max
  description: Annual support and membership fee scaled by member share class
  dimensions:
  - member_class
  name: annual_membership
  unit: year
- aggregation: sum
  description: Service-specific fees (gpi, KYC Registry, Sanctions Screening, Transaction Screening, Compliance Analytics)
  dimensions:
  - service
  name: service_charges
  unit: varies
name: Swift Finops
provider_name: SWIFT
provider_slug: swift
publisher_name: S.W.I.F.T. SC
service_category: Financial Messaging & Cross-Border Payments
slug: swift-finops
source_filename: swift-finops.yml
source_heading: FinOps Profile
source_url: https://www.swift.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SWIFT\nproviderId: swift\npublisherName: S.W.I.F.T. SC\nserviceCategory: Financial Messaging & Cross-Border Payments\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Banking\n  - Financial Messaging\n  - Payments\n  - ISO 20022\ndescription: SWIFT bills members under the cooperative's published-but-member-only pricing schedule\n  (annual support charges, traffic charges by message class, service-specific fees). This artifact captures\n  publisher and category surface only; meters are placeholders pending member-only pricing access.\nsources:\n  - https://www.swift.com\nnotes: 'Reconciliation marked\
  \ false: SWIFT pricing is private to members. No public per-call rate card.'\nbillingModel:\n  pricingCategory: Member-Tiered Cooperative Pricing\n  billingFrequency: Annual + Per-Message Settlement\n  billingCurrency: EUR\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: SWIFT\n  ServiceCategory: Financial Messaging\n  ProviderName: SWIFT\n  PublisherName: S.W.I.F.T. SC\n  InvoiceIssuerName: S.W.I.F.T. SC\n  BillingCurrency: EUR\nmeters:\n  - name: messaging_traffic\n    description: SWIFT message traffic billed by tier and message type (FIN, MX, ISO 20022); rates per\n      member's traffic band\n    unit: message\n    aggregation: sum\n    dimensions:\n      - message_type\n      - service\n      - member_tier\n  - name: annual_membership\n    description: Annual support and membership fee scaled by member share class\n    unit: year\n    aggregation: max\n    dimensions:\n      - member_class\n  - name: service_charges\n \
  \   description: Service-specific fees (gpi, KYC Registry, Sanctions Screening, Transaction Screening,\n      Compliance Analytics)\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Visibility into SWIFT spend is via the member's SWIFTNet billing files and the swift.com\n      member portal, not a public usage API.\n  - name: Allocation\n    description: Allocate by message type and originating business line; SWIFT bill files itemize traffic\n      by service and BIC.\n  - name: Optimization\n    description: Optimization levers include traffic-band selection at year-end, consolidating BICs,\n      using Alliance Cloud or Lite2 to reduce on-prem operating cost, and leaning on shared services.\n  - name: Accountability\n    description: Account ownership rests with the institution's payments operations and SWIFT relationship\n      manager; review against the annual SWIFT pricing notification.\nmaintainers:\n \
  \ - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/swift/refs/heads/main/finops/swift-finops.yml
sources:
- https://www.swift.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking
- Financial Messaging
- Payments
- ISO 20022
---
