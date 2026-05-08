---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: treblle-api-openapi.yml
  format: yaml
  label: Treblle Platform API
  slug: treblle-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/treblle/refs/heads/main/openapi/treblle-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Treblle: tiered subscription with hard monthly request caps on the self-serve Core plan and contract-negotiated request, retention, and workspace ceilings on Growth and Enterprise.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Treblle Limited
  ProviderName: Treblle
  PublisherName: Treblle Limited
  ServiceCategory: Developer Tools / API Observability
  ServiceName: Treblle
layout: finops
meters:
- aggregation: sum
  dimensions:
  - plan
  name: subscription_month
  unit: month
- aggregation: sum
  dimensions:
  - workspace
  - api
  name: api_requests
  unit: request
- aggregation: max
  dimensions:
  - workspace
  name: tracked_apis
  unit: api
- aggregation: max
  dimensions:
  - account
  name: workspaces
  unit: workspace
- aggregation: max
  dimensions:
  - workspace
  name: data_retention_days
  unit: day
name: Treblle Finops
provider_name: Treblle
provider_slug: treblle
publisher_name: Treblle Limited
service_category: Developer Tools / API Observability
slug: treblle-finops
source_filename: treblle-finops.yml
source_heading: FinOps Profile
source_url: https://www.treblle.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Treblle\nproviderId: treblle\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - API Observability\n  - API Intelligence\n  - Developer Tools\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Treblle: tiered subscription with hard monthly request caps\n  on the self-serve Core plan and contract-negotiated request, retention, and workspace ceilings on\n  Growth and Enterprise.'\nsources:\n  - https://www.treblle.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Treblle Limited\nserviceCategory: Developer Tools / API Observability\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Treblle\n  ServiceCategory: Developer Tools / API Observability\n  ProviderName: Treblle\n  PublisherName: Treblle Limited\n  InvoiceIssuerName: Treblle Limited\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_month\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - workspace\n      - api\n  - name: tracked_apis\n    unit: api\n    aggregation: max\n    dimensions:\n      - workspace\n  - name: workspaces\n    unit: workspace\n    aggregation: max\n    dimensions:\n      - account\n  - name: data_retention_days\n    unit: day\n    aggregation: max\n    dimensions:\n      - workspace\nprinciples:\n  - name: Visibility\n    description: Workspace usage (APIs tracked, monthly request counts, retention) is exposed in the\n      Treblle dashboard against the contracted\
  \ plan caps; finance teams reconcile against the annual\n      Core invoice or the negotiated Growth/Enterprise contract.\n  - name: Allocation\n    description: Allocate cost using Treblle workspaces and the per-API tag set already collected by\n      Treblle's API Intelligence; one workspace per Core plan, multiple on Enterprise.\n  - name: Optimization\n    description: On Core, optimize by consolidating low-volume APIs into the 10-API / 50M-request cap\n      before triggering an upgrade; on Growth and Enterprise, right-size the contracted requests-per-minute\n      and retention window to the SLO actually required by API Security and Governance use cases.\n  - name: Accountability\n    description: API platform / DevEx team owns the Treblle subscription; per-API owners are responsible\n      for keeping ingested request volume inside the workspace cap.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/treblle/refs/heads/main/finops/treblle-finops.yml
sources:
- https://www.treblle.com/pricing
specification: FinOps Framework
tags:
- API Observability
- API Intelligence
- Developer Tools
- FinOps
- FOCUS
---
