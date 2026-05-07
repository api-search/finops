---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ciena-blue-planet-openapi.yml
  format: yaml
  label: Ciena Blue Planet Open API
  slug: blue-planet-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ciena/refs/heads/main/openapi/ciena-blue-planet-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Project / Annual Support
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: License + Hardware + Services
description: 'FOCUS-aligned FinOps for Ciena: telecom-vendor capex + opex shape. Network operators pay for hardware (optical / packet platforms), perpetual or term software licenses (Blue Planet, MCP), support, and professional services. APIs are bundled into the software entitlement and not separately metered.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Ciena Corporation
  PricingCategory: License + Hardware
  ProviderName: Ciena
  PublisherName: Ciena Corporation
  ServiceCategory: Network Infrastructure / SDN
  ServiceName: Ciena Blue Planet / MCP
layout: finops
meters:
- aggregation: sum
  description: Blue Planet or MCP software license line items
  dimensions:
  - product
  - sku
  name: software_license
  unit: license-year
- aggregation: sum
  description: Optical and packet platform hardware purchases
  dimensions:
  - platform
  - site
  name: hardware_capex
  unit: chassis
- aggregation: sum
  description: Annual support and maintenance contract
  dimensions:
  - tier
  - product
  name: support_subscription
  unit: month
- aggregation: sum
  description: Implementation, integration, and customization services
  dimensions:
  - project
  name: professional_services
  unit: hour
name: Ciena Finops
provider_name: Ciena
provider_slug: ciena
publisher_name: Ciena Corporation
service_category: Network Infrastructure / SDN
slug: ciena-finops
source_filename: ciena-finops.yml
source_heading: FinOps Profile
source_url: https://www.ciena.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ciena\nproviderId: ciena\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - MEF\n  - Network Automation\n  - Optical\n  - SDN\n  - Telecom\n  - TM Forum\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Ciena: telecom-vendor capex + opex shape. Network operators\n  pay for hardware (optical / packet platforms), perpetual or term software licenses (Blue Planet,\n  MCP), support, and professional services. APIs are bundled into the software entitlement and not\n  separately metered.'\nnotes: Ciena does not expose a per-API metered billing surface. The FinOps shape below reflects the\n  carrier-vendor commercial structure.\nsources:\n  - https://www.ciena.com/\n  - https://www.blueplanet.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Ciena Corporation\nserviceCategory: Network Infrastructure / SDN\nbillingModel:\n  pricingCategory: License + Hardware + Services\n  billingFrequency: Per-Project / Annual Support\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Ciena Blue Planet / MCP\n  ServiceCategory: Network Infrastructure / SDN\n  ProviderName: Ciena\n  PublisherName: Ciena Corporation\n  InvoiceIssuerName: Ciena Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: License + Hardware\nmeters:\n  - name: software_license\n    description: Blue Planet or MCP software license line items\n    unit: license-year\n    aggregation: sum\n    dimensions:\n      - product\n      - sku\n  - name: hardware_capex\n    description: Optical and packet platform hardware purchases\n    unit: chassis\n    aggregation: sum\n   \
  \ dimensions:\n      - platform\n      - site\n  - name: support_subscription\n    description: Annual support and maintenance contract\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - product\n  - name: professional_services\n    description: Implementation, integration, and customization services\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - project\nprinciples:\n  - name: Visibility\n    description: Track Ciena spend through purchase orders, hardware asset registers, software\n      entitlement records in the Ciena customer portal, and annual support invoices.\n  - name: Allocation\n    description: Allocate hardware and license cost to network domains (metro, long-haul, DCI) and\n      service products (Ethernet, wavelength, IP transit) so each carrier service line carries its\n      vendor cost.\n  - name: Optimization\n    description: Align refresh cycles with network growth, negotiate multi-year support, consolidate\n      management\
  \ on MCP / Blue Planet to reduce OSS sprawl, and use Emulation Cloud to validate\n      automation before paying for production licenses.\n  - name: Accountability\n    description: Network engineering owns design and capacity; operations owns MCP / Blue Planet\n      runtime; supply chain and finance own purchase orders and asset lifecycle.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ciena/refs/heads/main/finops/ciena-finops.yml
sources:
- https://www.ciena.com/
- https://www.blueplanet.com/
specification: FinOps Framework
tags:
- MEF
- Network Automation
- Optical
- SDN
- Telecom
- TM Forum
- FinOps
- FOCUS
---
