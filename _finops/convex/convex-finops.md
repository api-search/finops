---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: convex-http-api-openapi.yml
  format: yaml
  label: Convex HTTP API
  slug: http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/convex/refs/heads/main/openapi/convex-http-api-openapi.yml
- filename: openapi.json
  format: json
  label: Convex Management API
  slug: management-api
  spec_type: OpenAPI
  url: https://api.convex.dev/v1/openapi.json
- filename: convex-deployment-platform-api-openapi.yml
  format: yaml
  label: Convex Deployment Platform API
  slug: deployment-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/convex/refs/heads/main/openapi/convex-deployment-platform-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Subscription + Pay-As-You-Go
description: FOCUS-aligned FinOps for Convex - per-developer subscription seats on the Professional tier plus pay-as-you-go meters for function calls, database/file/search storage, database I/O, action compute (GB-hours), search queries, and egress. Business/Enterprise tiers add a monthly minimum and optional CPU-time pricing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Convex, Inc.
  PricingCategory: Usage-Based
  ProviderName: Convex
  PublisherName: Convex, Inc.
  ServiceCategory: Backend-as-a-Service
  ServiceName: Convex
layout: finops
meters:
- aggregation: max
  description: Developer seats on the Professional plan ($25/seat/month)
  dimensions:
  - plan
  - team
  name: developer_seats
  unit: seat
- aggregation: sum
  description: Convex function (query / mutation / action) invocations
  dimensions:
  - deployment
  - function
  - environment
  name: function_calls
  unit: request
- aggregation: avg
  description: Document database storage consumed
  dimensions:
  - deployment
  - environment
  name: database_storage
  unit: GB-month
- aggregation: sum
  description: Database I/O bandwidth (read + write payload)
  dimensions:
  - deployment
  - operation
  - environment
  name: database_io
  unit: GB
- aggregation: avg
  description: File storage consumed
  dimensions:
  - deployment
  - environment
  name: file_storage
  unit: GB-month
- aggregation: avg
  description: Search index storage consumed
  dimensions:
  - deployment
  - index
  - environment
  name: search_storage
  unit: GB-month
- aggregation: sum
  description: Search query throughput measured in query-GB
  dimensions:
  - deployment
  - index
  - environment
  name: search_queries
  unit: query-GB
- aggregation: sum
  description: Action compute time billed in GB-hours
  dimensions:
  - deployment
  - function
  - runtime
  - environment
  name: action_compute
  unit: GB-hour
- aggregation: sum
  description: Outbound bytes returned to clients
  dimensions:
  - deployment
  - environment
  name: data_egress
  unit: GB
name: Convex Finops
provider_name: Convex
provider_slug: convex
publisher_name: Convex, Inc.
service_category: Backend-as-a-Service
slug: convex-finops
source_filename: convex-finops.yml
source_heading: FinOps Profile
source_url: https://www.convex.dev/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Convex\nproviderId: convex\npublisherName: Convex, Inc.\nserviceCategory: Backend-as-a-Service\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Backend\n  - Database\n  - Functions\n  - Real-Time\n  - Reactive\n  - Serverless\n  - TypeScript\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Convex - per-developer subscription seats on the Professional\n  tier plus pay-as-you-go meters for function calls, database/file/search storage, database I/O, action\n  compute (GB-hours), search queries, and egress. Business/Enterprise tiers add a monthly minimum and\n  optional CPU-time pricing.\n\
  sources:\n  - https://www.convex.dev/pricing\n  - https://docs.convex.dev/production/state/limits\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Convex\n  ServiceCategory: Backend-as-a-Service\n  ProviderName: Convex\n  PublisherName: Convex, Inc.\n  InvoiceIssuerName: Convex, Inc.\n  PricingCategory: Usage-Based\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: developer_seats\n    description: Developer seats on the Professional plan ($25/seat/month)\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\n      - team\n  - name: function_calls\n    description: Convex function (query / mutation / action) invocations\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - deployment\n      - function\n      - environment\n  - name: database_storage\n    description: Document database storage consumed\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - deployment\n      - environment\n  - name: database_io\n    description: Database I/O bandwidth (read + write payload)\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - deployment\n      - operation\n      - environment\n  - name: file_storage\n    description: File storage consumed\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - deployment\n      - environment\n  - name: search_storage\n    description: Search index storage consumed\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - deployment\n      - index\n      - environment\n  - name: search_queries\n    description: Search query throughput measured in query-GB\n    unit: query-GB\n    aggregation: sum\n    dimensions:\n      - deployment\n      - index\n      - environment\n \
  \ - name: action_compute\n    description: Action compute time billed in GB-hours\n    unit: GB-hour\n    aggregation: sum\n    dimensions:\n      - deployment\n      - function\n      - runtime\n      - environment\n  - name: data_egress\n    description: Outbound bytes returned to clients\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - deployment\n      - environment\nprinciples:\n  - name: Visibility\n    description: Use the Convex dashboard usage views and per-deployment metrics to track function\n      calls, action compute (GB-hours), storage, and egress. Export usage from the Management API\n      and join to FOCUS-aligned billing exports for per-team allocation.\n  - name: Allocation\n    description: Allocate cost by deployment, environment (dev / preview / prod), and team. Tag deployments\n      using project naming conventions; the Management API exposes deployment-level usage that can be\n      broken down by environment and function.\n  - name: Optimization\n\
  \    description: Move long-running or third-party-fanout work into actions (avoid the 1s mutation budget),\n      cache reactive query results on the client, narrow document scans with indexes (32k scan ceiling),\n      keep file/search storage tidy, and consider the CPU-time pricing model on Business/Enterprise\n      for compute-heavy workloads.\n  - name: Accountability\n    description: Set monthly soft quotas and overage budgets per deployment/environment; designate\n      a Convex billing owner per project; alert on action GB-hours and database I/O spikes that historically\n      drive overage.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/convex/refs/heads/main/finops/convex-finops.yml
sources:
- https://www.convex.dev/pricing
- https://docs.convex.dev/production/state/limits
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Backend
- Database
- Functions
- Real-Time
- Reactive
- Serverless
- TypeScript
- FinOps
- Cost Management
- FOCUS
---
