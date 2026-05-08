---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: acc-admin-openapi.yml
  format: yaml
  label: Autodesk Construction Cloud Admin API
  slug: acc-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/openapi/acc-admin-openapi.yml
- filename: acc-issues-openapi.yml
  format: yaml
  label: Autodesk Construction Cloud Issues API
  slug: acc-issues-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/openapi/acc-issues-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription (Per-User / Per-Project)
description: FOCUS-aligned FinOps for Autodesk Construction Cloud — per-user / per-project subscription bundles (Model Management, Preconstruction, Construction Operations) plus standalone products (Build, Docs, BIM Collaborate Pro, Takeoff, Cost Management). API access is bundled with the underlying ACC product entitlement; no separate per-API metering. Storage in Autodesk Docs counts toward project entitlements.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Autodesk, Inc.
  PricingCategory: Subscription
  ProviderName: Autodesk
  PublisherName: Autodesk, Inc.
  ServiceCategory: Construction Software
  ServiceName: Autodesk Construction Cloud
  ServiceSubcategory: Project Management & Field Execution
layout: finops
meters:
- aggregation: max
  description: Per-user ACC product subscriptions (Build, Docs, BIM Collaborate Pro, etc.)
  dimensions:
  - product
  - bundle
  - hub
  name: acc_user_seats
  unit: seat-month
- aggregation: max
  description: Active ACC projects under the account
  dimensions:
  - hub
  - project_type
  name: acc_project_count
  unit: project
- aggregation: max
  description: Project storage consumed in Autodesk Docs / BIM 360 Docs
  dimensions:
  - hub
  - project
  name: acc_storage
  unit: GB-month
- aggregation: sum
  description: ACC API call activity — included with product entitlement, not separately billed
  dimensions:
  - api
  - app
  - project
  name: acc_api_calls
  unit: request
- aggregation: sum
  description: ACC Data Connector bulk-export jobs run
  dimensions:
  - module
  - project
  name: data_connector_exports
  unit: job
name: Autodesk Construction Cloud Finops
provider_name: Autodesk Construction Cloud
provider_slug: autodesk-construction-cloud
publisher_name: Autodesk, Inc.
service_category: Construction Software / Project Management
slug: autodesk-construction-cloud-finops
source_filename: autodesk-construction-cloud-finops.yml
source_heading: FinOps Profile
source_url: https://construction.autodesk.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Autodesk Construction Cloud\nproviderId: autodesk-construction-cloud\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Construction\n  - BIM\n  - Project Management\n  - AEC\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Autodesk Construction Cloud — per-user / per-project subscription\n  bundles (Model Management, Preconstruction, Construction Operations) plus standalone products\n  (Build, Docs, BIM Collaborate Pro, Takeoff, Cost Management). API access is bundled with the\n  underlying ACC product entitlement; no separate per-API metering. Storage in Autodesk Docs counts\n  toward project entitlements.\nsources:\n  - https://construction.autodesk.com/pricing/\n  - https://aps.autodesk.com/en/docs/acc/v1/overview/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: ACC pricing is quote-based; per-seat list\
  \ rates not publicly published. Meters below describe\n  the entitlement axes for showback rather than direct invoice lines.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Autodesk, Inc.\nserviceCategory: Construction Software / Project Management\nbillingModel:\n  pricingCategory: Subscription (Per-User / Per-Project)\n  billingFrequency: Annual\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Autodesk Construction Cloud\n  ServiceCategory: Construction Software\n  ServiceSubcategory: Project Management & Field Execution\n  ProviderName: Autodesk\n  PublisherName: Autodesk, Inc.\n  InvoiceIssuerName: Autodesk, Inc.\n  BillingCurrency: USD\n  PricingCategory: Subscription\nmeters:\n  - name: acc_user_seats\n\
  \    description: Per-user ACC product subscriptions (Build, Docs, BIM Collaborate Pro, etc.)\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - product\n      - bundle\n      - hub\n  - name: acc_project_count\n    description: Active ACC projects under the account\n    unit: project\n    aggregation: max\n    dimensions:\n      - hub\n      - project_type\n  - name: acc_storage\n    description: Project storage consumed in Autodesk Docs / BIM 360 Docs\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - hub\n      - project\n  - name: acc_api_calls\n    description: ACC API call activity — included with product entitlement, not separately billed\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - app\n      - project\n  - name: data_connector_exports\n    description: ACC Data Connector bulk-export jobs run\n    unit: job\n    aggregation: sum\n    dimensions:\n      - module\n      - project\nprinciples:\n  - name: Visibility\n\
  \    description: Use the Autodesk Account portal and ACC Admin reports to surface seat utilization,\n      active project count, and storage per hub. Pair with the ACC Data Connector to export usage\n      data for showback.\n  - name: Allocation\n    description: Allocate ACC seats and project counts by ACC hub, project owner, and division using\n      the ACC company directory and project metadata; tag APS apps by integration owner.\n  - name: Optimization\n    description: Reclaim inactive ACC seats at renewal; consolidate dormant projects; archive completed\n      projects from active storage. For data-heavy integrations, schedule Data Connector exports off-peak\n      to avoid contention with interactive users.\n  - name: Accountability\n    description: Construction IT or VDC/BIM-platform team owns ACC entitlement; review seat utilization\n      quarterly. Project executives own per-project storage and active-project counts.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/finops/autodesk-construction-cloud-finops.yml
sources:
- https://construction.autodesk.com/pricing/
- https://aps.autodesk.com/en/docs/acc/v1/overview/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Construction
- BIM
- Project Management
- AEC
- FinOps
- FOCUS
---
