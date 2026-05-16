---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-teams-graph-api.yaml
  format: yaml
  label: Microsoft Graph Teams API
  slug: microsoft-graph-teams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-teams/refs/heads/main/openapi/microsoft-teams-graph-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Microsoft Teams.
focus_columns:
  BillingCurrency: USD
  ProviderName: Microsoft Teams
  PublisherName: Microsoft Teams
  ServiceCategory: Collaboration
  ServiceName: Microsoft Teams
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
name: Microsoft Teams Finops
provider_name: Microsoft Teams
provider_slug: microsoft-teams
publisher_name: Microsoft Teams
service_category: Collaboration
slug: microsoft-teams-finops
source_filename: microsoft-teams-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/microsoft-teams/compare-microsoft-teams-options
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Teams\nproviderId: microsoft-teams\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Collaboration\ndescription: FOCUS-aligned FinOps for Microsoft Teams.\nsources:\n  - https://www.microsoft.com/en-us/microsoft-teams/compare-microsoft-teams-options\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Teams\nserviceCategory: Collaboration\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Microsoft Teams\n  ServiceCategory: Collaboration\n  ProviderName: Microsoft Teams\n  PublisherName:\
  \ Microsoft Teams\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Microsoft Teams consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly\
  \ review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-teams/refs/heads/main/finops/microsoft-teams-finops.yml
sources:
- https://www.microsoft.com/en-us/microsoft-teams/compare-microsoft-teams-options
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Collaboration
---
