---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: 42crunch-scand-manager.yaml
  format: yaml
  label: 42Crunch API Conformance Scan Jobs Manager
  slug: 42crunch-scand-manager
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/42crunch/refs/heads/main/openapi/42crunch-scand-manager.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps for 42Crunch — tiered subscription priced on seats and contracted endpoints, with operation quotas on Free / Single User and unlimited operations on Teams / Enterprise.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: 42Crunch Ltd.
  PricingCategory: Tiered Subscription
  PricingUnit: seat-month
  ProviderName: 42Crunch
  PublisherName: 42Crunch Ltd.
  ServiceCategory: API Security
  ServiceName: 42Crunch API Security Platform
layout: finops
meters:
- aggregation: sum
  description: Active platform user seats per month.
  dimensions:
  - plan
  - role
  name: seat_month
  unit: seat
- aggregation: max
  description: API endpoints under contract on Teams / Enterprise plans (drives plan minimums and renewal sizing).
  dimensions:
  - plan
  - api
  name: contracted_endpoints
  unit: endpoint
- aggregation: sum
  description: API Audit static-analysis runs (counts against Free/Single User quota; uncapped on Teams/Enterprise).
  dimensions:
  - plan
  - api
  name: audit_operations
  unit: operation
- aggregation: sum
  description: API Scan dynamic-test runs.
  dimensions:
  - plan
  - api
  name: scan_operations
  unit: operation
- aggregation: sum
  description: API Contract Generator runs.
  dimensions:
  - plan
  - api
  name: contract_generator_operations
  unit: operation
name: 42Crunch Finops
provider_name: 42Crunch
provider_slug: 42crunch
publisher_name: 42Crunch Ltd.
service_category: API Security
slug: 42crunch-finops
source_filename: 42crunch-finops.yml
source_heading: FinOps Profile
source_url: https://42crunch.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: 42Crunch\nproviderId: 42crunch\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - API Security\n  - DevSecOps\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for 42Crunch — tiered subscription priced on seats and contracted endpoints,\n  with operation quotas on Free / Single User and unlimited operations on Teams / Enterprise.\nsources:\n  - https://42crunch.com/pricing/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: 42Crunch Ltd.\nserviceCategory: API Security\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: 42Crunch API Security Platform\n  ServiceCategory: API Security\n  ProviderName: 42Crunch\n  PublisherName: 42Crunch Ltd.\n  InvoiceIssuerName: 42Crunch Ltd.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Tiered Subscription\n  PricingUnit: seat-month\nmeters:\n  - name: seat_month\n    description: Active platform user seats per month.\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - plan\n      - role\n  - name: contracted_endpoints\n    description: API endpoints under contract on Teams / Enterprise plans (drives plan minimums and renewal\n      sizing).\n    unit: endpoint\n    aggregation: max\n    dimensions:\n      - plan\n      - api\n  - name: audit_operations\n    description: API Audit static-analysis runs (counts against Free/Single User quota; uncapped on Teams/Enterprise).\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - plan\n      - api\n\
  \  - name: scan_operations\n    description: API Scan dynamic-test runs.\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - plan\n      - api\n  - name: contract_generator_operations\n    description: API Contract Generator runs.\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - plan\n      - api\nprinciples:\n  - name: Visibility\n    description: Use the 42Crunch SaaS platform dashboards to track operations consumed vs plan ceiling\n      and contracted-endpoint utilization.\n  - name: Allocation\n    description: Tag APIs by team / business unit in the platform to attribute operation counts and endpoint\n      coverage to the responsible product groups.\n  - name: Optimization\n    description: Reduce redundant scans by gating CI/CD runs to changed contracts; right-size the contracted\n      endpoint count at renewal rather than provisioning Teams/Enterprise above actual API surface.\n  - name: Accountability\n    description: AppSec or Platform\
  \ Security team owns the subscription; product engineering owners are\n      accountable for keeping their APIs inside the contracted endpoint count.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/42crunch/refs/heads/main/finops/42crunch-finops.yml
sources:
- https://42crunch.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- API Security
- DevSecOps
- FinOps
- FOCUS
---
