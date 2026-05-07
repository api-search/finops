---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: RHEL 8 Subscription Management API
  slug: subscription-management-api
  spec_type: OpenAPI
  url: https://api.access.redhat.com/management/v1/openapi.json
- filename: openapi.json
  format: json
  label: RHEL 8 Insights API
  slug: insights-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/insights/v1/openapi.json
- filename: openapi.json
  format: json
  label: RHEL 8 Image Builder API
  slug: image-builder-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/image-builder/v1/openapi.json
- filename: openapi.json
  format: json
  label: RHEL 8 Patch Management API
  slug: patch-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/patch/v3/openapi.json
- filename: openapi.json
  format: json
  label: RHEL 8 Vulnerability Management API
  slug: vulnerability-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/vulnerability/v1/openapi.json
- filename: openapi.json
  format: json
  label: RHEL 8 Compliance API
  slug: compliance-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/compliance/v2/openapi.json
- filename: red-hat-enterprise-linux-8-security-data-openapi.yml
  format: yaml
  label: RHEL 8 Security Data API
  slug: security-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-enterprise-linux-8/refs/heads/main/openapi/red-hat-enterprise-linux-8-security-data-openapi.yml
- filename: openapi.json
  format: json
  label: RHEL 8 Host Inventory API
  slug: host-inventory-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/inventory/v1/openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps shape for Red Hat Enterprise Linux subscriptions. Billing is per-system / per-socket-pair / per-hypervisor on annual or multi-year terms; cloud-marketplace (AWS / Azure / GCP) consumption shifts the same SKUs onto pay-as-you-go hourly metering.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Red Hat, Inc.
  ProviderName: Red Hat
  PublisherName: Red Hat, Inc.
  ServiceCategory: Operating System Subscription
  ServiceName: Red Hat Enterprise Linux
layout: finops
meters:
- aggregation: sum
  description: Annual RHEL Server subscription per pair of sockets / pair of virtual guests
  dimensions:
  - sku
  - support_level
  - architecture
  name: server_subscription
  unit: socket-pair-year
- aggregation: sum
  description: Annual RHEL Workstation subscription per system
  dimensions:
  - sku
  - support_level
  name: workstation_subscription
  unit: system-year
- aggregation: sum
  description: Annual RHEL for Virtual Datacenters subscription per hypervisor (unlimited guests)
  dimensions:
  - sku
  - support_level
  name: virtual_datacenter_subscription
  unit: hypervisor-year
- aggregation: sum
  description: Annual RHEL for SAP Solutions subscription
  dimensions:
  - sku
  - support_level
  name: sap_subscription
  unit: socket-pair-year
- aggregation: sum
  description: Annual RHEL for IBM Power Little Endian subscription
  dimensions:
  - sku
  - support_level
  name: power_le_subscription
  unit: socket-pair-year
name: Red Hat Enterprise Linux 8 Finops
provider_name: Red Hat Enterprise Linux 8
provider_slug: red-hat-enterprise-linux-8
publisher_name: Red Hat, Inc.
service_category: Operating System Subscription
slug: red-hat-enterprise-linux-8-finops
source_filename: red-hat-enterprise-linux-8-finops.yml
source_heading: FinOps Profile
source_url: https://www.redhat.com/en/store/linux-platforms
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red Hat Enterprise Linux 8\nproviderId: red-hat-enterprise-linux-8\npublisherName: Red Hat, Inc.\nserviceCategory: Operating System Subscription\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Linux\n  - Operating System\n  - Subscription\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Red Hat Enterprise Linux subscriptions. Billing is\n  per-system / per-socket-pair / per-hypervisor on annual or multi-year terms; cloud-marketplace\n  (AWS / Azure / GCP) consumption shifts the same SKUs onto pay-as-you-go hourly metering.\nsources:\n  - https://www.redhat.com/en/store/linux-platforms\nbillingModel:\n\
  \  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Red Hat Enterprise Linux\n  ServiceCategory: Operating System Subscription\n  ProviderName: Red Hat\n  PublisherName: Red Hat, Inc.\n  InvoiceIssuerName: Red Hat, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: server_subscription\n    description: Annual RHEL Server subscription per pair of sockets / pair of virtual guests\n    unit: socket-pair-year\n    aggregation: sum\n    dimensions:\n      - sku\n      - support_level\n      - architecture\n  - name: workstation_subscription\n    description: Annual RHEL Workstation subscription per system\n    unit: system-year\n    aggregation: sum\n    dimensions:\n      - sku\n      - support_level\n  - name: virtual_datacenter_subscription\n    description: Annual RHEL for Virtual Datacenters subscription per hypervisor (unlimited guests)\n    unit: hypervisor-year\n    aggregation: sum\n\
  \    dimensions:\n      - sku\n      - support_level\n  - name: sap_subscription\n    description: Annual RHEL for SAP Solutions subscription\n    unit: socket-pair-year\n    aggregation: sum\n    dimensions:\n      - sku\n      - support_level\n  - name: power_le_subscription\n    description: Annual RHEL for IBM Power Little Endian subscription\n    unit: socket-pair-year\n    aggregation: sum\n    dimensions:\n      - sku\n      - support_level\nprinciples:\n  - name: Visibility\n    description: Use Red Hat Subscription Management and Red Hat Insights to inventory which\n      systems are consuming which RHEL SKUs against active entitlements.\n  - name: Allocation\n    description: Allocate entitlement consumption to teams via Red Hat Customer Portal account\n      hierarchy or via host-level CMDB tags; cloud-marketplace RHEL is allocated through the\n      cloud bill instead.\n  - name: Optimization\n    description: Convert dense virtualization estates from per-socket Server SKUs\
  \ to RH00002\n      (Virtual Datacenter) for unlimited guests; consolidate SAP workloads on RH00764; commit\n      to multi-year terms for renewal discount.\n  - name: Accountability\n    description: Procurement owns the master Red Hat agreement; platform/infrastructure teams\n      own per-system entitlement consumption.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/red-hat-enterprise-linux-8/refs/heads/main/finops/red-hat-enterprise-linux-8-finops.yml
sources:
- https://www.redhat.com/en/store/linux-platforms
specification: FinOps Framework
tags:
- Linux
- Operating System
- Subscription
- FinOps
- FOCUS
---
