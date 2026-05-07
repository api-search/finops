---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sisense-rest-api-openapi.yml
  format: yaml
  label: Sisense REST API v1
  slug: rest-api-v1
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sisense/refs/heads/main/openapi/sisense-rest-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Sisense: tiered subscription with bundled storage, Sisense credits, and seat counts; per-seat and per-credit add-ons; Scale tier negotiated.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Sisense Inc.
  ProviderName: Sisense
  PublisherName: Sisense Inc.
  ServiceCategory: Analytics / Business Intelligence
  ServiceName: Sisense
layout: finops
meters:
- aggregation: sum
  description: Monthly subscription fee for the selected plan tier (Launch, Grow, Scale).
  dimensions:
  - plan
  name: subscription_month
  unit: month
- aggregation: max
  description: Storage consumed against plan allowance (20 GB / 80 GB / custom).
  dimensions:
  - plan
  - environment
  name: storage
  unit: GB-month
- aggregation: sum
  description: Compute / query credits consumed; pool replenishes monthly per plan.
  dimensions:
  - plan
  - workload
  name: sisense_credits
  unit: varies
- aggregation: max
  description: Active designer seats counted against plan minimums; additional seats are billable.
  dimensions:
  - plan
  name: designer_seats
  unit: seat
- aggregation: max
  description: Active viewer seats counted against plan minimums; additional seats are billable.
  dimensions:
  - plan
  name: viewer_seats
  unit: seat
name: Sisense Finops
provider_name: Sisense
provider_slug: sisense
publisher_name: Sisense Inc.
service_category: Analytics / Business Intelligence
slug: sisense-finops
source_filename: sisense-finops.yml
source_heading: FinOps Profile
source_url: https://www.sisense.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Sisense\nproviderId: sisense\npublisherName: Sisense Inc.\nserviceCategory: Analytics / Business Intelligence\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Analytics\n  - Business Intelligence\n  - Embedded Analytics\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Sisense: tiered subscription with bundled storage, Sisense\n  credits, and seat counts; per-seat and per-credit add-ons; Scale tier negotiated.'\nsources:\n  - https://www.sisense.com/pricing/\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n\
  \    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Sisense\n  ServiceCategory: Analytics / Business Intelligence\n  ProviderName: Sisense\n  PublisherName: Sisense Inc.\n  InvoiceIssuerName: Sisense Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: subscription_month\n    description: Monthly subscription fee for the selected plan tier (Launch, Grow, Scale).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: storage\n    description: Storage consumed against plan allowance (20 GB / 80 GB / custom).\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - plan\n      - environment\n  - name: sisense_credits\n    description: Compute / query credits consumed; pool replenishes monthly per plan.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - plan\n      - workload\n  - name: designer_seats\n    description: Active designer seats counted against plan minimums; additional seats are billable.\n    unit:\
  \ seat\n    aggregation: max\n    dimensions:\n      - plan\n  - name: viewer_seats\n    description: Active viewer seats counted against plan minimums; additional seats are billable.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n    description: Track Sisense credit burn, storage utilization, and seat counts in the Sisense\n      admin console; alert before any pool reaches 80% to time tier upgrades.\n  - name: Allocation\n    description: Allocate cost per embedding tenant or workload by tagging dashboards and using\n      multi-environment support (Grow and above) to separate dev/staging/production credit usage.\n  - name: Optimization\n    description: Optimize credit consumption by caching dashboards, reducing query frequency, and\n      consolidating viewer seats; consider BYO LLM (Grow+) to control AI inference cost externally.\n  - name: Accountability\n    description: Embedded-analytics product owner reviews monthly credit\
  \ / seat / storage telemetry\n      and approves seat or credit purchases vs. plan upgrades.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sisense/refs/heads/main/finops/sisense-finops.yml
sources:
- https://www.sisense.com/pricing/
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- Embedded Analytics
- FinOps
- FOCUS
---
