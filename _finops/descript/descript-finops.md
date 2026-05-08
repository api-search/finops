---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: descript-openapi.yml
  format: yaml
  label: Descript Platform API
  slug: descript-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/descript/refs/heads/main/openapi/descript-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Tiered Subscription + Included AI Credits and Media Minutes
description: FOCUS-aligned FinOps view of Descript — a tiered SaaS subscription where consumption is metered in AI credits and media (transcription) minutes drawn from a shared monthly bucket per Drive. API usage during early access does not bill separately; it depletes the same media-minute and AI-credit pools as the in-app editor. reconciled false because Descript does not yet publish a granular usage / billing API to back per-meter reconciliation against FOCUS columns.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Descript, Inc.
  ProviderName: Descript
  PublisherName: Descript, Inc.
  ServiceCategory: Media Editing
  ServiceName: Descript
  ServiceSubcategory: AI Video and Audio Editing
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  - billing_cycle
  name: subscription_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - drive
  - source
  name: media_minutes_consumed
  unit: minute
- aggregation: sum
  dimensions:
  - feature
  - drive
  - underlord_action
  name: ai_credits_consumed
  unit: credit
- aggregation: sum
  dimensions:
  - job_type
  - drive
  name: api_jobs_executed
  unit: job
- aggregation: max
  dimensions:
  - drive
  - access_level
  name: published_project_storage
  unit: project
- aggregation: sum
  dimensions:
  - target_language
  name: translated_minutes
  unit: minute
name: Descript Finops
provider_name: Descript
provider_slug: descript
publisher_name: Descript, Inc.
service_category: Media Editing
slug: descript-finops
source_filename: descript-finops.yml
source_heading: FinOps Profile
source_url: https://www.descript.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Descript\nproviderId: descript\ncreated: '2026-05-06'\nmodified: '2026-05-06'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Video Editing\n  - Audio Editing\n  - AI\ndescription: FOCUS-aligned FinOps view of Descript — a tiered SaaS subscription where consumption is metered in\n  AI credits and media (transcription) minutes drawn from a shared monthly bucket per Drive. API usage during\n  early access does not bill separately; it depletes the same media-minute and AI-credit pools as the in-app\n  editor. reconciled false because Descript does not yet publish a granular usage / billing API to back per-meter\n  reconciliation against FOCUS columns.\nsources:\n  - https://www.descript.com/pricing\n  - https://www.descript.com/api\n  - https://docs.descriptapi.com/\n  - https://help.descript.com/hc/en-us/articles/43370311322509-Descript-API-beta\nalignedWith:\n\
  \  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Descript, Inc.\nserviceCategory: Media Editing\nbillingModel:\n  pricingCategory: Tiered Subscription + Included AI Credits and Media Minutes\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Descript\n  ServiceCategory: Media Editing\n  ServiceSubcategory: AI Video and Audio Editing\n  ProviderName: Descript\n  PublisherName: Descript, Inc.\n  InvoiceIssuerName: Descript, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n      - billing_cycle\n  - name: media_minutes_consumed\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - drive\n\
  \      - source\n  - name: ai_credits_consumed\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - feature\n      - drive\n      - underlord_action\n  - name: api_jobs_executed\n    unit: job\n    aggregation: sum\n    dimensions:\n      - job_type\n      - drive\n  - name: published_project_storage\n    unit: project\n    aggregation: max\n    dimensions:\n      - drive\n      - access_level\n  - name: translated_minutes\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - target_language\nprinciples:\n  - name: Visibility\n    description: Track Drive-level media-minute and AI-credit burn from the Descript Settings > Usage view; correlate API consumption by listing jobs via GET /v1/jobs and inspecting media_seconds_used and ai_credits_used in job results.\n  - name: Allocation\n    description: Use one Drive per cost center or product line so plan seats, media minutes, and AI credits roll up to a single owner. Tag automation by giving each integration its own\
  \ API token scoped to the Drive that should bear the cost.\n  - name: Optimization\n    description: Right-size plan tier to actual monthly transcription minutes; avoid wasted AI credits by batching Underlord prompts into one-shot agent calls rather than chained edits, and pre-trim source media before import. Switch to annual billing for up to 35% savings.\n  - name: Accountability\n    description: Designate a Drive admin to monitor usage, set alerts before media-minute or AI-credit thresholds are reached, and request top-ups during early access. Quarterly reviews should reconcile API job counts against perceived business value.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/descript/refs/heads/main/finops/descript-finops.yml
sources:
- https://www.descript.com/pricing
- https://www.descript.com/api
- https://docs.descriptapi.com/
- https://help.descript.com/hc/en-us/articles/43370311322509-Descript-API-beta
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Video Editing
- Audio Editing
- AI
---
