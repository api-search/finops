---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: blissfully-vendr-catalog-api-openapi.yaml
  format: yaml
  label: Vendr Catalog API
  slug: vendr-catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/blissfully/refs/heads/main/openapi/blissfully-vendr-catalog-api-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription + Credit-Based Usage
description: 'FOCUS-aligned FinOps for the Blissfully product line, now sold under Vendr: an annual Platform-Access subscription combined with usage-based negotiation credits whose burn rate scales with negotiated deal value.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Vendr, Inc.
  ProviderName: Vendr
  PublisherName: Vendr, Inc.
  ServiceCategory: SaaS Management
  ServiceName: Vendr (formerly Blissfully)
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  name: platform_subscription
  unit: year
- aggregation: sum
  dimensions:
  - mode
  - vendor
  - deal_size_bucket
  name: negotiation_credits_consumed
  unit: credit
- aggregation: sum
  dimensions:
  - vendor
  - mode
  name: negotiated_deal_volume
  unit: USD
- aggregation: count
  dimensions:
  - vendor
  - department
  name: contracts_under_management
  unit: contract
name: Blissfully Finops
provider_name: Blissfully
provider_slug: blissfully
publisher_name: Vendr, Inc.
service_category: SaaS Management / Procurement
slug: blissfully-finops
source_filename: blissfully-finops.yml
source_heading: FinOps Profile
source_url: https://www.vendr.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Blissfully\nproviderId: blissfully\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - SaaS Management\n  - Procurement\ndescription: 'FOCUS-aligned FinOps for the Blissfully product line, now sold under Vendr: an annual\n  Platform-Access subscription combined with usage-based negotiation credits whose burn rate scales\n  with negotiated deal value.'\nsources:\n  - https://www.vendr.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Vendr, Inc.\nserviceCategory: SaaS Management / Procurement\nbillingModel:\n  pricingCategory: Subscription + Credit-Based Usage\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Vendr (formerly Blissfully)\n  ServiceCategory: SaaS Management\n  ProviderName: Vendr\n  PublisherName: Vendr, Inc.\n  InvoiceIssuerName: Vendr, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: platform_subscription\n    unit: year\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: negotiation_credits_consumed\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - mode\n      - vendor\n      - deal_size_bucket\n  - name: negotiated_deal_volume\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - vendor\n      - mode\n  - name: contracts_under_management\n    unit: contract\n    aggregation: count\n    dimensions:\n      - vendor\n      - department\nprinciples:\n  - name: Visibility\n    description: Use the Vendr SaaS inventory and contract repository to see active subscriptions and\n      renewal dates; export the credit ledger to track\
  \ Advisory vs Autonomous burn.\n  - name: Allocation\n    description: Tag each contract with department / cost center on intake so renewal spend and\n      negotiation savings can be attributed back to budget owners.\n  - name: Optimization\n    description: Use Advisory mode (~600 credits / $1M) for deals where internal procurement leads;\n      reserve Autonomous mode (~1000 credits / $1M) for high-volume or low-internal-capacity deals;\n      stack credit purchases at higher volume tiers (down to ~1.2%) for largest renewals.\n  - name: Accountability\n    description: Treat 17% average savings claim as the unit-economics floor; review credit\n      consumption and realized savings each quarter against the platform-access subscription cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/blissfully/refs/heads/main/finops/blissfully-finops.yml
sources:
- https://www.vendr.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- SaaS Management
- Procurement
---
