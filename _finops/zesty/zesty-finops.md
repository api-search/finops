---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: zesty-auth-api-openapi.yml
  format: yaml
  label: Zesty Auth API
  slug: auth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zesty/refs/heads/main/openapi/zesty-auth-api-openapi.yml
- filename: zesty-accounts-api-openapi.yml
  format: yaml
  label: Zesty Accounts API
  slug: accounts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zesty/refs/heads/main/openapi/zesty-accounts-api-openapi.yml
- filename: zesty-instances-api-openapi.yml
  format: yaml
  label: Zesty Instances API
  slug: instances-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zesty/refs/heads/main/openapi/zesty-instances-api-openapi.yml
- filename: zesty-media-api-openapi.yml
  format: yaml
  label: Zesty Media API
  slug: media-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zesty/refs/heads/main/openapi/zesty-media-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps view for Zesty.io: a tiered monthly subscription that bundles

  CDN bandwidth, CDN requests, API calls, storage, and users, with per-user add-ons

  on the Free tier and custom commitments at Enterprise.

  '
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Zesty, Inc.
  ProviderName: Zesty
  PublisherName: Zesty, Inc.
  ServiceCategory: Headless CMS
  ServiceName: Zesty.io
layout: finops
meters:
- aggregation: max
  description: Monthly plan subscription (Free / Start Up / Business / Enterprise); the primary Zesty billing line.
  dimensions:
  - plan_tier
  name: plan_subscription
  unit: month
- aggregation: count
  description: Add-on users beyond the plan's bundled allowance (e.g. $9/user/month on the Free Community plan).
  dimensions:
  - plan_tier
  name: additional_users
  unit: seat-month
- aggregation: sum
  description: CDN bandwidth consumed against the plan's bundled GB / TB allowance.
  name: cdn_bandwidth
  unit: GB
- aggregation: sum
  description: CDN requests served against the plan's bundled monthly allowance.
  name: cdn_requests
  unit: request
- aggregation: sum
  description: Headless API calls served against the plan's bundled monthly allowance (3K / 10K / 50K / custom).
  name: api_calls
  unit: request
- aggregation: max
  description: Stored content / asset volume against the plan's bundled allowance.
  name: storage
  unit: GB
name: Zesty Finops
provider_name: Zesty
provider_slug: zesty
publisher_name: Zesty, Inc.
service_category: Headless CMS
slug: zesty-finops
source_filename: zesty-finops.yml
source_heading: FinOps Profile
source_url: https://www.zesty.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Zesty\nproviderId: zesty\npublisherName: Zesty, Inc.\nserviceCategory: Headless CMS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - CMS\n  - Composable\n  - Headless\n  - FinOps\n  - FOCUS\ndescription: |\n  FOCUS-aligned FinOps view for Zesty.io: a tiered monthly subscription that bundles\n  CDN bandwidth, CDN requests, API calls, storage, and users, with per-user add-ons\n  on the Free tier and custom commitments at Enterprise.\nsources:\n  - https://www.zesty.io/pricing/\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n\
  \    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Zesty.io\n  ServiceCategory: Headless CMS\n  ProviderName: Zesty\n  PublisherName: Zesty, Inc.\n  InvoiceIssuerName: Zesty, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: plan_subscription\n    description: Monthly plan subscription (Free / Start Up / Business / Enterprise);\n      the primary Zesty billing line.\n    unit: month\n    aggregation: max\n    dimensions:\n      - plan_tier\n  - name: additional_users\n    description: Add-on users beyond the plan's bundled allowance (e.g. $9/user/month\n      on the Free Community plan).\n    unit: seat-month\n    aggregation: count\n    dimensions:\n      - plan_tier\n  - name: cdn_bandwidth\n    description: CDN bandwidth consumed against the plan's bundled GB / TB allowance.\n    unit: GB\n    aggregation: sum\n  - name: cdn_requests\n    description: CDN requests served against the plan's bundled monthly allowance.\n    unit: request\n    aggregation:\
  \ sum\n  - name: api_calls\n    description: Headless API calls served against the plan's bundled monthly allowance\n      (3K / 10K / 50K / custom).\n    unit: request\n    aggregation: sum\n  - name: storage\n    description: Stored content / asset volume against the plan's bundled allowance.\n    unit: GB\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Use the Zesty Manager dashboards for plan utilization (CDN bandwidth,\n      CDN requests, API calls, storage) and confirm bundled quotas against the plan\n      tier each billing cycle.\n  - name: Allocation\n    description: Allocate Zesty cost by site / instance and per-user seats; tag enterprise\n      contracts to the owning brand or product line.\n  - name: Optimization\n    description: Optimize via CDN caching policies (raise hit rate to reduce origin\n      requests), pruning unused users, and right-sizing the plan tier rather than\n      paying per-user add-ons on the Free tier.\n  - name: Accountability\n\
  \    description: Spend ownership sits with the digital / web team that operates the\n      Zesty instance; renewal review is monthly for Start Up / Business and at contract\n      term for Enterprise.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zesty/refs/heads/main/finops/zesty-finops.yml
sources:
- https://www.zesty.io/pricing/
specification: FinOps Framework
tags:
- CMS
- Composable
- Headless
- FinOps
- FOCUS
---
