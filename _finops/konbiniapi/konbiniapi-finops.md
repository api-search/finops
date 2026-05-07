---
aligned_with: {}
api_specs:
- filename: openapi.json
  format: json
  label: KonbiniAPI Main Spec
  slug: main
  spec_type: OpenAPI
  url: https://docs.konbiniapi.com/openapi.json
billing_model: {}
description: ''
focus_columns: {}
layout: finops
meters: []
name: Konbiniapi Finops
provider_name: KonbiniAPI
provider_slug: konbiniapi
publisher_name: ''
service_category: ''
slug: konbiniapi-finops
source_filename: konbiniapi-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "finopsFramework:\n  version: focus-1.0\n  alignment: api-commons-finops-0.1\n\nprovider:\n  id: konbiniapi\n  name: KonbiniAPI\n  url: https://konbiniapi.com/\n\nbillingSurface:\n  pricingModel: prepaid-credits\n  unit: credit\n  unitDefinition: One credit equals one successful API request.\n  currency: USD\n  cycle: monthly\n  paymentProvider: Stripe\n  rollover: false\n  overage: none\n\ncharges:\n  - chargeType: Usage\n    chargeCategory: Subscription\n    serviceName: KonbiniAPI\n    serviceCategory: Social Media Data\n    chargeDescription: >-\n      Monthly subscription that includes a fixed credit allowance. Each successful\n      API request consumes 1 credit; failed requests refund the credit (X-Credits-Used: 0).\n    pricingMethod: Tier\n    pricingCurrency: USD\n    tiers:\n      - sku: plus\n        listPrice: 49.00\n        includedQuantity: 25000\n      - sku: pro\n        listPrice: 99.00\n        includedQuantity: 55000\n      - sku: max\n        listPrice:\
  \ 199.00\n        includedQuantity: 160000\n      - sku: ultra\n        listPrice: 499.00\n        includedQuantity: 450000\n      - sku: custom\n        listPrice: null\n        includedQuantity: null\n\ncostAllocation:\n  taggingSupport:\n    apiKeyTagging: true\n    notes: >-\n      Each account holds one rotatable API key, with credits tied to the account\n      rather than the key. There is no native multi-tenant tagging — teams that need\n      project- or environment-level chargeback should split workloads across\n      separate accounts.\n\nreconciliationData:\n  invoiceSource: Stripe receipts\n  meteringSource:\n    responseHeaders:\n      - X-Credits-Used\n      - X-Credits-Remaining\n    dashboard: https://app.konbiniapi.com\n  refundEvents:\n    - HTTP 4xx (selected) and 5xx are refunded automatically at request time.\n\npractices:\n  inform:\n    - Track X-Credits-Remaining in production telemetry to project burn-down.\n    - Tag outgoing requests with internal cost-center\
  \ labels in your client wrapper\n      (KonbiniAPI does not echo custom tags back).\n  optimize:\n    - Avoid duplicate calls; the API does not cache, so identical lookups burn credits.\n    - Use search endpoints with narrow filters before deep-fetching individual resources.\n    - Choose the smallest tier that satisfies monthly burn; credits do not roll over.\n  operate:\n    - Alert on X-Credits-Remaining below a configurable threshold (e.g., 10%).\n    - Implement HTTP 402 handling that pages the operator before traffic stalls.\n\nsource:\n  reconciledAt: '2026-05-06'\n  reconciledBy: api-evangelist pipeline\n  reconciled: true\n  notes: >-\n    Public pricing and metering captured from konbiniapi.com/pricing and\n    docs.konbiniapi.com on 2026-05-06. Custom tier values omitted (negotiated).\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/konbiniapi/refs/heads/main/finops/konbiniapi-finops.yml
sources: []
specification: ''
tags:
- API
- Social Media
- Instagram
- TikTok
- ActivityStreams 2.0
- Scraping
- Data Extraction
- Public Data
- Influencer Marketing
- Social Listening
- Creator Tools
- MCP
- Model Context Protocol
---
