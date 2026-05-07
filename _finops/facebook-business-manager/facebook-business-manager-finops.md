---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: facebook-marketing-openapi.yml
  format: yaml
  label: Facebook Marketing API
  slug: facebook-marketing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/facebook-business-manager/refs/heads/main/openapi/facebook-marketing-openapi.yml
- filename: facebook-pages-openapi.yml
  format: yaml
  label: Facebook Pages API
  slug: facebook-pages-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/facebook-business-manager/refs/heads/main/openapi/facebook-pages-openapi.yml
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
description: 'FOCUS-aligned FinOps for Meta Business Manager (now Meta Business Suite): the API surface is free; spend lands as Meta Ads campaign cost (CPM/CPC/CPA) and per-conversation WhatsApp Business pricing. API-level FinOps focuses on App Review tier and BUC quota burn.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Meta Platforms, Inc.
  PricingCategory: Free API + Usage (downstream)
  PricingUnit: varies (impression, conversation, ad-spend USD)
  ProviderName: Meta
  PublisherName: Meta Platforms, Inc.
  ServiceCategory: Advertising / Business Management
  ServiceName: Meta Business Manager / Business Suite
layout: finops
meters:
- aggregation: sum
  description: Count of Marketing/Pages/Conversions/Catalog Graph API calls; not directly billed but governs rate-limit burn.
  dimensions:
  - app
  - business_id
  - ad_account
  - endpoint
  name: graph_api_calls
  unit: call
- aggregation: sum
  description: Meta Ads campaign spend.
  dimensions:
  - ad_account
  - campaign
  - placement
  - country
  name: ad_spend
  unit: USD
- aggregation: sum
  description: 24-hour WhatsApp Business conversations.
  dimensions:
  - waba_id
  - category
  - country
  name: whatsapp_conversations
  unit: conversation
- aggregation: sum
  description: Conversions API events ingested.
  dimensions:
  - pixel_id
  - event_name
  name: conversion_events
  unit: event
name: Facebook Business Manager Finops
provider_name: Facebook Business Manager
provider_slug: facebook-business-manager
publisher_name: Meta Platforms, Inc.
service_category: Advertising / Business Management
slug: facebook-business-manager-finops
source_filename: facebook-business-manager-finops.yml
source_heading: FinOps Profile
source_url: https://developers.facebook.com/docs/graph-api/overview/rate-limiting
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Facebook Business Manager\nproviderId: facebook-business-manager\npublisherName: Meta Platforms, Inc.\nserviceCategory: Advertising / Business Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Advertising\n  - Analytics\n  - Business Management\n  - Marketing\n  - Social Media\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Meta Business Manager (now Meta Business Suite): the API surface\n  is free; spend lands as Meta Ads campaign cost (CPM/CPC/CPA) and per-conversation WhatsApp Business\n  pricing. API-level FinOps focuses on App Review tier and BUC quota burn.'\nsources:\n  - https://developers.facebook.com/docs/graph-api/overview/rate-limiting\n\
  \  - https://www.facebook.com/business/ads/pricing\n  - https://developers.facebook.com/docs/whatsapp/pricing\nprinciples:\n  - name: Visibility\n    description: Read X-App-Usage, X-Business-Use-Case-Usage, X-Ad-Account-Usage, X-Page-Usage on every\n      response; pull Ads Manager spend reports daily; export WhatsApp conversation logs.\n  - name: Allocation\n    description: Allocate ad spend by ad account → campaign → ad set → ad; allocate WhatsApp spend by\n      WABA ID, category, and country. Tag each Conversions API event with the originating product/team.\n  - name: Optimization\n    description: Batch Marketing/Insights calls (use ?fields= and the batch endpoint); reduce User Errors\n      that erode the Standard Access Ads Insights ceiling; route WhatsApp conversation traffic into the\n      24h customer-service window where free service conversations apply.\n  - name: Accountability\n    description: Per-app owners own the App Review tier; per-ad-account owners own ad spend;\
  \ per-WABA\n      owners own conversation cost. Reconcile Meta Ads invoices and WhatsApp reports monthly against\n      finance ledgers.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - Invoicing and Chargeback\nbillingModel:\n  pricingCategory: Free API + Downstream Ad Spend + Per-Conversation Messaging\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies by country)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n\
  \    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Meta Business Manager / Business Suite\n  ServiceCategory: Advertising / Business Management\n  ProviderName: Meta\n  PublisherName: Meta Platforms, Inc.\n  InvoiceIssuerName: Meta Platforms, Inc.\n  PricingCategory: Free API + Usage (downstream)\n  PricingUnit: varies (impression, conversation, ad-spend USD)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: graph_api_calls\n    description: Count of Marketing/Pages/Conversions/Catalog Graph API calls; not directly billed but\n      governs rate-limit burn.\n    unit: call\n    aggregation: sum\n    dimensions:\n      - app\n      - business_id\n      - ad_account\n      - endpoint\n  - name: ad_spend\n    description: Meta Ads campaign spend.\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - ad_account\n      - campaign\n      - placement\n      - country\n  - name: whatsapp_conversations\n    description: 24-hour WhatsApp Business\
  \ conversations.\n    unit: conversation\n    aggregation: sum\n    dimensions:\n      - waba_id\n      - category\n      - country\n  - name: conversion_events\n    description: Conversions API events ingested.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - pixel_id\n      - event_name\napis:\n  - name: Facebook Marketing API\n    baseURL: https://graph.facebook.com/v18.0\n    serviceName: Facebook Marketing API\n    serviceCategory: API\n  - name: Facebook Pages API\n    baseURL: https://graph.facebook.com/v18.0\n    serviceName: Facebook Pages API\n    serviceCategory: API\n  - name: Facebook Conversions API\n    baseURL: https://graph.facebook.com/v18.0\n    serviceName: Facebook Conversions API\n    serviceCategory: API\n  - name: Facebook Business Asset API\n    baseURL: https://graph.facebook.com/v18.0\n    serviceName: Facebook Business Asset API\n    serviceCategory: API\n  - name: Facebook Insights API\n    baseURL: https://graph.facebook.com/v25.0\n    serviceName:\
  \ Facebook Insights API\n    serviceCategory: API\n  - name: Facebook Catalog API\n    baseURL: https://graph.facebook.com/v25.0\n    serviceName: Facebook Catalog API\n    serviceCategory: API\n  - name: Facebook WhatsApp Business Platform API\n    baseURL: https://graph.facebook.com/v25.0\n    serviceName: Facebook WhatsApp Business Platform API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Impressions (CPM)\n    metric: ad_spend / (impressions / 1000)\n    target: campaign-dependent\n  - name: Cost per WhatsApp Conversation\n    metric: whatsapp_spend / whatsapp_conversations\n    target: see WhatsApp Business pricing by country\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/facebook-business-manager/refs/heads/main/finops/facebook-business-manager-finops.yml
sources:
- https://developers.facebook.com/docs/graph-api/overview/rate-limiting
- https://www.facebook.com/business/ads/pricing
- https://developers.facebook.com/docs/whatsapp/pricing
specification: FinOps Framework
tags:
- Advertising
- Analytics
- Business Management
- Marketing
- Social Media
- FinOps
- Cost Management
- FOCUS
---
