---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-planner-openapi.yml
  format: yaml
  label: Microsoft Planner API
  slug: microsoft-planner-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-planner/refs/heads/main/openapi/microsoft-planner-openapi.yml
- filename: microsoft-planner-openapi.yml
  format: yaml
  label: Microsoft Graph Plans API
  slug: microsoft-graph-plans-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-planner/refs/heads/main/openapi/microsoft-planner-openapi.yml
- filename: microsoft-planner-openapi.yml
  format: yaml
  label: Microsoft Graph Tasks API
  slug: microsoft-graph-tasks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-planner/refs/heads/main/openapi/microsoft-planner-openapi.yml
- filename: microsoft-planner-openapi.yml
  format: yaml
  label: Microsoft Graph Buckets API
  slug: microsoft-graph-buckets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-planner/refs/heads/main/openapi/microsoft-planner-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription (bundled with Microsoft 365)
description: 'FOCUS-aligned FinOps for Microsoft Planner: basic Planner is bundled with all paid Microsoft 365 SKUs; advanced Project capabilities are sold as Planner Plan 1 / 3 / 5 per-user-per-month subscriptions. APIs included with the seat licence; no per-call charge.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Project and Task Management
  ServiceName: Microsoft Planner
layout: finops
meters:
- aggregation: sum
  description: Microsoft 365 seats that grant basic Planner
  dimensions:
  - tenant
  - sku
  name: m365_seats
  unit: seat
- aggregation: sum
  description: Planner Plan 1 / 3 / 5 seats (formerly Project Plan 1 / 3 / 5)
  dimensions:
  - tenant
  - sku
  name: planner_premium_seats
  unit: seat
- aggregation: sum
  description: Microsoft Graph planner API calls (no charge; tracked for throttling)
  dimensions:
  - application
  - tenant
  name: planner_api_requests
  unit: request
- aggregation: max
  description: Plans currently owned by Microsoft 365 Groups in the tenant
  dimensions:
  - tenant
  name: active_plans
  unit: plan
name: Microsoft Planner Finops
provider_name: Microsoft Planner
provider_slug: microsoft-planner
publisher_name: Microsoft Corporation
service_category: Project and Task Management
slug: microsoft-planner-finops
source_filename: microsoft-planner-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/microsoft-365/planner/microsoft-planner-pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Planner\nproviderId: microsoft-planner\npublisherName: Microsoft Corporation\nserviceCategory: Project and Task Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Project Management\n  - Tasks\n  - Microsoft 365\n  - Planner\n  - Microsoft\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Microsoft Planner: basic Planner is bundled with all paid Microsoft\n  365 SKUs; advanced Project capabilities are sold as Planner Plan 1 / 3 / 5 per-user-per-month subscriptions.\n  APIs included with the seat licence; no per-call charge.'\nsources:\n  - https://www.microsoft.com/en-us/microsoft-365/planner/microsoft-planner-pricing\n\
  \  - https://learn.microsoft.com/en-us/graph/api/resources/planner-overview\nbillingModel:\n  pricingCategory: Tiered Subscription (bundled with Microsoft 365)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Microsoft Planner\n  ServiceCategory: Project and Task Management\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: m365_seats\n    description: Microsoft 365 seats that grant basic Planner\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - sku\n  - name: planner_premium_seats\n    description: Planner Plan 1 / 3 / 5 seats (formerly Project Plan 1 / 3 / 5)\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - sku\n  - name: planner_api_requests\n    description: Microsoft Graph planner\
  \ API calls (no charge; tracked for throttling)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - application\n      - tenant\n  - name: active_plans\n    description: Plans currently owned by Microsoft 365 Groups in the tenant\n    unit: plan\n    aggregation: max\n    dimensions:\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Use Microsoft 365 admin centre licence reports for seat utilisation; capture Microsoft\n      Graph throttling telemetry from request-id and x-ms-throttle headers for Planner API consumers.\n  - name: Allocation\n    description: Tag premium Planner Plan 1 / 3 / 5 seats to projects / business-units via Entra group-based\n      licensing.\n  - name: Optimization\n    description: Stay on basic Planner for routine task management; reserve Plan 3 / 5 for portfolio-managed\n      projects; replace polling code with Graph change notifications.\n  - name: Accountability\n    description: Project Management Office (PMO) owns Plan\
  \ 3 / 5 utilisation; workplace IT owns the M365\n      SKU mix; engineering owns Graph API consumption.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-planner/refs/heads/main/finops/microsoft-planner-finops.yml
sources:
- https://www.microsoft.com/en-us/microsoft-365/planner/microsoft-planner-pricing
- https://learn.microsoft.com/en-us/graph/api/resources/planner-overview
specification: FinOps Framework
tags:
- Project Management
- Tasks
- Microsoft 365
- Planner
- Microsoft
- FinOps
- FOCUS
---
