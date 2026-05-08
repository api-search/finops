---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: jb-hunt-360-connect-api.yml
  format: yaml
  label: J.B. Hunt 360 Connect API
  slug: jb-hunt-360-connect-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jb-hunt-transport-services/refs/heads/main/openapi/jb-hunt-360-connect-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Adjustment
  - Tax
  pricingCategory: Per-Load + Accessorial
description: 'FOCUS-aligned FinOps placeholder for J.B. Hunt 360 Connect: API access is bundled with the underlying freight relationship; the billable surface is the freight contract (linehaul, fuel surcharge, accessorials, demurrage), not API calls.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: J.B. Hunt Transport Services, Inc.
  ProviderName: J.B. Hunt Transport Services
  PublisherName: J.B. Hunt Transport Services, Inc.
  ServiceCategory: Logistics / Transportation
  ServiceName: J.B. Hunt 360
layout: finops
meters:
- aggregation: sum
  dimensions:
  - mode
  - origin_region
  - destination_region
  name: linehaul_charge
  unit: load
- aggregation: sum
  dimensions:
  - mode
  name: fuel_surcharge
  unit: load
- aggregation: sum
  dimensions:
  - accessorial_type
  name: accessorials
  unit: event
- aggregation: sum
  dimensions:
  - endpoint
  - partner
  name: api_requests
  unit: request
name: Jb Hunt Transport Services Finops
provider_name: J.B. Hunt Transport Services
provider_slug: jb-hunt-transport-services
publisher_name: J.B. Hunt Transport Services, Inc.
service_category: Logistics / Transportation
slug: jb-hunt-transport-services-finops
source_filename: jb-hunt-transport-services-finops.yml
source_heading: FinOps Profile
source_url: https://www.jbhunt.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: J.B. Hunt Transport Services\nproviderId: jb-hunt-transport-services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Logistics\n  - Freight\n  - Transportation\ndescription: 'FOCUS-aligned FinOps placeholder for J.B. Hunt 360 Connect: API access is bundled with\n  the underlying freight relationship; the billable surface is the freight contract (linehaul, fuel\n  surcharge, accessorials, demurrage), not API calls.'\nnotes: J.B. Hunt does not publish a public API rate card. Meters below model the economic surface a\n  shipper or partner sees on a J.B. Hunt invoice.\nsources:\n  - https://www.jbhunt.com/\n  - https://apiportal.jbhunt.com/docs/services\n  - https://developer.jbhunt.com/connect-360\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: J.B. Hunt Transport Services, Inc.\nserviceCategory: Logistics / Transportation\nbillingModel:\n  pricingCategory: Per-Load + Accessorial\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: J.B. Hunt 360\n  ServiceCategory: Logistics / Transportation\n  ProviderName: J.B. Hunt Transport Services\n  PublisherName: J.B. Hunt Transport Services, Inc.\n  InvoiceIssuerName: J.B. Hunt Transport Services, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: linehaul_charge\n    unit: load\n    aggregation: sum\n    dimensions:\n      - mode\n      - origin_region\n      - destination_region\n  - name: fuel_surcharge\n    unit: load\n    aggregation: sum\n    dimensions:\n      - mode\n  - name: accessorials\n    unit: event\n    aggregation: sum\n    dimensions:\n      - accessorial_type\n\
  \  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - partner\nprinciples:\n  - name: Visibility\n    description: Use the J.B. Hunt 360 platform's invoice and shipment APIs to extract per-load cost\n      and accessorials; reconcile against carrier invoices monthly.\n  - name: Allocation\n    description: Tag shipments with cost center, business unit, and customer order so freight cost\n      is allocated to the revenue line that drove the load.\n  - name: Optimization\n    description: Use 360 quoting to compare rates, consolidate LTL into FTL where possible, plan appointments\n      to avoid detention/demurrage accessorials.\n  - name: Accountability\n    description: Logistics manager owns load-level cost and accessorial overruns; weekly review of\n      anomalies in the 360 platform.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jb-hunt-transport-services/refs/heads/main/finops/jb-hunt-transport-services-finops.yml
sources:
- https://www.jbhunt.com/
- https://apiportal.jbhunt.com/docs/services
- https://developer.jbhunt.com/connect-360
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Logistics
- Freight
- Transportation
---
