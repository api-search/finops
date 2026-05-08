---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: llamaindex-llamacloud-api-openapi.yml
  format: yaml
  label: LlamaIndex LlamaCloud API
  slug: llamacloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/llamaindex/refs/heads/main/openapi/llamaindex-llamacloud-api-openapi.yml
- filename: llamaindex-llamaparse-api-openapi.yml
  format: yaml
  label: LlamaIndex LlamaParse API
  slug: llamaparse-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/llamaindex/refs/heads/main/openapi/llamaindex-llamaparse-api-openapi.yml
- filename: llamaindex-llamaextract-api-openapi.yml
  format: yaml
  label: LlamaIndex LlamaExtract API
  slug: llamaextract-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/llamaindex/refs/heads/main/openapi/llamaindex-llamaextract-api-openapi.yml
- filename: llamaindex-llamacloud-index-api-openapi.yml
  format: yaml
  label: LlamaIndex LlamaCloud Index API
  slug: llamacloud-index-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/llamaindex/refs/heads/main/openapi/llamaindex-llamacloud-index-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Subscription + Usage
description: 'FOCUS-aligned FinOps for LlamaIndex / LlamaCloud: tiered subscription with included monthly credits plus pay-as-you-go credits at $1.25 per 1,000 credits. Credits are consumed per parsed page with cost varying by parsing tier (basic vs. agentic).'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: LlamaIndex, Inc.
  ProviderName: LlamaIndex
  PublisherName: LlamaIndex, Inc.
  ServiceCategory: AI Infrastructure
  ServiceName: LlamaIndex
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  name: subscription_fee
  unit: month
- aggregation: sum
  dimensions:
  - api
  - tier
  - parsing_mode
  name: credits_consumed
  unit: credit
- aggregation: sum
  dimensions:
  - api
  - parsing_mode
  name: pages_parsed
  unit: page
- aggregation: max
  dimensions:
  - tier
  name: seats
  unit: seat
name: Llamaindex Finops
provider_name: llamaindex
provider_slug: llamaindex
publisher_name: LlamaIndex, Inc.
service_category: AI Infrastructure
slug: llamaindex-finops
source_filename: llamaindex-finops.yml
source_heading: FinOps Profile
source_url: https://www.llamaindex.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: LlamaIndex\nproviderId: llamaindex\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI Infrastructure\n  - LLM\n  - RAG\ndescription: 'FOCUS-aligned FinOps for LlamaIndex / LlamaCloud: tiered subscription with included monthly\n  credits plus pay-as-you-go credits at $1.25 per 1,000 credits. Credits are consumed per parsed page\n  with cost varying by parsing tier (basic vs. agentic).'\nsources:\n  - https://www.llamaindex.ai/pricing\n  - https://developers.llamaindex.ai/python/cloud/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: LlamaIndex, Inc.\nserviceCategory: AI Infrastructure\nbillingModel:\n  pricingCategory: Subscription\
  \ + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: LlamaIndex\n  ServiceCategory: AI Infrastructure\n  ProviderName: LlamaIndex\n  PublisherName: LlamaIndex, Inc.\n  InvoiceIssuerName: LlamaIndex, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subscription_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: credits_consumed\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - api\n      - tier\n      - parsing_mode\n  - name: pages_parsed\n    unit: page\n    aggregation: sum\n    dimensions:\n      - api\n      - parsing_mode\n  - name: seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Track credit consumption in the LlamaCloud dashboard; reconcile parsing-mode usage against\n      the 1,000 credits = $1.25 conversion.\n  - name:\
  \ Allocation\n    description: Tag jobs by team/app via API metadata; map LlamaCloud projects to chargeback codes.\n  - name: Optimization\n    description: Use Auto Mode to route pages between basic and agentic parsing (saves up to 80%); right-size\n      tier vs. PAYG ceiling; cache parsed outputs to avoid re-parsing.\n  - name: Accountability\n    description: Set monthly PAYG ceilings by tier ($500 Starter, $5,000 Pro); Enterprise contract owners\n      review monthly credit burn and renegotiate at scale.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/llamaindex/refs/heads/main/finops/llamaindex-finops.yml
sources:
- https://www.llamaindex.ai/pricing
- https://developers.llamaindex.ai/python/cloud/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI Infrastructure
- LLM
- RAG
---
