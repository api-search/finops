---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: agco-agcommand-api-openapi.yml
  format: yaml
  label: AGCO AgCommand API
  slug: agcommand-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/agco/refs/heads/main/openapi/agco-agcommand-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: OEM / Dealer Contract
description: FOCUS-aligned FinOps shape for AGCO's AgCommand telematics. AGCO is an OEM; telematics access is bundled with equipment and dealer agreements rather than billed as a standalone API.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: AGCO Corporation
  ProviderName: AGCO Corporation
  PublisherName: AGCO Corporation
  ServiceCategory: Agriculture / Telematics
  ServiceName: AGCO AgCommand
layout: finops
meters:
- aggregation: sum
  description: Telemetry subscription per piece of connected AGCO equipment
  dimensions:
  - brand
  - model
  - dealer
  name: equipment_subscription
  unit: equipment-month
- aggregation: count
  description: Telematics data-feed delivery to a customer system
  dimensions:
  - feed_type
  - integration
  name: data_feed
  unit: feed
name: Agco Finops
provider_name: agco
provider_slug: agco
publisher_name: AGCO Corporation
service_category: Agriculture / Telematics
slug: agco-finops
source_filename: agco-finops.yml
source_heading: FinOps Profile
source_url: https://www.agcocorp.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AGCO Corporation\nproviderId: agco\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: AGCO Corporation\nserviceCategory: Agriculture / Telematics\ntags:\n  - Agriculture\n  - Farm Equipment\n  - Telematics\n  - IoT\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for AGCO's AgCommand telematics. AGCO is an OEM; telematics\n  access is bundled with equipment and dealer agreements rather than billed as a standalone API.\nnotes: No public pricing; meters reflect the contract dimensions used by AGCO dealers (equipment count,\n  fleet size, telemetry feed type).\nsources:\n  - https://www.agcocorp.com/\nbillingModel:\n\
  \  pricingCategory: OEM / Dealer Contract\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: AGCO AgCommand\n  ServiceCategory: Agriculture / Telematics\n  ProviderName: AGCO Corporation\n  PublisherName: AGCO Corporation\n  InvoiceIssuerName: AGCO Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: equipment_subscription\n    description: Telemetry subscription per piece of connected AGCO equipment\n    unit: equipment-month\n    aggregation: sum\n    dimensions:\n      - brand\n      - model\n      - dealer\n  - name: data_feed\n    description: Telematics data-feed delivery to a customer system\n    unit: feed\n    aggregation: count\n    dimensions:\n      - feed_type\n      - integration\nprinciples:\n  - name: Visibility\n    description: Track AgCommand cost via the dealer's invoice and the AgCommand fleet portal; correlate\n      with the equipment register so cost\
  \ ties to specific machines.\n  - name: Allocation\n    description: Allocate cost by farm / business unit / equipment cohort using the equipment serial\n      number as the allocation key.\n  - name: Optimization\n    description: Optimize by deactivating telemetry on idled or sold equipment, consolidating data feeds,\n      and aligning telemetry scope with what fleet operations actually use.\n  - name: Accountability\n    description: Fleet operations or farm-management leadership owns the AgCommand subscription line;\n      reviews typically align with the equipment lease or service-contract renewal cycle.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/agco/refs/heads/main/finops/agco-finops.yml
sources:
- https://www.agcocorp.com/
specification: FinOps Framework
tags:
- Agriculture
- Farm Equipment
- Telematics
- IoT
- FinOps
- FOCUS
---
