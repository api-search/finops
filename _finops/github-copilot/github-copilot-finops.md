---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: api.github.com.json
  format: json
  label: GitHub Copilot API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
- filename: api.github.com.json
  format: json
  label: GitHub Copilot for Business API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
- filename: api.github.com.json
  format: json
  label: GitHub Copilot User Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
- filename: api.github.com.json
  format: json
  label: GitHub Copilot Metrics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
- filename: api.github.com.json
  format: json
  label: GitHub Copilot Usage Metrics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
- filename: api.github.com.json
  format: json
  label: GitHub Copilot Content Exclusion API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Credit
  pricingCategory: Subscription + Metered Overage
description: 'FOCUS-aligned FinOps for GitHub Copilot: per-seat subscription with included premium-request budgets and metered overage at $0.04 per premium request.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: GitHub, Inc.
  PricingCategory: Subscription
  PricingUnit: seat-month
  ProviderName: GitHub
  PublisherName: GitHub, Inc.
  ServiceCategory: Developer Tools
  ServiceName: GitHub Copilot
  ServiceSubcategory: AI Code Assistance
layout: finops
meters:
- aggregation: max
  description: Number of paid Copilot seats assigned in the billing period
  dimensions:
  - plan
  - org
  - team
  name: copilot_seats
  unit: seat
- aggregation: sum
  description: Premium model invocations (chat, agent mode, code review) consumed against plan budget
  dimensions:
  - plan
  - org
  - user
  - model
  name: premium_requests
  unit: request
- aggregation: sum
  description: Premium requests beyond the included monthly budget; billed at $0.04 each
  dimensions:
  - plan
  - org
  - user
  name: premium_request_overage
  unit: request
- aggregation: sum
  description: Inline code completion suggestions issued
  dimensions:
  - org
  - user
  - language
  name: completions
  unit: completion
- aggregation: sum
  description: GitHub REST/GraphQL requests against Copilot management endpoints
  dimensions:
  - org
  - endpoint
  name: api_requests
  unit: request
name: Github Copilot Finops
provider_name: GitHub Copilot
provider_slug: github-copilot
publisher_name: GitHub, Inc.
service_category: Developer Tools / AI
slug: github-copilot-finops
source_filename: github-copilot-finops.yml
source_heading: FinOps Profile
source_url: https://github.com/features/copilot/plans
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: GitHub Copilot\nproviderId: github-copilot\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI\n  - Developer Tools\ndescription: 'FOCUS-aligned FinOps for GitHub Copilot: per-seat subscription with included premium-request\n  budgets and metered overage at $0.04 per premium request.'\nsources:\n  - https://github.com/features/copilot/plans\n  - https://docs.github.com/en/billing/concepts/product-billing/github-copilot\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: GitHub, Inc.\nserviceCategory: Developer Tools / AI\nbillingModel:\n  pricingCategory: Subscription + Metered Overage\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: GitHub Copilot\n  ServiceCategory: Developer Tools\n  ServiceSubcategory: AI Code Assistance\n  ProviderName: GitHub\n  PublisherName: GitHub, Inc.\n  InvoiceIssuerName: GitHub, Inc.\n  BillingCurrency: USD\n  PricingCategory: Subscription\n  PricingUnit: seat-month\nmeters:\n  - name: copilot_seats\n    description: Number of paid Copilot seats assigned in the billing period\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\n      - org\n      - team\n  - name: premium_requests\n    description: Premium model invocations (chat, agent mode, code review) consumed against plan budget\n    unit: request\n    aggregation: sum\n    dimensions:\n      - plan\n      - org\n      - user\n      - model\n  - name: premium_request_overage\n    description: Premium requests beyond the included monthly budget; billed at $0.04 each\n    unit: request\n    aggregation:\
  \ sum\n    dimensions:\n      - plan\n      - org\n      - user\n  - name: completions\n    description: Inline code completion suggestions issued\n    unit: completion\n    aggregation: sum\n    dimensions:\n      - org\n      - user\n      - language\n  - name: api_requests\n    description: GitHub REST/GraphQL requests against Copilot management endpoints\n    unit: request\n    aggregation: sum\n    dimensions:\n      - org\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: Use the Copilot Usage Metrics API and the org Billing dashboard to attribute premium\n      request consumption per user and team; export GitHub usage CSVs for ledger reconciliation.\n  - name: Allocation\n    description: Tag seats by team via SAML/SCIM groups; route Copilot Business invoices through the cost\n      center owning the org.\n  - name: Optimization\n    description: Right-size seat counts using the Copilot Usage Metrics API to identify dormant seats;\n      educate users on when\
  \ to use chat vs agent mode to avoid burning premium-request budget; opt low-volume\n      teams onto Pro instead of Business.\n  - name: Accountability\n    description: Engineering leaders own seat allocation and premium-request overage budgets; finance\n      reviews monthly Copilot line item against developer headcount.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: http://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github-copilot/refs/heads/main/finops/github-copilot-finops.yml
sources:
- https://github.com/features/copilot/plans
- https://docs.github.com/en/billing/concepts/product-billing/github-copilot
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI
- Developer Tools
---
