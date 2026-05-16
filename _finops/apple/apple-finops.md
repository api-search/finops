---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: app-store-connect-openapi-specification.zip
  format: yaml
  label: App Store Connect API
  slug: app-store-connect-api
  spec_type: OpenAPI
  url: https://developer.apple.com/sample-code/app-store-connect/app-store-connect-openapi-specification.zip
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Apple (App Store + iCloud + Apple Music + Maps).
focus_columns:
  BillingCurrency: USD
  ProviderName: Apple (App Store + iCloud + Apple Music + Maps)
  PublisherName: Apple (App Store + iCloud + Apple Music + Maps)
  ServiceCategory: Consumer Cloud + Developer
  ServiceName: Apple (App Store + iCloud + Apple Music + Maps)
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
name: Apple Finops
provider_name: Apple
provider_slug: apple
publisher_name: Apple (App Store + iCloud + Apple Music + Maps)
service_category: Consumer Cloud + Developer
slug: apple-finops
source_filename: apple-finops.yml
source_heading: FinOps Profile
source_url: https://developer.apple.com/programs/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Apple (App Store + iCloud + Apple Music + Maps)\nproviderId: apple\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Consumer Cloud + Developer\ndescription: FOCUS-aligned FinOps for Apple (App Store + iCloud + Apple Music + Maps).\nsources:\n  - https://developer.apple.com/programs/\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Apple (App Store + iCloud + Apple Music + Maps)\nserviceCategory: Consumer Cloud + Developer\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Apple (App Store + iCloud + Apple\
  \ Music + Maps)\n  ServiceCategory: Consumer Cloud + Developer\n  ProviderName: Apple (App Store + iCloud + Apple Music + Maps)\n  PublisherName: Apple (App Store + iCloud + Apple Music + Maps)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Apple (App Store + iCloud + Apple Music + Maps) consumption monthly.\n  - name: Allocation\n    description:\
  \ Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apple/refs/heads/main/finops/apple-finops.yml
sources:
- https://developer.apple.com/programs/
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Consumer Cloud + Developer
---
