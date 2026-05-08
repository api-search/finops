---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: veriff-openapi.yml
  format: yaml
  label: Veriff Sessions API
  slug: sessions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veriff/refs/heads/main/openapi/veriff-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Tax
  - Credit
  pricingCategory: Per-Verification (Tiered) + Monthly Minimum + Add-Ons
description: FOCUS-aligned FinOps for Veriff. Cost is dominated by per-verification consumption against the active tier (Essential $0.80, Plus $1.39, Premium $1.89, Enterprise custom) up to the monthly minimum, plus stacked add-on per-verification surcharges for extended retention (+$0.30), PEP/sanctions screening (+$0.64), and ongoing monitoring (+$0.09). The web and mobile SDKs are free; cost begins when a session reaches a billable terminal state. Optimisation levers are reducing duplicate or abandoned sessions, choosing the lowest tier that meets the regulatory profile, and selectively enabling add-ons.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Veriff OU
  ProviderName: Veriff
  PublisherName: Veriff OU
  ServiceCategory: Identity Verification
  ServiceName: Veriff
layout: finops
meters:
- aggregation: sum
  description: Per-completed verification (terminal session decision); the dominant usage meter, billed at the active tier's per-verification rate.
  dimensions:
  - account_id
  - plan_tier
  - country
  - document_type
  name: verification
  unit: verification
- aggregation: max
  description: Monthly minimum charge for the active tier ($49 Essential / $99 Plus / $209 Premium / custom Enterprise); whichever is greater (minimum or actual usage) is billed.
  dimensions:
  - account_id
  - plan_tier
  name: monthly_minimum
  unit: month
- aggregation: sum
  description: Per-verification PEP / sanctions / adverse-media screening surcharge (+$0.64).
  dimensions:
  - account_id
  name: pep_screening
  unit: verification
- aggregation: sum
  description: Per-verification ongoing-monitoring surcharge (+$0.09).
  dimensions:
  - account_id
  name: ongoing_monitoring
  unit: verification
- aggregation: sum
  description: Per-verification extended-retention surcharge for retaining records 2 years instead of the tier default (+$0.30).
  dimensions:
  - account_id
  name: extended_retention
  unit: verification
name: Veriff Finops
provider_name: Veriff
provider_slug: veriff
publisher_name: Veriff OU
service_category: Identity Verification
slug: veriff-finops
source_filename: veriff-finops.yml
source_heading: FinOps Profile
source_url: https://www.veriff.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Veriff\nproviderId: veriff\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - KYC\n  - Identity Verification\n  - Biometrics\n  - Fraud Prevention\n  - AML\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for Veriff. Cost is dominated by per-verification consumption\n  against the active tier (Essential $0.80, Plus $1.39, Premium $1.89, Enterprise\n  custom) up to the monthly minimum, plus stacked add-on per-verification surcharges\n  for extended retention (+$0.30), PEP/sanctions screening (+$0.64), and ongoing\n  monitoring (+$0.09). The web and mobile SDKs are free; cost begins when a session\n  reaches a billable terminal state. Optimisation levers are reducing duplicate or\n  abandoned sessions, choosing the lowest tier that meets the regulatory profile, and\n  selectively enabling add-ons.\nsources:\n  - https://www.veriff.com/pricing\n\
  \  - https://devdocs.veriff.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Veriff OU\nserviceCategory: Identity Verification\nbillingModel:\n  pricingCategory: Per-Verification (Tiered) + Monthly Minimum + Add-Ons\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: Veriff\n  ServiceCategory: Identity Verification\n  ProviderName: Veriff\n  PublisherName: Veriff OU\n  InvoiceIssuerName: Veriff OU\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: verification\n    description: >-\n      Per-completed verification (terminal session decision); the dominant usage\n      meter, billed at the active tier's per-verification rate.\n    unit: verification\n    aggregation:\
  \ sum\n    dimensions:\n      - account_id\n      - plan_tier\n      - country\n      - document_type\n  - name: monthly_minimum\n    description: >-\n      Monthly minimum charge for the active tier ($49 Essential / $99 Plus /\n      $209 Premium / custom Enterprise); whichever is greater (minimum or actual\n      usage) is billed.\n    unit: month\n    aggregation: max\n    dimensions:\n      - account_id\n      - plan_tier\n  - name: pep_screening\n    description: >-\n      Per-verification PEP / sanctions / adverse-media screening surcharge (+$0.64).\n    unit: verification\n    aggregation: sum\n    dimensions:\n      - account_id\n  - name: ongoing_monitoring\n    description: >-\n      Per-verification ongoing-monitoring surcharge (+$0.09).\n    unit: verification\n    aggregation: sum\n    dimensions:\n      - account_id\n  - name: extended_retention\n    description: >-\n      Per-verification extended-retention surcharge for retaining records 2 years\n      instead of the tier\
  \ default (+$0.30).\n    unit: verification\n    aggregation: sum\n    dimensions:\n      - account_id\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Veriff Customer Portal usage report to track per-tier verifications and\n      add-on attach rate. Use webhook events and the Decisions API to confirm session\n      lifecycle counts and reconcile against the invoice.\n  - name: Allocation\n    description: >-\n      Pass a vendorData reference per session keyed to a business unit or product\n      flow, so attribution is preserved on the invoice. Separate sandbox and\n      production accounts to keep pre-prod testing off the production meter.\n  - name: Optimization\n    description: >-\n      Avoid double-billing by collapsing duplicate sessions for the same end user.\n      Choose the lowest tier consistent with the regulatory profile. Enable add-ons\n      (PEP/sanctions, monitoring, extended retention) only on flows where they are\n      legally or contractually\
  \ required. Use the 50-session free trial to size\n      production volume before committing to a tier.\n  - name: Accountability\n    description: >-\n      Assign a compliance / fraud owner per Veriff account. Track actual usage against\n      the monthly minimum and renegotiate the tier and add-ons at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veriff/refs/heads/main/finops/veriff-finops.yml
sources:
- https://www.veriff.com/pricing
- https://devdocs.veriff.com/
specification: FinOps Framework
tags:
- KYC
- Identity Verification
- Biometrics
- Fraud Prevention
- AML
- FinOps
- FOCUS
---
