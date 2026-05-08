---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription with Operation Quota
description: FOCUS-aligned FinOps for Make.com.
focus_columns:
  BillingCurrency: USD
  ProviderName: Make.com
  PublisherName: Make.com
  ServiceCategory: iPaaS
  ServiceName: Make.com
layout: finops
meters:
- aggregation: sum
  dimensions:
  - scenario
  name: operations_consumed
  unit: operation
- aggregation: max
  name: active_scenarios
  unit: scenario-month
- aggregation: max
  name: user_seats
  unit: seat-month
name: Make Finops
provider_name: Make
provider_slug: make
publisher_name: Make.com
service_category: iPaaS
slug: make-finops
source_filename: make-finops.yml
source_heading: FinOps Profile
source_url: https://www.make.com/en/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Make.com\nproviderId: make\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - iPaaS\ndescription: FOCUS-aligned FinOps for Make.com.\nsources:\n  - https://www.make.com/en/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Make.com\nserviceCategory: iPaaS\nbillingModel:\n  pricingCategory: Subscription with Operation Quota\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Make.com\n  ServiceCategory: iPaaS\n  ProviderName: Make.com\n  PublisherName: Make.com\n  BillingCurrency: USD\nmeters:\n  - name: operations_consumed\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - scenario\n\
  \  - name: active_scenarios\n    unit: scenario-month\n    aggregation: max\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Make.com consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/make/refs/heads/main/finops/make-finops.yml
sources:
- https://www.make.com/en/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- iPaaS
---
