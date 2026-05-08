---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: jetbrains-space-openapi.yml
  format: yaml
  label: JetBrains Space HTTP API
  slug: space-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jetbrains/refs/heads/main/openapi/jetbrains-space-openapi.yml
- filename: jetbrains-teamcity-openapi.yml
  format: yaml
  label: JetBrains TeamCity REST API
  slug: teamcity-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jetbrains/refs/heads/main/openapi/jetbrains-teamcity-openapi.yml
- filename: jetbrains-youtrack-openapi.yml
  format: yaml
  label: JetBrains YouTrack REST API
  slug: youtrack-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jetbrains/refs/heads/main/openapi/jetbrains-youtrack-openapi.yml
- filename: jetbrains-hub-openapi.yml
  format: yaml
  label: JetBrains Hub REST API
  slug: hub-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jetbrains/refs/heads/main/openapi/jetbrains-hub-openapi.yml
- filename: jetbrains-marketplace-openapi.yml
  format: yaml
  label: JetBrains Marketplace API
  slug: marketplace-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jetbrains/refs/heads/main/openapi/jetbrains-marketplace-openapi.yml
billing_model:
  billingCurrency: USD/EUR/GBP
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for JetBrains: per-seat IDE subscriptions, per-build-agent CI subscriptions, per-user collaboration subscriptions (Space, YouTrack), and AI-credit metering for JetBrains AI.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: JetBrains s.r.o.
  ProviderName: JetBrains
  PublisherName: JetBrains s.r.o.
  ServiceCategory: Developer Tools
  ServiceName: JetBrains
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  - audience
  - billing_term
  name: ide_seat
  unit: seat
- aggregation: max
  dimensions:
  - audience
  - billing_term
  name: all_products_pack_seat
  unit: seat
- aggregation: max
  dimensions:
  - deployment
  name: teamcity_build_agent
  unit: build_agent
- aggregation: max
  dimensions:
  - deployment
  name: youtrack_user
  unit: seat
- aggregation: max
  dimensions:
  - tier
  name: space_user
  unit: seat
- aggregation: sum
  dimensions:
  - tier
  - model
  name: ai_credits
  unit: credit
name: Jetbrains Finops
provider_name: JetBrains
provider_slug: jetbrains
publisher_name: JetBrains s.r.o.
service_category: Developer Tools
slug: jetbrains-finops
source_filename: jetbrains-finops.yml
source_heading: FinOps Profile
source_url: https://www.jetbrains.com/store/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: JetBrains\nproviderId: jetbrains\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Developer Tools\n  - IDE\n  - DevOps\ndescription: 'FOCUS-aligned FinOps for JetBrains: per-seat IDE subscriptions, per-build-agent CI subscriptions,\n  per-user collaboration subscriptions (Space, YouTrack), and AI-credit metering for JetBrains AI.'\nsources:\n  - https://www.jetbrains.com/store/\n  - https://www.jetbrains.com/ai-ides/buy/\n  - https://sales.jetbrains.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: JetBrains s.r.o.\nserviceCategory: Developer Tools\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n\
  \  billingCurrency: USD/EUR/GBP\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: JetBrains\n  ServiceCategory: Developer Tools\n  ProviderName: JetBrains\n  PublisherName: JetBrains s.r.o.\n  InvoiceIssuerName: JetBrains s.r.o.\n  BillingCurrency: USD\nmeters:\n  - name: ide_seat\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\n      - audience\n      - billing_term\n  - name: all_products_pack_seat\n    unit: seat\n    aggregation: max\n    dimensions:\n      - audience\n      - billing_term\n  - name: teamcity_build_agent\n    unit: build_agent\n    aggregation: max\n    dimensions:\n      - deployment\n  - name: youtrack_user\n    unit: seat\n    aggregation: max\n    dimensions:\n      - deployment\n  - name: space_user\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tier\n  - name: ai_credits\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - tier\n      - model\n\
  principles:\n  - name: Visibility\n    description: Use the JetBrains License Vault / Customer Portal to see active subscriptions, seat\n      assignments, and AI-credit consumption per user and per team.\n  - name: Allocation\n    description: Tag licenses with cost center / team via the JetBrains License Server or License Vault;\n      attribute AI credits to the developer who consumes them.\n  - name: Optimization\n    description: Reclaim unused seats; consolidate single-product subscriptions into the All Products\n      Pack at scale; lock in 3-year loyalty pricing where commitment is stable; choose AI tier (Pro\n      vs Ultimate) based on observed credit burn.\n  - name: Accountability\n    description: DevOps / Engineering Operations owns the JetBrains tenancy, runs quarterly seat reviews,\n      and reconciles AI-credit overages against developer productivity metrics.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jetbrains/refs/heads/main/finops/jetbrains-finops.yml
sources:
- https://www.jetbrains.com/store/
- https://www.jetbrains.com/ai-ides/buy/
- https://sales.jetbrains.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Developer Tools
- IDE
- DevOps
---
