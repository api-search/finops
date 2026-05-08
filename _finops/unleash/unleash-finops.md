---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: unleash-admin-api-openapi.yml
  format: yaml
  label: Unleash Admin API
  slug: admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unleash/refs/heads/main/openapi/unleash-admin-api-openapi.yml
- filename: unleash-client-api-openapi.yml
  format: yaml
  label: Unleash Client API
  slug: client-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unleash/refs/heads/main/openapi/unleash-client-api-openapi.yml
- filename: unleash-frontend-api-openapi.yml
  format: yaml
  label: Unleash Frontend API
  slug: frontend-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unleash/refs/heads/main/openapi/unleash-frontend-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (Pay-As-You-Go) / Annual (Enterprise)
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Usage Overage
description: 'FOCUS-aligned FinOps for Unleash: per-seat subscription with a monthly included API request allowance and per-million overage. Enterprise contracts swap the seat list price and overage for negotiated commitments.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Bricks Software AS
  ProviderName: Unleash
  PublisherName: Bricks Software AS
  ServiceCategory: Developer Tools
  ServiceName: Unleash
layout: finops
meters:
- aggregation: max
  description: Active named seats on the Unleash subscription
  dimensions:
  - plan
  name: seats
  unit: seat
- aggregation: sum
  description: API requests counted against the monthly included allowance
  dimensions:
  - api
  - environment
  name: api_requests_included
  unit: request
- aggregation: sum
  description: API requests above the included monthly allowance, billed per million
  dimensions:
  - api
  - environment
  name: api_requests_overage
  unit: request
name: Unleash Finops
provider_name: Unleash
provider_slug: unleash
publisher_name: Bricks Software AS (Unleash)
service_category: Developer Tools
slug: unleash-finops
source_filename: unleash-finops.yml
source_heading: FinOps Profile
source_url: https://www.getunleash.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Unleash\nproviderId: unleash\npublisherName: Bricks Software AS (Unleash)\nserviceCategory: Developer Tools\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Feature Flags\n  - Developer Tools\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Unleash: per-seat subscription with a monthly included API request allowance and per-million overage. Enterprise contracts swap the seat list price and overage for negotiated commitments.'\nsources:\n  - https://www.getunleash.io/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Subscription + Usage Overage\n  billingFrequency:\
  \ Monthly (Pay-As-You-Go) / Annual (Enterprise)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Unleash\n  ServiceCategory: Developer Tools\n  ProviderName: Unleash\n  PublisherName: Bricks Software AS\n  InvoiceIssuerName: Bricks Software AS\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: seats\n    description: Active named seats on the Unleash subscription\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\n  - name: api_requests_included\n    description: API requests counted against the monthly included allowance\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n  - name: api_requests_overage\n    description: API requests above the included monthly allowance, billed per million\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\nprinciples:\n  - name: Visibility\n\
  \    description: Use the Unleash admin UI usage views and exported audit logs (up to 2 years) to track API request volume against the monthly allowance and seat counts.\n  - name: Allocation\n    description: Allocate cost by Unleash project and environment; tag SDK clients with consumer identifiers and reconcile via project/environment dimensions in the metrics export.\n  - name: Optimization\n    description: Use SDK-side caching and the Unleash Edge / Frontend API to reduce direct Admin API hits; right-size seats by reviewing inactive users; consider self-hosted or hybrid for high-volume workloads where overage outweighs infrastructure cost.\n  - name: Accountability\n    description: Assign a feature-flag platform owner who reviews monthly seat changes and request overage charges; alert when monthly request volume approaches the 53M included threshold.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/unleash/refs/heads/main/finops/unleash-finops.yml
sources:
- https://www.getunleash.io/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Feature Flags
- Developer Tools
- FinOps
- FOCUS
---
