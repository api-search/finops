---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi
  format: yaml
  label: Lusha Enrichment API
  slug: enrichment
  spec_type: OpenAPI
  url: https://docs.lusha.com/apis/openapi
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Subscription
  - Usage
  pricingCategory: Subscription + Credits
description: FOCUS-aligned FinOps profile for Lusha. Cost is driven by seat-based subscription plus monthly credit consumption. Optimize by matching seat tier to user roles and tracking credit-per-enrichment ratios; consolidate with overlapping vendors (Cognism, Apollo, ZoomInfo) at renewal.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Lusha
  ProviderName: Lusha
  PublisherName: Lusha
  ServiceCategory: Sales Intelligence
  ServiceName: Lusha API
layout: finops
meters:
- aggregation: max
  description: Active user seats.
  dimensions:
  - team
  name: seats
  unit: seat-month
- aggregation: sum
  description: Enrichment credits used.
  dimensions:
  - api
  - endpoint
  name: credits_consumed
  unit: credit
name: Lusha Finops
provider_name: Lusha
provider_slug: lusha
publisher_name: Lusha
service_category: Sales Intelligence
slug: lusha-finops
source_filename: lusha-finops.yml
source_heading: FinOps Profile
source_url: https://www.lusha.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lusha\nproviderId: lusha\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Sales Intelligence\n- B2B\n- Enrichment\n- Contact Data\n- Prospecting\n- Intent\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Lusha. Cost is driven by seat-based subscription plus monthly\n  credit consumption. Optimize by matching seat tier to user roles and tracking credit-per-enrichment\n  ratios; consolidate with overlapping vendors (Cognism, Apollo, ZoomInfo) at renewal.\nnotes: Seat + credits model; renewal-time optimization.\nsources:\n- https://www.lusha.com/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Lusha\nserviceCategory: Sales Intelligence\nbillingModel:\n  pricingCategory: Subscription + Credits\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Subscription\n  - Usage\nfocusColumns:\n  ServiceName: Lusha API\n  ServiceCategory: Sales Intelligence\n  ProviderName: Lusha\n  PublisherName: Lusha\n  InvoiceIssuerName: Lusha\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n- name: seats\n  description: Active user seats.\n  unit: seat-month\n  aggregation: max\n  dimensions:\n  - team\n- name: credits_consumed\n  description: Enrichment credits used.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - api\n  - endpoint\nprinciples:\n- name: Visibility\n  description: Pull monthly credit consumption from the dashboard; reconcile against contract.\n- name: Allocation\n  description: Allocate seats and credits to consuming revenue teams.\n- name: Optimization\n  description: Right-size seat tier; cache enrichments\
  \ to avoid double-charging on dedupe.\n- name: Accountability\n  description: RevOps owns the contract; admin controls credit-pool reset cadence.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lusha/refs/heads/main/finops/lusha-finops.yml
sources:
- https://www.lusha.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Sales Intelligence
- B2B
- Enrichment
- Contact Data
- Prospecting
- Intent
- FinOps
- Cost Management
- FOCUS
---
