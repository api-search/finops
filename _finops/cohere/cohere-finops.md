---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cohere-chat-api-openapi.yml
  format: yaml
  label: Cohere Chat API
  slug: chat-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-chat-api-openapi.yml
- filename: cohere-embed-api-openapi.yml
  format: yaml
  label: Cohere Embed API
  slug: embed-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-embed-api-openapi.yml
- filename: cohere-rerank-api-openapi.yml
  format: yaml
  label: Cohere Rerank API
  slug: rerank-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-rerank-api-openapi.yml
- filename: cohere-classify-api-openapi.yml
  format: yaml
  label: Cohere Classify API
  slug: classify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-classify-api-openapi.yml
- filename: cohere-embed-jobs-api-openapi.yml
  format: yaml
  label: Cohere Embed Jobs API
  slug: embed-jobs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-embed-jobs-api-openapi.yml
- filename: cohere-datasets-api-openapi.yml
  format: yaml
  label: Cohere Datasets API
  slug: datasets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-datasets-api-openapi.yml
- filename: cohere-models-api-openapi.yml
  format: yaml
  label: Cohere Models API
  slug: models-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-models-api-openapi.yml
- filename: cohere-tokenize-api-openapi.yml
  format: yaml
  label: Cohere Tokenize API
  slug: tokenize-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-tokenize-api-openapi.yml
- filename: cohere-detokenize-api-openapi.yml
  format: yaml
  label: Cohere Detokenize API
  slug: detokenize-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-detokenize-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Token
description: FOCUS-aligned FinOps for Cohere.
focus_columns:
  BillingCurrency: USD
  ProviderName: Cohere
  PublisherName: Cohere
  ServiceCategory: AI and Machine Learning
  ServiceName: Cohere
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
  name: embed_tokens
  unit: token
- aggregation: sum
  name: rerank_searches
  unit: search
name: Cohere Finops
provider_name: cohere
provider_slug: cohere
publisher_name: Cohere
service_category: AI and Machine Learning
slug: cohere-finops
source_filename: cohere-finops.yml
source_heading: FinOps Profile
source_url: https://cohere.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cohere\nproviderId: cohere\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI and Machine Learning\ndescription: FOCUS-aligned FinOps for Cohere.\nsources:\n  - https://cohere.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cohere\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Per-Token\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Cohere\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Cohere\n  PublisherName: Cohere\n  BillingCurrency: USD\nmeters:\n  - name: input_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n     \
  \ - model\n  - name: output_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n  - name: embed_tokens\n    unit: token\n    aggregation: sum\n  - name: rerank_searches\n    unit: search\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Cohere consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size models/tiers; use caching and batching.\n  - name: Accountability\n    description: Set hard spend limits; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/finops/cohere-finops.yml
sources:
- https://cohere.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI and Machine Learning
---
