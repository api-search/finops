---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: chase-account-and-customer-information-api-openapi.yml
  format: yaml
  label: Chase Account and Customer Information API
  slug: account-and-customer-information-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-account-and-customer-information-api-openapi.yml
- filename: chase-account-aggregation-user-consent-api-openapi.yml
  format: yaml
  label: Chase Account Aggregation User Consent API
  slug: account-aggregation-user-consent-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-account-aggregation-user-consent-api-openapi.yml
- filename: chase-rewards-balance-api-openapi.yml
  format: yaml
  label: Chase Rewards Balance API
  slug: rewards-balance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-rewards-balance-api-openapi.yml
- filename: chase-loyalty-pay-with-points-order-service-api-openapi.yml
  format: yaml
  label: Chase Loyalty Pay with Points Order Service API
  slug: loyalty-pay-with-points-order-service-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-loyalty-pay-with-points-order-service-api-openapi.yml
- filename: chase-loyalty-pay-with-points-enrollment-service-api-openapi.yml
  format: yaml
  label: Chase Loyalty Pay with Points Enrollment Service API
  slug: loyalty-pay-with-points-enrollment-service-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-loyalty-pay-with-points-enrollment-service-api-openapi.yml
- filename: chase-loyalty-pci-merchant-relationship-manager-api-openapi.yml
  format: yaml
  label: Chase Loyalty PCI Merchant Relationship Manager API
  slug: loyalty-pci-merchant-relationship-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-loyalty-pci-merchant-relationship-manager-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Partner Contract + Interchange
description: 'FOCUS-aligned FinOps framing for Chase developer APIs: API access is partner-contracted; underlying revenue/cost flows from interchange, rewards economics, and partner integration fees rather than a separate per-API price list.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: JPMorgan Chase Bank, N.A.
  ProviderName: Chase
  PublisherName: JPMorgan Chase Bank, N.A.
  ServiceCategory: Financial Services
  ServiceName: Chase Developer APIs
layout: finops
meters:
- aggregation: sum
  name: fdx_consents
  unit: consent
- aggregation: sum
  dimensions:
  - dataType
  name: aggregation_requests
  unit: request
- aggregation: sum
  dimensions:
  - merchant
  name: points_redemption_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - merchant
  name: points_redeemed
  unit: point
name: Chase Finops
provider_name: Chase
provider_slug: chase
publisher_name: JPMorgan Chase Bank, N.A.
service_category: Financial Services / Banking
slug: chase-finops
source_filename: chase-finops.yml
source_heading: FinOps Profile
source_url: https://developer.chase.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Chase\nproviderId: chase\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Banking\n  - Open Banking\ndescription: 'FOCUS-aligned FinOps framing for Chase developer APIs: API access is partner-contracted;\n  underlying revenue/cost flows from interchange, rewards economics, and partner integration fees rather\n  than a separate per-API price list.'\nnotes: APIs are not separately priced; meters reflect partner integration billing surface.\nsources:\n  - https://developer.chase.com/\n  - https://www.jpmorganchase.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: JPMorgan Chase Bank, N.A.\nserviceCategory: Financial Services /\
  \ Banking\nbillingModel:\n  pricingCategory: Partner Contract + Interchange\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Chase Developer APIs\n  ServiceCategory: Financial Services\n  ProviderName: Chase\n  PublisherName: JPMorgan Chase Bank, N.A.\n  InvoiceIssuerName: JPMorgan Chase Bank, N.A.\n  BillingCurrency: USD\nmeters:\n  - name: fdx_consents\n    unit: consent\n    aggregation: sum\n  - name: aggregation_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - dataType\n  - name: points_redemption_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant\n  - name: points_redeemed\n    unit: point\n    aggregation: sum\n    dimensions:\n      - merchant\nprinciples:\n  - name: Visibility\n    description: Track FDX consent counts, aggregation request volume, and Pay with Points redemption\n   \
  \   reports through the partner portal.\n  - name: Allocation\n    description: Allocate by merchant ID / aggregator ID; tie redemption costs to the corresponding loyalty\n      campaign.\n  - name: Optimization\n    description: Cache FDX data within consent windows, batch read requests, and tune redemption UX to\n      lift conversion without inflating points liability.\n  - name: Accountability\n    description: Partner relationship owner reviews monthly partner statements and FDX consent telemetry;\n      treasury / loyalty finance owns points liability.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/finops/chase-finops.yml
sources:
- https://developer.chase.com/
- https://www.jpmorganchase.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking
- Open Banking
---
