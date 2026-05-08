---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: weatherbit-current-weather-openapi-original.yml
  format: yaml
  label: Weatherbit Current Weather API
  slug: weatherbit-current-weather-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/weatherbit/refs/heads/main/openapi/weatherbit-current-weather-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps for Weatherbit. Weatherbit bills as a tiered subscription (Free / Standard / Plus / Business / Enterprise) with a daily call quota and per-second burst limit per tier, plus an optional Premium Support add-on at $500/mo. Cost optimization is dominated by tier selection and call discipline (caching, batching) since billable units are daily call counts within tier.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Weatherbit.io
  ProviderName: Weatherbit
  PublisherName: Weatherbit.io
  ServiceCategory: Weather Data API
  ServiceName: Weatherbit
layout: finops
meters:
- aggregation: sum
  description: Count of billable API calls per key per day across all data endpoints; the daily quota scales by subscription tier.
  dimensions:
  - tier
  - api_key
  - endpoint
  name: api_calls
  unit: request
- aggregation: sum
  description: Calls against the historical-weather endpoints; separately capped on the Free tier.
  dimensions:
  - tier
  - api_key
  name: historical_calls
  unit: request
- aggregation: sum
  description: Recurring monthly subscription fee for the chosen tier (Standard / Plus / Business / Enterprise).
  dimensions:
  - tier
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Optional Premium Support add-on at $500/mo.
  name: premium_support
  unit: month
name: Weatherbit Finops
provider_name: Weatherbit
provider_slug: weatherbit
publisher_name: Weatherbit.io
service_category: Weather Data API
slug: weatherbit-finops
source_filename: weatherbit-finops.yml
source_heading: FinOps Profile
source_url: https://www.weatherbit.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Weatherbit\nproviderId: weatherbit\npublisherName: Weatherbit.io\nserviceCategory: Weather Data API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Weather\n  - Forecasting\n  - Historical Data\n  - Air Quality\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Weatherbit. Weatherbit bills as a tiered subscription (Free /\n  Standard / Plus / Business / Enterprise) with a daily call quota and per-second burst limit per tier,\n  plus an optional Premium Support add-on at $500/mo. Cost optimization is dominated by tier selection\n  and call discipline (caching, batching) since billable units are daily call counts\
  \ within tier.\nsources:\n  - https://www.weatherbit.io/pricing\n  - https://www.weatherbit.io/api\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Weatherbit\n  ServiceCategory: Weather Data API\n  ProviderName: Weatherbit\n  PublisherName: Weatherbit.io\n  InvoiceIssuerName: Weatherbit.io\n  BillingCurrency: USD\nmeters:\n  - name: api_calls\n    description: Count of billable API calls per key per day across all data endpoints; the daily\n      quota scales by subscription tier.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - tier\n      - api_key\n      - endpoint\n  - name: historical_calls\n    description: Calls against the historical-weather endpoints; separately capped on the Free tier.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - tier\n      - api_key\n  - name: subscription_fee\n    description: Recurring\
  \ monthly subscription fee for the chosen tier (Standard / Plus / Business /\n      Enterprise).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: premium_support\n    description: Optional Premium Support add-on at $500/mo.\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track call counts via the API key's dashboard at weatherbit.io; the dashboard surfaces\n      per-key daily consumption and remaining quota for the tier.\n  - name: Allocation\n    description: Use one API key per consuming application or environment so tier cost can be allocated\n      cleanly to the owning team. Tag keys in the dashboard with the consuming service name.\n  - name: Optimization\n    description: Cache forecast and current-weather responses (forecast data updates on a coarse cycle),\n      batch geocodes via location lookups, and right-size the tier — moving from Plus to Business is\n      worthwhile only when sustained calls exceed\
  \ 250,000/day.\n  - name: Accountability\n    description: The integration owner holds accountability; review the dashboard's monthly call trend\n      versus tier quota at each renewal cycle and before launching new endpoints / locations.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/weatherbit/refs/heads/main/finops/weatherbit-finops.yml
sources:
- https://www.weatherbit.io/pricing
- https://www.weatherbit.io/api
specification: FinOps Framework
tags:
- Weather
- Forecasting
- Historical Data
- Air Quality
- FinOps
- FOCUS
---
