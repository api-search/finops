---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-edge-addons-api.yaml
  format: yaml
  label: Microsoft Edge Add-ons API
  slug: edge-addons-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-edge/refs/heads/main/openapi/microsoft-edge-addons-api.yaml
- filename: microsoft-edge-devtools-api.yaml
  format: yaml
  label: Microsoft Edge DevTools Protocol HTTP API
  slug: edge-devtools-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-edge/refs/heads/main/openapi/microsoft-edge-devtools-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Bundled with Microsoft 365
description: 'FOCUS-aligned FinOps for Microsoft Edge: the browser and developer APIs are free, with enterprise management surfaced as a no-incremental-charge feature of Microsoft 365 and Entra ID subscriptions. Costs flow through the bundled Microsoft 365 SKU rather than per-call metering.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Developer Tools
  ServiceName: Microsoft Edge
layout: finops
meters:
- aggregation: sum
  description: Active Edge for Business users counted via the parent Microsoft 365 / Entra ID seat licenses
  dimensions:
  - tenant
  - sku
  name: edge_for_business_seats
  unit: seat
- aggregation: sum
  description: Calls to the Edge Add-ons publishing API (no charge; tracked for fair-use)
  dimensions:
  - partner_center_account
  name: addons_api_calls
  unit: request
name: Microsoft Edge Finops
provider_name: Microsoft Edge
provider_slug: microsoft-edge
publisher_name: Microsoft Corporation
service_category: Developer Tools
slug: microsoft-edge-finops
source_filename: microsoft-edge-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/edge/business
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Edge\nproviderId: microsoft-edge\npublisherName: Microsoft Corporation\nserviceCategory: Developer Tools\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Browser\n  - Chromium\n  - Developer Tools\n  - Edge\n  - Microsoft\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Microsoft Edge: the browser and developer APIs are free, with enterprise\n  management surfaced as a no-incremental-charge feature of Microsoft 365 and Entra ID subscriptions.\n  Costs flow through the bundled Microsoft 365 SKU rather than per-call metering.'\nsources:\n  - https://www.microsoft.com/en-us/edge/business\n  - https://learn.microsoft.com/en-us/microsoft-edge/\n\
  billingModel:\n  pricingCategory: Bundled with Microsoft 365\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Microsoft Edge\n  ServiceCategory: Developer Tools\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: edge_for_business_seats\n    description: Active Edge for Business users counted via the parent Microsoft 365 / Entra ID seat licenses\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - sku\n  - name: addons_api_calls\n    description: Calls to the Edge Add-ons publishing API (no charge; tracked for fair-use)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner_center_account\nprinciples:\n  - name: Visibility\n    description: Edge consumption is observable via Microsoft 365 admin center\
  \ usage reports and Entra\n      sign-in logs; there is no separate Edge billing meter.\n  - name: Allocation\n    description: Allocate Edge for Business usage to teams via the M365 / Entra group memberships that\n      control license assignment.\n  - name: Optimization\n    description: There is no per-seat charge for Edge itself; optimization focuses on the bundled M365\n      SKU and on reducing DevTools / extension complexity inside the enterprise.\n  - name: Accountability\n    description: IT owns Edge configuration via Intune / Group Policy; finance owns the underlying M365\n      SKU.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-edge/refs/heads/main/finops/microsoft-edge-finops.yml
sources:
- https://www.microsoft.com/en-us/edge/business
- https://learn.microsoft.com/en-us/microsoft-edge/
specification: FinOps Framework
tags:
- Browser
- Chromium
- Developer Tools
- Edge
- Microsoft
- FinOps
- FOCUS
---
