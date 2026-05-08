---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cloudinary-openapi.yml
  format: yaml
  label: Cloudinary Upload API
  slug: upload
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cloudinary/refs/heads/main/openapi/cloudinary-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Credits
description: FOCUS-aligned FinOps for Cloudinary.
focus_columns:
  BillingCurrency: USD
  ProviderName: Cloudinary
  PublisherName: Cloudinary
  ServiceCategory: Media Cloud
  ServiceName: Cloudinary
layout: finops
meters:
- aggregation: sum
  dimensions:
  - operation
  name: credits_used
  notes: Credits = transformations + storage + bandwidth
  unit: credit
- aggregation: sum
  name: transformations
  unit: transformation
- aggregation: max
  name: managed_storage
  unit: GB-month
- aggregation: sum
  name: delivered_bandwidth
  unit: GB
name: Cloudinary Finops
provider_name: Cloudinary
provider_slug: cloudinary
publisher_name: Cloudinary
service_category: Media Cloud
slug: cloudinary-finops
source_filename: cloudinary-finops.yml
source_heading: FinOps Profile
source_url: https://cloudinary.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cloudinary\nproviderId: cloudinary\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Media Cloud\ndescription: FOCUS-aligned FinOps for Cloudinary.\nsources:\n  - https://cloudinary.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cloudinary\nserviceCategory: Media Cloud\nbillingModel:\n  pricingCategory: Subscription + Credits\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Cloudinary\n  ServiceCategory: Media Cloud\n  ProviderName: Cloudinary\n  PublisherName: Cloudinary\n  BillingCurrency: USD\nmeters:\n  - name: credits_used\n    unit: credit\n    aggregation: sum\n    dimensions:\n\
  \      - operation\n    notes: Credits = transformations + storage + bandwidth\n  - name: transformations\n    unit: transformation\n    aggregation: sum\n  - name: managed_storage\n    unit: GB-month\n    aggregation: max\n  - name: delivered_bandwidth\n    unit: GB\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Cloudinary consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size tier; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudinary/refs/heads/main/finops/cloudinary-finops.yml
sources:
- https://cloudinary.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Media Cloud
---
