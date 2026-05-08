---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: facebook-graph-api.yaml
  format: yaml
  label: Facebook Graph API
  slug: facebook-graph-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/facebook/refs/heads/main/openapi/facebook-graph-api.yaml
- filename: facebook-marketing-api.yaml
  format: yaml
  label: Facebook Marketing API
  slug: facebook-marketing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/facebook/refs/heads/main/openapi/facebook-marketing-api.yaml
- filename: facebook-instagram-api.yaml
  format: yaml
  label: Instagram API
  slug: instagram-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/facebook/refs/heads/main/openapi/facebook-instagram-api.yaml
- filename: facebook-messenger-api.yaml
  format: yaml
  label: Messenger Platform API
  slug: messenger-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/facebook/refs/heads/main/openapi/facebook-messenger-api.yaml
- filename: facebook-threads-api.yaml
  format: yaml
  label: Threads API
  slug: threads-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/facebook/refs/heads/main/openapi/facebook-threads-api.yaml
- filename: facebook-whatsapp-api.yaml
  format: yaml
  label: WhatsApp Business API
  slug: whatsapp-business-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/facebook/refs/heads/main/openapi/facebook-whatsapp-api.yaml
billing_model:
  billingCurrency: USD (settlement varies by country)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Free API + Downstream Ad Spend + Per-Conversation Messaging
description: 'FOCUS-aligned FinOps for Facebook (Meta) APIs: the Graph and Marketing APIs are free at the API layer; spend is downstream — ad campaign budgets billed by Meta Ads, and per-conversation pricing for WhatsApp Business. API-level FinOps focuses on quota burn (rate-limit headers) rather than direct API charges.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Meta Platforms, Inc.
  PricingCategory: Free API + Usage (downstream)
  PricingUnit: varies (impression, conversation, ad-spend USD)
  ProviderName: Meta
  PublisherName: Meta Platforms, Inc.
  ServiceCategory: Advertising / Social Media
  ServiceName: Facebook (Meta) APIs
layout: finops
meters:
- aggregation: sum
  description: Count of Graph/Marketing API calls; not directly billed but counts against rate-limit formulas.
  dimensions:
  - app
  - business_id
  - ad_account
  - endpoint
  name: graph_api_calls
  unit: call
- aggregation: sum
  description: Ad campaign spend billed via Meta Ads.
  dimensions:
  - ad_account
  - campaign
  - placement
  - country
  name: ad_spend
  unit: USD
- aggregation: sum
  description: 24-hour WhatsApp Business conversations, billed by category and country.
  dimensions:
  - waba_id
  - category
  - country
  name: whatsapp_conversations
  unit: conversation
- aggregation: max
  description: X-App-Usage percentage (call_count / total_cputime / total_time) — operational meter for throttling proximity.
  dimensions:
  - app
  name: app_usage_pct
  unit: percent
name: Facebook Finops
provider_name: Facebook
provider_slug: facebook
publisher_name: Meta Platforms, Inc.
service_category: Advertising / Social Media
slug: facebook-finops
source_filename: facebook-finops.yml
source_heading: FinOps Profile
source_url: https://developers.facebook.com/docs/graph-api/overview/rate-limiting
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Facebook\nproviderId: facebook\npublisherName: Meta Platforms, Inc.\nserviceCategory: Advertising / Social Media\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Advertising\n  - Content Publishing\n  - Messaging\n  - Social Media\n  - Social Networking\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Facebook (Meta) APIs: the Graph and Marketing APIs are free at\n  the API layer; spend is downstream — ad campaign budgets billed by Meta Ads, and per-conversation pricing\n  for WhatsApp Business. API-level FinOps focuses on quota burn (rate-limit headers) rather than direct\n  API charges.'\nsources:\n  - https://developers.facebook.com/docs/graph-api/overview/rate-limiting\n\
  \  - https://www.facebook.com/business/ads/pricing\n  - https://developers.facebook.com/docs/whatsapp/pricing\nprinciples:\n  - name: Visibility\n    description: Read X-App-Usage, X-Business-Use-Case-Usage, X-Ad-Account-Usage, and X-Page-Usage on every\n      response and feed those percentages into a dashboard so quota burn is observable per app and per\n      ad account.\n  - name: Allocation\n    description: Tag each Graph/Marketing call with the consuming app, ad account, page, and team; Meta\n      Ads spend is naturally allocated by ad account and campaign in Ads Manager.\n  - name: Optimization\n    description: Batch Graph API calls (use ?fields=, batch endpoint, or webhook subscriptions) to keep\n      total_cputime low; reduce User Errors to preserve the Standard-tier Ads Insights ceiling; route\n      WhatsApp messages through the customer-service window when possible (free service conversations).\n  - name: Accountability\n    description: Per-app owners own the App Review\
  \ tier; per-ad-account owners own campaign spend; per-WhatsApp-business-account\n      owners own conversation spend. Reconcile Meta Ads invoices and WhatsApp conversation reports monthly.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Free API + Downstream Ad Spend + Per-Conversation Messaging\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies by country)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Facebook (Meta) APIs\n  ServiceCategory: Advertising / Social Media\n  ProviderName: Meta\n  PublisherName: Meta Platforms, Inc.\n  InvoiceIssuerName: Meta Platforms, Inc.\n  PricingCategory: Free API + Usage (downstream)\n  PricingUnit: varies (impression, conversation, ad-spend USD)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: graph_api_calls\n    description: Count of Graph/Marketing API calls; not directly billed but counts against rate-limit\n      formulas.\n    unit: call\n    aggregation: sum\n    dimensions:\n      - app\n      - business_id\n      - ad_account\n      - endpoint\n  - name: ad_spend\n    description: Ad campaign spend billed via Meta Ads.\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - ad_account\n\
  \      - campaign\n      - placement\n      - country\n  - name: whatsapp_conversations\n    description: 24-hour WhatsApp Business conversations, billed by category and country.\n    unit: conversation\n    aggregation: sum\n    dimensions:\n      - waba_id\n      - category\n      - country\n  - name: app_usage_pct\n    description: X-App-Usage percentage (call_count / total_cputime / total_time) — operational meter\n      for throttling proximity.\n    unit: percent\n    aggregation: max\n    dimensions:\n      - app\napis:\n  - name: Facebook Graph API\n    baseURL: https://graph.facebook.com\n    tags:\n      - Comments\n      - Graph\n      - Pages\n      - Photos\n      - Posts\n      - Social\n      - Users\n      - Videos\n    serviceName: Facebook Graph API\n    serviceCategory: API\n  - name: Facebook Marketing API\n    baseURL: https://graph.facebook.com\n    tags:\n      - Ad Campaigns\n      - Advertising\n      - Audiences\n      - Insights\n      - Marketing\n    serviceName:\
  \ Facebook Marketing API\n    serviceCategory: API\n  - name: Instagram API\n    baseURL: https://graph.facebook.com\n    tags:\n      - Content Management\n      - Instagram\n      - Media\n      - Social Media\n    serviceName: Instagram API\n    serviceCategory: API\n  - name: Messenger Platform API\n    baseURL: https://graph.facebook.com\n    tags:\n      - Bots\n      - Chat\n      - Messaging\n      - Messenger\n    serviceName: Messenger Platform API\n    serviceCategory: API\n  - name: Threads API\n    baseURL: https://graph.threads.net\n    tags:\n      - Content Publishing\n      - Social Media\n      - Threads\n    serviceName: Threads API\n    serviceCategory: API\n  - name: WhatsApp Business API\n    baseURL: https://graph.facebook.com\n    tags:\n      - Business Messaging\n      - Customer Communication\n      - WhatsApp\n    serviceName: WhatsApp Business API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Impressions (CPM)\n    metric: ad_spend / (impressions\
  \ / 1000)\n    target: campaign-dependent\n  - name: Cost per WhatsApp Conversation\n    metric: whatsapp_spend / whatsapp_conversations\n    target: see WhatsApp Business pricing by country\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/facebook/refs/heads/main/finops/facebook-finops.yml
sources:
- https://developers.facebook.com/docs/graph-api/overview/rate-limiting
- https://www.facebook.com/business/ads/pricing
- https://developers.facebook.com/docs/whatsapp/pricing
specification: FinOps Framework
tags:
- Advertising
- Content Publishing
- Messaging
- Social Media
- Social Networking
- FinOps
- Cost Management
- FOCUS
---
