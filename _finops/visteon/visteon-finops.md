---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: visteon-phoenix-openapi.yml
  format: yaml
  label: Visteon Phoenix API
  slug: phoenix-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/visteon/refs/heads/main/openapi/visteon-phoenix-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Program / Supply Contract
description: Visteon is an automotive Tier-1 supplier; spend is dominated by hardware unit-price programs and engineering services, not metered API consumption. The artifact retains the FinOps shape only as a placeholder for catalog completeness.
focus_columns:
  BillingCurrency: USD
  ProviderName: Visteon
  PublisherName: Visteon Corporation
  ServiceCategory: Automotive Tier-1
  ServiceName: Visteon
layout: finops
meters:
- aggregation: sum
  name: program_engagement
  unit: varies
name: Visteon Finops
provider_name: Visteon
provider_slug: visteon
publisher_name: Visteon Corporation
service_category: Automotive Tier-1
slug: visteon-finops
source_filename: visteon-finops.yml
source_heading: FinOps Profile
source_url: https://www.visteon.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Visteon\nproviderId: visteon\npublisherName: Visteon Corporation\nserviceCategory: Automotive Tier-1\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Automotive\n  - OEM Tier-1\ndescription: Visteon is an automotive Tier-1 supplier; spend is dominated by hardware unit-price\n  programs and engineering services, not metered API consumption. The artifact retains the FinOps\n  shape only as a placeholder for catalog completeness.\nsources:\n  - https://www.visteon.com/\nnotes: No metered API billing or FOCUS-aligned cost-and-usage feed is published.\nbillingModel:\n  pricingCategory: Program / Supply Contract\n  billingFrequency: Per-Invoice\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Visteon\n  ServiceCategory: Automotive Tier-1\n  ProviderName: Visteon\n  PublisherName: Visteon Corporation\n  BillingCurrency: USD\nmeters:\n  - name: program_engagement\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Spend visibility is delivered through the OEM purchase-order / Tier-1 program\n      reporting cadence; there is no public Visteon usage API.\n  - name: Allocation\n    description: Costs allocate to the vehicle program / model line; allocation handled in the\n      OEM's PLM and program accounting.\n  - name: Optimization\n    description: Optimization levers are commercial - unit-price negotiation across vehicle\n      volume commitments and program lifetime.\n  - name: Accountability\n    description: OEM program management owns spend on the buyer side; Visteon's program account\n      manages the supplier-side commercial relationship.\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/visteon/refs/heads/main/finops/visteon-finops.yml
sources:
- https://www.visteon.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Automotive
- OEM Tier-1
---
