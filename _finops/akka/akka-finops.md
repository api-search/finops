---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: akka-management.json
  format: json
  label: Akka Management
  slug: akka-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/akka/refs/heads/main/openapi/akka-management.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (per-core / per-region) and Monthly (Serverless)
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Subscription + Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Akka: per-core annual subscriptions for self-managed Akka SDK and Akka Libraries, per-Akka-hour metered usage for Akka Serverless, and per-region subscriptions for in-VPC deployments. Committed-use contracts unlock volume discounts and multi-cloud credits.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Lightbend, Inc.
  ProviderName: Akka
  PublisherName: Lightbend, Inc.
  ServiceCategory: Application Platform
  ServiceName: Akka
layout: finops
meters:
- aggregation: sum
  description: Annual per-core licensing for self-managed Akka SDK and Akka Libraries
  dimensions:
  - product
  - cluster
  - environment
  name: per_core_year
  unit: core-year
- aggregation: sum
  description: Hourly compute metering for Akka Serverless
  dimensions:
  - service
  - region
  - environment
  name: akka_hours
  unit: akka-hour
- aggregation: sum
  description: Annual per-region subscription for Akka in Your VPC deployments
  dimensions:
  - region
  - cloud
  name: per_region_year
  unit: region-year
- aggregation: sum
  description: Committed-use spend tracked against multi-cloud credit pool
  dimensions:
  - cloud
  - product
  name: committed_spend
  unit: USD
name: Akka Finops
provider_name: Akka
provider_slug: akka
publisher_name: Lightbend, Inc.
service_category: Application Platform
slug: akka-finops
source_filename: akka-finops.yml
source_heading: FinOps Profile
source_url: https://akka.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Akka\nproviderId: akka\npublisherName: Lightbend, Inc.\nserviceCategory: Application Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Actor Model\n  - Distributed Systems\n  - Frameworks\n  - Java\n  - Microservices\n  - Reactive\n  - Scala\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Akka: per-core annual subscriptions for self-managed Akka SDK and\n  Akka Libraries, per-Akka-hour metered usage for Akka Serverless, and per-region subscriptions for in-VPC\n  deployments. Committed-use contracts unlock volume discounts and multi-cloud credits.'\nsources:\n  - https://akka.io/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\n\
  billingModel:\n  pricingCategory: Subscription + Pay-As-You-Go + Committed Use\n  billingFrequency: Annual (per-core / per-region) and Monthly (Serverless)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Akka\n  ServiceCategory: Application Platform\n  ProviderName: Akka\n  PublisherName: Lightbend, Inc.\n  InvoiceIssuerName: Lightbend, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: per_core_year\n    description: Annual per-core licensing for self-managed Akka SDK and Akka Libraries\n    unit: core-year\n    aggregation: sum\n    dimensions:\n      - product\n      - cluster\n      - environment\n  - name: akka_hours\n    description: Hourly compute metering for Akka Serverless\n    unit: akka-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - environment\n  - name: per_region_year\n    description: Annual per-region subscription\
  \ for Akka in Your VPC deployments\n    unit: region-year\n    aggregation: sum\n    dimensions:\n      - region\n      - cloud\n  - name: committed_spend\n    description: Committed-use spend tracked against multi-cloud credit pool\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - cloud\n      - product\nprinciples:\n  - name: Visibility\n    description: Track Akka Serverless consumption via the Akka console and per-tenant Akka-hour reports.\n      Self-managed deployments correlate cost to provisioned cores via license inventories.\n  - name: Allocation\n    description: Tag Akka Serverless services and Akka in-VPC regions by team, environment, and product\n      so per-core and per-Akka-hour spend can be attributed to consuming applications.\n  - name: Optimization\n    description: Right-size core counts for self-managed Akka clusters; use elastic scaling on Akka Serverless;\n      adopt committed-use contracts for steady-state workloads to capture volume discounts and\
  \ multi-cloud\n      credit flexibility.\n  - name: Accountability\n    description: Establish budget owners per Akka cluster or Serverless tenant; integrate Akka invoices\n      into chargeback/showback workflows alongside underlying cloud spend.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/akka/refs/heads/main/finops/akka-finops.yml
sources:
- https://akka.io/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Actor Model
- Distributed Systems
- Frameworks
- Java
- Microservices
- Reactive
- Scala
- FinOps
- FOCUS
---
