---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: google-drive-openapi.yml
  format: yaml
  label: Google Drive API v3
  slug: google-drive-api-v3
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-drive/refs/heads/main/openapi/google-drive-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Google Drive (and Workspace).
focus_columns:
  BillingCurrency: USD
  ProviderName: Google Drive (and Workspace)
  PublisherName: Google Drive (and Workspace)
  ServiceCategory: File Storage and Productivity
  ServiceName: Google Drive (and Workspace)
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
name: Google Drive Finops
provider_name: Google Drive
provider_slug: google-drive
publisher_name: Google Drive (and Workspace)
service_category: File Storage and Productivity
slug: google-drive-finops
source_filename: google-drive-finops.yml
source_heading: FinOps Profile
source_url: https://workspace.google.com/pricing.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Google Drive (and Workspace)\nproviderId: google-drive\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - File Storage and Productivity\ndescription: FOCUS-aligned FinOps for Google Drive (and Workspace).\nsources:\n  - https://workspace.google.com/pricing.html\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Google Drive (and Workspace)\nserviceCategory: File Storage and Productivity\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Google Drive (and Workspace)\n  ServiceCategory: File Storage and Productivity\n\
  \  ProviderName: Google Drive (and Workspace)\n  PublisherName: Google Drive (and Workspace)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Google Drive (and Workspace) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused\
  \ entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-drive/refs/heads/main/finops/google-drive-finops.yml
sources:
- https://workspace.google.com/pricing.html
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- File Storage and Productivity
---
