---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-excel-graph-api.yaml
  format: yaml
  label: Microsoft Graph Excel API
  slug: microsoft-graph-excel-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-excel/refs/heads/main/openapi/microsoft-excel-graph-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Subscription (bundled with Microsoft 365)
description: 'FOCUS-aligned FinOps for Microsoft Excel: bundled with Microsoft 365 / Office 365 per-user-per-month subscriptions; no incremental per-call API charge. Costs flow through the parent Microsoft 365 SKU.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Productivity
  ServiceName: Microsoft Excel
layout: finops
meters:
- aggregation: sum
  description: Microsoft 365 seats granting Excel entitlement (Business Basic / Standard / Premium / E3 / E5 / Apps for Business / Apps for Enterprise)
  dimensions:
  - tenant
  - sku
  name: m365_seats
  unit: seat
- aggregation: sum
  description: Microsoft Graph workbook API calls (no charge; tracked for capacity and throttling)
  dimensions:
  - tenant
  - application
  name: workbook_api_requests
  unit: request
- aggregation: sum
  description: Storage consumed by .xlsx files in OneDrive / SharePoint
  dimensions:
  - drive
  - tenant
  name: workbook_storage
  unit: GB
name: Microsoft Excel Finops
provider_name: Microsoft Excel
provider_slug: microsoft-excel
publisher_name: Microsoft Corporation
service_category: Productivity
slug: microsoft-excel-finops
source_filename: microsoft-excel-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/microsoft-365/business/compare-all-plans
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Excel\nproviderId: microsoft-excel\npublisherName: Microsoft Corporation\nserviceCategory: Productivity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Spreadsheets\n  - Productivity\n  - Microsoft 365\n  - Microsoft\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Microsoft Excel: bundled with Microsoft 365 / Office 365 per-user-per-month\n  subscriptions; no incremental per-call API charge. Costs flow through the parent Microsoft 365 SKU.'\nsources:\n  - https://www.microsoft.com/en-us/microsoft-365/business/compare-all-plans\n  - https://www.microsoft.com/en-us/microsoft-365/enterprise/microsoft365-plans-and-pricing\n\
  billingModel:\n  pricingCategory: Subscription (bundled with Microsoft 365)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Microsoft Excel\n  ServiceCategory: Productivity\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: m365_seats\n    description: Microsoft 365 seats granting Excel entitlement (Business Basic / Standard / Premium /\n      E3 / E5 / Apps for Business / Apps for Enterprise)\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - sku\n  - name: workbook_api_requests\n    description: Microsoft Graph workbook API calls (no charge; tracked for capacity and throttling)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - tenant\n      - application\n  - name: workbook_storage\n    description:\
  \ Storage consumed by .xlsx files in OneDrive / SharePoint\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - drive\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Use the Microsoft 365 admin centre Active Users report and Microsoft 365 Usage Analytics\n      to see Excel consumption; capture Microsoft Graph throttling telemetry from request-id and x-ms-throttle-scope\n      headers.\n  - name: Allocation\n    description: Map Microsoft 365 seat assignments to Entra groups bound to cost-centres for chargeback;\n      tag programmatic Excel API access by the calling application.\n  - name: Optimization\n    description: Right-size the Microsoft 365 SKU mix (downgrade rarely-used desktop seats to Business\n      Basic); persist workbook sessions and use $batch to reduce throttling exposure.\n  - name: Accountability\n    description: Workplace IT owns the M365 SKU mix; engineering owns Office Add-in / Graph workbook automations\n      and their throttling\
  \ budget.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-excel/refs/heads/main/finops/microsoft-excel-finops.yml
sources:
- https://www.microsoft.com/en-us/microsoft-365/business/compare-all-plans
- https://www.microsoft.com/en-us/microsoft-365/enterprise/microsoft365-plans-and-pricing
specification: FinOps Framework
tags:
- Spreadsheets
- Productivity
- Microsoft 365
- Microsoft
- FinOps
- FOCUS
---
