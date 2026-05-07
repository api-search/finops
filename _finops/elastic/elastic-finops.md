---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: elastic-elasticsearch-openapi.yml
  format: yaml
  label: Elasticsearch REST API
  slug: elasticsearch
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elastic/refs/heads/main/openapi/elastic-elasticsearch-openapi.yml
- filename: elastic-kibana-openapi.yml
  format: yaml
  label: Kibana API
  slug: kibana
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elastic/refs/heads/main/openapi/elastic-kibana-openapi.yml
- filename: elastic-cloud-openapi.yml
  format: yaml
  label: Elastic Cloud API
  slug: elastic-cloud
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elastic/refs/heads/main/openapi/elastic-cloud-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Resource-Based + Usage-Based
description: FOCUS-aligned FinOps for Elastic.
focus_columns:
  BillingCurrency: USD
  ProviderName: Elastic
  PublisherName: Elastic
  ServiceCategory: Search and Observability
  ServiceName: Elastic
layout: finops
meters:
- aggregation: max
  dimensions:
  - deployment
  - data_tier
  name: data_storage
  unit: GB-month
- aggregation: sum
  name: cpu_hours
  unit: hour
- aggregation: sum
  name: vcu_hours
  unit: VCU-hour
- aggregation: sum
  name: ingest_volume
  unit: GB
- aggregation: sum
  name: data_transfer
  unit: GB
name: Elastic Finops
provider_name: Elastic
provider_slug: elastic
publisher_name: Elastic
service_category: Search and Observability
slug: elastic-finops
source_filename: elastic-finops.yml
source_heading: FinOps Profile
source_url: https://www.elastic.co/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Elastic\nproviderId: elastic\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Search and Observability\ndescription: FOCUS-aligned FinOps for Elastic.\nsources:\n  - https://www.elastic.co/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Elastic\nserviceCategory: Search and Observability\nbillingModel:\n  pricingCategory: Resource-Based + Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Elastic\n  ServiceCategory: Search and Observability\n  ProviderName: Elastic\n  PublisherName: Elastic\n  BillingCurrency: USD\nmeters:\n  - name: data_storage\n    unit: GB-month\n    aggregation:\
  \ max\n    dimensions:\n      - deployment\n      - data_tier\n  - name: cpu_hours\n    unit: hour\n    aggregation: sum\n  - name: vcu_hours\n    unit: VCU-hour\n    aggregation: sum\n  - name: ingest_volume\n    unit: GB\n    aggregation: sum\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Elastic consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/elastic/refs/heads/main/finops/elastic-finops.yml
sources:
- https://www.elastic.co/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Search and Observability
---
