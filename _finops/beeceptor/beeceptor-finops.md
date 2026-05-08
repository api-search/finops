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
  pricingCategory: Free / Donation-Funded
description: FOCUS-aligned FinOps for Beeceptor.
focus_columns:
  BillingCurrency: USD
  ProviderName: Beeceptor
  PublisherName: Beeceptor
  ServiceCategory: API Mocking
  ServiceName: Beeceptor
layout: finops
meters:
- aggregation: sum
  name: api_calls
  unit: call
name: Beeceptor Finops
provider_name: Beeceptor
provider_slug: beeceptor
publisher_name: Beeceptor
service_category: API Mocking
slug: beeceptor-finops
source_filename: beeceptor-finops.yml
source_heading: FinOps Profile
source_url: https://beeceptor.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Beeceptor\nproviderId: beeceptor\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - API Mocking\ndescription: FOCUS-aligned FinOps for Beeceptor.\nsources:\n  - https://beeceptor.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Beeceptor\nserviceCategory: API Mocking\nbillingModel:\n  pricingCategory: Free / Donation-Funded\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Beeceptor\n  ServiceCategory: API Mocking\n  ProviderName: Beeceptor\n  PublisherName: Beeceptor\n  BillingCurrency: USD\nmeters:\n  - name: api_calls\n    unit: call\n    aggregation: sum\nprinciples:\n  - name: Visibility\n\
  \    description: Track Beeceptor consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/beeceptor/refs/heads/main/finops/beeceptor-finops.yml
sources:
- https://beeceptor.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- API Mocking
---
