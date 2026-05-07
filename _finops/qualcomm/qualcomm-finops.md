---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: qualcomm-qualcomm-api-openapi.yml
  format: yaml
  label: Qualcomm Developer API
  slug: qualcomm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qualcomm/refs/heads/main/openapi/qualcomm-qualcomm-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Partner Program / Licensing
description: FinOps for the Qualcomm developer surface is not metered per-API; consumption is governed by Qualcomm Developer Network registration and partner-program contracts rather than by FOCUS-shaped invoices.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Qualcomm Technologies, Inc.
  ProviderName: Qualcomm
  PublisherName: Qualcomm Technologies, Inc.
  ServiceCategory: Semiconductors
  ServiceName: Qualcomm Developer Network
layout: finops
meters:
- aggregation: sum
  description: Partner-program or licensing engagement under the Qualcomm Developer Network.
  dimensions:
  - program
  name: program_engagement
  unit: varies
name: Qualcomm Finops
provider_name: qualcomm
provider_slug: qualcomm
publisher_name: Qualcomm Technologies, Inc.
service_category: Semiconductors
slug: qualcomm-finops
source_filename: qualcomm-finops.yml
source_heading: FinOps Profile
source_url: https://www.qualcomm.com/developer
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: qualcomm\nproviderId: qualcomm\npublisherName: Qualcomm Technologies, Inc.\nserviceCategory: Semiconductors\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Mobile\n  - Semiconductors\n  - FinOps\n  - FOCUS\nnotes: Qualcomm does not publish a per-API meter or invoice surface for its developer SDKs; the company's\n  revenue is principally chipset and licensing rather than API metering. FinOps mapping is left at the\n  partner-program contract level.\ndescription: FinOps for the Qualcomm developer surface is not metered per-API; consumption is governed\n  by Qualcomm Developer Network registration and partner-program contracts\
  \ rather than by FOCUS-shaped\n  invoices.\nsources:\n  - https://www.qualcomm.com/developer\nbillingModel:\n  pricingCategory: Partner Program / Licensing\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Qualcomm Developer Network\n  ServiceCategory: Semiconductors\n  ProviderName: Qualcomm\n  PublisherName: Qualcomm Technologies, Inc.\n  InvoiceIssuerName: Qualcomm Technologies, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: program_engagement\n    description: Partner-program or licensing engagement under the Qualcomm Developer Network.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - program\nprinciples:\n  - name: Visibility\n    description: Surface Qualcomm Developer Network entitlements through internal procurement records;\n      the developer portal does not expose a usage-meter API.\n  - name: Allocation\n    description: Allocate program fees and licensing costs to the device-engineering\
  \ or product-platform\n      cost centers that consume the SDKs and AI Hub access.\n  - name: Optimization\n    description: Optimization happens at program renewal; consolidate developer accounts under the appropriate\n      program tier and avoid duplicate registrations.\n  - name: Accountability\n    description: Engineering leadership owns Qualcomm Developer Network entitlements; route program\n      changes through the Qualcomm account team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/qualcomm/refs/heads/main/finops/qualcomm-finops.yml
sources:
- https://www.qualcomm.com/developer
specification: FinOps Framework
tags:
- Mobile
- Semiconductors
- FinOps
- FOCUS
---
