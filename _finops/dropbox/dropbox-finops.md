---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: dropbox-openapi-original.yml
  format: yaml
  label: Dropbox API
  slug: dropbox-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dropbox/refs/heads/main/openapi/dropbox-openapi-original.yml
- filename: dropbox-sign-openapi-original.yml
  format: yaml
  label: Dropbox Sign API
  slug: dropbox-sign-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dropbox/refs/heads/main/openapi/dropbox-sign-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Seat Subscription
description: FOCUS-aligned FinOps for Dropbox.
focus_columns:
  BillingCurrency: USD
  ProviderName: Dropbox
  PublisherName: Dropbox
  ServiceCategory: File Storage
  ServiceName: Dropbox
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: max
  name: pooled_storage
  unit: TB-month
- aggregation: sum
  name: transfer_volume
  unit: GB
- aggregation: sum
  name: sign_requests
  unit: request
name: Dropbox Finops
provider_name: Dropbox
provider_slug: dropbox
publisher_name: Dropbox
service_category: File Storage
slug: dropbox-finops
source_filename: dropbox-finops.yml
source_heading: FinOps Profile
source_url: https://www.dropbox.com/plans
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Dropbox\nproviderId: dropbox\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - File Storage\ndescription: FOCUS-aligned FinOps for Dropbox.\nsources:\n  - https://www.dropbox.com/plans\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Dropbox\nserviceCategory: File Storage\nbillingModel:\n  pricingCategory: Per-Seat Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Dropbox\n  ServiceCategory: File Storage\n  ProviderName: Dropbox\n  PublisherName: Dropbox\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n\
  \  - name: pooled_storage\n    unit: TB-month\n    aggregation: max\n  - name: transfer_volume\n    unit: GB\n    aggregation: sum\n  - name: sign_requests\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Dropbox consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dropbox/refs/heads/main/finops/dropbox-finops.yml
sources:
- https://www.dropbox.com/plans
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- File Storage
---
