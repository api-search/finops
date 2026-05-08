---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: perplexity-openapi.json
  format: json
  label: Perplexity Sonar API
  slug: sonar-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/perplexity/refs/heads/main/openapi/perplexity-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Token + Per-Search
description: FOCUS-aligned FinOps for Perplexity.
focus_columns:
  BillingCurrency: USD
  ProviderName: Perplexity
  PublisherName: Perplexity
  ServiceCategory: AI Search
  ServiceName: Perplexity
layout: finops
meters:
- aggregation: sum
  dimensions:
  - model
  name: input_tokens
  unit: token
- aggregation: sum
  dimensions:
  - model
  name: output_tokens
  unit: token
- aggregation: sum
  dimensions:
  - context_size
  name: search_requests
  unit: search
- aggregation: sum
  name: citation_tokens
  unit: token
- aggregation: sum
  name: reasoning_tokens
  unit: token
name: Perplexity Finops
provider_name: Perplexity
provider_slug: perplexity
publisher_name: Perplexity
service_category: AI Search
slug: perplexity-finops
source_filename: perplexity-finops.yml
source_heading: FinOps Profile
source_url: https://docs.perplexity.ai/guides/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Perplexity\nproviderId: perplexity\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI Search\ndescription: FOCUS-aligned FinOps for Perplexity.\nsources:\n  - https://docs.perplexity.ai/guides/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Perplexity\nserviceCategory: AI Search\nbillingModel:\n  pricingCategory: Per-Token + Per-Search\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Perplexity\n  ServiceCategory: AI Search\n  ProviderName: Perplexity\n  PublisherName: Perplexity\n  BillingCurrency: USD\nmeters:\n  - name: input_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n\
  \      - model\n  - name: output_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n  - name: search_requests\n    unit: search\n    aggregation: sum\n    dimensions:\n      - context_size\n  - name: citation_tokens\n    unit: token\n    aggregation: sum\n  - name: reasoning_tokens\n    unit: token\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Perplexity consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size models/tiers; use caching and batching.\n  - name: Accountability\n    description: Set hard spend limits; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/perplexity/refs/heads/main/finops/perplexity-finops.yml
sources:
- https://docs.perplexity.ai/guides/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI Search
---
