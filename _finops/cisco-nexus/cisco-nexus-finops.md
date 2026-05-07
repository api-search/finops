---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cisco-nexus-nxapi-rest.yml
  format: yaml
  label: Cisco NX-API REST
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-nexus/refs/heads/main/openapi/cisco-nexus-nxapi-rest.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription + Perpetual License
description: FOCUS-aligned FinOps shape for Cisco Nexus Dashboard and its NX-API / gRPC management surface. Cost is driven by Cisco Data Center Networking software subscriptions (Essentials / Advantage / Premier), Nexus 9000 hardware, and Cisco DC Power-of-Subscription term agreements — not by per-API metering.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Cisco Systems, Inc.
  ProviderName: Cisco
  PublisherName: Cisco Systems, Inc.
  ServiceCategory: Data Center Networking
  ServiceName: Cisco Nexus Dashboard
layout: finops
meters:
- aggregation: sum
  description: Cisco Data Center Networking software subscription (Essentials / Advantage / Premier) tied to Nexus switches.
  dimensions:
  - tier
  - sku
  - term
  - region
  name: dcn_software_license
  unit: license
- aggregation: sum
  description: Nexus 9000 / 7000 hardware purchases under support contract.
  dimensions:
  - platform
  - region
  name: nexus_switch_hardware
  unit: chassis
- aggregation: max
  description: Nexus Dashboard cluster footprint hosting Insights / Orchestrator / Fabric Controller.
  dimensions:
  - service
  - size
  - region
  name: nexus_dashboard_cluster
  unit: cluster
name: Cisco Nexus Finops
provider_name: Cisco Nexus Dashboard
provider_slug: cisco-nexus
publisher_name: Cisco Systems, Inc.
service_category: Data Center Networking
slug: cisco-nexus-finops
source_filename: cisco-nexus-finops.yml
source_heading: FinOps Profile
source_url: https://www.cisco.com/site/us/en/products/networking/cloud-networking/nexus-platform/index.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cisco Nexus Dashboard\nproviderId: cisco-nexus\npublisherName: Cisco Systems, Inc.\nserviceCategory: Data Center Networking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Data Center\n  - Networking\n  - SDN\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Cisco Nexus Dashboard and its NX-API / gRPC management\n  surface. Cost is driven by Cisco Data Center Networking software subscriptions (Essentials /\n  Advantage / Premier), Nexus 9000 hardware, and Cisco DC Power-of-Subscription term agreements —\n  not by per-API metering.\nnotes: Per-API meters below are placeholders modeled on operational\
  \ dimensions; real billing flows\n  through Cisco DCN licensing line items, hardware POs, and Smart Licensing usage.\nsources:\n  - https://www.cisco.com/site/us/en/products/networking/cloud-networking/nexus-platform/index.html\n  - https://www.cisco.com/c/en/us/products/software/dcn-software-subscriptions/index.html\nbillingModel:\n  pricingCategory: Subscription + Perpetual License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Cisco Nexus Dashboard\n  ServiceCategory: Data Center Networking\n  ProviderName: Cisco\n  PublisherName: Cisco Systems, Inc.\n  InvoiceIssuerName: Cisco Systems, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: dcn_software_license\n    description: Cisco Data Center Networking software subscription (Essentials / Advantage / Premier)\n      tied to Nexus switches.\n    unit: license\n    aggregation: sum\n    dimensions:\n\
  \      - tier\n      - sku\n      - term\n      - region\n  - name: nexus_switch_hardware\n    description: Nexus 9000 / 7000 hardware purchases under support contract.\n    unit: chassis\n    aggregation: sum\n    dimensions:\n      - platform\n      - region\n  - name: nexus_dashboard_cluster\n    description: Nexus Dashboard cluster footprint hosting Insights / Orchestrator / Fabric Controller.\n    unit: cluster\n    aggregation: max\n    dimensions:\n      - service\n      - size\n      - region\nprinciples:\n  - name: Visibility\n    description: Use Cisco Smart Software Manager (CSSM) for license consumption and Nexus Dashboard\n      Insights for fabric utilization and capacity reporting.\n  - name: Allocation\n    description: Allocate switch and DCN software cost to the network cost center; chargeback by\n      tenant / VRF / fabric using Nexus Dashboard tenant separation.\n  - name: Optimization\n    description: Match DCN tier (Essentials / Advantage / Premier) to required\
  \ features, retire\n      under-utilized switches, and prefer streaming telemetry over REST polling.\n  - name: Accountability\n    description: Network platform owner is accountable for Nexus Smart License renewals, hardware\n      refresh planning, and Nexus Dashboard scale targets.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-nexus/refs/heads/main/finops/cisco-nexus-finops.yml
sources:
- https://www.cisco.com/site/us/en/products/networking/cloud-networking/nexus-platform/index.html
- https://www.cisco.com/c/en/us/products/software/dcn-software-subscriptions/index.html
specification: FinOps Framework
tags:
- Data Center
- Networking
- SDN
- FinOps
- FOCUS
---
