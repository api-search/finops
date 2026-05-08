---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: netlify-openapi-original.yml
  format: yaml
  label: Netlify API
  slug: netlify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/netlify/refs/heads/main/openapi/netlify-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Credit-Based
description: FOCUS-aligned FinOps for Netlify.
focus_columns:
  BillingCurrency: USD
  ProviderName: Netlify
  PublisherName: Netlify
  ServiceCategory: Edge Hosting
  ServiceName: Netlify
layout: finops
meters:
- aggregation: sum
  name: credits_consumed
  unit: credit
- aggregation: sum
  name: bandwidth
  unit: GB
- aggregation: sum
  name: function_invocations
  unit: invocation
- aggregation: sum
  name: build_minutes
  unit: minute
- aggregation: max
  name: blob_storage
  unit: GB-month
name: Netlify Finops
provider_name: Netlify
provider_slug: netlify
publisher_name: Netlify
service_category: Edge Hosting
slug: netlify-finops
source_filename: netlify-finops.yml
source_heading: FinOps Profile
source_url: https://www.netlify.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Netlify\nproviderId: netlify\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Edge Hosting\ndescription: FOCUS-aligned FinOps for Netlify.\nsources:\n  - https://www.netlify.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Netlify\nserviceCategory: Edge Hosting\nbillingModel:\n  pricingCategory: Subscription + Credit-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Netlify\n  ServiceCategory: Edge Hosting\n  ProviderName: Netlify\n  PublisherName: Netlify\n  BillingCurrency: USD\nmeters:\n  - name: credits_consumed\n    unit: credit\n    aggregation: sum\n  - name: bandwidth\n\
  \    unit: GB\n    aggregation: sum\n  - name: function_invocations\n    unit: invocation\n    aggregation: sum\n  - name: build_minutes\n    unit: minute\n    aggregation: sum\n  - name: blob_storage\n    unit: GB-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Netlify consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/netlify/refs/heads/main/finops/netlify-finops.yml
sources:
- https://www.netlify.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Edge Hosting
---
