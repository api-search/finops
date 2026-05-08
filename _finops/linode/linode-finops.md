---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: linode-api-v4-openapi.yml
  format: yaml
  label: Linode API V4
  slug: api-v4
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linode/refs/heads/main/openapi/linode-api-v4-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Instance Subscription + Hourly Metered
description: FOCUS-aligned FinOps for Linode (Akamai Cloud).
focus_columns:
  BillingCurrency: USD
  ProviderName: Linode (Akamai Cloud)
  PublisherName: Linode (Akamai Cloud)
  ServiceCategory: Cloud Compute
  ServiceName: Linode (Akamai Cloud)
layout: finops
meters:
- aggregation: sum
  dimensions:
  - plan
  - region
  name: instance_hours
  unit: instance-hour
- aggregation: max
  name: object_storage
  unit: GB-month
- aggregation: sum
  name: data_transfer_egress
  unit: GB
- aggregation: sum
  name: managed_db_hours
  unit: instance-hour
- aggregation: sum
  name: lke_node_hours
  unit: node-hour
name: Linode Finops
provider_name: linode
provider_slug: linode
publisher_name: Linode (Akamai Cloud)
service_category: Cloud Compute
slug: linode-finops
source_filename: linode-finops.yml
source_heading: FinOps Profile
source_url: https://www.linode.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Linode (Akamai Cloud)\nproviderId: linode\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cloud Compute\ndescription: FOCUS-aligned FinOps for Linode (Akamai Cloud).\nsources:\n  - https://www.linode.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Linode (Akamai Cloud)\nserviceCategory: Cloud Compute\nbillingModel:\n  pricingCategory: Per-Instance Subscription + Hourly Metered\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Linode (Akamai Cloud)\n  ServiceCategory: Cloud Compute\n  ProviderName: Linode (Akamai Cloud)\n  PublisherName: Linode (Akamai Cloud)\n  BillingCurrency: USD\n\
  meters:\n  - name: instance_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - plan\n      - region\n  - name: object_storage\n    unit: GB-month\n    aggregation: max\n  - name: data_transfer_egress\n    unit: GB\n    aggregation: sum\n  - name: managed_db_hours\n    unit: instance-hour\n    aggregation: sum\n  - name: lke_node_hours\n    unit: node-hour\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Linode (Akamai Cloud) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/linode/refs/heads/main/finops/linode-finops.yml
sources:
- https://www.linode.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cloud Compute
---
