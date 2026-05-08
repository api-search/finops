---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: alaska-air-flight-status-openapi.yaml
  format: yaml
  label: Alaska Airlines Flight Status API
  slug: flight-status-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alaska-air/refs/heads/main/openapi/alaska-air-flight-status-openapi.yaml
- filename: alaska-air-flight-schedules-openapi.yaml
  format: yaml
  label: Alaska Airlines Flight Schedules API
  slug: flight-schedules-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alaska-air/refs/heads/main/openapi/alaska-air-flight-schedules-openapi.yaml
- filename: alaska-air-cargo-openapi.yaml
  format: yaml
  label: Alaska Air Cargo API
  slug: cargo-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alaska-air/refs/heads/main/openapi/alaska-air-cargo-openapi.yaml
- filename: alaska-air-mileage-plan-openapi.yaml
  format: yaml
  label: Alaska Airlines Mileage Plan API
  slug: mileage-plan-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alaska-air/refs/heads/main/openapi/alaska-air-mileage-plan-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps shell for Alaska Airlines APIs: no public commercial surface - cost is determined by partner / GDS / NDC / cargo / loyalty contracts. Reconcile against the specific commercial agreement covering each integration.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Alaska Airlines, Inc.
  ProviderName: Alaska Airlines
  PublisherName: Alaska Airlines, Inc.
  ServiceCategory: Travel & Transportation
  ServiceName: Alaska Airlines APIs
layout: finops
meters:
- aggregation: sum
  description: Annual partner agreement value for API channel access
  dimensions:
  - channel
  - product
  name: partner_contract
  unit: contract-year
- aggregation: sum
  description: API call volume across distribution / cargo / loyalty endpoints (where contractually metered)
  dimensions:
  - api
  - channel
  name: api_calls
  unit: request
name: Alaska Air Finops
provider_name: Alaska Airlines
provider_slug: alaska-air
publisher_name: Alaska Airlines, Inc.
service_category: Travel & Transportation
slug: alaska-air-finops
source_filename: alaska-air-finops.yml
source_heading: FinOps Profile
source_url: https://www.alaskaair.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Alaska Airlines\nproviderId: alaska-air\npublisherName: Alaska Airlines, Inc.\nserviceCategory: Travel & Transportation\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Airlines\n  - Aviation\n  - Travel\n  - Cargo\n  - Loyalty\n  - Flight Status\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shell for Alaska Airlines APIs: no public commercial surface - cost\n  is determined by partner / GDS / NDC / cargo / loyalty contracts. Reconcile against the specific commercial\n  agreement covering each integration.'\nsources:\n  - https://www.alaskaair.com\n  - https://www.alaskacargo.com\n  - https://focus.finops.org/focus-specification/v1-3/\n\
  billingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Alaska Airlines APIs\n  ServiceCategory: Travel & Transportation\n  ProviderName: Alaska Airlines\n  PublisherName: Alaska Airlines, Inc.\n  InvoiceIssuerName: Alaska Airlines, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: partner_contract\n    description: Annual partner agreement value for API channel access\n    unit: contract-year\n    aggregation: sum\n    dimensions:\n      - channel\n      - product\n  - name: api_calls\n    description: API call volume across distribution / cargo / loyalty endpoints (where contractually\n      metered)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - channel\nprinciples:\n  - name: Visibility\n    description: Track Alaska partner-channel costs through the partner-management billing relationship;\n   \
  \   no public usage telemetry is available.\n  - name: Allocation\n    description: Allocate channel contract costs to the consuming product line (corporate booking, GDS\n      distribution, cargo, loyalty integration).\n  - name: Optimization\n    description: Right-size partner integrations during annual renewals; deprecate unused channels; consolidate\n      where possible.\n  - name: Accountability\n    description: Owned by the partner-integration / distribution leads on the consuming side; reviewed\n      against fare / cargo revenue contribution.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/alaska-air/refs/heads/main/finops/alaska-air-finops.yml
sources:
- https://www.alaskaair.com
- https://www.alaskacargo.com
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Airlines
- Aviation
- Travel
- Cargo
- Loyalty
- Flight Status
- FinOps
- FOCUS
---
