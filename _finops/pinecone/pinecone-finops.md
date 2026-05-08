---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: pinecone-db-control-openapi.yaml
  format: yaml
  label: Pinecone Database Control API
  slug: pinecone-database-control
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/openapi/pinecone-db-control-openapi.yaml
- filename: pinecone-db-data-openapi.yaml
  format: yaml
  label: Pinecone Database Data API
  slug: pinecone-database-data
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/openapi/pinecone-db-data-openapi.yaml
- filename: pinecone-inference-openapi.yaml
  format: yaml
  label: Pinecone Inference API
  slug: pinecone-inference
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/openapi/pinecone-inference-openapi.yaml
- filename: pinecone-assistant-control-openapi.yaml
  format: yaml
  label: Pinecone Assistant Control API
  slug: pinecone-assistant-control
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/openapi/pinecone-assistant-control-openapi.yaml
- filename: pinecone-assistant-data-openapi.yaml
  format: yaml
  label: Pinecone Assistant Data API
  slug: pinecone-assistant-data
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/openapi/pinecone-assistant-data-openapi.yaml
- filename: pinecone-admin-openapi.yaml
  format: yaml
  label: Pinecone Admin API
  slug: pinecone-admin
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/openapi/pinecone-admin-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Usage-Based
description: FOCUS-aligned FinOps for Pinecone.
focus_columns:
  BillingCurrency: USD
  ProviderName: Pinecone
  PublisherName: Pinecone
  ServiceCategory: Vector Database
  ServiceName: Pinecone
layout: finops
meters:
- aggregation: max
  dimensions:
  - index
  name: storage
  unit: GB-month
- aggregation: sum
  name: write_units
  unit: million_writes
- aggregation: sum
  name: read_units
  unit: million_reads
- aggregation: sum
  name: dedicated_read_nodes
  unit: node-hour
- aggregation: max
  name: backups
  unit: GB-month
name: Pinecone Finops
provider_name: Pinecone
provider_slug: pinecone
publisher_name: Pinecone
service_category: Vector Database
slug: pinecone-finops
source_filename: pinecone-finops.yml
source_heading: FinOps Profile
source_url: https://www.pinecone.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Pinecone\nproviderId: pinecone\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Vector Database\ndescription: FOCUS-aligned FinOps for Pinecone.\nsources:\n  - https://www.pinecone.io/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Pinecone\nserviceCategory: Vector Database\nbillingModel:\n  pricingCategory: Subscription + Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Pinecone\n  ServiceCategory: Vector Database\n  ProviderName: Pinecone\n  PublisherName: Pinecone\n  BillingCurrency: USD\nmeters:\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n\
  \      - index\n  - name: write_units\n    unit: million_writes\n    aggregation: sum\n  - name: read_units\n    unit: million_reads\n    aggregation: sum\n  - name: dedicated_read_nodes\n    unit: node-hour\n    aggregation: sum\n  - name: backups\n    unit: GB-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Pinecone consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size models/tiers; use caching and batching.\n  - name: Accountability\n    description: Set hard spend limits; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/finops/pinecone-finops.yml
sources:
- https://www.pinecone.io/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Vector Database
---
