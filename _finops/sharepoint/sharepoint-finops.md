---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sharepoint-rest-openapi.json
  format: json
  label: SharePoint REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://example.com/sharepoint-rest-openapi.json
- filename: graph-sharepoint-openapi.json
  format: json
  label: Microsoft Graph API (SharePoint)
  slug: graph-api-sharepoint
  spec_type: OpenAPI
  url: https://example.com/graph-sharepoint-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  pricingCategory: Per-User Subscription
description: FOCUS-aligned FinOps shape for SharePoint Online. Cost is dominated by per-user Microsoft 365 / SharePoint subscription licensing; storage overages, additional file storage SKUs, and Copilot add-ons are layered on top. SharePoint API throttling is enforced in Resource Units (not dollars), so RUs serve as an internal capacity meter rather than a billable line. Microsoft invoices SharePoint as part of the Microsoft 365 invoice via the customer's licensing channel (EA, CSP, MCA, web direct).
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Collaboration / Document Management SaaS
  ServiceName: Microsoft SharePoint
layout: finops
meters:
- aggregation: max
  description: Per-user license count (drives the bulk of SharePoint subscription cost)
  dimensions:
  - sku
  name: licensed_users
  unit: seat
- aggregation: max
  description: Microsoft 365 Copilot add-on seats ($30/user/month)
  dimensions:
  - base_sku
  name: copilot_addon_users
  unit: seat
- aggregation: sum
  description: Site collection storage consumed (drives storage add-on purchases above pooled allocation)
  dimensions:
  - site
  name: site_storage
  unit: GB
- aggregation: sum
  description: Microsoft Graph Resource Units consumed by integrations (operational meter for throttling, not directly billed)
  dimensions:
  - app
  - tenant
  name: graph_resource_units
  unit: resource-unit
- aggregation: sum
  description: Raw SharePoint REST / CSOM / Graph requests (operational meter)
  dimensions:
  - app
  - api_type
  name: api_requests
  unit: request
name: Sharepoint Finops
provider_name: Microsoft SharePoint
provider_slug: sharepoint
publisher_name: Microsoft Corporation
service_category: Collaboration / Document Management SaaS
slug: sharepoint-finops
source_filename: sharepoint-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/microsoft-365/sharepoint/compare-sharepoint-plans
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft SharePoint\nproviderId: sharepoint\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - SharePoint\n  - Microsoft 365\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for SharePoint Online. Cost is dominated by per-user Microsoft\n  365 / SharePoint subscription licensing; storage overages, additional file storage SKUs, and Copilot\n  add-ons are layered on top. SharePoint API throttling is enforced in Resource Units (not dollars), so\n  RUs serve as an internal capacity meter rather than a billable line. Microsoft invoices SharePoint as\n  part of the Microsoft 365 invoice via the customer's licensing channel (EA, CSP, MCA, web direct).\nsources:\n  - https://www.microsoft.com/en-us/microsoft-365/sharepoint/compare-sharepoint-plans\n  - https://learn.microsoft.com/en-us/sharepoint/dev/general-development/how-to-avoid-getting-throttled-or-blocked-in-sharepoint-online\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Collaboration / Document Management SaaS\nbillingModel:\n  pricingCategory: Per-User Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Microsoft SharePoint\n  ServiceCategory: Collaboration / Document Management SaaS\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\nmeters:\n  - name: licensed_users\n    description: Per-user license count (drives the bulk of SharePoint subscription cost)\n    unit: seat\n    aggregation: max\n    dimensions:\n      - sku\n  - name: copilot_addon_users\n    description: Microsoft 365 Copilot add-on seats ($30/user/month)\n\
  \    unit: seat\n    aggregation: max\n    dimensions:\n      - base_sku\n  - name: site_storage\n    description: Site collection storage consumed (drives storage add-on purchases above pooled allocation)\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - site\n  - name: graph_resource_units\n    description: Microsoft Graph Resource Units consumed by integrations (operational meter for throttling,\n      not directly billed)\n    unit: resource-unit\n    aggregation: sum\n    dimensions:\n      - app\n      - tenant\n  - name: api_requests\n    description: Raw SharePoint REST / CSOM / Graph requests (operational meter)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - app\n      - api_type\nprinciples:\n  - name: Visibility\n    description: Use the Microsoft 365 admin center license-usage reports plus the SharePoint admin center\n      storage and activity reports for the licensing side. For API consumption, instrument apps to log\n      Graph Resource Units\
  \ and track 429/503 rates against the published per-app per-tenant RU limits.\n  - name: Allocation\n    description: Allocate license cost by department / cost center via Entra (Azure AD) group attributes.\n      Storage attribution maps cleanly to site collections — tag site collections with owning team metadata.\n      Multi-Geo deployments require per-geo allocation since usage measurement isn't shared.\n  - name: Optimization\n    description: Right-size licenses against active-user reports; reclaim inactive seats. Prefer Microsoft\n      Graph over CSOM/REST in integrations (lower RU cost). Use delta queries with tokens (1 RU instead\n      of 2). Decorate traffic with proper User-Agent and AppID to avoid soft prioritization penalties.\n      Run bulk-scanning workloads off-peak.\n  - name: Accountability\n    description: IT / Workplace Engineering owns the M365 license bundle; integration-platform / app\n      owners are accountable for staying inside per-app RU limits. Finance\
  \ reviews the consolidated\n      Microsoft 365 invoice; security reviews tenant-level throttling and external-sharing telemetry\n      monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sharepoint/refs/heads/main/finops/sharepoint-finops.yml
sources:
- https://www.microsoft.com/en-us/microsoft-365/sharepoint/compare-sharepoint-plans
- https://learn.microsoft.com/en-us/sharepoint/dev/general-development/how-to-avoid-getting-throttled-or-blocked-in-sharepoint-online
specification: FinOps Framework
tags:
- SharePoint
- Microsoft 365
- FinOps
- FOCUS
---
