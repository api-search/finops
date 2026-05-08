---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Subscription
  - Usage
  pricingCategory: Subscription + Credits
description: FOCUS-aligned FinOps profile for Clearbit. With HubSpot's acquisition, cost is consolidating onto HubSpot's invoice as a Breeze Intelligence add-on (credit-based). Legacy Clearbit annual contracts remain in force for existing customers. Optimize by tracking credit-per-enrichment, eliminating duplicate vendors, and right-sizing the Breeze credit pack at renewal.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: HubSpot
  ProviderName: HubSpot
  PublisherName: HubSpot
  ServiceCategory: Sales Intelligence
  ServiceName: Clearbit / Breeze Intelligence
layout: finops
meters:
- aggregation: sum
  description: Credits consumed per enrichment call.
  dimensions:
  - endpoint
  name: enrichment_credits
  unit: credit
- aggregation: sum
  description: Reveal IP lookups.
  dimensions:
  - domain
  name: reveal_lookups
  unit: lookup
name: Clearbit Finops
provider_name: Clearbit (HubSpot Breeze Intelligence)
provider_slug: clearbit
publisher_name: HubSpot (Clearbit)
service_category: Sales Intelligence
slug: clearbit-finops
source_filename: clearbit-finops.yml
source_heading: FinOps Profile
source_url: https://www.hubspot.com/products/breeze-intelligence
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Clearbit (HubSpot Breeze Intelligence)\nproviderId: clearbit\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Sales Intelligence\n- B2B\n- Enrichment\n- Reveal\n- HubSpot\n- Marketing\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Clearbit. With HubSpot's acquisition, cost is consolidating onto\n  HubSpot's invoice as a Breeze Intelligence add-on (credit-based). Legacy Clearbit annual contracts\n  remain in force for existing customers. Optimize by tracking credit-per-enrichment, eliminating\n  duplicate vendors, and right-sizing the Breeze credit pack at renewal.\nnotes: Migrating onto HubSpot invoice as Breeze Intelligence credits.\nsources:\n- https://www.hubspot.com/products/breeze-intelligence\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation\
  \ Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: HubSpot (Clearbit)\nserviceCategory: Sales Intelligence\nbillingModel:\n  pricingCategory: Subscription + Credits\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Subscription\n  - Usage\nfocusColumns:\n  ServiceName: Clearbit / Breeze Intelligence\n  ServiceCategory: Sales Intelligence\n  ProviderName: HubSpot\n  PublisherName: HubSpot\n  InvoiceIssuerName: HubSpot\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n- name: enrichment_credits\n  description: Credits consumed per enrichment call.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - endpoint\n- name: reveal_lookups\n  description: Reveal IP lookups.\n  unit: lookup\n  aggregation: sum\n  dimensions:\n  - domain\nprinciples:\n- name: Visibility\n  description: Pull HubSpot Breeze\
  \ Intelligence credit reports; reconcile with marketing automation usage.\n- name: Allocation\n  description: Allocate credits to marketing-ops and revenue programs.\n- name: Optimization\n  description: Cache enrichments aggressively; consolidate vendors with overlap.\n- name: Accountability\n  description: Marketing-Ops owns Breeze pack purchasing and renewal.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/clearbit/refs/heads/main/finops/clearbit-finops.yml
sources:
- https://www.hubspot.com/products/breeze-intelligence
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Sales Intelligence
- B2B
- Enrichment
- Reveal
- HubSpot
- Marketing
- FinOps
- Cost Management
- FOCUS
---
