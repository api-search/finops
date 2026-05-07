---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: books-api-openapi.yml
  format: yaml
  label: Books API
  slug: books-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/books-api-openapi.yml
- filename: google-drive-api-openapi.yml
  format: yaml
  label: Google Drive API
  slug: google-drive-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-drive-api-openapi.yml
- filename: google-drive-activity-api-openapi.yml
  format: yaml
  label: Google Drive Activity API
  slug: google-drive-activity-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-drive-activity-api-openapi.yml
- filename: google-drive-labels-api-openapi.yml
  format: yaml
  label: Google Drive Labels API
  slug: google-drive-labels-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-drive-labels-api-openapi.yml
- filename: google-calendar-api-openapi.yml
  format: yaml
  label: Google Calendar API
  slug: google-calendar-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-calendar-api-openapi.yml
- filename: google-gmail-api-openapi.yml
  format: yaml
  label: Google Gmail API
  slug: google-gmail-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-gmail-api-openapi.yml
- filename: google-sheets-api-openapi.yml
  format: yaml
  label: Google Sheets API
  slug: google-sheets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-sheets-api-openapi.yml
- filename: google-docs-api-openapi.yml
  format: yaml
  label: Google Docs API
  slug: google-docs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-docs-api-openapi.yml
- filename: google-gemini-api-openapi.yml
  format: yaml
  label: Google Gemini API
  slug: google-gemini-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-gemini-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Google (Cloud + Ads + Workspace + Maps + YouTube).
focus_columns:
  BillingCurrency: USD
  ProviderName: Google (Cloud + Ads + Workspace + Maps + YouTube)
  PublisherName: Google (Cloud + Ads + Workspace + Maps + YouTube)
  ServiceCategory: Cloud + Ads + Productivity
  ServiceName: Google (Cloud + Ads + Workspace + Maps + YouTube)
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
name: Google Finops
provider_name: Google
provider_slug: google
publisher_name: Google (Cloud + Ads + Workspace + Maps + YouTube)
service_category: Cloud + Ads + Productivity
slug: google-finops
source_filename: google-finops.yml
source_heading: FinOps Profile
source_url: https://cloud.google.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Google (Cloud + Ads + Workspace + Maps + YouTube)\nproviderId: google\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cloud + Ads + Productivity\ndescription: FOCUS-aligned FinOps for Google (Cloud + Ads + Workspace + Maps + YouTube).\nsources:\n  - https://cloud.google.com/pricing\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Google (Cloud + Ads + Workspace + Maps + YouTube)\nserviceCategory: Cloud + Ads + Productivity\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Google (Cloud + Ads + Workspace\
  \ + Maps + YouTube)\n  ServiceCategory: Cloud + Ads + Productivity\n  ProviderName: Google (Cloud + Ads + Workspace + Maps + YouTube)\n  PublisherName: Google (Cloud + Ads + Workspace + Maps + YouTube)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Google (Cloud + Ads + Workspace + Maps + YouTube) consumption monthly.\n  - name: Allocation\n \
  \   description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/finops/google-finops.yml
sources:
- https://cloud.google.com/pricing
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cloud + Ads + Productivity
---
