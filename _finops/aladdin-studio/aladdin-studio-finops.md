---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: aladdin-studio-graph-openapi.yaml
  format: yaml
  label: Aladdin Graph API
  slug: graph-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/openapi/aladdin-studio-graph-openapi.yaml
- filename: aladdin-studio-data-cloud-openapi.yaml
  format: yaml
  label: Aladdin Data Cloud API
  slug: data-cloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/openapi/aladdin-studio-data-cloud-openapi.yaml
- filename: aladdin-studio-trading-openapi.yaml
  format: yaml
  label: Aladdin Trading API
  slug: trading-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/openapi/aladdin-studio-trading-openapi.yaml
- filename: aladdin-studio-investment-research-openapi.yaml
  format: yaml
  label: Aladdin Investment Research API
  slug: investment-research-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/openapi/aladdin-studio-investment-research-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps shell for BlackRock Aladdin Studio: enterprise contract billing with no public meter rates. Concrete meters and FOCUS values must be reconciled against the negotiated agreement for each client.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: BlackRock, Inc.
  ProviderName: BlackRock
  PublisherName: BlackRock, Inc.
  ServiceCategory: Investment Management Platform
  ServiceName: Aladdin Studio
layout: finops
meters:
- aggregation: sum
  description: Annual contract value for the Aladdin engagement
  dimensions:
  - module
  - aum_band
  name: contract_subscription
  unit: contract-year
- aggregation: sum
  description: API call volume across Aladdin module APIs (where contractually metered)
  dimensions:
  - module
  - endpoint
  name: api_calls
  unit: request
- aggregation: max
  description: Named user seats in the Aladdin platform
  dimensions:
  - role
  - module
  name: seats
  unit: seat
name: Aladdin Studio Finops
provider_name: Aladdin Studio
provider_slug: aladdin-studio
publisher_name: BlackRock, Inc.
service_category: Investment Management Platform
slug: aladdin-studio-finops
source_filename: aladdin-studio-finops.yml
source_heading: FinOps Profile
source_url: https://www.blackrock.com/aladdin
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Aladdin Studio\nproviderId: aladdin-studio\npublisherName: BlackRock, Inc.\nserviceCategory: Investment Management Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Financial\n  - Investment Management\n  - Portfolio Analytics\n  - Risk Management\n  - Asset Management\n  - BlackRock\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shell for BlackRock Aladdin Studio: enterprise contract billing with\n  no public meter rates. Concrete meters and FOCUS values must be reconciled against the negotiated agreement\n  for each client.'\nsources:\n  - https://www.blackrock.com/aladdin\n  - https://focus.finops.org/focus-specification/v1-3/\n\
  billingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Aladdin Studio\n  ServiceCategory: Investment Management Platform\n  ProviderName: BlackRock\n  PublisherName: BlackRock, Inc.\n  InvoiceIssuerName: BlackRock, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract_subscription\n    description: Annual contract value for the Aladdin engagement\n    unit: contract-year\n    aggregation: sum\n    dimensions:\n      - module\n      - aum_band\n  - name: api_calls\n    description: API call volume across Aladdin module APIs (where contractually metered)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - module\n      - endpoint\n  - name: seats\n    description: Named user seats in the Aladdin platform\n    unit: seat\n    aggregation: max\n    dimensions:\n      - role\n      - module\n\
  principles:\n  - name: Visibility\n    description: Aladdin invoicing and seat utilization are surfaced through BlackRock client services\n      reports. API call volume reporting is negotiated per contract.\n  - name: Allocation\n    description: Allocate Aladdin contract spend to investment teams, fund families, and trading desks\n      consuming each module.\n  - name: Optimization\n    description: Right-size seat counts and module subscriptions during annual renewals; consolidate redundant\n      seats; review API integration footprint to drop unused module access.\n  - name: Accountability\n    description: Aladdin contracts are typically owned by the COO / CIO office; integrate the contracted\n      spend into the firm's investment-platform budget review.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/finops/aladdin-studio-finops.yml
sources:
- https://www.blackrock.com/aladdin
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Financial
- Investment Management
- Portfolio Analytics
- Risk Management
- Asset Management
- BlackRock
- FinOps
- FOCUS
---
