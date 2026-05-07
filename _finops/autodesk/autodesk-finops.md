---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: autodesk-authentication-openapi.yml
  format: yaml
  label: Autodesk Authentication API
  slug: authentication-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-authentication-openapi.yml
- filename: autodesk-data-management-openapi.yml
  format: yaml
  label: Autodesk Data Management API
  slug: data-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-data-management-openapi.yml
- filename: autodesk-model-derivative-openapi.yml
  format: yaml
  label: Autodesk Model Derivative API
  slug: model-derivative-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-model-derivative-openapi.yml
- filename: autodesk-design-automation-openapi.yml
  format: yaml
  label: Autodesk Design Automation API
  slug: design-automation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-design-automation-openapi.yml
- filename: autodesk-webhooks-openapi.yml
  format: yaml
  label: Autodesk Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-webhooks-openapi.yml
- filename: autodesk-reality-capture-openapi.yml
  format: yaml
  label: Autodesk Reality Capture API
  slug: reality-capture-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-reality-capture-openapi.yml
- filename: autodesk-sustainability-data-openapi.yml
  format: yaml
  label: Autodesk Sustainability Data API
  slug: sustainability-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-sustainability-data-openapi.yml
- filename: autodesk-parameters-openapi.yml
  format: yaml
  label: Autodesk Parameters API
  slug: parameters-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-parameters-openapi.yml
- filename: autodesk-tandem-data-openapi.yml
  format: yaml
  label: Autodesk Tandem Data API
  slug: tandem-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-tandem-data-openapi.yml
- filename: autodesk-flow-graph-engine-openapi.yml
  format: yaml
  label: Autodesk Flow Graph Engine API
  slug: flow-graph-engine-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-flow-graph-engine-openapi.yml
- filename: autodesk-acc-account-admin-openapi.yml
  format: yaml
  label: Autodesk ACC Account Admin API
  slug: acc-account-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-acc-account-admin-openapi.yml
- filename: autodesk-bim360-openapi.yml
  format: yaml
  label: Autodesk BIM 360 API
  slug: bim-360-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-bim360-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies by region)
  billingFrequency: Monthly / Annual (subscriptions); On-Demand (Cloud Credits)
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Pay-As-You-Go (Cloud Credits)
description: FOCUS-aligned FinOps for Autodesk — hybrid model combining (a) per-seat product subscriptions for desktop/cloud apps (AutoCAD, Revit, etc.) and (b) Cloud Credit-metered APS API consumption for Model Derivative, Design Automation, Reality Capture, and Data Exchange. Authentication / Data Management / Webhooks / Viewer APIs are free.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Autodesk, Inc.
  PricingCategory: Subscription + Pay-As-You-Go
  ProviderName: Autodesk
  PublisherName: Autodesk, Inc.
  ServiceCategory: Design / Engineering Software
  ServiceName: Autodesk Platform Services
  ServiceSubcategory: Platform APIs (APS)
layout: finops
meters:
- aggregation: sum
  description: Cloud Credits consumed by chargeable APS API operations
  dimensions:
  - api
  - operation
  - app
  - region
  name: cloud_credits_consumed
  unit: credit
- aggregation: sum
  description: Model Derivative translation jobs (counted toward Cloud Credits)
  dimensions:
  - source_format
  - target_format
  - app
  name: model_derivative_translations
  unit: job
- aggregation: sum
  description: Design Automation cloud-engine minutes consumed
  dimensions:
  - engine
  - work_item
  - app
  name: design_automation_minutes
  unit: minute
- aggregation: sum
  description: Reality Capture photo-processing jobs (Cloud Credits)
  dimensions:
  - resolution
  - photo_count
  name: reality_capture_processing
  unit: job
- aggregation: max
  description: Per-seat Autodesk product subscriptions (AutoCAD, Revit, Inventor, Maya, etc.)
  dimensions:
  - product
  - plan
  name: product_seats
  unit: seat-month
- aggregation: max
  description: Storage consumed in Autodesk Docs / BIM 360 Docs / OSS buckets
  dimensions:
  - hub
  - region
  name: storage_consumption
  unit: GB-month
name: Autodesk Finops
provider_name: Autodesk
provider_slug: autodesk
publisher_name: Autodesk, Inc.
service_category: Design / Engineering Software / Platform APIs
slug: autodesk-finops
source_filename: autodesk-finops.yml
source_heading: FinOps Profile
source_url: https://aps.autodesk.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Autodesk\nproviderId: autodesk\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - 3D Modeling\n  - BIM\n  - CAD\n  - Construction\n  - Engineering\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Autodesk — hybrid model combining (a) per-seat product subscriptions\n  for desktop/cloud apps (AutoCAD, Revit, etc.) and (b) Cloud Credit-metered APS API consumption for\n  Model Derivative, Design Automation, Reality Capture, and Data Exchange. Authentication / Data Management\n  / Webhooks / Viewer APIs are free.\nsources:\n  - https://aps.autodesk.com/pricing\n  - https://www.autodesk.com/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Autodesk, Inc.\nserviceCategory: Design / Engineering Software / Platform APIs\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go (Cloud Credits)\n  billingFrequency: Monthly / Annual (subscriptions); On-Demand (Cloud Credits)\n  billingCurrency: USD (settlement varies by region)\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Autodesk Platform Services\n  ServiceCategory: Design / Engineering Software\n  ServiceSubcategory: Platform APIs (APS)\n  ProviderName: Autodesk\n  PublisherName: Autodesk, Inc.\n  InvoiceIssuerName: Autodesk, Inc.\n  BillingCurrency: USD\n  PricingCategory: Subscription + Pay-As-You-Go\nmeters:\n  - name: cloud_credits_consumed\n    description: Cloud Credits consumed by chargeable APS API operations\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - api\n      - operation\n      - app\n      - region\n  - name: model_derivative_translations\n\
  \    description: Model Derivative translation jobs (counted toward Cloud Credits)\n    unit: job\n    aggregation: sum\n    dimensions:\n      - source_format\n      - target_format\n      - app\n  - name: design_automation_minutes\n    description: Design Automation cloud-engine minutes consumed\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - engine\n      - work_item\n      - app\n  - name: reality_capture_processing\n    description: Reality Capture photo-processing jobs (Cloud Credits)\n    unit: job\n    aggregation: sum\n    dimensions:\n      - resolution\n      - photo_count\n  - name: product_seats\n    description: Per-seat Autodesk product subscriptions (AutoCAD, Revit, Inventor, Maya, etc.)\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - product\n      - plan\n  - name: storage_consumption\n    description: Storage consumed in Autodesk Docs / BIM 360 Docs / OSS buckets\n    unit: GB-month\n    aggregation: max\n    dimensions:\n    \
  \  - hub\n      - region\nprinciples:\n  - name: Visibility\n    description: Use the APS console Cloud Credit usage report and the Autodesk Account portal to surface\n      credit consumption per app and per API; pair with the Authentication API audit logs to attribute\n      activity to specific tokens/integrations.\n  - name: Allocation\n    description: Tag APS apps (client_id) by consuming team or product line; map Autodesk product seats\n      to cost centers via Autodesk Account groups. Allocate Cloud Credits by API and by source/target\n      format dimensions.\n  - name: Optimization\n    description: Cache Model Derivative translations by source-file SHA and parameters to avoid re-translating\n      identical inputs. Tear down Design Automation work items promptly; choose the smallest engine variant\n      that satisfies the job. For Reality Capture, downsample photo sets and avoid re-processing on metadata-only\n      changes.\n  - name: Accountability\n    description: Engineering\
  \ / BIM-platform team owns APS app entitlements and Cloud Credit budget; review\n      monthly via the APS usage dashboard. Set alerts on Cloud Credit balance thresholds (e.g. 25% remaining)\n      to prevent translation outages.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/finops/autodesk-finops.yml
sources:
- https://aps.autodesk.com/pricing
- https://www.autodesk.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- 3D Modeling
- BIM
- CAD
- Construction
- Engineering
- FinOps
- FOCUS
---
