---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: plausible-stats-openapi.yml
  format: yaml
  label: Plausible Stats API
  slug: stats-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/plausible/refs/heads/main/openapi/plausible-stats-openapi.yml
- filename: plausible-events-openapi.yml
  format: yaml
  label: Plausible Events API
  slug: events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/plausible/refs/heads/main/openapi/plausible-events-openapi.yml
- filename: plausible-sites-openapi.yml
  format: yaml
  label: Plausible Sites API
  slug: sites-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/plausible/refs/heads/main/openapi/plausible-sites-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps for Plausible Analytics - tiered SaaS subscription gated by monthly pageview volume, sites, team members, and API quota. Bills monthly or annually in USD on a single invoice line per site/account.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Plausible Insights OU
  PricingCategory: Subscription
  ProviderName: Plausible
  PublisherName: Plausible Insights OU
  ServiceCategory: Analytics
  ServiceName: Plausible Analytics
  ServiceSubcategory: Web Analytics
layout: finops
meters:
- aggregation: sum
  description: Monthly subscription fee for the chosen tier (Starter / Growth / Business / Enterprise).
  dimensions:
  - plan
  - billing_cycle
  name: subscription_month
  unit: month
- aggregation: sum
  description: Pageviews included in the chosen tier; overage triggers an upgrade rather than metered billing.
  dimensions:
  - site
  - plan
  name: monthly_pageviews_included
  unit: pageview
- aggregation: count
  description: Number of sites tracked under the account; capped per plan.
  dimensions:
  - plan
  name: sites_included
  unit: site
- aggregation: count
  description: Number of team members on the account; capped per plan.
  dimensions:
  - plan
  name: team_seats
  unit: seat
- aggregation: sum
  description: Stats API request count; not separately billed but governed by the per-hour quota tied to the plan.
  dimensions:
  - api_key
  - plan
  name: stats_api_calls
  unit: request
name: Plausible Finops
provider_name: Plausible
provider_slug: plausible
publisher_name: Plausible Insights OU
service_category: Analytics
slug: plausible-finops
source_filename: plausible-finops.yml
source_heading: FinOps Profile
source_url: https://plausible.io/#pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Plausible\nproviderId: plausible\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Analytics\n  - Web Analytics\n  - SaaS\n  - Privacy\ndescription: FOCUS-aligned FinOps for Plausible Analytics - tiered SaaS subscription gated by monthly\n  pageview volume, sites, team members, and API quota. Bills monthly or annually in USD on a single\n  invoice line per site/account.\nsources:\n  - https://plausible.io/#pricing\n  - https://plausible.io/docs/stats-api\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Plausible Insights OU\nserviceCategory: Analytics\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Plausible Analytics\n  ServiceCategory: Analytics\n  ServiceSubcategory: Web Analytics\n  ProviderName: Plausible\n  PublisherName: Plausible Insights OU\n  InvoiceIssuerName: Plausible Insights OU\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\nmeters:\n  - name: subscription_month\n    description: Monthly subscription fee for the chosen tier (Starter / Growth / Business / Enterprise).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - billing_cycle\n  - name: monthly_pageviews_included\n    description: Pageviews included in the chosen tier; overage triggers an upgrade rather than\n      metered billing.\n    unit: pageview\n    aggregation: sum\n    dimensions:\n      - site\n      - plan\n  - name: sites_included\n    description: Number of sites tracked under the account; capped per\
  \ plan.\n    unit: site\n    aggregation: count\n    dimensions:\n      - plan\n  - name: team_seats\n    description: Number of team members on the account; capped per plan.\n    unit: seat\n    aggregation: count\n    dimensions:\n      - plan\n  - name: stats_api_calls\n    description: Stats API request count; not separately billed but governed by the per-hour quota\n      tied to the plan.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key\n      - plan\nprinciples:\n  - name: Visibility\n    description: Pageview consumption is visible in the Plausible dashboard; subscription cost is\n      visible on the billing page and via Stripe-issued invoices.\n  - name: Allocation\n    description: Allocate cost per site or per team by tagging Plausible sites to a product/team and\n      mapping subscription tier and seat count to the owner.\n  - name: Optimization\n    description: Right-size the plan to the smallest pageview tier that fits monthly traffic; switch\n\
  \      to annual billing for the published discount; consolidate sites under one Business plan rather\n      than running multiple Starter accounts.\n  - name: Accountability\n    description: Account owner receives upgrade prompts when pageview limits are exceeded; finance\n      and analytics-team owner should jointly review monthly pageview trend versus tier.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/plausible/refs/heads/main/finops/plausible-finops.yml
sources:
- https://plausible.io/#pricing
- https://plausible.io/docs/stats-api
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Analytics
- Web Analytics
- SaaS
- Privacy
---
