---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: v0-platform-openapi.json
  format: json
  label: v0 Platform API
  slug: platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/v0/refs/heads/main/openapi/v0-platform-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Subscription + Usage
description: v0 is metered as subscription + monthly credits. FinOps levers center on credit consumption per chat/deployment and per-seat scaling on Team plans.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Vercel
  ProviderName: Vercel
  PublisherName: Vercel
  ServiceCategory: AI
  ServiceName: v0
layout: finops
meters:
- aggregation: sum
  description: v0 credits consumed by chat generations, deployments, and other Platform API operations.
  dimensions:
  - account
  - workspace
  - api_key
  name: credits
  unit: credit
- aggregation: max
  description: Active seats on Team plans.
  dimensions:
  - workspace
  name: seats
  unit: seat
name: V0 Finops
provider_name: v0
provider_slug: v0
publisher_name: Vercel Inc.
service_category: AI
slug: v0-finops
source_filename: v0-finops.yml
source_heading: FinOps Profile
source_url: https://v0.app/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: v0\nproviderId: v0\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- App Builder\n- Vercel\n- FinOps\n- FOCUS\ndescription: v0 is metered as subscription + monthly credits. FinOps levers center on credit consumption per chat/deployment and per-seat scaling on Team plans.\nnotes: Credits are consumed by chat generations and deployments. Invoiced via Vercel.\nsources:\n- https://v0.app/pricing\n- https://vercel.com/docs/v0/api\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Vercel Inc.\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n  - Usage\n  - Purchase\nfocusColumns:\n  ServiceName: v0\n  ServiceCategory: AI\n  ProviderName: Vercel\n  PublisherName: Vercel\n  InvoiceIssuerName: Vercel\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: credits\n  description: v0 credits consumed by chat generations, deployments, and other Platform API operations.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - account\n  - workspace\n  - api_key\n- name: seats\n  description: Active seats on Team plans.\n  unit: seat\n  aggregation: max\n  dimensions:\n  - workspace\nprinciples:\n- name: Visibility\n  description: Use the Platform API rate-limits / usage endpoints and Vercel invoices to track credit burn.\n- name: Allocation\n  description: Allocate by API key or workspace to attribute spend to internal teams.\n- name: Optimization\n  description: Cache prompts, scope generations narrowly, prefer chat reuse over new chats.\n- name: Accountability\n  description: Designate workspace\
  \ owners to monitor monthly credit consumption.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/v0/refs/heads/main/finops/v0-finops.yml
sources:
- https://v0.app/pricing
- https://vercel.com/docs/v0/api
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- App Builder
- Vercel
- FinOps
- FOCUS
---
