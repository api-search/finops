---
aligned_with: {}
api_specs:
- filename: sorsa-openapi.yml
  format: yaml
  label: Sorsa API v3
  slug: sorsa-api-v3
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sorsa/refs/heads/main/openapi/sorsa-openapi.yml
billing_model: {}
description: ''
focus_columns: {}
layout: finops
meters: []
name: Sorsa Finops
provider_name: Sorsa
provider_slug: sorsa
publisher_name: ''
service_category: ''
slug: sorsa-finops
source_filename: sorsa-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "apiCommons: finops/0.1\nfocusAlignment: FOCUS v1.0\nprovider:\n  id: sorsa\n  name: Sorsa Labs\n  url: https://sorsa.io/\ncaptured: '2026-05-16'\nreconciled: false\nreconciliationNotes: >-\n  Sorsa does not publish a FOCUS-aligned billing export or detailed usage CSV\n  schema externally; FinOps mapping below is derived from the public pricing\n  and rate-limits documentation. Fields requiring access to the customer\n  billing portal (invoice line items, usage-by-time, applied discounts) are\n  marked as null and should be confirmed via the Sorsa application UI or a\n  direct request to sales@sorsa.io.\n\nbillingSurface:\n  model: subscription-with-fixed-quota\n  unitOfMeasure: api-call\n  unitDefinition: 1 API call = 1 unit charged against the monthly quota.\n  meteringDimensions:\n    - name: ServiceName\n      value: Sorsa API v3\n    - name: ServiceCategory\n      value: Social Media Data\n    - name: SubServiceCategory\n      value: X (Twitter) Real-Time Data\n    - name:\
  \ ResourceType\n      value: HTTPRequest\n    - name: ChargeCategory\n      value: Usage\n    - name: PricingUnit\n      value: requests\n    - name: PricingQuantity\n      value: integer\n    - name: ListUnitPrice\n      values:\n        starter: 0.0049\n        pro: 0.00199\n        enterprise: 0.0018\n    - name: BillingCurrency\n      value: USD\n    - name: BillingPeriodStart\n      value: subscription anniversary date\n    - name: BillingPeriodEnd\n      value: subscription anniversary date + 30d\n\ncharges:\n  - chargeCategory: Usage\n    description: Included monthly requests on the active plan.\n    pricingUnit: requests\n    listUnitPrice:\n      starter: 0.0049\n      pro: 0.00199\n      enterprise: 0.0018\n    billingPeriod: monthly\n  - chargeCategory: Subscription\n    description: Flat monthly subscription fee covering the plan's included quota.\n    billingPeriod: monthly\n    plans:\n      starter: 49\n      pro: 199\n      enterprise: 899\n\ndiscountModel:\n  type: tier-volume-discount\n\
  \  description: >-\n    Effective per-request price decreases at higher tiers — 63% reduction from\n    Starter to Enterprise. No publicly documented overage or commitment-based\n    discount; volume-based custom pricing is available above 500K req/mo.\n\nallocation:\n  costAllocationTags:\n    - name: api-key\n      value: per-API-key (single tenant per key by default)\n    - name: workspace\n      value: not surfaced externally\n  notes: >-\n    Customers can implement multi-tenant allocation by provisioning one Sorsa\n    API key per internal team or product line.\n\ninvoicing:\n  cadence: monthly\n  paymentMethods:\n    - card\n  invoiceAccessPortal: https://app.sorsa.io/\n  invoiceFormat: null\n  usageExport:\n    available: false\n    notes: >-\n      Real-time per-key usage available via GET /key-usage-info, but no\n      downloadable usage CSV/JSON export is documented.\n\nforecasting:\n  approach: linear-from-historical-quota-consumption\n  recommendedPractices:\n    - Poll /key-usage-info\
  \ daily to track burn rate against quota.\n    - Use batch endpoints (/tweet-info-bulk, /info-batch) to reduce request count by up to 100x.\n    - Insert a 50 ms client-side delay between requests to stay under 20 rps without bursts.\n\noptimization:\n  recommendations:\n    - Prefer batch endpoints for any list of profiles or tweets longer than one item.\n    - Cache user profile data; it does not change frequently.\n    - Right-size plan against measured monthly burn — moving from Starter to Pro at sustained 10K+ requests dramatically lowers per-call cost.\n    - Use /username-to-id and /id-to-username conversion endpoints once and store stable user IDs to avoid repeated lookups.\n\nslaAndCredits:\n  publishedSla: false\n  statusPage: https://uptime.sorsa.io/status/v3\n  notes: >-\n    Sorsa publishes a public status page (Uptime Kuma) for the v3 surface but\n    no explicit SLA or service-credit policy is documented externally.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sorsa/refs/heads/main/finops/sorsa-finops.yml
sources: []
specification: ''
tags:
- Twitter
- X
- Social Media
- Data Extraction
- Real-Time
---
