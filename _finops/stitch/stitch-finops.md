---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: stitch-openapi.yml
  format: yaml
  label: Stitch GraphQL API
  slug: stitch-graphql
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stitch/refs/heads/main/openapi/stitch-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Stitch (Talend / Qlik).
focus_columns:
  BillingCurrency: USD
  ProviderName: Stitch (Talend / Qlik)
  PublisherName: Stitch (Talend / Qlik)
  ServiceCategory: Data Integration
  ServiceName: Stitch (Talend / Qlik)
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
name: Stitch Finops
provider_name: Stitch
provider_slug: stitch
publisher_name: Stitch (Talend / Qlik)
service_category: Data Integration
slug: stitch-finops
source_filename: stitch-finops.yml
source_heading: FinOps Profile
source_url: https://www.stitchdata.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Stitch (Talend / Qlik)\nproviderId: stitch\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Data Integration\ndescription: FOCUS-aligned FinOps for Stitch (Talend / Qlik).\nsources:\n  - https://www.stitchdata.com/pricing/\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Stitch (Talend / Qlik)\nserviceCategory: Data Integration\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Stitch (Talend / Qlik)\n  ServiceCategory: Data Integration\n  ProviderName: Stitch (Talend / Qlik)\n  PublisherName: Stitch (Talend\
  \ / Qlik)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Stitch (Talend / Qlik) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stitch/refs/heads/main/finops/stitch-finops.yml
sources:
- https://www.stitchdata.com/pricing/
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Data Integration
---
