---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Subscription
  pricingCategory: Subscription
description: FOCUS-aligned FinOps profile for Ocean.io. Cost driver is the annual seat-based contract with bundled API credits. Optimize at renewal by right-sizing seats and verifying credit consumption against ICP and lookalike workflow needs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Ocean.io
  ProviderName: Ocean.io
  PublisherName: Ocean.io
  ServiceCategory: Sales Intelligence
  ServiceName: Ocean.io
layout: finops
meters:
- aggregation: max
  description: Active user seats.
  dimensions:
  - team
  name: seats
  unit: seat-month
- aggregation: sum
  description: API credits consumed for enrichment / lookalike calls.
  dimensions:
  - endpoint
  name: api_credits
  unit: credit
name: Ocean Io Finops
provider_name: Ocean.io
provider_slug: ocean-io
publisher_name: Ocean.io
service_category: Sales Intelligence
slug: ocean-io-finops
source_filename: ocean-io-finops.yml
source_heading: FinOps Profile
source_url: https://ocean.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ocean.io\nproviderId: ocean-io\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Sales Intelligence\n- B2B\n- Enrichment\n- Lookalike\n- ABM\n- Prospecting\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Ocean.io. Cost driver is the annual seat-based contract with\n  bundled API credits. Optimize at renewal by right-sizing seats and verifying credit consumption\n  against ICP and lookalike workflow needs.\nnotes: Annual prepaid contract; renewal-time optimization.\nsources:\n- https://ocean.io/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Ocean.io\nserviceCategory:\
  \ Sales Intelligence\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Subscription\nfocusColumns:\n  ServiceName: Ocean.io\n  ServiceCategory: Sales Intelligence\n  ProviderName: Ocean.io\n  PublisherName: Ocean.io\n  InvoiceIssuerName: Ocean.io\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n- name: seats\n  description: Active user seats.\n  unit: seat-month\n  aggregation: max\n  dimensions:\n  - team\n- name: api_credits\n  description: API credits consumed for enrichment / lookalike calls.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - endpoint\nprinciples:\n- name: Visibility\n  description: Track seat utilization and API credit burn monthly.\n- name: Allocation\n  description: Allocate seats and credits to ABM/RevOps teams.\n- name: Optimization\n  description: Right-size at renewal; consolidate with overlapping vendors (Lusha, Cognism).\n- name: Accountability\n  description:\
  \ RevOps owns the contract.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ocean-io/refs/heads/main/finops/ocean-io-finops.yml
sources:
- https://ocean.io/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Sales Intelligence
- B2B
- Enrichment
- Lookalike
- ABM
- Prospecting
- FinOps
- Cost Management
- FOCUS
---
