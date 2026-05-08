---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: docs
  format: yaml
  label: SimpleLocalize Translation API
  slug: translation-api
  spec_type: OpenAPI
  url: https://api.simplelocalize.io/openapi/docs
billing_model:
  billingCurrency: EUR
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for SimpleLocalize: tiered EUR-denominated subscription with plan caps on translation keys, seats, and auto-translation characters; enterprise plans negotiated.'
focus_columns:
  BillingCurrency: EUR
  ChargeCategory: Usage
  InvoiceIssuerName: SimpleLocalize
  ProviderName: SimpleLocalize
  PublisherName: SimpleLocalize
  ServiceCategory: Localization / Translation Management
  ServiceName: SimpleLocalize
layout: finops
meters:
- aggregation: sum
  description: Monthly subscription fee for the selected plan tier (Developer, Team, Business).
  dimensions:
  - plan
  name: subscription_month
  unit: month
- aggregation: max
  description: Active translation keys counted against the plan cap.
  dimensions:
  - plan
  - project
  name: translation_keys
  unit: varies
- aggregation: sum
  description: Machine-translation characters consumed against initial allowance plus monthly top-up.
  dimensions:
  - plan
  - language_pair
  name: auto_translation_characters
  unit: varies
- aggregation: max
  description: Team-member seats provisioned against the plan cap.
  dimensions:
  - plan
  name: team_seats
  unit: seat
name: Simplelocalize Finops
provider_name: SimpleLocalize
provider_slug: simplelocalize
publisher_name: SimpleLocalize
service_category: Localization / Translation Management
slug: simplelocalize-finops
source_filename: simplelocalize-finops.yml
source_heading: FinOps Profile
source_url: https://simplelocalize.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SimpleLocalize\nproviderId: simplelocalize\npublisherName: SimpleLocalize\nserviceCategory: Localization / Translation Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Localization\n  - Translation\n  - Internationalization\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for SimpleLocalize: tiered EUR-denominated subscription with plan\n  caps on translation keys, seats, and auto-translation characters; enterprise plans negotiated.'\nsources:\n  - https://simplelocalize.io/pricing/\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: EUR\n  chargeCategories:\n\
  \    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: SimpleLocalize\n  ServiceCategory: Localization / Translation Management\n  ProviderName: SimpleLocalize\n  PublisherName: SimpleLocalize\n  InvoiceIssuerName: SimpleLocalize\n  BillingCurrency: EUR\n  ChargeCategory: Usage\nmeters:\n  - name: subscription_month\n    description: Monthly subscription fee for the selected plan tier (Developer, Team, Business).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: translation_keys\n    description: Active translation keys counted against the plan cap.\n    unit: varies\n    aggregation: max\n    dimensions:\n      - plan\n      - project\n  - name: auto_translation_characters\n    description: Machine-translation characters consumed against initial allowance plus monthly top-up.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - plan\n      - language_pair\n  - name: team_seats\n    description: Team-member seats\
  \ provisioned against the plan cap.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n    description: Track translation-key utilization and auto-translation character burn against plan\n      caps via the SimpleLocalize dashboard; alert before keys, seats, or character pool exhaust.\n  - name: Allocation\n    description: Allocate cost per project (each project maps to a product or customer locale set)\n      and per team member where seat economics matter.\n  - name: Optimization\n    description: Audit unused translation keys and stale languages to stay within tier caps; batch\n      auto-translation runs to make best use of the rolling character pool before paying for higher\n      tiers.\n  - name: Accountability\n    description: Localization owner reviews monthly key/seat/character utilization and approves tier\n      upgrades or downgrades based on observed activity-log trends.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/simplelocalize/refs/heads/main/finops/simplelocalize-finops.yml
sources:
- https://simplelocalize.io/pricing/
specification: FinOps Framework
tags:
- Localization
- Translation
- Internationalization
- FinOps
- FOCUS
---
