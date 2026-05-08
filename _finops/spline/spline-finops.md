---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Subscription (Seat-Based)
description: FOCUS-aligned FinOps view of Spline. Spline bills as seat-based design subscriptions with bundled SDK access. There is no per-API-call line item; FinOps centers on right-sizing designer seats and tracking AI credit consumption per plan.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Spline
  ProviderName: Spline
  PublisherName: Spline
  ServiceCategory: 3D
  ServiceName: Spline 3D Design Platform
layout: finops
meters:
- aggregation: max
  description: Spline subscription seats (Super/Super Team/Enterprise).
  dimensions:
  - account
  - plan
  name: designer_seats
  unit: seat
- aggregation: sum
  description: AI generation credits consumed per plan tier.
  dimensions:
  - account
  - feature
  name: ai_credits
  unit: credit
name: Spline Finops
provider_name: Spline
provider_slug: spline
publisher_name: Spline
service_category: 3D
slug: spline-finops
source_filename: spline-finops.yml
source_heading: FinOps Profile
source_url: https://spline.design/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Spline\nproviderId: spline\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: partial\ntags:\n- 3D\n- Design\n- AI\n- Collaboration\n- Web\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Spline. Spline bills as seat-based design subscriptions with\n  bundled SDK access. There is no per-API-call line item; FinOps centers on right-sizing\n  designer seats and tracking AI credit consumption per plan.\nnotes: Designer seat sizing is the primary cost lever; SDK embedding does not generate per-call charges directly.\nsources:\n- https://spline.design/pricing\n- https://docs.spline.design/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Spline\nserviceCategory: 3D\nbillingModel:\n  pricingCategory: Subscription (Seat-Based)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Spline 3D Design Platform\n  ServiceCategory: 3D\n  ProviderName: Spline\n  PublisherName: Spline\n  InvoiceIssuerName: Spline\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: designer_seats\n  description: Spline subscription seats (Super/Super Team/Enterprise).\n  unit: seat\n  aggregation: max\n  dimensions:\n  - account\n  - plan\n- name: ai_credits\n  description: AI generation credits consumed per plan tier.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - account\n  - feature\nprinciples:\n- name: Visibility\n  description: Track designer seats and AI credit burn in Spline workspace billing.\n- name: Allocation\n  description: Allocate seats to design teams; tag scenes to consuming product surfaces.\n- name: Optimization\n\
  \  description: Right-size seat count; downgrade idle designers.\n- name: Accountability\n  description: Assign workspace admin to manage seat sprawl.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spline/refs/heads/main/finops/spline-finops.yml
sources:
- https://spline.design/pricing
- https://docs.spline.design/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- 3D
- Design
- AI
- Collaboration
- Web
- FinOps
- Cost Management
- FOCUS
---
