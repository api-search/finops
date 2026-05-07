---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: jones-lang-lasalle-corrigo-rest-api-openapi.yml
  format: yaml
  label: JLL Corrigo Enterprise REST API
  slug: corrigo-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jones-lang-lasalle/refs/heads/main/openapi/jones-lang-lasalle-corrigo-rest-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription + Services
description: FOCUS-aligned FinOps scaffold for JLL integration surfaces. Treated as a hybrid professional-services + technology-subscription model with no first-party billing API.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Jones Lang LaSalle IP, Inc.
  ProviderName: Jones Lang LaSalle
  PublisherName: Jones Lang LaSalle IP, Inc.
  ServiceCategory: Commercial Real Estate / Facility Management
  ServiceName: JLL Integration APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  - client
  - integration
  name: api_requests
  unit: request
- aggregation: count
  dimensions:
  - portfolio
  - property
  name: work_orders
  unit: work_order
- aggregation: count
  dimensions:
  - portfolio
  - property
  name: asset_records
  unit: record
name: Jones Lang Lasalle Finops
provider_name: Jones Lang LaSalle
provider_slug: jones-lang-lasalle
publisher_name: Jones Lang LaSalle IP, Inc.
service_category: Commercial Real Estate / Facility Management
slug: jones-lang-lasalle-finops
source_filename: jones-lang-lasalle-finops.yml
source_heading: FinOps Profile
source_url: https://www.jll.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Jones Lang LaSalle\nproviderId: jones-lang-lasalle\npublisherName: Jones Lang LaSalle IP, Inc.\nserviceCategory: Commercial Real Estate / Facility Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: JLL does not expose a public usage-billing surface. FinOps shape inferred from a\n  service-firm + technology-product hybrid model (advisory + JLL Technologies subscriptions).\n  Meters reflect plausible product line items (work orders, asset records).\ntags:\n  - Commercial Real Estate\n  - Facility Management\n  - Asset Management\n  - Work Orders\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for\
  \ JLL integration surfaces. Treated as a hybrid\n  professional-services + technology-subscription model with no first-party billing API.\nsources:\n  - https://www.jll.com/\n  - https://www.jllt.com/\n  - https://www.finops.org/framework/\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Subscription + Services\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: JLL Integration APIs\n  ServiceCategory: Commercial Real Estate / Facility Management\n  ProviderName: Jones Lang LaSalle\n  PublisherName: Jones Lang LaSalle IP, Inc.\n  InvoiceIssuerName: Jones Lang LaSalle IP, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\n      - client\n      - integration\n  - name: work_orders\n    unit: work_order\n    aggregation: count\n    dimensions:\n      - portfolio\n\
  \      - property\n  - name: asset_records\n    unit: record\n    aggregation: count\n    dimensions:\n      - portfolio\n      - property\nprinciples:\n  - name: Visibility\n    description: Track integration usage at the JLL Technologies product level; instrument\n      consumer-side calls since JLL does not publish a usage-billing API.\n  - name: Allocation\n    description: Allocate spend by portfolio / property / client engagement to mirror how\n      JLL contracts are scoped.\n  - name: Optimization\n    description: Reconcile work-order and asset-record volumes against subscription tiers;\n      use bulk export interfaces where contracts allow.\n  - name: Accountability\n    description: Each engagement has a JLL account team and an internal real-estate / FM\n      product owner who jointly own integration cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jones-lang-lasalle/refs/heads/main/finops/jones-lang-lasalle-finops.yml
sources:
- https://www.jll.com/
- https://www.jllt.com/
- https://www.finops.org/framework/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Commercial Real Estate
- Facility Management
- Asset Management
- Work Orders
- FinOps
- FOCUS
---
