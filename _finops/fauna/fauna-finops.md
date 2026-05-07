---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fauna-core-http-api-openapi.yml
  format: yaml
  label: Fauna Core HTTP API
  slug: core-http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fauna/refs/heads/main/openapi/fauna-core-http-api-openapi.yml
- filename: fauna-event-streaming-asyncapi.yml
  format: yaml
  label: Fauna Event Streaming API
  slug: event-streaming-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/fauna/refs/heads/main/asyncapi/fauna-event-streaming-asyncapi.yml
- filename: fauna-graphql-api-openapi.yml
  format: yaml
  label: Fauna GraphQL API
  slug: graphql-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fauna/refs/heads/main/openapi/fauna-graphql-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (historical)
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  chargeFrequency: Recurring (historical)
  pricingCategory: Usage-Based (Discontinued)
description: FOCUS-aligned FinOps for Fauna (archival). Fauna service was decommissioned on 2025-05-30 following a March 2025 End-of-Service announcement. Historically Fauna billed usage-based on TROs (Transactional Read Operations), TWOs (Transactional Write Operations), TCOs (Transactional Compute Operations), storage (GB-month), and outbound transfer (GB), with optional monthly platform fees on Team / Business plans. This artifact preserves the FinOps shape for cost-archive and migration accounting purposes.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Fauna, Inc.
  PricingCategory: Usage-Based (discontinued)
  PricingUnit: operation | GB
  ProviderName: Fauna
  PublisherName: Fauna, Inc.
  ServiceCategory: Database / Serverless
  ServiceName: Fauna
layout: finops
meters:
- aggregation: sum
  description: Transactional Read Operations.
  dimensions:
  - database
  - region
  name: tros
  unit: operation
- aggregation: sum
  description: Transactional Write Operations.
  dimensions:
  - database
  - region
  name: twos
  unit: operation
- aggregation: sum
  description: Transactional Compute Operations.
  dimensions:
  - database
  - region
  name: tcos
  unit: operation
- aggregation: sum
  description: Stored data per GB-month.
  dimensions:
  - database
  - region
  name: storage_gb_month
  unit: GB-month
- aggregation: sum
  description: Outbound data transfer.
  dimensions:
  - database
  - region
  name: egress_gb
  unit: GB
name: Fauna Finops
provider_name: fauna
provider_slug: fauna
publisher_name: Fauna, Inc.
service_category: Database / Serverless
slug: fauna-finops
source_filename: fauna-finops.yml
source_heading: FinOps Profile
source_url: https://fauna.com/blog/announcing-fauna-end-of-service
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Fauna\nproviderId: fauna\npublisherName: Fauna, Inc.\nserviceCategory: Database / Serverless\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Database\n  - Document Database\n  - Serverless\n  - End of Service\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Fauna (archival). Fauna service was decommissioned on 2025-05-30\n  following a March 2025 End-of-Service announcement. Historically Fauna billed usage-based on TROs (Transactional\n  Read Operations), TWOs (Transactional Write Operations), TCOs (Transactional Compute Operations), storage\n  (GB-month), and outbound transfer (GB), with optional monthly platform fees on Team\
  \ / Business plans.\n  This artifact preserves the FinOps shape for cost-archive and migration accounting purposes.'\nnotes: Fauna End-of-Service 2025-05-30. FinOps levers below are archival; for live workloads see migration\n  guidance.\nsources:\n  - https://fauna.com/blog/announcing-fauna-end-of-service\n  - https://fauna.com/pricing\nprinciples:\n  - name: Visibility\n    description: Historically — pull TRO/TWO/TCO/storage usage from the Fauna Dashboard or the /usage\n      API endpoints; reconcile against monthly invoice. Now archival.\n  - name: Allocation\n    description: Historically — allocate by Fauna database (each database had its own usage counters);\n      tag with team/product. Now archival.\n  - name: Optimization\n    description: Historical levers were — index design (avoid full-collection scans that drove TROs);\n      batch FQL queries; minimize streaming subscriptions; choose region carefully to limit egress.\n  - name: Accountability\n    description: Historically\
  \ the data platform team owned Fauna entitlement; per-database owners owned\n      usage. Now — accountability shifts to migration completion and shutdown reconciliation.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Onboarding Workloads\n      - Invoicing and Chargeback\nbillingModel:\n  pricingCategory: Usage-Based (Discontinued)\n  billingFrequency: Monthly (historical)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n  chargeFrequency: Recurring (historical)\nfocusColumns:\n  ServiceName:\
  \ Fauna\n  ServiceCategory: Database / Serverless\n  ProviderName: Fauna\n  PublisherName: Fauna, Inc.\n  InvoiceIssuerName: Fauna, Inc.\n  PricingCategory: Usage-Based (discontinued)\n  PricingUnit: operation | GB\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: tros\n    description: Transactional Read Operations.\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - database\n      - region\n  - name: twos\n    description: Transactional Write Operations.\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - database\n      - region\n  - name: tcos\n    description: Transactional Compute Operations.\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - database\n      - region\n  - name: storage_gb_month\n    description: Stored data per GB-month.\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - database\n      - region\n  - name: egress_gb\n    description: Outbound data transfer.\n    unit: GB\n  \
  \  aggregation: sum\n    dimensions:\n      - database\n      - region\napis:\n  - name: Fauna Core HTTP API\n    baseURL: https://db.fauna.com\n    serviceName: Fauna Core HTTP API\n    serviceCategory: API\n  - name: Fauna GraphQL API\n    baseURL: https://graphql.fauna.com\n    serviceName: Fauna GraphQL API\n    serviceCategory: API\n  - name: Fauna Event Streaming API\n    baseURL: https://db.fauna.com\n    serviceName: Fauna Event Streaming API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1M TROs (historical)\n    metric: tro_cost / (tros / 1000000)\n    target: see fauna.com/pricing snapshot\n  - name: Cost per 1M TWOs (historical)\n    metric: two_cost / (twos / 1000000)\n    target: see fauna.com/pricing snapshot\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fauna/refs/heads/main/finops/fauna-finops.yml
sources:
- https://fauna.com/blog/announcing-fauna-end-of-service
- https://fauna.com/pricing
specification: FinOps Framework
tags:
- Database
- Document Database
- Serverless
- End of Service
- FinOps
- Cost Management
- FOCUS
---
