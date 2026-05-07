---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: abstract-api-email-reputation.yaml
  format: yaml
  label: Email Reputation API
  slug: email-reputation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-email-reputation.yaml
- filename: abstract-api-phone-intelligence.yaml
  format: yaml
  label: Phone Intelligence API
  slug: phone-intelligence
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-phone-intelligence.yaml
- filename: abstract-api-ip-geolocation.yaml
  format: yaml
  label: IP Geolocation API
  slug: ip-geolocation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-ip-geolocation.yaml
- filename: abstract-api-ip-intelligence.yaml
  format: yaml
  label: IP Intelligence API
  slug: ip-intelligence
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-ip-intelligence.yaml
- filename: abstract-api-company-enrichment.yaml
  format: yaml
  label: Company Enrichment API
  slug: company-enrichment
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-company-enrichment.yaml
- filename: abstract-api-exchange-rates.yaml
  format: yaml
  label: Exchange Rates API
  slug: exchange-rates
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-exchange-rates.yaml
- filename: abstract-api-public-holidays.yaml
  format: yaml
  label: Public Holidays API
  slug: public-holidays
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-public-holidays.yaml
- filename: abstract-api-timezones.yaml
  format: yaml
  label: Timezone API
  slug: timezones
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-timezones.yaml
- filename: abstract-api-vat-validation.yaml
  format: yaml
  label: VAT Validation API
  slug: vat-validation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-vat-validation.yaml
- filename: abstract-api-iban-validation.yaml
  format: yaml
  label: IBAN Validation API
  slug: iban-validation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-iban-validation.yaml
- filename: abstract-api-website-screenshot.yaml
  format: yaml
  label: Website Screenshot API
  slug: website-screenshot
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-website-screenshot.yaml
- filename: abstract-api-image-processing.yaml
  format: yaml
  label: Image Processing API
  slug: image-processing
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-image-processing.yaml
- filename: abstract-api-web-scraping.yaml
  format: yaml
  label: Web Scraping API
  slug: web-scraping
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-web-scraping.yaml
- filename: abstract-api-avatars.yaml
  format: yaml
  label: Avatars API
  slug: avatars
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-avatars.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps for Abstract API — tiered subscription with selectable monthly request volume per product. Each product (email, phone, IP, company) is a separate billable line and meter.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Abstract API, Inc.
  PricingCategory: Tiered Subscription
  PricingUnit: request
  ProviderName: Abstract API
  PublisherName: Abstract API, Inc.
  ServiceCategory: Data Validation / Enrichment
  ServiceName: Abstract API
layout: finops
meters:
- aggregation: max
  description: Selected monthly request volume for the active plan/product (e.g., 5k, 25k, 150k).
  dimensions:
  - product
  - plan
  - tier
  name: monthly_request_quota
  unit: request
- aggregation: sum
  description: Actual request count made against the API key, drawn from the monthly quota.
  dimensions:
  - product
  - api_key
  - status_code
  name: requests_consumed
  unit: request
- aggregation: sum
  description: Count of 429 throttled responses (signals that the 3 req/sec ceiling is being hit).
  dimensions:
  - product
  - api_key
  name: rate_throttle_events
  unit: event
- aggregation: count
  description: Monthly subscription line item for the active plan tier.
  dimensions:
  - product
  - plan
  name: plan_month
  unit: month
name: Abstract Api Finops
provider_name: Abstract API
provider_slug: abstract-api
publisher_name: Abstract API, Inc.
service_category: Data Validation / Enrichment
slug: abstract-api-finops
source_filename: abstract-api-finops.yml
source_heading: FinOps Profile
source_url: https://www.abstractapi.com/api/email-verification-validation-api
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Abstract API\nproviderId: abstract-api\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Data Validation\n  - Geolocation\n  - Email Verification\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Abstract API — tiered subscription with selectable monthly request\n  volume per product. Each product (email, phone, IP, company) is a separate billable line and meter.\nsources:\n  - https://www.abstractapi.com/api/email-verification-validation-api\n  - https://docs.abstractapi.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Abstract API, Inc.\nserviceCategory: Data Validation / Enrichment\n\
  billingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Abstract API\n  ServiceCategory: Data Validation / Enrichment\n  ProviderName: Abstract API\n  PublisherName: Abstract API, Inc.\n  InvoiceIssuerName: Abstract API, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Tiered Subscription\n  PricingUnit: request\nmeters:\n  - name: monthly_request_quota\n    description: Selected monthly request volume for the active plan/product (e.g., 5k, 25k, 150k).\n    unit: request\n    aggregation: max\n    dimensions:\n      - product\n      - plan\n      - tier\n  - name: requests_consumed\n    description: Actual request count made against the API key, drawn from the monthly quota.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\n      - api_key\n      - status_code\n\
  \  - name: rate_throttle_events\n    description: Count of 429 throttled responses (signals that the 3 req/sec ceiling is being hit).\n    unit: event\n    aggregation: sum\n    dimensions:\n      - product\n      - api_key\n  - name: plan_month\n    description: Monthly subscription line item for the active plan tier.\n    unit: month\n    aggregation: count\n    dimensions:\n      - product\n      - plan\nprinciples:\n  - name: Visibility\n    description: Use the Abstract API dashboard's request-counter and the per-product usage page to track\n      consumption against the selected monthly volume tier.\n  - name: Allocation\n    description: Issue separate API keys per product / service / environment so requests can be attributed\n      to consuming applications when reconciling the monthly invoice.\n  - name: Optimization\n    description: Cache validation results client-side (especially email and IP enrichment) to stay inside\n      the tier; right-size the monthly volume sub-tier\
  \ each renewal cycle and switch to annual for the\n      10% discount when usage is steady.\n  - name: Accountability\n    description: Engineering owns API key issuance and caching; the consuming product team owns the monthly\n      request budget; finance owns the renewal decision and annual-vs-monthly billing trade-off.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/finops/abstract-api-finops.yml
sources:
- https://www.abstractapi.com/api/email-verification-validation-api
- https://docs.abstractapi.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Data Validation
- Geolocation
- Email Verification
- FinOps
- FOCUS
---
