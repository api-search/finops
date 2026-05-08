---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fly-io-machines-api-openapi.yml
  format: yaml
  label: Fly.io Machines API
  slug: machines-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fly-io/refs/heads/main/openapi/fly-io-machines-api-openapi.yml
- filename: fly-io-extensions-api-openapi.yml
  format: yaml
  label: Fly.io Extensions API
  slug: extensions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fly-io/refs/heads/main/openapi/fly-io-extensions-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go (Per-Second)
description: FOCUS-aligned FinOps for Fly.io.
focus_columns:
  BillingCurrency: USD
  ProviderName: Fly.io
  PublisherName: Fly.io
  ServiceCategory: Edge Hosting
  ServiceName: Fly.io
layout: finops
meters:
- aggregation: sum
  dimensions:
  - machine_size
  - region
  name: machine_seconds
  unit: second
- aggregation: max
  name: rootfs_storage
  unit: GB-month
- aggregation: max
  name: volumes
  unit: GB-month
- aggregation: max
  name: snapshots
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  name: egress
  unit: GB
- aggregation: max
  name: ipv4_addresses
  unit: ip-month
- aggregation: max
  name: managed_certificates
  unit: cert-month
name: Fly Io Finops
provider_name: fly-io
provider_slug: fly-io
publisher_name: Fly.io
service_category: Edge Hosting
slug: fly-io-finops
source_filename: fly-io-finops.yml
source_heading: FinOps Profile
source_url: https://fly.io/docs/about/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Fly.io\nproviderId: fly-io\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Edge Hosting\ndescription: FOCUS-aligned FinOps for Fly.io.\nsources:\n  - https://fly.io/docs/about/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Fly.io\nserviceCategory: Edge Hosting\nbillingModel:\n  pricingCategory: Pay-As-You-Go (Per-Second)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Fly.io\n  ServiceCategory: Edge Hosting\n  ProviderName: Fly.io\n  PublisherName: Fly.io\n  BillingCurrency: USD\nmeters:\n  - name: machine_seconds\n    unit: second\n    aggregation: sum\n    dimensions:\n      - machine_size\n\
  \      - region\n  - name: rootfs_storage\n    unit: GB-month\n    aggregation: max\n  - name: volumes\n    unit: GB-month\n    aggregation: max\n  - name: snapshots\n    unit: GB-month\n    aggregation: max\n  - name: egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n  - name: ipv4_addresses\n    unit: ip-month\n    aggregation: max\n  - name: managed_certificates\n    unit: cert-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Fly.io consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fly-io/refs/heads/main/finops/fly-io-finops.yml
sources:
- https://fly.io/docs/about/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Edge Hosting
---
