---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: None (bundled)
  chargeCategories:
  - Usage
  chargeFrequency: None
  pricingCategory: Bundled with Customer Relationship
description: 'FOCUS-aligned FinOps for Nordson: API access is bundled with the underlying industrial customer/partner relationship and is not invoiced separately. Cost dimensions are operational — integration build cost rather than per-call invoicing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Nordson Corporation (equipment/service contracts; API not separately billed)
  PricingCategory: Bundled
  PricingUnit: request
  ProviderName: Nordson Corporation
  PublisherName: Nordson Corporation
  ServiceCategory: Industrial Equipment / Manufacturing
  ServiceName: Nordson Corporation API
layout: finops
meters:
- aggregation: sum
  description: Operationally tracked API request count per key (not invoiced)
  dimensions:
  - api
  - api_key
  - endpoint
  name: api_requests
  unit: request
- aggregation: sum
  description: Equipment telemetry payloads uploaded
  dimensions:
  - device_id
  name: telemetry_uploads
  unit: payload
name: Nordson Finops
provider_name: Nordson Corporation
provider_slug: nordson
publisher_name: Nordson Corporation
service_category: Industrial Equipment / Manufacturing
slug: nordson-finops
source_filename: nordson-finops.yml
source_heading: FinOps Profile
source_url: https://www.nordson.com/en
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Nordson Corporation\nproviderId: nordson\npublisherName: Nordson Corporation\nserviceCategory: Industrial Equipment / Manufacturing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Dispensing\n  - Testing\n  - Industrial\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Nordson: API access is bundled with the underlying industrial\n  customer/partner relationship and is not invoiced separately. Cost dimensions are operational — integration\n  build cost rather than per-call invoicing.'\nnotes: Nordson does not invoice API consumers separately. Update once Nordson publishes a public developer\n\
  \  portal with explicit billing.\nsources:\n  - https://www.nordson.com/en\nprinciples:\n  - name: Visibility\n    description: Nordson does not bill per-call. Track per-API-key request volumes internally for capacity\n      planning across the consuming manufacturing/IT systems.\n  - name: Allocation\n    description: Allocate integration cost (engineering time, monitoring) to the consuming product line\n      or business unit. Tag Nordson API keys per app or factory for attribution.\n  - name: Optimization\n    description: Cache equipment configuration and reference data; batch telemetry uploads where Nordson\n      equipment supports it. Avoid sub-minute polling per device.\n  - name: Accountability\n    description: Designate an OT/IT owner for the Nordson API credential and integration health. Coordinate\n      with the Nordson account team for credential rotation and SLA reviews.\nbillingModel:\n  pricingCategory: Bundled with Customer Relationship\n  billingFrequency: None (bundled)\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Usage\n  chargeFrequency: None\nfocusColumns:\n  ServiceName: Nordson Corporation API\n  ServiceCategory: Industrial Equipment / Manufacturing\n  ProviderName: Nordson Corporation\n  PublisherName: Nordson Corporation\n  InvoiceIssuerName: Nordson Corporation (equipment/service contracts; API not separately billed)\n  PricingCategory: Bundled\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Operationally tracked API request count per key (not invoiced)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - api_key\n      - endpoint\n  - name: telemetry_uploads\n    description: Equipment telemetry payloads uploaded\n    unit: payload\n    aggregation: sum\n    dimensions:\n      - device_id\napis:\n  - name: Nordson Corporation API\n    baseURL: https://api.nordson.com\n    tags:\n      - Dispensing\n      - Testing\n      - Industrial\n\
  \    serviceName: Nordson Corporation API\n    serviceCategory: Industrial Equipment\nunitEconomics:\n  - name: Integration cost per device\n    metric: integration_engineering_cost / connected_devices\n    target: declining over time via reuse\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nordson/refs/heads/main/finops/nordson-finops.yml
sources:
- https://www.nordson.com/en
specification: FinOps Framework
tags:
- Dispensing
- Testing
- Industrial
- FinOps
- Cost Management
- FOCUS
---
