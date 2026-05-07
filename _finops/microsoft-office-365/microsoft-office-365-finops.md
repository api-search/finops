---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/openapi.yaml
- filename: mail.yaml
  format: yaml
  label: Outlook Mail API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/mail.yaml
- filename: calendar.yaml
  format: yaml
  label: Outlook Calendar API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/calendar.yaml
- filename: files.yaml
  format: yaml
  label: OneDrive API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/files.yaml
- filename: sites.yaml
  format: yaml
  label: SharePoint API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/sites.yaml
- filename: teams.yaml
  format: yaml
  label: Microsoft Teams API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/teams.yaml
- filename: users.yaml
  format: yaml
  label: Office 365 Users API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/users.yaml
- filename: planner.yaml
  format: yaml
  label: Planner API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/planner.yaml
- filename: microsoft-graph-api-openapi.yml
  format: yaml
  label: Office 365 Groups API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-office-365/refs/heads/main/openapi/microsoft-graph-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Microsoft 365 / Office 365: tiered per-user-per-month subscriptions across Business (Basic / Standard / Premium) and Enterprise (E3 / E5 / E7) plans plus frontline F1 / F3 SKUs; programmatic access via Microsoft Graph included at no incremental per-call charge.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Productivity
  ServiceName: Microsoft 365
layout: finops
meters:
- aggregation: sum
  description: Microsoft 365 seat licences across Business and Enterprise SKUs
  dimensions:
  - tenant
  - sku
  - with_teams
  name: m365_seats
  unit: seat
- aggregation: sum
  description: Exchange Online mailbox storage in use
  dimensions:
  - mailbox
  name: mailbox_storage
  unit: GB
- aggregation: sum
  description: OneDrive for Business storage in use per user
  dimensions:
  - user
  - tenant
  name: onedrive_storage
  unit: GB
- aggregation: sum
  description: SharePoint storage in use per site
  dimensions:
  - site
  - tenant
  name: sharepoint_storage
  unit: GB
- aggregation: sum
  description: Microsoft Graph API calls (no charge; tracked for throttling)
  dimensions:
  - application
  - tenant
  - service
  name: graph_api_requests
  unit: request
name: Microsoft Office 365 Finops
provider_name: Microsoft Office 365
provider_slug: microsoft-office-365
publisher_name: Microsoft Corporation
service_category: Productivity
slug: microsoft-office-365-finops
source_filename: microsoft-office-365-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/microsoft-365/business/compare-all-plans
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Office 365\nproviderId: microsoft-office-365\npublisherName: Microsoft Corporation\nserviceCategory: Productivity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Productivity\n  - Microsoft 365\n  - Microsoft\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Microsoft 365 / Office 365: tiered per-user-per-month subscriptions\n  across Business (Basic / Standard / Premium) and Enterprise (E3 / E5 / E7) plans plus frontline F1 /\n  F3 SKUs; programmatic access via Microsoft Graph included at no incremental per-call charge.'\nsources:\n  - https://www.microsoft.com/en-us/microsoft-365/business/compare-all-plans\n\
  \  - https://www.microsoft.com/en-us/microsoft-365/enterprise/microsoft365-plans-and-pricing\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Microsoft 365\n  ServiceCategory: Productivity\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: m365_seats\n    description: Microsoft 365 seat licences across Business and Enterprise SKUs\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - sku\n      - with_teams\n  - name: mailbox_storage\n    description: Exchange Online mailbox storage in use\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - mailbox\n  - name: onedrive_storage\n    description: OneDrive for Business storage in use per user\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - user\n      - tenant\n  - name: sharepoint_storage\n    description: SharePoint storage in use per site\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - site\n      - tenant\n  - name: graph_api_requests\n    description: Microsoft Graph API calls (no charge; tracked for throttling)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - application\n      - tenant\n      - service\nprinciples:\n  - name: Visibility\n    description: Use the Microsoft 365 admin centre Active Users and product-usage reports, plus Microsoft\n      Cost Management for the SKU billing line.\n  - name: Allocation\n    description: Map seat licences to Entra groups bound to cost-centres for chargeback / showback; use\n      group-based licensing to keep allocation in sync.\n  - name: Optimization\n    description: Right-size SKU mix (Business Basic for kiosk/web users, Standard / E3 for desktop power\n      users, E5 only where Power BI\
  \ Pro / Defender P2 / Entra ID P2 is needed); reclaim inactive licences\n      via Microsoft 365 admin centre activity reports.\n  - name: Accountability\n    description: IT owns SKU mix and Entra group-based licence assignment; finance owns the contract;\n      app owners reconcile programmatic Graph usage to the throttling budget.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-office-365/refs/heads/main/finops/microsoft-office-365-finops.yml
sources:
- https://www.microsoft.com/en-us/microsoft-365/business/compare-all-plans
- https://www.microsoft.com/en-us/microsoft-365/enterprise/microsoft365-plans-and-pricing
specification: FinOps Framework
tags:
- Productivity
- Microsoft 365
- Microsoft
- FinOps
- FOCUS
---
