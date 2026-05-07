---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: vitess-vtadmin-openapi.yml
  format: yaml
  label: Vitess VTAdmin API
  slug: vtadmin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vitess/refs/heads/main/openapi/vitess-vtadmin-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories: []
  pricingCategory: Open Source (Apache 2.0)
description: Vitess is an Apache-2.0 open-source project; there is no project-level invoice or metered billing surface. Operator cost lives in the underlying compute / storage / network resources that run Vitess and its MySQL shards, which are reported by the underlying cloud provider's FOCUS feed.
focus_columns:
  BillingCurrency: USD
  ProviderName: Cloud Native Computing Foundation
  PublisherName: Cloud Native Computing Foundation
  ServiceCategory: Open Source Database
  ServiceName: Vitess
layout: finops
meters:
- aggregation: sum
  dimensions:
  - role
  - instance_type
  name: compute_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - shard
  name: storage_capacity
  unit: GB-month
- aggregation: sum
  dimensions:
  - direction
  name: network_egress
  unit: GB
name: Vitess Finops
provider_name: Vitess
provider_slug: vitess
publisher_name: Cloud Native Computing Foundation
service_category: Open Source Database
slug: vitess-finops
source_filename: vitess-finops.yml
source_heading: FinOps Profile
source_url: https://vitess.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Vitess\nproviderId: vitess\npublisherName: Cloud Native Computing Foundation\nserviceCategory: Open Source Database\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Open Source\n  - Database\n  - MySQL\ndescription: Vitess is an Apache-2.0 open-source project; there is no project-level invoice or\n  metered billing surface. Operator cost lives in the underlying compute / storage / network\n  resources that run Vitess and its MySQL shards, which are reported by the underlying cloud\n  provider's FOCUS feed.\nsources:\n  - https://vitess.io/\nnotes: No commercial billing surface. Treat Vitess cost as a workload allocation against the\n  hosting\
  \ cloud's compute, storage, and network meters.\nbillingModel:\n  pricingCategory: Open Source (Apache 2.0)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Vitess\n  ServiceCategory: Open Source Database\n  ProviderName: Cloud Native Computing Foundation\n  PublisherName: Cloud Native Computing Foundation\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - role\n      - instance_type\n  - name: storage_capacity\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - shard\n  - name: network_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - direction\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the hosting cloud's cost-and-usage report and from Vitess\n      operational dashboards (vtgate / vtablet metrics, query stats); there is no Vitess-issued\n      invoice.\n  - name: Allocation\n    description:\
  \ Tag the cloud resources that run Vitess (Kubernetes namespace, instance group,\n      EBS volume) with the consuming workload to attribute cost back to product teams.\n  - name: Optimization\n    description: Levers are infrastructure-driven - shard right-sizing, autoscaling vtgate,\n      reserved-instance commitments on the MySQL backends, query consolidator tuning, and shard\n      consolidation as workloads shrink.\n  - name: Accountability\n    description: The platform / database team that operates the Vitess deployment owns the cost\n      line; finance allocates back to consuming teams via tagging rules.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vitess/refs/heads/main/finops/vitess-finops.yml
sources:
- https://vitess.io/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Open Source
- Database
- MySQL
---
