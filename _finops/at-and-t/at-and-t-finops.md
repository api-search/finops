---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: at-and-t-sms-api.yaml
  format: yaml
  label: AT&T SMS API
  slug: att-sms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/at-and-t/refs/heads/main/openapi/at-and-t-sms-api.yaml
- filename: at-and-t-in-app-messaging-api.yaml
  format: yaml
  label: AT&T In-App Messaging API
  slug: att-in-app-messaging-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/at-and-t/refs/heads/main/openapi/at-and-t-in-app-messaging-api.yaml
- filename: at-and-t-mvnx-api.yaml
  format: yaml
  label: AT&T MVNX API
  slug: att-mvnx-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/at-and-t/refs/heads/main/openapi/at-and-t-mvnx-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom B2B Contract
description: FOCUS-aligned FinOps for AT&T.
focus_columns:
  BillingCurrency: USD
  ProviderName: AT&T
  PublisherName: AT&T
  ServiceCategory: Telecommunications
  ServiceName: AT&T
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
name: At And T Finops
provider_name: AT&T
provider_slug: at-and-t
publisher_name: AT&T
service_category: Telecommunications
slug: at-and-t-finops
source_filename: at-and-t-finops.yml
source_heading: FinOps Profile
source_url: https://developer.att.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AT&T\nproviderId: at-and-t\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Telecommunications\ndescription: FOCUS-aligned FinOps for AT&T.\nsources:\n  - https://developer.att.com/\n  - https://www.att.com/business/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: AT&T\nserviceCategory: Telecommunications\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: AT&T\n  ServiceCategory: Telecommunications\n  ProviderName: AT&T\n  PublisherName: AT&T\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n    unit: transaction\n    aggregation: sum\n\
  \    dimensions:\n      - product\n  - name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track AT&T consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/at-and-t/refs/heads/main/finops/at-and-t-finops.yml
sources:
- https://developer.att.com/
- https://www.att.com/business/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Telecommunications
---
