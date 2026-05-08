---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: airbyte-openapi.yml
  format: yaml
  label: Airbyte
  slug: airbyte
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airbyte/refs/heads/main/openapi/airbyte-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Volume-Based / Capacity
description: FOCUS-aligned FinOps for Airbyte.
focus_columns:
  BillingCurrency: USD
  ProviderName: Airbyte
  PublisherName: Airbyte
  ServiceCategory: Data Integration
  ServiceName: Airbyte
layout: finops
meters:
- aggregation: sum
  dimensions:
  - source
  - destination
  name: rows_synced
  unit: row
- aggregation: max
  name: active_connections
  unit: connection-month
- aggregation: sum
  name: credits_used
  unit: credit
name: Airbyte Finops
provider_name: Airbyte
provider_slug: airbyte
publisher_name: Airbyte
service_category: Data Integration
slug: airbyte-finops
source_filename: airbyte-finops.yml
source_heading: FinOps Profile
source_url: https://airbyte.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Airbyte\nproviderId: airbyte\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Data Integration\ndescription: FOCUS-aligned FinOps for Airbyte.\nsources:\n  - https://airbyte.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Airbyte\nserviceCategory: Data Integration\nbillingModel:\n  pricingCategory: Volume-Based / Capacity\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Airbyte\n  ServiceCategory: Data Integration\n  ProviderName: Airbyte\n  PublisherName: Airbyte\n  BillingCurrency: USD\nmeters:\n  - name: rows_synced\n    unit: row\n    aggregation: sum\n    dimensions:\n      -\
  \ source\n      - destination\n  - name: active_connections\n    unit: connection-month\n    aggregation: max\n  - name: credits_used\n    unit: credit\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Airbyte consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/airbyte/refs/heads/main/finops/airbyte-finops.yml
sources:
- https://airbyte.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Data Integration
---
