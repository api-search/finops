---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Kombo Unified API
  slug: unified-api
  spec_type: OpenAPI
  url: https://api.kombo.dev/openapi.json
- filename: openapi.json
  format: json
  label: Kombo Unified HRIS API
  slug: hris-api
  spec_type: OpenAPI
  url: https://api.kombo.dev/openapi.json
- filename: openapi.json
  format: json
  label: Kombo Unified ATS API
  slug: ats-api
  spec_type: OpenAPI
  url: https://api.kombo.dev/openapi.json
- filename: openapi.json
  format: json
  label: Kombo Unified ATS-Assessment API
  slug: ats-assessment-api
  spec_type: OpenAPI
  url: https://api.kombo.dev/openapi.json
- filename: openapi.json
  format: json
  label: Kombo Unified LMS API
  slug: lms-api
  spec_type: OpenAPI
  url: https://api.kombo.dev/openapi.json
billing_model:
  billingCurrency: EUR/USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Tiered Subscription + Per-Customer
description: 'FOCUS-aligned FinOps for Kombo: tiered annual platform fee plus per-connected-customer charges, with unlimited API calls and data volume. Inactive integrations are not billed.'
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: Kombo Technologies GmbH
  ProviderName: Kombo
  PublisherName: Kombo Technologies GmbH
  ServiceCategory: Developer Tools
  ServiceName: Kombo
  ServiceSubcategory: Unified API
layout: finops
meters:
- aggregation: max
  dimensions:
  - integration
  - category
  name: connected_customers
  unit: customer
- aggregation: max
  dimensions:
  - source_system
  - category
  name: active_integrations
  unit: integration
- aggregation: sum
  dimensions:
  - plan
  name: platform_fee
  unit: year
- aggregation: sum
  dimensions:
  - integration
  - endpoint
  name: api_calls
  notes: Tracked for visibility; not billed (unlimited per pricing page).
  unit: request
- aggregation: sum
  dimensions:
  - integration
  - object_type
  name: synced_records
  unit: record
name: Kombo Finops
provider_name: Kombo
provider_slug: kombo
publisher_name: Kombo Technologies GmbH
service_category: HR Tech / Unified API
slug: kombo-finops
source_filename: kombo-finops.yml
source_heading: FinOps Profile
source_url: https://kombo.dev/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Kombo\nproviderId: kombo\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - HRIS\n  - Unified API\n  - HR Tech\ndescription: 'FOCUS-aligned FinOps for Kombo: tiered annual platform fee plus per-connected-customer\n  charges, with unlimited API calls and data volume. Inactive integrations are not billed.'\nsources:\n  - https://kombo.dev/pricing\n  - https://docs.kombo.dev/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Kombo Technologies GmbH\nserviceCategory: HR Tech / Unified API\nbillingModel:\n  pricingCategory: Tiered Subscription + Per-Customer\n  billingFrequency: Annual\n  billingCurrency: EUR/USD\n  chargeCategories:\n\
  \    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Kombo\n  ServiceCategory: Developer Tools\n  ServiceSubcategory: Unified API\n  ProviderName: Kombo\n  PublisherName: Kombo Technologies GmbH\n  InvoiceIssuerName: Kombo Technologies GmbH\n  BillingCurrency: EUR\nmeters:\n  - name: connected_customers\n    unit: customer\n    aggregation: max\n    dimensions:\n      - integration\n      - category\n  - name: active_integrations\n    unit: integration\n    aggregation: max\n    dimensions:\n      - source_system\n      - category\n  - name: platform_fee\n    unit: year\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - integration\n      - endpoint\n    notes: Tracked for visibility; not billed (unlimited per pricing page).\n  - name: synced_records\n    unit: record\n    aggregation: sum\n    dimensions:\n      - integration\n      - object_type\nprinciples:\n  - name: Visibility\n\
  \    description: Use the Kombo developer dashboard to monitor connected customers, active integrations,\n      and sync errors per plan tier; pull the same data from the API for finance dashboards.\n  - name: Allocation\n    description: Tag connected customers with internal account IDs so per-customer Kombo cost can be allocated\n      to the revenue line that customer represents.\n  - name: Optimization\n    description: Disconnect / pause integrations for churned or inactive end-customers (Kombo does not\n      charge for inactive integrations); review tier upgrades against need for sandbox / SFTP / SLAs.\n  - name: Accountability\n    description: Account managers reconcile Kombo's connected-customer count quarterly against active\n      revenue customers; renegotiate per-customer rate at the next annual cycle as volume grows.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kombo/refs/heads/main/finops/kombo-finops.yml
sources:
- https://kombo.dev/pricing
- https://docs.kombo.dev/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- HRIS
- Unified API
- HR Tech
---
