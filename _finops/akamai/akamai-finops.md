---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: akamai-edgekv-openapi.json
  format: json
  label: Akamai EdgeKV API
  slug: akamai-edgekv-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/akamai/refs/heads/main/openapi/akamai-edgekv-openapi.json
- filename: akamai-edgeworkers-openapi.json
  format: json
  label: Akamai EdgeWorkers API
  slug: akamai-edgeworkers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/akamai/refs/heads/main/openapi/akamai-edgeworkers-openapi.json
- filename: akamai-network-lists-openapi.json
  format: json
  label: Akamai Network Lists API
  slug: akamai-network-lists-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/akamai/refs/heads/main/openapi/akamai-network-lists-openapi.json
- filename: akamai-papi-openapi.json
  format: json
  label: Akamai Property Manager API
  slug: akamai-property-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/akamai/refs/heads/main/openapi/akamai-papi-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Akamai (CDN + Cloud + Security).
focus_columns:
  BillingCurrency: USD
  ProviderName: Akamai (CDN + Cloud + Security)
  PublisherName: Akamai (CDN + Cloud + Security)
  ServiceCategory: CDN + Edge + Cloud
  ServiceName: Akamai (CDN + Cloud + Security)
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
name: Akamai Finops
provider_name: Akamai
provider_slug: akamai
publisher_name: Akamai (CDN + Cloud + Security)
service_category: CDN + Edge + Cloud
slug: akamai-finops
source_filename: akamai-finops.yml
source_heading: FinOps Profile
source_url: https://www.akamai.com/products/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Akamai (CDN + Cloud + Security)\nproviderId: akamai\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - CDN + Edge + Cloud\ndescription: FOCUS-aligned FinOps for Akamai (CDN + Cloud + Security).\nsources:\n  - https://www.akamai.com/products/pricing\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Akamai (CDN + Cloud + Security)\nserviceCategory: CDN + Edge + Cloud\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Akamai (CDN + Cloud + Security)\n  ServiceCategory: CDN + Edge + Cloud\n  ProviderName: Akamai\
  \ (CDN + Cloud + Security)\n  PublisherName: Akamai (CDN + Cloud + Security)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Akamai (CDN + Cloud + Security) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n\
  \  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/akamai/refs/heads/main/finops/akamai-finops.yml
sources:
- https://www.akamai.com/products/pricing
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- CDN + Edge + Cloud
---
