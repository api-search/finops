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
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Cisco (Networking + Security + Collaboration).
focus_columns:
  BillingCurrency: USD
  ProviderName: Cisco (Networking + Security + Collaboration)
  PublisherName: Cisco (Networking + Security + Collaboration)
  ServiceCategory: Networking + Security
  ServiceName: Cisco (Networking + Security + Collaboration)
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
name: Cisco Finops
provider_name: Cisco
provider_slug: cisco
publisher_name: Cisco (Networking + Security + Collaboration)
service_category: Networking + Security
slug: cisco-finops
source_filename: cisco-finops.yml
source_heading: FinOps Profile
source_url: https://www.cisco.com/c/en/us/products/index.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cisco (Networking + Security + Collaboration)\nproviderId: cisco\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Networking + Security\ndescription: FOCUS-aligned FinOps for Cisco (Networking + Security + Collaboration).\nsources:\n  - https://www.cisco.com/c/en/us/products/index.html\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cisco (Networking + Security + Collaboration)\nserviceCategory: Networking + Security\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Cisco (Networking + Security + Collaboration)\n\
  \  ServiceCategory: Networking + Security\n  ProviderName: Cisco (Networking + Security + Collaboration)\n  PublisherName: Cisco (Networking + Security + Collaboration)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Cisco (Networking + Security + Collaboration) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost\
  \ centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco/refs/heads/main/finops/cisco-finops.yml
sources:
- https://www.cisco.com/c/en/us/products/index.html
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Networking + Security
---
