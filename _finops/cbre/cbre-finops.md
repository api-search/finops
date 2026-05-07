---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cbre-cbre-api-openapi.yml
  format: yaml
  label: CBRE Developer API
  slug: cbre-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cbre/refs/heads/main/openapi/cbre-cbre-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Service Contract (API Bundled)
description: FOCUS-aligned FinOps scaffold for CBRE. CBRE invoices are dominated by service-line fees (transaction services, project management, facilities management, valuation, investment management); the API surface is bundled into those engagements. FinOps reporting tracks API consumption to allocate the bundled cost rather than to drive a per-call invoice.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: CBRE Group, Inc.
  ProviderName: CBRE
  PublisherName: CBRE Group, Inc.
  ServiceCategory: Commercial Real Estate Services
  ServiceName: CBRE Developer API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - application
  - service_line
  name: api_requests
  unit: request
- aggregation: count
  dimensions:
  - region
  - service_line
  name: properties_under_management
  unit: property
- aggregation: sum
  dimensions:
  - region
  - service_line
  name: square_feet_managed
  unit: sqft
- aggregation: count
  dimensions:
  - region
  name: work_orders_processed
  unit: work_order
name: Cbre Finops
provider_name: CBRE
provider_slug: cbre
publisher_name: CBRE Group, Inc.
service_category: Commercial Real Estate Services
slug: cbre-finops
source_filename: cbre-finops.yml
source_heading: FinOps Profile
source_url: https://developer.cbre.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CBRE\nproviderId: cbre\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Commercial Real Estate\n  - Real Estate\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps scaffold for CBRE. CBRE invoices are dominated by service-line fees\n  (transaction services, project management, facilities management, valuation, investment management);\n  the API surface is bundled into those engagements. FinOps reporting tracks API consumption to allocate\n  the bundled cost rather than to drive a per-call invoice.'\nnotes: Direct per-call API pricing is not published; cost is captured within the parent CBRE service\n  contract.\nsources:\n  - https://developer.cbre.com/\n  - https://www.cbre.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CBRE Group, Inc.\nserviceCategory: Commercial Real Estate Services\nbillingModel:\n  pricingCategory: Service Contract (API Bundled)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: CBRE Developer API\n  ServiceCategory: Commercial Real Estate Services\n  ProviderName: CBRE\n  PublisherName: CBRE Group, Inc.\n  InvoiceIssuerName: CBRE Group, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - application\n      - service_line\n  - name: properties_under_management\n    unit: property\n    aggregation: count\n    dimensions:\n      - region\n      - service_line\n  - name: square_feet_managed\n    unit: sqft\n    aggregation: sum\n    dimensions:\n      - region\n      - service_line\n  - name: work_orders_processed\n    unit: work_order\n\
  \    aggregation: count\n    dimensions:\n      - region\nprinciples:\n  - name: Visibility\n    description: Pair API call volume from the developer-portal application reports with the CBRE service-line\n      invoice to see where consumption concentrates.\n  - name: Allocation\n    description: Allocate CBRE service fees to the property / portfolio they support; tag API calls with\n      the same property identifier for consistency.\n  - name: Optimization\n    description: Cache market analytics that update at low cadence; pull facilities work-order data on\n      change events rather than polling; consolidate reporting queries.\n  - name: Accountability\n    description: Real-estate leader owns CBRE service spend; integration platform owner ensures API consumption\n      stays within the entitlement bundled into the contract.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cbre/refs/heads/main/finops/cbre-finops.yml
sources:
- https://developer.cbre.com/
- https://www.cbre.com
specification: FinOps Framework
tags:
- Commercial Real Estate
- Real Estate
- FinOps
- FOCUS
---
