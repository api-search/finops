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
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Comcast: consumer/business telecom services priced per published consumer plans; no public API consumption pricing. Meters cover invoice abstractions for Xfinity Business and X1/Flex partner relationships.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Comcast Cable Communications, LLC
  ProviderName: Comcast
  PublisherName: Comcast Cable Communications, LLC
  ServiceCategory: Telecommunications
  ServiceName: Comcast / Xfinity
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service_tier
  - location
  name: business_internet_subscription
  unit: month
- aggregation: sum
  name: voice_lines
  unit: line-month
- aggregation: sum
  dimensions:
  - package
  name: tv_video
  unit: month
- aggregation: sum
  dimensions:
  - device_type
  name: equipment_rental
  unit: month
name: Comcast Finops
provider_name: Comcast
provider_slug: comcast
publisher_name: Comcast Cable Communications, LLC
service_category: Telecommunications
slug: comcast-finops
source_filename: comcast-finops.yml
source_heading: FinOps Profile
source_url: https://developer.comcast.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Comcast\nproviderId: comcast\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Telecommunications\n  - Cable\ndescription: 'FOCUS-aligned FinOps for Comcast: consumer/business telecom services priced per published\n  consumer plans; no public API consumption pricing. Meters cover invoice abstractions for Xfinity Business\n  and X1/Flex partner relationships.'\nsources:\n  - https://developer.comcast.com/\n  - https://www.xfinity.com/business\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Comcast Cable Communications, LLC\nserviceCategory: Telecommunications\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Comcast / Xfinity\n  ServiceCategory: Telecommunications\n  ProviderName: Comcast\n  PublisherName: Comcast Cable Communications, LLC\n  InvoiceIssuerName: Comcast Cable Communications, LLC\n  BillingCurrency: USD\nmeters:\n  - name: business_internet_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - service_tier\n      - location\n  - name: voice_lines\n    unit: line-month\n    aggregation: sum\n  - name: tv_video\n    unit: month\n    aggregation: sum\n    dimensions:\n      - package\n  - name: equipment_rental\n    unit: month\n    aggregation: sum\n    dimensions:\n      - device_type\nprinciples:\n  - name: Visibility\n    description: Reconcile Xfinity Business invoices monthly; pull line-of-business breakdown from the\n      Xfinity Business portal.\n  - name: Allocation\n    description: Tag service IDs\
  \ to site, cost center, or business unit.\n  - name: Optimization\n    description: Right-size service tier per location; consolidate invoices; review at contract renewal.\n  - name: Accountability\n    description: IT or facilities owns each circuit/site; finance owns multi-year contract decisions.\nnotes: No public API consumption pricing; meters cover commercial telecom invoice lines.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/comcast/refs/heads/main/finops/comcast-finops.yml
sources:
- https://developer.comcast.com/
- https://www.xfinity.com/business
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Telecommunications
- Cable
---
