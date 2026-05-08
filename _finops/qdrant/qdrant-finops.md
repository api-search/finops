---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: qdrant-openapi-original.json
  format: json
  label: Qdrant API
  slug: qdrant-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qdrant/refs/heads/main/openapi/qdrant-openapi-original.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Resource-Based
description: FOCUS-aligned FinOps for Qdrant.
focus_columns:
  BillingCurrency: USD
  ProviderName: Qdrant
  PublisherName: Qdrant
  ServiceCategory: Vector Database
  ServiceName: Qdrant
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cluster
  - tier
  name: cluster_resources
  unit: vCPU-hour + GB-RAM-hour + GB-disk-month
- aggregation: max
  name: backup_storage
  unit: GB-month
- aggregation: sum
  name: inference_tokens
  unit: token
name: Qdrant Finops
provider_name: Qdrant
provider_slug: qdrant
publisher_name: Qdrant
service_category: Vector Database
slug: qdrant-finops
source_filename: qdrant-finops.yml
source_heading: FinOps Profile
source_url: https://qdrant.tech/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Qdrant\nproviderId: qdrant\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Vector Database\ndescription: FOCUS-aligned FinOps for Qdrant.\nsources:\n  - https://qdrant.tech/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Qdrant\nserviceCategory: Vector Database\nbillingModel:\n  pricingCategory: Resource-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Qdrant\n  ServiceCategory: Vector Database\n  ProviderName: Qdrant\n  PublisherName: Qdrant\n  BillingCurrency: USD\nmeters:\n  - name: cluster_resources\n    unit: vCPU-hour + GB-RAM-hour + GB-disk-month\n    aggregation: sum\n\
  \    dimensions:\n      - cluster\n      - tier\n  - name: backup_storage\n    unit: GB-month\n    aggregation: max\n  - name: inference_tokens\n    unit: token\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Qdrant consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size models/tiers; use caching and batching.\n  - name: Accountability\n    description: Set hard spend limits; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/qdrant/refs/heads/main/finops/qdrant-finops.yml
sources:
- https://qdrant.tech/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Vector Database
---
