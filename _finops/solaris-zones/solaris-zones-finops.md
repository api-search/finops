---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: solaris-zones-management-openapi.yml
  format: yaml
  label: Solaris Zones Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-zones-management-openapi.yml
- filename: solaris-zone-configuration-openapi.yml
  format: yaml
  label: Zone Configuration API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-zone-configuration-openapi.yml
- filename: solaris-zone-administration-openapi.yml
  format: yaml
  label: Zone Administration API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-zone-administration-openapi.yml
- filename: solaris-zone-monitoring-openapi.yml
  format: yaml
  label: Zone Monitoring API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-zone-monitoring-openapi.yml
- filename: solaris-rad-zonemgr-openapi.yml
  format: yaml
  label: RAD Zone Management REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-rad-zonemgr-openapi.yml
- filename: solaris-zone-stats-openapi.yml
  format: yaml
  label: Zones Monitoring Statistics API (libzonestat)
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-zone-stats-openapi.yml
- filename: solaris-kernel-zones-openapi.yml
  format: yaml
  label: Oracle Solaris Kernel Zones API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-kernel-zones-openapi.yml
- filename: solaris-statsstore-openapi.yml
  format: yaml
  label: Oracle Solaris StatsStore and Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-statsstore-openapi.yml
- filename: solaris-unified-archives-openapi.yml
  format: yaml
  label: Oracle Solaris Unified Archives Zones API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/openapi/solaris-unified-archives-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Bundled with Operating System Subscription
description: FOCUS-aligned FinOps placeholder for Solaris Zones. Zones is an OS feature of Oracle Solaris, not a metered API product; cost flows through the Oracle Solaris OS subscription and underlying SPARC/x86 hardware support contracts.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Oracle America, Inc.
  ProviderName: Oracle
  PublisherName: Oracle Corporation
  ServiceCategory: Operating System Virtualization
  ServiceName: Oracle Solaris Zones
layout: finops
meters:
- aggregation: max
  dimensions:
  - host
  - zone_brand
  name: active_zones
  unit: zone
- aggregation: sum
  dimensions:
  - host
  - zone
  name: zone_cpu_seconds
  unit: second
- aggregation: avg
  dimensions:
  - host
  - zone
  name: zone_memory_gb
  unit: GB-month
name: Solaris Zones Finops
provider_name: Solaris Zones
provider_slug: solaris-zones
publisher_name: Oracle Corporation
service_category: Operating System Virtualization
slug: solaris-zones-finops
source_filename: solaris-zones-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/solaris/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Solaris Zones\nproviderId: solaris-zones\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Solaris\n  - Zones\n  - Virtualization\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Solaris Zones. Zones is an OS feature of Oracle Solaris,\n  not a metered API product; cost flows through the Oracle Solaris OS subscription and underlying SPARC/x86\n  hardware support contracts.'\nsources:\n  - https://www.oracle.com/solaris/\n  - https://docs.oracle.com/cd/E37838_01/html/E61038/index.html\nnotes: Solaris Zones is not separately invoiced; Oracle does not publish a per-Zone or per-API-call price.\n  Meters here describe the consumption shape customers should observe locally (zone count, libzonestat\n  CPU/memory, network traffic) so they can model the share of Solaris support cost a workload represents.\nalignedWith:\n\
  \  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Oracle Corporation\nserviceCategory: Operating System Virtualization\nbillingModel:\n  pricingCategory: Bundled with Operating System Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Oracle Solaris Zones\n  ServiceCategory: Operating System Virtualization\n  ProviderName: Oracle\n  PublisherName: Oracle Corporation\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: active_zones\n    unit: zone\n    aggregation: max\n    dimensions:\n      - host\n      - zone_brand\n  - name: zone_cpu_seconds\n    unit: second\n    aggregation: sum\n    dimensions:\n      - host\n      - zone\n  - name: zone_memory_gb\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n\
  \      - host\n      - zone\nprinciples:\n  - name: Visibility\n    description: Use libzonestat, the Solaris StatsStore Analytics REST API, and zonestat(1) to surface\n      per-zone CPU, memory, and IO utilization on each Solaris host.\n  - name: Allocation\n    description: Tag each zone (via zonecfg attributes or naming convention) to the consuming application\n      / cost center; aggregate libzonestat output to produce showback per business unit.\n  - name: Optimization\n    description: Consolidate underutilized zones, prefer non-global zones over kernel zones where isolation\n      requirements allow, and use Unified Archives to migrate workloads onto better-utilized hosts.\n  - name: Accountability\n    description: Solaris platform owner reviews zone density vs. Oracle Solaris support contract to ensure\n      hosts are sized to license obligations and to avoid stranded support cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n\
  \  - FN: Oracle Corporation\n    email: solaris-feedback@oracle.com\n    url: https://www.oracle.com/solaris/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/solaris-zones/refs/heads/main/finops/solaris-zones-finops.yml
sources:
- https://www.oracle.com/solaris/
- https://docs.oracle.com/cd/E37838_01/html/E61038/index.html
specification: FinOps Framework
tags:
- Solaris
- Zones
- Virtualization
- FinOps
- FOCUS
---
