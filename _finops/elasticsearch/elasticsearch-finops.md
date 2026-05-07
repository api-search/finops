---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: elasticsearch-specification
  format: yaml
  label: Elasticsearch REST API
  slug: elasticsearch-rest-api
  spec_type: OpenAPI
  url: https://github.com/elastic/elasticsearch-specification
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Elasticsearch (Elastic).
focus_columns:
  BillingCurrency: USD
  ProviderName: Elasticsearch (Elastic)
  PublisherName: Elasticsearch (Elastic)
  ServiceCategory: Search and Observability
  ServiceName: Elasticsearch (Elastic)
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  - region
  - instance_type
  - tenant
  name: compute_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - service
  - tier
  name: storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - egress_type
  - region_pair
  name: data_transfer
  unit: GB
- aggregation: sum
  dimensions:
  - service
  - operation
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - service
  name: managed_services
  unit: varies
name: Elasticsearch Finops
provider_name: Elasticsearch
provider_slug: elasticsearch
publisher_name: Elasticsearch (Elastic)
service_category: Search and Observability
slug: elasticsearch-finops
source_filename: elasticsearch-finops.yml
source_heading: FinOps Profile
source_url: https://www.elastic.co/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Elasticsearch (Elastic)\nproviderId: elasticsearch\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Search and Observability\ndescription: FOCUS-aligned FinOps for Elasticsearch (Elastic).\nsources:\n  - https://www.elastic.co/pricing\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Elasticsearch (Elastic)\nserviceCategory: Search and Observability\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Elasticsearch (Elastic)\n  ServiceCategory: Search and Observability\n  ProviderName: Elasticsearch (Elastic)\n\
  \  PublisherName: Elasticsearch (Elastic)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Elasticsearch (Elastic) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description:\
  \ Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/elasticsearch/refs/heads/main/finops/elasticsearch-finops.yml
sources:
- https://www.elastic.co/pricing
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Search and Observability
---
