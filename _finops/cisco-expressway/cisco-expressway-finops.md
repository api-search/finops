---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cisco-expressway-configuration-api-openapi.yml
  format: yaml
  label: Cisco Expressway Configuration API
  slug: cisco-expressway-configuration-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-expressway/refs/heads/main/openapi/cisco-expressway-configuration-api-openapi.yml
- filename: cisco-expressway-status-api-openapi.yml
  format: yaml
  label: Cisco Expressway Status API
  slug: cisco-expressway-status-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-expressway/refs/heads/main/openapi/cisco-expressway-status-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription + Perpetual License
description: FOCUS-aligned FinOps shape for Cisco Expressway. Cost is driven by Cisco Smart Licensing entitlements (Webex Suite / Collaboration Flex Plan / UCM CL) plus underlying compute for the VM appliance — not by per-API metering.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Cisco Systems, Inc.
  ProviderName: Cisco
  PublisherName: Cisco Systems, Inc.
  ServiceCategory: Unified Communications
  ServiceName: Cisco Expressway
layout: finops
meters:
- aggregation: sum
  description: Cisco Smart Licensing entitlements that authorize Expressway capacity (registrations, MRA users, B2B traversal).
  dimensions:
  - sku
  - tier
  - region
  name: collaboration_license
  unit: license
- aggregation: max
  description: Concurrent traversal calls (rich-media sessions) supported by the appliance.
  dimensions:
  - appliance_size
  - region
  name: traversal_calls
  unit: concurrent_session
- aggregation: max
  description: Registered Mobile and Remote Access users.
  dimensions:
  - region
  name: mra_users
  unit: user
name: Cisco Expressway Finops
provider_name: Cisco Expressway
provider_slug: cisco-expressway
publisher_name: Cisco Systems, Inc.
service_category: Unified Communications
slug: cisco-expressway-finops
source_filename: cisco-expressway-finops.yml
source_heading: FinOps Profile
source_url: https://www.cisco.com/c/en/us/products/unified-communications/expressway-series/index.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cisco Expressway\nproviderId: cisco-expressway\npublisherName: Cisco Systems, Inc.\nserviceCategory: Unified Communications\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Collaboration\n  - Unified Communications\n  - Video Conferencing\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Cisco Expressway. Cost is driven by Cisco Smart Licensing\n  entitlements (Webex Suite / Collaboration Flex Plan / UCM CL) plus underlying compute for the VM\n  appliance — not by per-API metering.\nnotes: Per-API meters below are modeled placeholders; real billing flows through Cisco's collaboration\n  licensing line\
  \ items, not metered API consumption.\nsources:\n  - https://www.cisco.com/c/en/us/products/unified-communications/expressway-series/index.html\n  - https://www.cisco.com/c/en/us/products/collaboration-endpoints/collaboration-flex-plan/index.html\nbillingModel:\n  pricingCategory: Subscription + Perpetual License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Cisco Expressway\n  ServiceCategory: Unified Communications\n  ProviderName: Cisco\n  PublisherName: Cisco Systems, Inc.\n  InvoiceIssuerName: Cisco Systems, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: collaboration_license\n    description: Cisco Smart Licensing entitlements that authorize Expressway capacity (registrations,\n      MRA users, B2B traversal).\n    unit: license\n    aggregation: sum\n    dimensions:\n      - sku\n      - tier\n      - region\n  - name: traversal_calls\n\
  \    description: Concurrent traversal calls (rich-media sessions) supported by the appliance.\n    unit: concurrent_session\n    aggregation: max\n    dimensions:\n      - appliance_size\n      - region\n  - name: mra_users\n    description: Registered Mobile and Remote Access users.\n    unit: user\n    aggregation: max\n    dimensions:\n      - region\nprinciples:\n  - name: Visibility\n    description: Use Cisco Smart Software Manager (CSSM) to observe license consumption; pair with\n      Expressway's built-in usage and call detail reports.\n  - name: Allocation\n    description: Allocate Expressway license cost to the collaboration cost center; tag VM hosting\n      cost by datacenter/region and apply showback to UC service owners.\n  - name: Optimization\n    description: Right-size Expressway VM appliances (Small/Medium/Large), consolidate traversal\n      capacity across regions, and align Smart License count with peak concurrent usage.\n  - name: Accountability\n    description:\
  \ Collaboration platform owner is accountable for Expressway license forecasting,\n      renewal cadence, and capacity planning against Cisco's True Forward licensing model.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-expressway/refs/heads/main/finops/cisco-expressway-finops.yml
sources:
- https://www.cisco.com/c/en/us/products/unified-communications/expressway-series/index.html
- https://www.cisco.com/c/en/us/products/collaboration-endpoints/collaboration-flex-plan/index.html
specification: FinOps Framework
tags:
- Collaboration
- Unified Communications
- Video Conferencing
- FinOps
- FOCUS
---
