---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: trimble-connect-openapi.yml
  format: yaml
  label: Trimble Connect API
  slug: trimble-connect
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/trimble/refs/heads/main/openapi/trimble-connect-openapi.yml
- filename: trimble-maps-openapi.yml
  format: yaml
  label: Trimble Maps API
  slug: trimble-maps
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/trimble/refs/heads/main/openapi/trimble-maps-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Contract / Negotiated
description: FinOps shape for Trimble cannot be reconciled from public sources; pricing is contact-sales / per-product license and per-API consumption telemetry sits inside each Trimble product's authenticated portal.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Trimble Inc.
  ProviderName: Trimble
  PublisherName: Trimble Inc.
  ServiceCategory: Industrial Software
  ServiceName: Trimble
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  name: license_seats
  unit: seat
name: Trimble Finops
provider_name: Trimble
provider_slug: trimble
publisher_name: Trimble Inc.
service_category: Industrial Software
slug: trimble-finops
source_filename: trimble-finops.yml
source_heading: FinOps Profile
source_url: https://www.trimble.com/en/developer
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Trimble\nproviderId: trimble\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Construction\n  - Transportation\n  - Geospatial\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Trimble cannot be reconciled from public sources; pricing is\n  contact-sales / per-product license and per-API consumption telemetry sits inside each Trimble\n  product's authenticated portal.\nsources:\n  - https://www.trimble.com/en/developer\n  - https://marketplace.trimble.com\nnotes: Trimble does not publish a unified billing or usage telemetry surface across its product\n  portfolio. FOCUS column values and meters can only be confirmed against the executed product\n  license and the per-product portal.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Trimble Inc.\nserviceCategory: Industrial Software\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Trimble\n  ServiceCategory: Industrial Software\n  ProviderName: Trimble\n  PublisherName: Trimble Inc.\n  InvoiceIssuerName: Trimble Inc.\n  BillingCurrency: USD\nmeters:\n  - name: license_seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Each Trimble product (Tekla, TMW, Trimble Connect, Viewpoint, Agriculture) exposes\n      its own usage console; finance reconciles against the per-product annual contract.\n  - name: Allocation\n    description: Allocate cost by Trimble product family and by the consuming project / fleet /\n      site identifier already used inside each product.\n  - name: Optimization\n\
  \    description: Optimization is contractual — right-size seat counts and consolidate product\n      modules at renewal across the construction / transportation / geospatial portfolio.\n  - name: Accountability\n    description: Per-product business owners (construction PM, fleet operations, GIS lead) co-own\n      the Trimble contracts; procurement manages renewals.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/trimble/refs/heads/main/finops/trimble-finops.yml
sources:
- https://www.trimble.com/en/developer
- https://marketplace.trimble.com
specification: FinOps Framework
tags:
- Construction
- Transportation
- Geospatial
- FinOps
- FOCUS
---
