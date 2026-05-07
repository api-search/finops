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
  pricingCategory: Subscription + Credit-Based
description: FOCUS-aligned FinOps for imgix.
focus_columns:
  BillingCurrency: USD
  ProviderName: imgix
  PublisherName: imgix
  ServiceCategory: Image CDN
  ServiceName: imgix
layout: finops
meters:
- aggregation: sum
  name: credits_used
  unit: credit
- aggregation: max
  name: storage
  unit: GB-month
- aggregation: sum
  name: bandwidth
  unit: GB
- aggregation: max
  name: master_images
  unit: image-month
name: Imgix Finops
provider_name: Imgix
provider_slug: imgix
publisher_name: imgix
service_category: Image CDN
slug: imgix-finops
source_filename: imgix-finops.yml
source_heading: FinOps Profile
source_url: https://imgix.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: imgix\nproviderId: imgix\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Image CDN\ndescription: FOCUS-aligned FinOps for imgix.\nsources:\n  - https://imgix.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: imgix\nserviceCategory: Image CDN\nbillingModel:\n  pricingCategory: Subscription + Credit-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: imgix\n  ServiceCategory: Image CDN\n  ProviderName: imgix\n  PublisherName: imgix\n  BillingCurrency: USD\nmeters:\n  - name: credits_used\n    unit: credit\n    aggregation: sum\n  - name: storage\n    unit: GB-month\n    aggregation:\
  \ max\n  - name: bandwidth\n    unit: GB\n    aggregation: sum\n  - name: master_images\n    unit: image-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track imgix consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/imgix/refs/heads/main/finops/imgix-finops.yml
sources:
- https://imgix.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Image CDN
---
