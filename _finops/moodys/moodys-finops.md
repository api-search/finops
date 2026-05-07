---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: moodys-data-buffet-api-openapi.yml
  format: yaml
  label: Moody's Data Buffet API
  slug: data-buffet-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/moodys/refs/heads/main/openapi/moodys-data-buffet-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom B2B Contract
description: FOCUS-aligned FinOps for Moody's.
focus_columns:
  BillingCurrency: USD
  ProviderName: Moody's
  PublisherName: Moody's
  ServiceCategory: Financial Data / Ratings
  ServiceName: Moody's
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  name: transactions
  unit: transaction
- aggregation: sum
  name: api_calls
  unit: call
- aggregation: max
  name: annual_contract
  unit: year
name: Moodys Finops
provider_name: Moody's
provider_slug: moodys
publisher_name: Moody's
service_category: Financial Data / Ratings
slug: moodys-finops
source_filename: moodys-finops.yml
source_heading: FinOps Profile
source_url: https://developer.moodys.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Moody's\nproviderId: moodys\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Financial Data / Ratings\ndescription: FOCUS-aligned FinOps for Moody's.\nsources:\n  - https://developer.moodys.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Moody's\nserviceCategory: Financial Data / Ratings\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Moody's\n  ServiceCategory: Financial Data / Ratings\n  ProviderName: Moody's\n  PublisherName: Moody's\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n    unit: transaction\n    aggregation:\
  \ sum\n    dimensions:\n      - product\n  - name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Moody's consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/moodys/refs/heads/main/finops/moodys-finops.yml
sources:
- https://developer.moodys.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Financial Data / Ratings
---
