---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise Subscription (Negotiated)
description: 'FOCUS-aligned FinOps placeholder for BlackRock: spend is dominated by enterprise Aladdin / eFront subscription contracts plus negotiated per-asset / per-AUM fee components. No public per-call billing surface.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: BlackRock, Inc.
  ProviderName: BlackRock
  PublisherName: BlackRock, Inc.
  ServiceCategory: Investment Management Platform
  ServiceName: Aladdin
layout: finops
meters:
- aggregation: sum
  dimensions:
  - module
  - tenant
  name: aladdin_subscription
  unit: year
- aggregation: avg
  dimensions:
  - asset_class
  - region
  name: aum_under_management
  unit: USD
- aggregation: max
  dimensions:
  - tenant
  - role
  name: named_users
  unit: seat
- aggregation: sum
  dimensions:
  - api
  - tenant
  name: api_requests
  unit: request
name: Blackrock Finops
provider_name: BlackRock
provider_slug: blackrock
publisher_name: BlackRock, Inc.
service_category: Asset Management Technology
slug: blackrock-finops
source_filename: blackrock-finops.yml
source_heading: FinOps Profile
source_url: https://www.blackrock.com/aladdin
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: BlackRock\nproviderId: blackrock\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Asset Management\n  - Investment Management\ndescription: 'FOCUS-aligned FinOps placeholder for BlackRock: spend is dominated by enterprise Aladdin\n  / eFront subscription contracts plus negotiated per-asset / per-AUM fee components. No public\n  per-call billing surface.'\nsources:\n  - https://www.blackrock.com/aladdin\nnotes: Aladdin commercial terms are private; reconcile against the active enterprise contract for\n  the actual fee structure.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: BlackRock, Inc.\nserviceCategory: Asset Management Technology\n\
  billingModel:\n  pricingCategory: Enterprise Subscription (Negotiated)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Aladdin\n  ServiceCategory: Investment Management Platform\n  ProviderName: BlackRock\n  PublisherName: BlackRock, Inc.\n  InvoiceIssuerName: BlackRock, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: aladdin_subscription\n    unit: year\n    aggregation: sum\n    dimensions:\n      - module\n      - tenant\n  - name: aum_under_management\n    unit: USD\n    aggregation: avg\n    dimensions:\n      - asset_class\n      - region\n  - name: named_users\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tenant\n      - role\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Use Aladdin Studio's tenant administration consoles\
  \ and the BlackRock client\n      reporting deliverables to track module activation and named-user counts.\n  - name: Allocation\n    description: Map Aladdin modules and AUM tracked on the platform to the consuming desk / fund\n      family for chargeback.\n  - name: Optimization\n    description: Reclaim unused named-user seats during annual renewal; consolidate eFront and\n      Aladdin Studio modules; align AUM-based fee triggers with portfolio rebalancing schedule.\n  - name: Accountability\n    description: Designate an Aladdin contract owner per legal entity; review the Aladdin Studio\n      utilization report quarterly with the BlackRock client services team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/blackrock/refs/heads/main/finops/blackrock-finops.yml
sources:
- https://www.blackrock.com/aladdin
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Asset Management
- Investment Management
---
