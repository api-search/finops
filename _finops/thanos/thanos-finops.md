---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: thanos-query-api.yml
  format: yaml
  label: Thanos Query API
  slug: thanos-query-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/thanos/refs/heads/main/openapi/thanos-query-api.yml
- filename: thanos-store-gateway-openapi.yml
  format: yaml
  label: Thanos Store Gateway API
  slug: thanos-store-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/thanos/refs/heads/main/openapi/thanos-store-gateway-openapi.yml
- filename: thanos-sidecar-openapi.yml
  format: yaml
  label: Thanos Sidecar API
  slug: thanos-sidecar-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/thanos/refs/heads/main/openapi/thanos-sidecar-openapi.yml
- filename: thanos-ruler-openapi.yml
  format: yaml
  label: Thanos Ruler API
  slug: thanos-ruler-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/thanos/refs/heads/main/openapi/thanos-ruler-openapi.yml
- filename: thanos-receive-openapi.yml
  format: yaml
  label: Thanos Receive API
  slug: thanos-receive-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/thanos/refs/heads/main/openapi/thanos-receive-openapi.yml
- filename: thanos-compact-openapi.yml
  format: yaml
  label: Thanos Compact API
  slug: thanos-compact-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/thanos/refs/heads/main/openapi/thanos-compact-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: On-Demand
  chargeCategories:
  - Usage
  pricingCategory: Open Source
description: 'FOCUS-aligned FinOps for Thanos: Thanos itself is free Apache 2.0 software; the FinOps surface is the underlying object storage (S3 / GCS / Azure Blob), compute, and egress that operators incur when running Thanos as long-term storage for Prometheus metrics.'
focus_columns:
  BillingCurrency: USD
  ProviderName: Thanos
  PublisherName: Thanos contributors (CNCF)
  ServiceCategory: Observability
  ServiceName: Thanos
layout: finops
meters:
- aggregation: avg
  dimensions:
  - storage_class
  - retention_tier
  name: object_storage_bytes
  unit: GB-month
- aggregation: sum
  dimensions:
  - operation
  - component
  name: object_storage_requests
  unit: request
- aggregation: sum
  dimensions:
  - component
  name: query_compute_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - direction
  name: cross_az_egress
  unit: GB
name: Thanos Finops
provider_name: Thanos
provider_slug: thanos
publisher_name: Thanos contributors (CNCF)
service_category: Observability
slug: thanos-finops
source_filename: thanos-finops.yml
source_heading: FinOps Profile
source_url: https://thanos.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Thanos\nproviderId: thanos\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Observability\n  - Open Source\ndescription: >-\n  FOCUS-aligned FinOps for Thanos: Thanos itself is free Apache 2.0 software; the FinOps surface is the\n  underlying object storage (S3 / GCS / Azure Blob), compute, and egress that operators incur when running\n  Thanos as long-term storage for Prometheus metrics.\nsources:\n  - https://thanos.io/\n  - https://thanos.io/tip/operating/cross-cluster-tls-communication.md/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Thanos contributors (CNCF)\nserviceCategory:\
  \ Observability\nbillingModel:\n  pricingCategory: Open Source\n  billingFrequency: On-Demand\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Thanos\n  ServiceCategory: Observability\n  ProviderName: Thanos\n  PublisherName: Thanos contributors (CNCF)\n  BillingCurrency: USD\nmeters:\n  - name: object_storage_bytes\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - storage_class\n      - retention_tier\n  - name: object_storage_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - operation\n      - component\n  - name: query_compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - component\n  - name: cross_az_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - direction\nprinciples:\n  - name: Visibility\n    description: Thanos itself emits Prometheus metrics for storage requests, blocks, and query latency;\n      pair these with the cloud object-store provider's\
  \ billing export to attribute spend.\n  - name: Allocation\n    description: Tag Thanos components by team / environment / tenant in the cloud where they run so object-storage\n      and compute spend is allocable in FOCUS-aligned exports.\n  - name: Optimization\n    description: Right-size retention, enable downsampling (5m/1h) for older data, configure storage classes\n      / tiering on the object store, tune Compactor cadence, and place Querier near data to reduce egress.\n  - name: Accountability\n    description: Observability platform team owns Thanos infra spend and reviews per-tenant cardinality\n      and retention against an agreed budget.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/thanos/refs/heads/main/finops/thanos-finops.yml
sources:
- https://thanos.io/
- https://thanos.io/tip/operating/cross-cluster-tls-communication.md/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Observability
- Open Source
---
