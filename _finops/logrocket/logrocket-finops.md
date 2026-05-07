---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: logrocket-rest-api-openapi.yml
  format: yaml
  label: LogRocket REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/logrocket/refs/heads/main/openapi/logrocket-rest-api-openapi.yml
- filename: logrocket-graphql-api-openapi.yml
  format: yaml
  label: LogRocket GraphQL API
  slug: graphql-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/logrocket/refs/heads/main/openapi/logrocket-graphql-api-openapi.yml
- filename: logrocket-highlights-webhook-asyncapi.yml
  format: yaml
  label: LogRocket Galileo Highlights API
  slug: session-highlights-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/logrocket/refs/heads/main/asyncapi/logrocket-highlights-webhook-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for LogRocket: tiered subscription priced by monthly session capacity, with seats and retention as secondary cost drivers. Annual commitment on paid tiers; Enterprise adds conditional recording and self-hosted options.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: LogRocket, Inc.
  ProviderName: LogRocket
  PublisherName: LogRocket, Inc.
  ServiceCategory: Observability
  ServiceName: LogRocket
layout: finops
meters:
- aggregation: sum
  dimensions:
  - environment
  - app
  name: sessions
  unit: session
- aggregation: max
  dimensions:
  - role
  name: seats
  unit: seat
- aggregation: max
  name: retention_months
  unit: month
- aggregation: sum
  dimensions:
  - tier
  name: subscription_fee
  unit: month
name: Logrocket Finops
provider_name: LogRocket
provider_slug: logrocket
publisher_name: LogRocket, Inc.
service_category: Observability
slug: logrocket-finops
source_filename: logrocket-finops.yml
source_heading: FinOps Profile
source_url: https://logrocket.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: LogRocket\nproviderId: logrocket\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Observability\n  - Session Replay\ndescription: 'FOCUS-aligned FinOps for LogRocket: tiered subscription priced by monthly session capacity,\n  with seats and retention as secondary cost drivers. Annual commitment on paid tiers; Enterprise adds\n  conditional recording and self-hosted options.'\nsources:\n  - https://logrocket.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: LogRocket, Inc.\nserviceCategory: Observability\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: LogRocket\n  ServiceCategory: Observability\n  ProviderName: LogRocket\n  PublisherName: LogRocket, Inc.\n  InvoiceIssuerName: LogRocket, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: sessions\n    unit: session\n    aggregation: sum\n    dimensions:\n      - environment\n      - app\n  - name: seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - role\n  - name: retention_months\n    unit: month\n    aggregation: max\n  - name: subscription_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Use the LogRocket Usage page and project dashboards to monitor session ingest vs. monthly\n      capacity; set alerts before plan caps.\n  - name: Allocation\n    description: Tag sessions by app/environment via the JS SDK; map projects to internal team owners\n      for chargeback.\n  - name: Optimization\n\
  \    description: Use Conditional Recording (Enterprise) to capture only impactful sessions; sample low-value\n      flows; right-size retention.\n  - name: Accountability\n    description: Owners review monthly session burn vs. plan tier; renegotiate at renewal if forecasted\n      sessions outgrow Team into Professional/Enterprise.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/logrocket/refs/heads/main/finops/logrocket-finops.yml
sources:
- https://logrocket.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Observability
- Session Replay
---
