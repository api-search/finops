---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: pinterest-openapi-original.yml
  format: yaml
  label: Pinterest API
  slug: pinterest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinterest/refs/heads/main/openapi/pinterest-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Pinterest.
focus_columns:
  BillingCurrency: USD
  ProviderName: Pinterest
  PublisherName: Pinterest
  ServiceCategory: Social Media + Ads
  ServiceName: Pinterest
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
name: Pinterest Finops
provider_name: Pinterest
provider_slug: pinterest
publisher_name: Pinterest
service_category: Social Media + Ads
slug: pinterest-finops
source_filename: pinterest-finops.yml
source_heading: FinOps Profile
source_url: https://developers.pinterest.com/docs/api/v5/introduction/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Pinterest\nproviderId: pinterest\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Social Media + Ads\ndescription: FOCUS-aligned FinOps for Pinterest.\nsources:\n  - https://developers.pinterest.com/docs/api/v5/introduction/\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Pinterest\nserviceCategory: Social Media + Ads\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Pinterest\n  ServiceCategory: Social Media + Ads\n  ProviderName: Pinterest\n  PublisherName: Pinterest\n  BillingCurrency: USD\nmeters:\n\
  \  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Pinterest consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pinterest/refs/heads/main/finops/pinterest-finops.yml
sources:
- https://developers.pinterest.com/docs/api/v5/introduction/
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Social Media + Ads
---
