---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Domain Search API
  slug: domain-search
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Email Finder API
  slug: email-finder
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Email Verifier API
  slug: email-verifier
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Email Count API
  slug: email-count
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Account API
  slug: account
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Discover API
  slug: discover
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Email Enrichment API
  slug: email-enrichment
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Company Enrichment API
  slug: company-enrichment
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Combined Enrichment API
  slug: combined-enrichment
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Leads API
  slug: leads
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Leads Lists API
  slug: leads-lists
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Campaigns API
  slug: campaigns
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
- filename: hunter-api-openapi.yml
  format: yaml
  label: Hunter Logo API
  slug: logo
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/openapi/hunter-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Credit
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Hunter: tiered subscription with monthly credit pools and fixed credit-consumption rates per API operation.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Hunter SAS
  ProviderName: Hunter
  PublisherName: Hunter SAS
  ServiceCategory: Sales Intelligence
  ServiceName: Hunter
layout: finops
meters:
- aggregation: max
  description: Flat monthly subscription per plan tier (Starter $49, Growth $149, Scale $299, Enterprise custom).
  dimensions:
  - plan
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Credits consumed by API operations within the monthly allotment.
  dimensions:
  - endpoint
  - team_member
  name: credits_consumed
  unit: credit
- aggregation: sum
  description: Domain Search and Email Finder API calls; 1 credit per email returned.
  dimensions:
  - endpoint
  name: domain_search_credits
  unit: credit
- aggregation: sum
  description: Email Verifier API calls; 0.5 credit per verified email.
  dimensions:
  - endpoint
  name: verifier_credits
  unit: credit
- aggregation: sum
  description: AI Assistant searches consumed against the monthly allotment.
  name: ai_searches
  unit: search
- aggregation: sum
  description: Sales Signals consumed against the monthly allotment.
  name: signals_consumed
  unit: signal
name: Hunter Finops
provider_name: Hunter
provider_slug: hunter
publisher_name: Hunter.io (Hunter SAS)
service_category: Sales Intelligence
slug: hunter-finops
source_filename: hunter-finops.yml
source_heading: FinOps Profile
source_url: https://hunter.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Hunter\nproviderId: hunter\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Sales Intelligence\n  - Email\ndescription: 'FOCUS-aligned FinOps for Hunter: tiered subscription with monthly credit pools and\n  fixed credit-consumption rates per API operation.'\nsources:\n  - https://hunter.io/pricing\n  - https://hunter.io/api-documentation/v2\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Hunter.io (Hunter SAS)\nserviceCategory: Sales Intelligence\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Credit\n    - Adjustment\n\
  focusColumns:\n  ServiceName: Hunter\n  ServiceCategory: Sales Intelligence\n  ProviderName: Hunter\n  PublisherName: Hunter SAS\n  InvoiceIssuerName: Hunter SAS\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_fee\n    description: Flat monthly subscription per plan tier (Starter $49, Growth $149, Scale $299, Enterprise\n      custom).\n    unit: month\n    aggregation: max\n    dimensions:\n      - plan\n  - name: credits_consumed\n    description: Credits consumed by API operations within the monthly allotment.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - team_member\n  - name: domain_search_credits\n    description: Domain Search and Email Finder API calls; 1 credit per email returned.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - endpoint\n  - name: verifier_credits\n    description: Email Verifier API calls; 0.5 credit per verified email.\n    unit: credit\n    aggregation: sum\n    dimensions:\n\
  \      - endpoint\n  - name: ai_searches\n    description: AI Assistant searches consumed against the monthly allotment.\n    unit: search\n    aggregation: sum\n  - name: signals_consumed\n    description: Sales Signals consumed against the monthly allotment.\n    unit: signal\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use GET /v2/account to track credits used vs available, searches used vs available,\n      and verifications used vs available in real time. Reconcile against the dashboard usage view.\n  - name: Allocation\n    description: Hunter tracks usage at the account/API-key level. Issue separate API keys per integration\n      (CRM, outreach tool, internal app) for chargeback and to isolate consumption per workflow.\n  - name: Optimization\n    description: Use Bulk Domain Search (1 credit per 10 emails) instead of repeated Email Finder\n      calls for high-volume prospecting. Verifier costs only 0.5 credit per email; cache verification\n     \
  \ results to avoid re-verifying. Annual billing yields a 30% discount.\n  - name: Accountability\n    description: Failed lookups do not consume credits, so monitor the success rate per API key as\n      a quality and cost-control signal. When approaching plan ceiling, choose between upgrading\n      tier vs annual billing for the better unit economics.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hunter/refs/heads/main/finops/hunter-finops.yml
sources:
- https://hunter.io/pricing
- https://hunter.io/api-documentation/v2
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Sales Intelligence
- Email
---
