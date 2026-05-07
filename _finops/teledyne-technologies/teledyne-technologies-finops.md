---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: teledyne-flir-camera-rest-openapi.yml
  format: yaml
  label: Teledyne FLIR Camera REST API
  slug: flir-camera-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/teledyne-technologies/refs/heads/main/openapi/teledyne-flir-camera-rest-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Capital Purchase + License
description: FOCUS-aligned FinOps shape for Teledyne Technologies. Spend is dominated by capital hardware purchase and bundled SDK / integration licenses sold through subsidiary brands, not by consumption-priced API calls.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Teledyne Technologies Incorporated
  ProviderName: Teledyne Technologies
  PublisherName: Teledyne Technologies Incorporated
  ServiceCategory: Instrumentation / Defense Electronics
  ServiceName: Teledyne Technologies
layout: finops
meters:
- aggregation: sum
  dimensions:
  - subsidiary
  - product_line
  name: hardware_units
  unit: unit
- aggregation: sum
  dimensions:
  - subsidiary
  - product_line
  name: sdk_seats
  unit: seat
name: Teledyne Technologies Finops
provider_name: Teledyne Technologies
provider_slug: teledyne-technologies
publisher_name: Teledyne Technologies Incorporated
service_category: Instrumentation / Defense Electronics
slug: teledyne-technologies-finops
source_filename: teledyne-technologies-finops.yml
source_heading: FinOps Profile
source_url: https://www.teledyne.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Teledyne Technologies\nproviderId: teledyne-technologies\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Aerospace\n  - Defense\n  - Digital Imaging\n  - Instrumentation\n  - Thermal Imaging\n  - Test and Measurement\n  - Fortune 500\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Teledyne Technologies. Spend is dominated by capital\n  hardware purchase and bundled SDK / integration licenses sold through subsidiary brands, not by\n  consumption-priced API calls.\nsources:\n  - https://www.teledyne.com/\n  - https://www.flir.com/\nnotes: Teledyne does not operate a usage-priced API surface. There is no consumption export to map\n  to FOCUS columns. Meters below describe instrument units sold and integration-license seats\n  rather than API requests.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl:\
  \ https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Teledyne Technologies Incorporated\nserviceCategory: Instrumentation / Defense Electronics\nbillingModel:\n  pricingCategory: Capital Purchase + License\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Teledyne Technologies\n  ServiceCategory: Instrumentation / Defense Electronics\n  ProviderName: Teledyne Technologies\n  PublisherName: Teledyne Technologies Incorporated\n  InvoiceIssuerName: Teledyne Technologies Incorporated\n  BillingCurrency: USD\nmeters:\n  - name: hardware_units\n    unit: unit\n    aggregation: sum\n    dimensions:\n      - subsidiary\n      - product_line\n  - name: sdk_seats\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - subsidiary\n      - product_line\nprinciples:\n  - name: Visibility\n    description: Spend\
  \ is observed through the buyer's procurement / ERP system; Teledyne does not\n      provide a usage-cost dashboard for SDK consumption.\n  - name: Allocation\n    description: Allocation is by subsidiary brand (FLIR, LeCroy, Imaging, API) and project /\n      program purchasing the instrument or SDK.\n  - name: Optimization\n    description: Optimization is procurement-driven (volume discounts, refurbished units, support\n      tier selection) rather than runtime consumption-driven.\n  - name: Accountability\n    description: The hardware-purchasing project owner is the accountable cost owner; integration\n      teams own the SDK seats they consume.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/teledyne-technologies/refs/heads/main/finops/teledyne-technologies-finops.yml
sources:
- https://www.teledyne.com/
- https://www.flir.com/
specification: FinOps Framework
tags:
- Aerospace
- Defense
- Digital Imaging
- Instrumentation
- Thermal Imaging
- Test and Measurement
- Fortune 500
- FinOps
- FOCUS
---
