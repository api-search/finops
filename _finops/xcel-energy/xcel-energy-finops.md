---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: xcel-energy-green-button-api.yaml
  format: yaml
  label: Xcel Energy Green Button Connect My Data API
  slug: xcel-energy-green-button-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xcel-energy/refs/heads/main/openapi/xcel-energy-green-button-api.yaml
- filename: xcel-energy-smart-meter-api.yaml
  format: yaml
  label: Xcel Energy Smart Meter IEEE 2030.5 API
  slug: xcel-energy-smart-meter-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xcel-energy/refs/heads/main/openapi/xcel-energy-smart-meter-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories: []
  pricingCategory: Non-Commercial (Regulated Data Sharing)
description: 'FinOps shape for Xcel Energy is non-commercial: API access is provided to customers and authorized third parties under ESPI / Green Button regulation rather than as a billable service. There is no Xcel-issued invoice for API usage and no public per-request meter.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Xcel Energy Inc.
  ProviderName: Xcel Energy
  PublisherName: Xcel Energy Inc.
  ServiceCategory: Regulated Utility / Energy Data
  ServiceName: Xcel Energy Developer APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - third_party_provider
  - customer_authorization
  name: espi_data_volume
  unit: GB
name: Xcel Energy Finops
provider_name: Xcel Energy
provider_slug: xcel-energy
publisher_name: Xcel Energy Inc.
service_category: Regulated Utility / Energy Data
slug: xcel-energy-finops
source_filename: xcel-energy-finops.yml
source_heading: FinOps Profile
source_url: https://developer-apim.aws.xcelenergy.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Xcel Energy\nproviderId: xcel-energy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Energy Data\n  - Utility\n  - Green Button\ndescription: 'FinOps shape for Xcel Energy is non-commercial: API access is provided to customers\n  and authorized third parties under ESPI / Green Button regulation rather than as a billable\n  service. There is no Xcel-issued invoice for API usage and no public per-request meter.'\nsources:\n  - https://developer-apim.aws.xcelenergy.com/\n  - https://my.xcelenergy.com/s/\nnotes: Xcel Energy does not bill for API access. The provider's commercial relationship with\n  customers is energy delivery, not data access. FOCUS columns are populated for completeness;\n  meters reflect data-volume telemetry rather than billable line items.\nalignedWith:\n  framework: FinOps Foundation Framework\n\
  \  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Xcel Energy Inc.\nserviceCategory: Regulated Utility / Energy Data\nbillingModel:\n  pricingCategory: Non-Commercial (Regulated Data Sharing)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Xcel Energy Developer APIs\n  ServiceCategory: Regulated Utility / Energy Data\n  ProviderName: Xcel Energy\n  PublisherName: Xcel Energy Inc.\n  InvoiceIssuerName: Xcel Energy Inc.\n  BillingCurrency: USD\nmeters:\n  - name: espi_data_volume\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - third_party_provider\n      - customer_authorization\nprinciples:\n  - name: Visibility\n    description: Third-party providers see ESPI data flow through their own ingestion pipeline;\n      Xcel does not publish a usage dashboard for downstream consumers.\n  - name: Allocation\n\
  \    description: Allocation occurs at the third-party provider's own infrastructure (per\n      authorized customer or per service offering), not on a Xcel invoice.\n  - name: Optimization\n    description: Levers are ESPI subscription cadence (daily vs. real-time), batch sizing on\n      NotificationLink callbacks, and limiting authorized data scope to what the application\n      needs.\n  - name: Accountability\n    description: The third-party provider's product team owns the integration; Xcel's role is\n      regulated data fiduciary rather than billable counterparty.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/xcel-energy/refs/heads/main/finops/xcel-energy-finops.yml
sources:
- https://developer-apim.aws.xcelenergy.com/
- https://my.xcelenergy.com/s/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Energy Data
- Utility
- Green Button
---
