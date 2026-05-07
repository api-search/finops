---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: splunk-enterprise-rest-api.yml
  format: yaml
  label: Splunk Enterprise REST API
  slug: splunk-enterprise-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/splunk/refs/heads/main/openapi/splunk-enterprise-rest-api.yml
- filename: openapi.json
  format: json
  label: Splunk Cloud ACS OpenAPI Specification
  slug: splunk-cloud-admin-config-service-openapi
  spec_type: OpenAPI
  url: https://admin.splunk.com/service/info/specs/v2/openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Splunk (now Cisco).
focus_columns:
  BillingCurrency: USD
  ProviderName: Splunk (now Cisco)
  PublisherName: Splunk (now Cisco)
  ServiceCategory: Observability + SIEM
  ServiceName: Splunk (now Cisco)
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
name: Splunk Finops
provider_name: Splunk
provider_slug: splunk
publisher_name: Splunk (now Cisco)
service_category: Observability + SIEM
slug: splunk-finops
source_filename: splunk-finops.yml
source_heading: FinOps Profile
source_url: https://www.splunk.com/en_us/products/pricing.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Splunk (now Cisco)\nproviderId: splunk\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Observability + SIEM\ndescription: FOCUS-aligned FinOps for Splunk (now Cisco).\nsources:\n  - https://www.splunk.com/en_us/products/pricing.html\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Splunk (now Cisco)\nserviceCategory: Observability + SIEM\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Splunk (now Cisco)\n  ServiceCategory: Observability + SIEM\n  ProviderName: Splunk (now Cisco)\n  PublisherName: Splunk\
  \ (now Cisco)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Splunk (now Cisco) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/splunk/refs/heads/main/finops/splunk-finops.yml
sources:
- https://www.splunk.com/en_us/products/pricing.html
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Observability + SIEM
---
