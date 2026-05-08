---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: google-sheets-openapi.yml
  format: yaml
  label: Google Sheets API
  slug: google-sheets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spreadsheets/refs/heads/main/openapi/google-sheets-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: FOCUS-aligned FinOps placeholder for the Spreadsheets category. No unified billing surface exists; cost and meters belong with each underlying provider (Google Workspace, Microsoft 365, SheetDB, Sheety).
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Multiple
  ProviderName: Multiple
  PublisherName: Multiple
  ServiceCategory: Productivity
  ServiceName: Spreadsheets
layout: finops
meters:
- aggregation: sum
  description: Placeholder; meters belong on each underlying provider's FinOps artifact (Google Sheets / Workspace, Microsoft Graph / 365, SheetDB, Sheety).
  name: see_component_providers
  unit: varies
name: Spreadsheets Finops
provider_name: Spreadsheets
provider_slug: spreadsheets
publisher_name: Multiple (see component providers)
service_category: Productivity / Spreadsheet Data Access
slug: spreadsheets-finops
source_filename: spreadsheets-finops.yml
source_heading: FinOps Profile
source_url: https://developers.google.com/sheets/api
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Spreadsheets\nproviderId: spreadsheets\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Spreadsheets\n  - Data\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for the Spreadsheets category. No\n  unified billing surface exists; cost and meters belong with each underlying\n  provider (Google Workspace, Microsoft 365, SheetDB, Sheety).\nsources:\n  - https://developers.google.com/sheets/api\n  - https://learn.microsoft.com/graph\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Multiple (see component providers)\nserviceCategory: Productivity / Spreadsheet Data Access\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency:\
  \ Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Spreadsheets\n  ServiceCategory: Productivity\n  ProviderName: Multiple\n  PublisherName: Multiple\n  InvoiceIssuerName: Multiple\n  BillingCurrency: USD\nmeters:\n  - name: see_component_providers\n    description: Placeholder; meters belong on each underlying provider's FinOps\n      artifact (Google Sheets / Workspace, Microsoft Graph / 365, SheetDB,\n      Sheety).\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use each underlying provider's billing dashboards (Google\n      Cloud Billing, Microsoft 365 admin, SheetDB / Sheety dashboards). No\n      cross-provider rollup is published at the Spreadsheets level.\n  - name: Allocation\n    description: Allocate per underlying provider; tag at the Google project,\n      Microsoft tenant, and SheetDB / Sheety workspace level rather than at this\n      aggregator.\n  - name: Optimization\n\
  \    description: Optimize each component independently — Google Sheets read\n      batching, Microsoft Graph delta queries, SheetDB / Sheety caching.\n  - name: Accountability\n    description: Each component sits with whoever owns the underlying tenant /\n      workspace (IT for Workspace / 365, the integration owner for SheetDB and\n      Sheety).\nnotes: Aggregator slug; see component providers for real meters and billing.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spreadsheets/refs/heads/main/finops/spreadsheets-finops.yml
sources:
- https://developers.google.com/sheets/api
- https://learn.microsoft.com/graph
specification: FinOps Framework
tags:
- Spreadsheets
- Data
- FinOps
- FOCUS
---
