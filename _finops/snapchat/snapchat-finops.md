---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: snapchat-ads-api-openapi.yml
  format: yaml
  label: Snapchat Ads API
  slug: snapchat-ads-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snapchat/refs/heads/main/openapi/snapchat-ads-api-openapi.yml
- filename: snapchat-conversions-api-openapi.yml
  format: yaml
  label: Snapchat Conversions API
  slug: snapchat-conversions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snapchat/refs/heads/main/openapi/snapchat-conversions-api-openapi.yml
- filename: snapchat-login-kit-openapi.yml
  format: yaml
  label: Snapchat Login Kit API
  slug: snapchat-login-kit
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snapchat/refs/heads/main/openapi/snapchat-login-kit-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Auction-Based Ad Spend
description: 'FOCUS-aligned FinOps for Snapchat: API access is free for approved developers; the billable surface is auction-based ad spend invoiced through Snap Business Manager.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Snap Inc.
  ProviderName: Snap
  PublisherName: Snap Inc.
  ServiceCategory: Advertising
  ServiceName: Snapchat Ads
layout: finops
meters:
- aggregation: sum
  dimensions:
  - ad_account
  - campaign
  - country
  name: ad_impressions
  unit: impression
- aggregation: sum
  dimensions:
  - ad_account
  - campaign
  name: ad_clicks
  unit: click
- aggregation: sum
  dimensions:
  - ad_account
  - campaign
  - objective
  name: ad_spend
  unit: USD
- aggregation: sum
  dimensions:
  - app
  - access_token
  name: api_requests
  unit: request
name: Snapchat Finops
provider_name: Snapchat
provider_slug: snapchat
publisher_name: Snap Inc.
service_category: Advertising
slug: snapchat-finops
source_filename: snapchat-finops.yml
source_heading: FinOps Profile
source_url: https://developers.snap.com/api/marketing-api/Ads-API/rate-limits
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Snapchat\nproviderId: snapchat\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Advertising\n  - Marketing\n  - Social Media\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Snapchat: API access is free for approved developers; the billable\n  surface is auction-based ad spend invoiced through Snap Business Manager.'\nsources:\n  - https://developers.snap.com/api/marketing-api/Ads-API/rate-limits\n  - https://developers.snap.com/api/marketing-api/Ads-API/getting-started\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Snap Inc.\nserviceCategory: Advertising\nbillingModel:\n  pricingCategory: Auction-Based Ad Spend\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Snapchat Ads\n  ServiceCategory: Advertising\n  ProviderName: Snap\n  PublisherName: Snap Inc.\n  InvoiceIssuerName: Snap Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: ad_impressions\n    unit: impression\n    aggregation: sum\n    dimensions:\n      - ad_account\n      - campaign\n      - country\n  - name: ad_clicks\n    unit: click\n    aggregation: sum\n    dimensions:\n      - ad_account\n      - campaign\n  - name: ad_spend\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - ad_account\n      - campaign\n      - objective\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - app\n      - access_token\nprinciples:\n  - name: Visibility\n    description: Use Snap Business Manager reporting plus the Marketing API stats endpoints to retrieve\n      spend, impressions, clicks, and\
  \ conversions per campaign and ad account.\n  - name: Allocation\n    description: Allocate ad spend by ad account, campaign, ad squad, and country dimensions returned\n      by the Marketing API; tag campaigns to the internal team or product driving them.\n  - name: Optimization\n    description: Tune bid strategy, audience targeting, and creative rotation; respect the 20 req/s app\n      and 10 req/s per-token Marketing API limits to avoid wasted retries.\n  - name: Accountability\n    description: Each Snap Business Manager organization assigns roles for finance and campaign owners\n      who reconcile invoices against Marketing API reporting.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/snapchat/refs/heads/main/finops/snapchat-finops.yml
sources:
- https://developers.snap.com/api/marketing-api/Ads-API/rate-limits
- https://developers.snap.com/api/marketing-api/Ads-API/getting-started
specification: FinOps Framework
tags:
- Advertising
- Marketing
- Social Media
- FinOps
- FOCUS
---
