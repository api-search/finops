---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rockwell-factorytalk-optix-openapi.yml
  format: yaml
  label: Rockwell FactoryTalk Optix REST API
  slug: factorytalk-optix-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rockwell-factorytalk/refs/heads/main/openapi/rockwell-factorytalk-optix-openapi.yml
- filename: rockwell-factorytalk-realtime-asyncapi.yml
  format: yaml
  label: Rockwell FactoryTalk Hub API
  slug: factorytalk-hub-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/rockwell-factorytalk/refs/heads/main/asyncapi/rockwell-factorytalk-realtime-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: License-Based
description: Rockwell FactoryTalk is licensed software sold through distributors. FinOps treatment is capex/opex license-driven rather than usage-metered.
focus_columns:
  BillingCurrency: USD
  ProviderName: Rockwell Automation
  PublisherName: Rockwell Automation, Inc.
  ServiceCategory: Industrial Automation Software
  ServiceName: Rockwell FactoryTalk
layout: finops
meters:
- aggregation: sum
  description: FactoryTalk licensed seats and tag counts per site
  dimensions:
  - product
  - site
  name: license_seats
  unit: license
- aggregation: sum
  description: FactoryTalk Hub annual subscription
  dimensions:
  - tier
  - site
  name: hub_subscription
  unit: month
name: Rockwell Factorytalk Finops
provider_name: rockwell-factorytalk
provider_slug: rockwell-factorytalk
publisher_name: Rockwell Automation, Inc.
service_category: Industrial Automation Software
slug: rockwell-factorytalk-finops
source_filename: rockwell-factorytalk-finops.yml
source_heading: FinOps Profile
source_url: https://www.rockwellautomation.com/en-us/products/software/factorytalk.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: rockwell-factorytalk\nproviderId: rockwell-factorytalk\npublisherName: Rockwell Automation, Inc.\nserviceCategory: Industrial Automation Software\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Manufacturing\n  - Industrial\n  - Automation\n  - FinOps\n  - FOCUS\ndescription: >-\n  Rockwell FactoryTalk is licensed software sold through distributors. FinOps treatment is\n  capex/opex license-driven rather than usage-metered.\nnotes: >-\n  No public usage API or itemized billing exists. Cost is dominated by perpetual or\n  subscription license SKUs and FactoryTalk Hub site contracts.\nsources:\n  - https://www.rockwellautomation.com/en-us/products/software/factorytalk.html\n\
  billingModel:\n  pricingCategory: License-Based\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Rockwell FactoryTalk\n  ServiceCategory: Industrial Automation Software\n  ProviderName: Rockwell Automation\n  PublisherName: Rockwell Automation, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: license_seats\n    description: FactoryTalk licensed seats and tag counts per site\n    unit: license\n    aggregation: sum\n    dimensions:\n      - product\n      - site\n  - name: hub_subscription\n    description: FactoryTalk Hub annual subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - site\nprinciples:\n  - name: Visibility\n    description: >-\n      Track FactoryTalk license entitlements and renewal dates through Rockwell's licensing\n      portal and the AP/procurement system.\n  - name: Allocation\n    description: >-\n      Allocate FactoryTalk costs to the manufacturing site\
  \ or production line that consumes\n      the licenses, not to corporate IT.\n  - name: Optimization\n    description: >-\n      Right-size license SKUs against actual tag and user counts; consolidate sites onto Hub\n      where it lowers the per-site total.\n  - name: Accountability\n    description: >-\n      Plant engineering and OT leadership own FactoryTalk license decisions; review annually\n      against site headcount and connected-tag growth.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rockwell-factorytalk/refs/heads/main/finops/rockwell-factorytalk-finops.yml
sources:
- https://www.rockwellautomation.com/en-us/products/software/factorytalk.html
specification: FinOps Framework
tags:
- Manufacturing
- Industrial
- Automation
- FinOps
- FOCUS
---
