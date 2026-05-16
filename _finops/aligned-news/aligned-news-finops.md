---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: aligned-news-openapi.yml
  format: yaml
  label: Aligned News
  slug: aligned-news
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aligned-news/refs/heads/main/openapi/aligned-news-openapi.yml
- filename: aligned-news-openapi.yml
  format: yaml
  label: Aligned News REST API
  slug: aligned-news-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aligned-news/refs/heads/main/openapi/aligned-news-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual (Pro); Contract (Enterprise)
  pricingCategory: Subscription (flat-rate)
description: Aligned News bills via flat-rate Pro and contact-sales Enterprise subscriptions managed through Clerk Billing on top of Stripe. There is no metered usage-based billing surface today (Free has no API access; Pro unlocks the entire content corpus and the API for a single recurring fee; Enterprise is contact sales). FOCUS-style cost tracking is best modelled at the seat/subscription level rather than per-token or per-call. Reconciled is false because the public site does not expose price values for the Pro or Enterprise tiers.
focus_columns:
  BillingCurrency: USD
  ProviderName: Aligned News
  PublisherName: Aligned News
  ServiceCategory: AI News Intelligence
  ServiceName: Aligned News
layout: finops
meters:
- aggregation: sum
  dimensions:
  - billing_period
  name: pro_subscription
  unit: seat-month
- aggregation: sum
  dimensions:
  - contract_term
  name: enterprise_subscription
  unit: contract
name: Aligned News Finops
provider_name: Aligned News
provider_slug: aligned-news
publisher_name: Aligned News
service_category: AI News Intelligence
slug: aligned-news-finops
source_filename: aligned-news-finops.yml
source_heading: FinOps Profile
source_url: https://alignednews.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Aligned News\nproviderId: aligned-news\ncreated: '2026-05-06'\nmodified: '2026-05-06'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - AI News\ndescription: >-\n  Aligned News bills via flat-rate Pro and contact-sales Enterprise\n  subscriptions managed through Clerk Billing on top of Stripe. There is no\n  metered usage-based billing surface today (Free has no API access; Pro\n  unlocks the entire content corpus and the API for a single recurring fee;\n  Enterprise is contact sales). FOCUS-style cost tracking is best modelled at\n  the seat/subscription level rather than per-token or per-call. Reconciled\n  is false because the public site does not expose price values for the Pro\n  or Enterprise tiers.\nsources:\n  - https://alignednews.com/pricing\n  - https://alignednews.com/developers\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl:\
  \ https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Aligned News\nserviceCategory: AI News Intelligence\nbillingModel:\n  pricingCategory: Subscription (flat-rate)\n  billingFrequency: Monthly or Annual (Pro); Contract (Enterprise)\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Aligned News\n  ServiceCategory: AI News Intelligence\n  ProviderName: Aligned News\n  PublisherName: Aligned News\n  BillingCurrency: USD\nnotes:\n  - No usage-metered billing surface is exposed publicly.\n  - Subscriptions are managed via Clerk Billing; payments via Stripe.\n  - Cost-allocation should attribute the seat/subscription to the consuming\n    team rather than per-call.\nmeters:\n  - name: pro_subscription\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - billing_period\n  - name: enterprise_subscription\n    unit: contract\n    aggregation: sum\n    dimensions:\n\
  \      - contract_term\nprinciples:\n  - name: Visibility\n    description: Track Aligned News spend at the subscription level via Stripe billing\n      exports.\n  - name: Allocation\n    description: Tag the subscription owner team or cost centre; Aligned News does\n      not break out per-key usage.\n  - name: Optimization\n    description: Right-size between Pro and Enterprise based on team size and need\n      for priority support and custom analysis.\n  - name: Accountability\n    description: Annual review of subscription value vs. usage of API and MCP\n      surfaces.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aligned-news/refs/heads/main/finops/aligned-news-finops.yml
sources:
- https://alignednews.com/pricing
- https://alignednews.com/developers
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI News
---
