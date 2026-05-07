---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: aerodatabox-openapi.yml
  format: yaml
  label: AeroDataBox Flight API
  slug: aerodatabox-flight-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aerodatabox/refs/heads/main/openapi/aerodatabox-openapi.yml
- filename: aerodatabox-openapi.yml
  format: yaml
  label: AeroDataBox Aircraft API
  slug: aerodatabox-aircraft-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aerodatabox/refs/heads/main/openapi/aerodatabox-openapi.yml
- filename: aerodatabox-openapi.yml
  format: yaml
  label: AeroDataBox Airport API
  slug: aerodatabox-airport-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aerodatabox/refs/heads/main/openapi/aerodatabox-openapi.yml
- filename: aerodatabox-openapi.yml
  format: yaml
  label: AeroDataBox Statistical API
  slug: aerodatabox-statistical-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aerodatabox/refs/heads/main/openapi/aerodatabox-openapi.yml
- filename: aerodatabox-openapi.yml
  format: yaml
  label: AeroDataBox Flight Alert API
  slug: aerodatabox-flight-alert-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aerodatabox/refs/heads/main/openapi/aerodatabox-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for AeroDataBox: marketplace-mediated tiered subscription with monthly quota and overage.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: RapidAPI / api.market
  ProviderName: AeroDataBox
  PublisherName: RapidAPI / api.market
  ServiceCategory: Aviation Data
  ServiceName: AeroDataBox
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint_group
  - tier
  name: api_requests
  unit: request
- aggregation: max
  dimensions:
  - tier
  name: monthly_quota
  unit: request
- aggregation: sum
  dimensions:
  - tier
  name: overage_requests
  unit: request
- aggregation: sum
  dimensions:
  - tier
  name: subscription_fees
  unit: month
name: Aerodatabox Finops
provider_name: AeroDataBox
provider_slug: aerodatabox
publisher_name: API Marketplace (RapidAPI / api.market)
service_category: Aviation Data
slug: aerodatabox-finops
source_filename: aerodatabox-finops.yml
source_heading: FinOps Profile
source_url: https://rapidapi.com/aedbx-aedbx/api/aerodatabox
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AeroDataBox\nproviderId: aerodatabox\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: AeroDataBox is billed via API marketplaces (RapidAPI, api.market). The marketplace is\n  the publisher/invoice issuer; AeroDataBox is the underlying data provider.\ntags:\n  - FinOps\n  - FOCUS\n  - Aviation\n  - Flights\ndescription: 'FOCUS-aligned FinOps for AeroDataBox: marketplace-mediated tiered subscription with\n  monthly quota and overage.'\nsources:\n  - https://rapidapi.com/aedbx-aedbx/api/aerodatabox\n  - https://prod.api.market/api/v1/aedbx/aerodatabox\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: API Marketplace (RapidAPI / api.market)\nserviceCategory:\
  \ Aviation Data\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: AeroDataBox\n  ServiceCategory: Aviation Data\n  ProviderName: AeroDataBox\n  PublisherName: RapidAPI / api.market\n  InvoiceIssuerName: RapidAPI / api.market\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint_group\n      - tier\n  - name: monthly_quota\n    unit: request\n    aggregation: max\n    dimensions:\n      - tier\n  - name: overage_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: subscription_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Use the marketplace dashboard (RapidAPI Hub or api.market) to monitor request\n      counts, quota burn-down, and overage\
  \ exposure.\n  - name: Allocation\n    description: Issue separate API keys per consuming team/product to attribute usage.\n  - name: Optimization\n    description: Cache static lookups (airports, aircraft); right-size tier monthly; drop unused\n      endpoints from polling loops.\n  - name: Accountability\n    description: Assign a tier-renewal owner; review monthly quota utilization and overage spend.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aerodatabox/refs/heads/main/finops/aerodatabox-finops.yml
sources:
- https://rapidapi.com/aedbx-aedbx/api/aerodatabox
- https://prod.api.market/api/v1/aedbx/aerodatabox
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Aviation
- Flights
---
