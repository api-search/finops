---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: lucidworks-ai-platform-openapi.yml
  format: yaml
  label: Lucidworks AI Platform API
  slug: ai-platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/openapi/lucidworks-ai-platform-openapi.yml
- filename: lucidworks-embeddings-openapi.yml
  format: yaml
  label: Lucidworks Embeddings and Classification API
  slug: embeddings
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/openapi/lucidworks-embeddings-openapi.yml
- filename: lucidworks-signals-openapi.yml
  format: yaml
  label: Lucidworks Signals API
  slug: signals
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/openapi/lucidworks-signals-openapi.yml
- filename: lucidworks-rules-openapi.yml
  format: yaml
  label: Lucidworks Rules and Query Rewrites API
  slug: rules
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/openapi/lucidworks-rules-openapi.yml
- filename: lucidworks-chunking-openapi.yml
  format: yaml
  label: Lucidworks Content Chunking API
  slug: chunking
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/openapi/lucidworks-chunking-openapi.yml
- filename: lucidworks-models-openapi.yml
  format: yaml
  label: Lucidworks Model Management API
  slug: models
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/openapi/lucidworks-models-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract
description: 'FOCUS-aligned FinOps for Lucidworks: enterprise contract-based pricing for AI Platform and Fusion. Cost is contract-driven; consumption meters are query-volume, document-volume, embedding inference, and Fusion compute footprint.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Lucidworks, Inc.
  ProviderName: Lucidworks
  PublisherName: Lucidworks, Inc.
  ServiceCategory: Enterprise Search
  ServiceName: Lucidworks
layout: finops
meters:
- aggregation: sum
  dimensions:
  - app
  - tenant
  name: queries
  unit: query
- aggregation: sum
  dimensions:
  - tenant
  name: documents_indexed
  unit: document
- aggregation: sum
  dimensions:
  - model
  - tenant
  name: embedding_inferences
  unit: inference
- aggregation: sum
  dimensions:
  - api
  - tenant
  name: ai_platform_calls
  unit: request
- aggregation: sum
  dimensions:
  - cluster
  name: fusion_compute
  unit: instance-hour
name: Lucidworks Finops
provider_name: Lucidworks
provider_slug: lucidworks
publisher_name: Lucidworks, Inc.
service_category: Enterprise Search
slug: lucidworks-finops
source_filename: lucidworks-finops.yml
source_heading: FinOps Profile
source_url: https://lucidworks.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lucidworks\nproviderId: lucidworks\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Enterprise Search\n  - Vector Search\n  - AI Infrastructure\ndescription: 'FOCUS-aligned FinOps for Lucidworks: enterprise contract-based pricing for AI Platform\n  and Fusion. Cost is contract-driven; consumption meters are query-volume, document-volume, embedding\n  inference, and Fusion compute footprint.'\nsources:\n  - https://lucidworks.com/\nnotes: No public pricing/billing docs at reconciliation time; meter list reflects typical billable\n  lines for enterprise search platforms.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Lucidworks,\
  \ Inc.\nserviceCategory: Enterprise Search\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Lucidworks\n  ServiceCategory: Enterprise Search\n  ProviderName: Lucidworks\n  PublisherName: Lucidworks, Inc.\n  InvoiceIssuerName: Lucidworks, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: queries\n    unit: query\n    aggregation: sum\n    dimensions:\n      - app\n      - tenant\n  - name: documents_indexed\n    unit: document\n    aggregation: sum\n    dimensions:\n      - tenant\n  - name: embedding_inferences\n    unit: inference\n    aggregation: sum\n    dimensions:\n      - model\n      - tenant\n  - name: ai_platform_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - tenant\n  - name: fusion_compute\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n\
  principles:\n  - name: Visibility\n    description: Pull tenant query / index / inference metrics from the Lucidworks admin UI; cross-reference\n      against contracted volumes.\n  - name: Allocation\n    description: Map Lucidworks tenants/apps to internal product lines; tag signals events for chargeback.\n  - name: Optimization\n    description: Use rules / query rewrites to reduce inference cost; cache embeddings; tune Fusion cluster\n      sizing to actual load.\n  - name: Accountability\n    description: Owners review contracted-volume burn quarterly; renegotiate at renewal if growth changes\n      mix between AI Platform inference and Fusion compute.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/finops/lucidworks-finops.yml
sources:
- https://lucidworks.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Enterprise Search
- Vector Search
- AI Infrastructure
---
