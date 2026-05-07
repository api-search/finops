---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tikv-http-api-openapi.yml
  format: yaml
  label: TiKV HTTP Management API
  slug: tikv-http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tikv/refs/heads/main/openapi/tikv-http-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories: []
  pricingCategory: Open Source / No Vendor Bill
description: 'FOCUS-aligned FinOps for TiKV: an Apache 2.0 open-source distributed key-value store with no software-license cost. FinOps focus is on the underlying infrastructure spend (compute, storage, network) the operator runs the cluster on, not on a vendor invoice.'
focus_columns:
  BillingCurrency: USD
  ProviderName: TiKV (CNCF)
  PublisherName: TiKV Authors
  ServiceCategory: Database
  ServiceName: TiKV
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cluster
  - host
  - region
  name: tikv_node_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - cluster
  - region
  name: tikv_storage
  unit: GB-month
name: Tikv Finops
provider_name: TiKV
provider_slug: tikv
publisher_name: TiKV Authors / CNCF
service_category: Database
slug: tikv-finops
source_filename: tikv-finops.yml
source_heading: FinOps Profile
source_url: https://github.com/tikv/tikv
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TiKV\nproviderId: tikv\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Database\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for TiKV: an Apache 2.0 open-source distributed key-value store with\n  no software-license cost. FinOps focus is on the underlying infrastructure spend (compute, storage,\n  network) the operator runs the cluster on, not on a vendor invoice.'\nsources:\n  - https://github.com/tikv/tikv\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: TiKV has no commercial product or vendor invoice. FinOps observability lives in the host cloud\n  (AWS/GCP/Azure FOCUS exports) and the operator's own platform telemetry.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: TiKV Authors / CNCF\nserviceCategory: Database\nbillingModel:\n  pricingCategory: Open Source / No Vendor Bill\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: TiKV\n  ServiceCategory: Database\n  ProviderName: TiKV (CNCF)\n  PublisherName: TiKV Authors\n  BillingCurrency: USD\nmeters:\n  - name: tikv_node_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - host\n      - region\n  - name: tikv_storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - cluster\n      - region\nprinciples:\n  - name: Visibility\n    description: TiKV emits no vendor invoice — pull cluster cost from the underlying cloud's FOCUS export\n      (AWS CUR 2.0, GCP Billing, Azure Cost Management) tagged with the TiKV cluster name.\n  - name: Allocation\n    description: Tag every TiKV node, PV, and load balancer with the owning team\
  \ so cluster cost rolls\n      up to the data-platform group rather than landing in a generic infrastructure bucket.\n  - name: Optimization\n    description: Right-size TiKV node counts based on Region count, replica factor, and gRPC concurrency;\n      use storage classes that match access patterns; consolidate small clusters where consistency boundaries\n      allow.\n  - name: Accountability\n    description: A platform owner is accountable for cluster sizing, upgrade cadence, and any third-party\n      support contract (e.g. PingCAP) used to operate TiKV.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tikv/refs/heads/main/finops/tikv-finops.yml
sources:
- https://github.com/tikv/tikv
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Database
- Open Source
- FinOps
- FOCUS
---
