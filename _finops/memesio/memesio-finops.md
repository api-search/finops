---
aligned_with: {}
api_specs:
- filename: openapi
  format: yaml
  label: Memesio API
  slug: ''
  spec_type: OpenAPI
  url: https://memesio.com/api/openapi
billing_model: {}
description: ''
focus_columns: {}
layout: finops
meters: []
name: Memesio Finops
provider_name: Memesio
provider_slug: memesio
publisher_name: ''
service_category: ''
slug: memesio-finops
source_filename: memesio-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "finopsFramework: 2024\nfocusVersion: '1.0'\nprovider:\n  id: memesio\n  name: Memesio\n  url: https://memesio.com/\n  documentation: https://memesio.com/developers/api\n\nreconciled: false\nreconciliationNotes: >\n  Memesio exposes a programmatic billing/usage surface at\n  https://memesio.com/api/billing/usage that returns metered usage events\n  (billing.ai_usage_metered, billing.asset_upload_metered) with estimated\n  USD cost per event and a 30-day window. AI costs are further broken down\n  by provider and capability via the same endpoint. The OpenAPI contract\n  also exposes /api/ai/jobs/{jobId}/complete which writes a metered AI\n  cost record (workerId, output, estimatedCostUsd) — i.e. cost is captured\n  at job completion time. No public price sheet is published, so the\n  unit prices that drive estimatedCostUsd are not externally documented;\n  the structure of the data is real but the rate card is not.\n\ncreated: '2026-05-16'\nmodified: '2026-05-16'\n\nusageSurface:\n\
  \  - id: billing-usage\n    type: HTTP\n    method: GET\n    url: https://memesio.com/api/billing/usage\n    description: 30-day metered usage and estimated cost in USD, including per-event counts and per-AI-provider/capability breakdown.\n    accessControl:\n      authentication: api-key\n      header: x-agent-api-key\n    sampleResponse:\n      windowDays: 30\n      totalEvents: 26\n      totalEstimatedCostUsd: 0.0028\n      byEvent:\n        - event: billing.ai_usage_metered\n          count: 10\n          estimatedCostUsd: 0.002\n        - event: billing.asset_upload_metered\n          count: 16\n          estimatedCostUsd: 0.0008\n      aiCosts:\n        windowDays: 30\n        jobCount: 0\n        byProvider: []\n        byCapability: []\n  - id: ai-job-complete\n    type: HTTP\n    method: POST\n    url: https://memesio.com/api/ai/jobs/{jobId}/complete\n    description: Logs the metered AI cost at job completion (workerId, output, estimatedCostUsd).\n    accessControl:\n      authentication:\
  \ api-key\n\nmeterEvents:\n  - id: billing.ai_usage_metered\n    description: AI consumption event (e.g. caption generation, meme generation, face swap, background remove).\n    chargeCategory: Usage\n    chargeSubcategory: AI\n  - id: billing.asset_upload_metered\n    description: Asset upload (image/video to media pipeline) event.\n    chargeCategory: Usage\n    chargeSubcategory: Storage\n\nfocusMapping:\n  ChargeCategory:\n    - Usage  # AI generation, asset upload\n  ChargeSubcategory:\n    - AI\n    - Storage\n  ServiceCategory:\n    - 'AI and Machine Learning'\n    - 'Storage'\n  BillingCurrency: USD\n  BillingPeriod: rolling-30-day\n  ResourceType:\n    - ai-job\n    - asset\n  ProviderName: Memesio\n  PublisherName: Memesio\n  InvoiceIssuerName: Memesio\n  notes: 'No invoiced billing surface is documented publicly. The /api/billing/usage endpoint returns estimated costs in USD, not invoiced amounts.'\n\ncapabilities:\n  budgetManagement: false\n  showback: true   # /api/billing/usage\
  \ shows per-actor usage and estimated cost\n  chargeback: unknown\n  anomalyDetection: true  # /api/analytics/anomalies/ai exists\n  forecasting: unknown\n  reservedCapacity: false\n\nrelated:\n  - description: Plans surface\n    url: https://raw.githubusercontent.com/api-evangelist/memesio/refs/heads/main/plans/memesio-plans-pricing.yml\n  - description: Rate limits surface\n    url: https://raw.githubusercontent.com/api-evangelist/memesio/refs/heads/main/rate-limits/memesio-rate-limits.yml\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/memesio/refs/heads/main/finops/memesio-finops.yml
sources: []
specification: ''
tags:
- Memes
- Media
- Image Generation
- Content
- Developer Tools
---
