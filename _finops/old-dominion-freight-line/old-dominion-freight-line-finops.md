---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: old-dominion-freight-line-bill-of-lading-api-openapi.yml
  format: yaml
  label: ODFL Bill of Lading API
  slug: bill-of-lading-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/old-dominion-freight-line/refs/heads/main/openapi/old-dominion-freight-line-bill-of-lading-api-openapi.yml
- filename: old-dominion-freight-line-pickup-api-openapi.yml
  format: yaml
  label: ODFL Pickup API
  slug: pickup-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/old-dominion-freight-line/refs/heads/main/openapi/old-dominion-freight-line-pickup-api-openapi.yml
- filename: old-dominion-freight-line-tracking-api-openapi.yml
  format: yaml
  label: ODFL Tracking API
  slug: tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/old-dominion-freight-line/refs/heads/main/openapi/old-dominion-freight-line-tracking-api-openapi.yml
- filename: old-dominion-freight-line-document-api-openapi.yml
  format: yaml
  label: ODFL Document API
  slug: document-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/old-dominion-freight-line/refs/heads/main/openapi/old-dominion-freight-line-document-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: None (bundled)
  chargeCategories:
  - Usage
  chargeFrequency: None
  pricingCategory: Bundled with Freight Relationship
description: 'FOCUS-aligned FinOps for ODFL: API access is bundled with the freight customer relationship and is not invoiced separately. Cost dimensions are operational — engineering integration time, polling cadence, and the SOAP-to-REST migration cost (SOAP retiring 2025-12-31).'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Old Dominion Freight Line, Inc. (freight invoice; API not separately billed)
  PricingCategory: Bundled
  PricingUnit: request
  ProviderName: Old Dominion Freight Line
  PublisherName: Old Dominion Freight Line, Inc.
  ServiceCategory: LTL Freight / Logistics
  ServiceName: Old Dominion Freight Line API
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
  description: Bills of lading submitted via the BOL API
  name: bol_submissions
  unit: bol
- aggregation: sum
  description: Pickup requests submitted
  name: pickup_requests
  unit: pickup
- aggregation: sum
  description: Tracking polls (track to optimize cadence)
  dimensions:
  - shipment_id
  name: tracking_polls
  unit: poll
- aggregation: sum
  description: Freight documents retrieved
  name: documents_retrieved
  unit: document
name: Old Dominion Freight Line Finops
provider_name: Old Dominion Freight Line
provider_slug: old-dominion-freight-line
publisher_name: Old Dominion Freight Line, Inc.
service_category: LTL Freight / Logistics
slug: old-dominion-freight-line-finops
source_filename: old-dominion-freight-line-finops.yml
source_heading: FinOps Profile
source_url: https://www.odfl.com/us/en/resources/shipping-api-integrations.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Old Dominion Freight Line\nproviderId: old-dominion-freight-line\npublisherName: Old Dominion Freight Line, Inc.\nserviceCategory: LTL Freight / Logistics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Freight\n  - Less-Than-Truckload\n  - Logistics\n  - Shipping\n  - Transportation\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for ODFL: API access is bundled with the freight customer relationship\n  and is not invoiced separately. Cost dimensions are operational — engineering integration time, polling\n  cadence, and the SOAP-to-REST migration cost (SOAP retiring 2025-12-31).'\nnotes:\
  \ ODFL does not invoice API consumers separately from freight services.\nsources:\n  - https://www.odfl.com/us/en/resources/shipping-api-integrations.html\nprinciples:\n  - name: Visibility\n    description: ODFL does not bill per-call. Track per-API-key request volume and tracking-poll rate\n      internally to ensure the integration scales with shipment volume.\n  - name: Allocation\n    description: Allocate engineering integration cost to the consuming TMS/WMS/logistics product. Tag\n      ODFL API keys per app/business unit for usage attribution.\n  - name: Optimization\n    description: Migrate from retiring SOAP services to REST before 2025-12-31. Cache tracking responses;\n      batch tracking-number lookups; avoid high-frequency polling for in-transit shipments.\n  - name: Accountability\n    description: Designate a logistics-IT owner for the ODFL API credential and SOAP-to-REST migration.\n      Reconcile shipment-document quality with ODFL Customer Service quarterly.\nbillingModel:\n\
  \  pricingCategory: Bundled with Freight Relationship\n  billingFrequency: None (bundled)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n  chargeFrequency: None\nfocusColumns:\n  ServiceName: Old Dominion Freight Line API\n  ServiceCategory: LTL Freight / Logistics\n  ProviderName: Old Dominion Freight Line\n  PublisherName: Old Dominion Freight Line, Inc.\n  InvoiceIssuerName: Old Dominion Freight Line, Inc. (freight invoice; API not separately billed)\n  PricingCategory: Bundled\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Operationally tracked API request count per key (not invoiced)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - api_key\n      - endpoint\n  - name: bol_submissions\n    description: Bills of lading submitted via the BOL API\n    unit: bol\n    aggregation: sum\n  - name: pickup_requests\n    description: Pickup requests submitted\n    unit: pickup\n\
  \    aggregation: sum\n  - name: tracking_polls\n    description: Tracking polls (track to optimize cadence)\n    unit: poll\n    aggregation: sum\n    dimensions:\n      - shipment_id\n  - name: documents_retrieved\n    description: Freight documents retrieved\n    unit: document\n    aggregation: sum\napis:\n  - name: ODFL Bill of Lading API\n    baseURL: https://www.odfl.com\n    tags:\n      - Bill of Lading\n      - Documents\n      - Freight\n    serviceName: ODFL Bill of Lading API\n    serviceCategory: LTL Freight\n  - name: ODFL Pickup API\n    baseURL: https://www.odfl.com\n    tags:\n      - Freight\n      - Pickup\n    serviceName: ODFL Pickup API\n    serviceCategory: LTL Freight\n  - name: ODFL Tracking API\n    baseURL: https://www.odfl.com\n    tags:\n      - Freight\n      - Tracking\n    serviceName: ODFL Tracking API\n    serviceCategory: LTL Freight\n  - name: ODFL Document API\n    baseURL: https://www.odfl.com\n    tags:\n      - Documents\n      - Freight\n    serviceName:\
  \ ODFL Document API\n    serviceCategory: LTL Freight\nunitEconomics:\n  - name: Polls per shipment\n    metric: tracking_polls / active_shipments\n    target: minimize via reduced polling cadence\n  - name: Integration cost per shipment\n    metric: integration_engineering_cost / shipments_processed\n    target: declining over time via reuse\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/old-dominion-freight-line/refs/heads/main/finops/old-dominion-freight-line-finops.yml
sources:
- https://www.odfl.com/us/en/resources/shipping-api-integrations.html
specification: FinOps Framework
tags:
- Freight
- Less-Than-Truckload
- Logistics
- Shipping
- Transportation
- FinOps
- Cost Management
- FOCUS
---
