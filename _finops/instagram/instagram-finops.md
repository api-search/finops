---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: instagram-graph-api.yaml
  format: yaml
  label: Instagram API with Instagram Login
  slug: instagram-api-with-instagram-login
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/instagram/refs/heads/main/openapi/instagram-graph-api.yaml
- filename: instagram-graph-api.yaml
  format: yaml
  label: Instagram API with Facebook Login
  slug: instagram-api-with-facebook-login
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/instagram/refs/heads/main/openapi/instagram-graph-api.yaml
billing_model:
  billingCurrency: Not Applicable
  billingFrequency: Not Applicable
  chargeCategories: []
  chargeFrequency: Not Applicable
  pricingCategory: Free (Rate-Limited)
description: FOCUS-aligned FinOps shape for Instagram Platform APIs. The APIs themselves are free; there is no Meta-issued invoice for API call volume. FinOps practice for Instagram-consuming apps therefore focuses on rate-limit budget consumption (treating X-App-Usage and BUC headers as the de-facto meter) and on the consuming app's own infrastructure cost (storage of media, egress, compute), plus any Instagram Ads (Marketing API) spend which is separately governed.
focus_columns:
  BillingCurrency: Not Applicable
  ChargeCategory: Usage
  InvoiceIssuerName: Meta Platforms, Inc.
  PricingCategory: Free
  PricingUnit: not-applicable
  ProviderName: Meta
  PublisherName: Meta Platforms, Inc.
  ServiceCategory: Social Media APIs
  ServiceName: Instagram Platform
layout: finops
meters:
- aggregation: sum
  description: Count of Graph API calls made on behalf of the app
  dimensions:
  - endpoint
  - access_tier
  - app_id
  name: api_calls
  unit: request
- aggregation: max
  description: Percentage of platform call_count budget consumed (X-App-Usage)
  dimensions:
  - app_id
  name: app_usage_call_count
  unit: percent
- aggregation: max
  description: Percentage of platform total_cputime consumed (X-App-Usage)
  dimensions:
  - app_id
  name: app_usage_cputime
  unit: percent
- aggregation: max
  description: BUC consumption percentage per business / Instagram account (X-Business-Use-Case-Usage)
  dimensions:
  - business_id
  - ig_business_account
  name: buc_usage
  unit: percent
name: Instagram Finops
provider_name: Instagram
provider_slug: instagram
publisher_name: Meta Platforms, Inc.
service_category: Social Media APIs
slug: instagram-finops
source_filename: instagram-finops.yml
source_heading: FinOps Profile
source_url: https://developers.facebook.com/docs/instagram-api/overview
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Instagram\nproviderId: instagram\npublisherName: Meta Platforms, Inc.\nserviceCategory: Social Media APIs\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Instagram\n  - Meta\n  - Social Media\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Instagram Platform APIs. The APIs themselves are free; there\n  is no Meta-issued invoice for API call volume. FinOps practice for Instagram-consuming apps therefore\n  focuses on rate-limit budget consumption (treating X-App-Usage and BUC headers as the de-facto meter)\n  and on the consuming app's own infrastructure cost (storage of media, egress, compute), plus\
  \ any\n  Instagram Ads (Marketing API) spend which is separately governed.\nnotes: No direct Meta charge for Instagram Graph API usage. The 'meter' here is the rate-limit budget;\n  treat X-App-Usage and X-Business-Use-Case-Usage as canonical telemetry. Instagram Ads spend should\n  be tracked separately via the Marketing API.\nsources:\n  - https://developers.facebook.com/docs/instagram-api/overview\n  - https://developers.facebook.com/docs/graph-api/overview/rate-limiting\nprinciples:\n  - name: Visibility\n    description: Log X-App-Usage and X-Business-Use-Case-Usage on every Graph API response and chart\n      call_count / total_cputime / total_time burn against the per-hour and per-day windows.\n  - name: Allocation\n    description: Allocate API budget by feature / account; tag requests in your own infrastructure with\n      the consuming product so per-feature rate-limit consumption can be reviewed.\n  - name: Optimization\n    description: Filter fields, batch with Field Expansion\
  \ judiciously, cache identifiers like Instagram\n      Business Account IDs, and prefer webhooks over polling to reduce calls.\n  - name: Accountability\n    description: Designate a Platform owner per app; review monthly App Review approvals, BUC tier upgrades,\n      and incident counts (4 / 17 / 80001 / 80002 / 80006 errors) in product reviews.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Workload Optimization\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Free (Rate-Limited)\n  billingFrequency: Not Applicable\n  billingCurrency:\
  \ Not Applicable\n  chargeCategories: []\n  chargeFrequency: Not Applicable\nfocusColumns:\n  ServiceName: Instagram Platform\n  ServiceCategory: Social Media APIs\n  ProviderName: Meta\n  PublisherName: Meta Platforms, Inc.\n  InvoiceIssuerName: Meta Platforms, Inc.\n  PricingCategory: Free\n  PricingUnit: not-applicable\n  BillingCurrency: Not Applicable\n  ChargeCategory: Usage\nmeters:\n  - name: api_calls\n    description: Count of Graph API calls made on behalf of the app\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - access_tier\n      - app_id\n  - name: app_usage_call_count\n    description: Percentage of platform call_count budget consumed (X-App-Usage)\n    unit: percent\n    aggregation: max\n    dimensions:\n      - app_id\n  - name: app_usage_cputime\n    description: Percentage of platform total_cputime consumed (X-App-Usage)\n    unit: percent\n    aggregation: max\n    dimensions:\n      - app_id\n  - name: buc_usage\n    description:\
  \ BUC consumption percentage per business / Instagram account (X-Business-Use-Case-Usage)\n    unit: percent\n    aggregation: max\n    dimensions:\n      - business_id\n      - ig_business_account\napis:\n  - name: Instagram Graph API\n    baseURL: https://graph.facebook.com\n    serviceCategory: API\n  - name: Instagram Business Discovery\n    baseURL: https://graph.facebook.com\n    serviceCategory: API\n  - name: Instagram Hashtag Search\n    baseURL: https://graph.facebook.com\n    serviceCategory: API\n  - name: Conversations / Messenger for Instagram\n    baseURL: https://graph.facebook.com\n    serviceCategory: API\nunitEconomics:\n  - name: Calls per Active User\n    metric: api_calls / active_users\n    target: TBD\n  - name: BUC Burn-Rate per Business Account\n    metric: buc_usage / ig_business_account\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/instagram/refs/heads/main/finops/instagram-finops.yml
sources:
- https://developers.facebook.com/docs/instagram-api/overview
- https://developers.facebook.com/docs/graph-api/overview/rate-limiting
specification: FinOps Framework
tags:
- Instagram
- Meta
- Social Media
- FinOps
- FOCUS
---
