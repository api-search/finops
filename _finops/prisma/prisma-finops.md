---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Prisma Data Platform API
  slug: prisma-data-platform-api
  spec_type: OpenAPI
  url: https://api.cloud.prisma.io/openapi.json
- filename: prisma-accelerate-openapi.yml
  format: yaml
  label: Prisma Accelerate API
  slug: prisma-accelerate-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prisma/refs/heads/main/openapi/prisma-accelerate-openapi.yml
- filename: prisma-pulse-openapi.yml
  format: yaml
  label: Prisma Pulse API
  slug: prisma-pulse-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prisma/refs/heads/main/openapi/prisma-pulse-openapi.yml
- filename: prisma-postgres-management-openapi.yml
  format: yaml
  label: Prisma Postgres Management API
  slug: prisma-postgres-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prisma/refs/heads/main/openapi/prisma-postgres-management-openapi.yml
- filename: prisma-client-openapi.yml
  format: yaml
  label: Prisma Client API
  slug: prisma-client-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prisma/refs/heads/main/openapi/prisma-client-openapi.yml
- filename: prisma-optimize-openapi.yml
  format: yaml
  label: Prisma Optimize API
  slug: prisma-optimize-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prisma/refs/heads/main/openapi/prisma-optimize-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription + Pay-As-You-Go
description: FOCUS-aligned FinOps for Prisma Data Platform — flat plan subscription plus per-1,000 metered overage on Prisma Postgres operations and Prisma Accelerate operations, plus per-GB storage and per-GiB Accelerate egress.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Prisma Data, Inc.
  ProviderName: Prisma
  PublisherName: Prisma Data, Inc.
  ServiceCategory: Database + Developer Tools
  ServiceName: Prisma Data Platform
layout: finops
meters:
- aggregation: sum
  dimensions:
  - plan
  name: plan_subscription
  unit: month
- aggregation: sum
  dimensions:
  - plan
  - database
  name: postgres_operations
  unit: operation
- aggregation: max
  dimensions:
  - plan
  - database
  name: postgres_storage
  unit: GB-month
- aggregation: max
  dimensions:
  - plan
  name: postgres_databases
  unit: database
- aggregation: sum
  dimensions:
  - plan
  - environment
  name: accelerate_operations
  unit: operation
- aggregation: sum
  dimensions:
  - plan
  name: accelerate_cache_tags
  unit: operation
- aggregation: sum
  dimensions:
  - plan
  - environment
  name: accelerate_egress
  unit: GiB
name: Prisma Finops
provider_name: Prisma
provider_slug: prisma
publisher_name: Prisma Data, Inc.
service_category: Database + Developer Tools
slug: prisma-finops
source_filename: prisma-finops.yml
source_heading: FinOps Profile
source_url: https://www.prisma.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Prisma\nproviderId: prisma\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Database\n  - ORM\n  - Postgres\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Prisma Data Platform — flat plan subscription plus per-1,000 metered\n  overage on Prisma Postgres operations and Prisma Accelerate operations, plus per-GB storage and per-GiB\n  Accelerate egress.\nsources:\n  - https://www.prisma.io/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Prisma Data, Inc.\nserviceCategory: Database + Developer Tools\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Prisma Data Platform\n  ServiceCategory: Database + Developer Tools\n  ProviderName: Prisma\n  PublisherName: Prisma Data, Inc.\n  InvoiceIssuerName: Prisma Data, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: plan_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: postgres_operations\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - plan\n      - database\n  - name: postgres_storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - plan\n      - database\n  - name: postgres_databases\n    unit: database\n    aggregation: max\n    dimensions:\n      - plan\n  - name: accelerate_operations\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - plan\n      - environment\n  - name: accelerate_cache_tags\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: accelerate_egress\n    unit: GiB\n    aggregation:\
  \ sum\n    dimensions:\n      - plan\n      - environment\nprinciples:\n  - name: Visibility\n    description: Track Postgres + Accelerate operation counts and storage per environment in the Prisma\n      Console; reconcile against the monthly invoice. Plan-level included quotas vs overage are the\n      primary cost line.\n  - name: Allocation\n    description: Allocate by Prisma project / environment / database; tag environments (dev / preview\n      / prod) and split overage cost back to the consuming feature team.\n  - name: Optimization\n    description: Use Accelerate's cache + cache tags to convert Postgres operations into cheaper cached\n      operations; right-size the plan when sustained overage on Postgres operations is cheaper at the\n      next tier (Pro $0.002/1k vs Starter $0.008/1k vs Business $0.001/1k); paginate to stay under\n      the 5 MB response ceiling.\n  - name: Accountability\n    description: Assign a plan and budget owner per Prisma workspace; alert on overage\
  \ when monthly\n      Postgres operations or Accelerate operations exceed the included allotment.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/prisma/refs/heads/main/finops/prisma-finops.yml
sources:
- https://www.prisma.io/pricing
specification: FinOps Framework
tags:
- Database
- ORM
- Postgres
- FinOps
- FOCUS
---
