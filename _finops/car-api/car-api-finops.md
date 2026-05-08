---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: car-api-openapi-original.yml
  format: yaml
  label: CarAPI Vehicle API
  slug: vehicle-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/car-api/refs/heads/main/openapi/car-api-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Refund
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for CarAPI: annual subscription tiers (Base, Plus, Premium) priced by daily request quota, billed yearly through Stripe.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Stripe (on behalf of CarAPI)
  ProviderName: CarAPI
  PublisherName: CarAPI LLC
  ServiceCategory: Automotive Data API
  ServiceName: CarAPI
layout: finops
meters:
- aggregation: sum
  dimensions:
  - plan
  name: annual_subscription
  unit: year
- aggregation: sum
  dimensions:
  - endpoint
  - api
  - plan
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - endpoint
  - plan
  name: overage_requests
  unit: request
name: Car Api Finops
provider_name: Car API (carapi.app)
provider_slug: car-api
publisher_name: CarAPI LLC
service_category: Automotive Data API
slug: car-api-finops
source_filename: car-api-finops.yml
source_heading: FinOps Profile
source_url: https://carapi.app/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Car API (carapi.app)\nproviderId: car-api\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cost Management\n  - Automotive Data\n  - Vehicle API\ndescription: 'FOCUS-aligned FinOps for CarAPI: annual subscription tiers (Base, Plus, Premium) priced\n  by daily request quota, billed yearly through Stripe.'\nsources:\n  - https://carapi.app/pricing\n  - https://carapi.app/docs/getting-started\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CarAPI LLC\nserviceCategory: Automotive Data API\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n\
  \    - Usage\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: CarAPI\n  ServiceCategory: Automotive Data API\n  ProviderName: CarAPI\n  PublisherName: CarAPI LLC\n  InvoiceIssuerName: Stripe (on behalf of CarAPI)\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: annual_subscription\n    unit: year\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - api\n      - plan\n  - name: overage_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - plan\nprinciples:\n  - name: Visibility\n    description: Track daily request consumption against the plan quota in the CarAPI account dashboard;\n      JWT payload exposes rate_limit_type for soft vs hard tracking.\n  - name: Allocation\n    description: Issue separate JWTs per consuming application or environment to attribute usage; CarAPI\n      bills per account, so\
  \ application-level chargeback requires upstream tagging.\n  - name: Optimization\n    description: Cache JWTs and entity responses (using the 'modified' timestamp filter) to avoid redundant\n      requests; right-size plan tier (Base/Plus/Premium) to actual daily peak rather than provisioning headroom.\n  - name: Accountability\n    description: Annual renewal cadence makes plan-tier review a yearly checkpoint; reconcile daily 429\n      counts against soft-limit overage charges before renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/car-api/refs/heads/main/finops/car-api-finops.yml
sources:
- https://carapi.app/pricing
- https://carapi.app/docs/getting-started
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cost Management
- Automotive Data
- Vehicle API
---
