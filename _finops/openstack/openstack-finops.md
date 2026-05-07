---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openstack-keystone-openapi.yml
  format: yaml
  label: OpenStack Identity (Keystone) API
  slug: keystone
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openstack/refs/heads/main/openapi/openstack-keystone-openapi.yml
- filename: openstack-nova-openapi.yml
  format: yaml
  label: OpenStack Compute (Nova) API
  slug: nova
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openstack/refs/heads/main/openapi/openstack-nova-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (operator-defined)
  chargeCategories:
  - Usage
  pricingCategory: Self-Hosted Open Source (operator chargeback)
description: 'FOCUS-aligned FinOps framing for self-hosted OpenStack: no upstream license fee; cost is driven by underlying hardware, power/cooling, and operator labor. Internal chargeback typically uses Ceilometer/Gnocchi metrics to bill tenants per-vCPU-hour, per-GB-month, and per-network-egress.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: N/A (operator chargeback)
  ProviderName: OpenStack (operator-deployed)
  PublisherName: Open Infrastructure Foundation
  ServiceCategory: Infrastructure / IaaS
  ServiceName: OpenStack
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  - flavor
  - region
  name: vcpu_hours
  unit: vCPU-hour
- aggregation: sum
  dimensions:
  - tenant
  - flavor
  name: memory_gb_hours
  unit: GB-hour
- aggregation: sum
  dimensions:
  - tenant
  - volume_type
  name: block_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - tenant
  - container
  name: object_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - tenant
  - region
  name: network_egress
  unit: GB
- aggregation: sum
  dimensions:
  - tenant
  name: floating_ip_hours
  unit: IP-hour
name: Openstack Finops
provider_name: OpenStack
provider_slug: openstack
publisher_name: Open Infrastructure Foundation
service_category: Infrastructure / IaaS
slug: openstack-finops
source_filename: openstack-finops.yml
source_heading: FinOps Profile
source_url: https://www.openstack.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: OpenStack\nproviderId: openstack\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cloud Platform\n  - Infrastructure as a Service\n  - Open Source\n  - FinOps\n  - FOCUS\nnotes: OpenStack is open-source software; there is no upstream invoice. FinOps shape here describes private-cloud\n  cost-of-running-OpenStack (capex + ops) and the meters operators commonly expose via Ceilometer / Gnocchi\n  / chargeback systems. Public-cloud providers running OpenStack issue their own invoices, modeled separately.\ndescription: 'FOCUS-aligned FinOps framing for self-hosted OpenStack: no upstream license fee; cost is\n  driven by underlying hardware, power/cooling, and operator labor. Internal chargeback typically uses\n  Ceilometer/Gnocchi metrics to bill tenants per-vCPU-hour, per-GB-month, and per-network-egress.'\nsources:\n  - https://www.openstack.org/\n\
  \  - https://docs.openstack.org/ceilometer/latest/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Open Infrastructure Foundation\nserviceCategory: Infrastructure / IaaS\nbillingModel:\n  pricingCategory: Self-Hosted Open Source (operator chargeback)\n  billingFrequency: Monthly (operator-defined)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: OpenStack\n  ServiceCategory: Infrastructure / IaaS\n  ProviderName: OpenStack (operator-deployed)\n  PublisherName: Open Infrastructure Foundation\n  InvoiceIssuerName: N/A (operator chargeback)\n  BillingCurrency: USD\nmeters:\n  - name: vcpu_hours\n    unit: vCPU-hour\n    aggregation: sum\n    dimensions:\n      - tenant\n      - flavor\n      - region\n  - name: memory_gb_hours\n    unit: GB-hour\n    aggregation: sum\n\
  \    dimensions:\n      - tenant\n      - flavor\n  - name: block_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - volume_type\n  - name: object_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - container\n  - name: network_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - tenant\n      - region\n  - name: floating_ip_hours\n    unit: IP-hour\n    aggregation: sum\n    dimensions:\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Use Ceilometer / Gnocchi (or a downstream telemetry stack like Monasca, Prometheus +\n      ceilometer-publisher-prom) to expose per-tenant consumption to finance and engineering.\n  - name: Allocation\n    description: Tag projects/tenants with cost-center metadata; chargeback or showback per project using\n      consumption events from Ceilometer.\n  - name: Optimization\n    description: Right-size flavors, use spot/preemptible-equivalent\
  \ host aggregates, reclaim orphaned\n      volumes and floating IPs, and consolidate idle workloads before adding hardware.\n  - name: Accountability\n    description: Platform/infra team owns operator cost; tenant teams own their project consumption with\n      quotas and chargeback reports.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openstack/refs/heads/main/finops/openstack-finops.yml
sources:
- https://www.openstack.org/
- https://docs.openstack.org/ceilometer/latest/
specification: FinOps Framework
tags:
- Cloud Platform
- Infrastructure as a Service
- Open Source
- FinOps
- FOCUS
---
