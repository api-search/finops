---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: taxi-language-openapi.yml
  format: yaml
  label: Taxi Language
  slug: taxi-language
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/taxi-describe-how-your-apis-and-data-relate/refs/heads/main/openapi/taxi-language-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps shape for the commercial Orbital platform that executes TaxiQL queries against the Taxi schema registry. Billing is a tiered subscription with monthly call quotas, per-additional-user fees, an AI Copilot add-on, and metered overage; the Taxi language itself is Apache 2.0 open source and not directly billed.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Orbital HQ
  PricingUnit: subscription-month
  ProviderName: Orbital
  PublisherName: Orbital HQ
  ServiceCategory: Data Integration
  ServiceName: Orbital
layout: finops
meters:
- aggregation: max
  dimensions:
  - tier
  name: subscription_tier
  unit: month
- aggregation: sum
  dimensions:
  - workspace
  - tier
  name: api_calls
  unit: request
- aggregation: max
  dimensions:
  - tier
  name: workspaces
  unit: workspace
- aggregation: max
  dimensions:
  - workspace
  name: endpoints
  unit: endpoint
- aggregation: max
  dimensions:
  - tier
  name: admin_users
  unit: seat
- aggregation: max
  dimensions:
  - tier
  name: additional_users
  unit: seat
- aggregation: max
  name: ai_copilot_seats
  unit: seat
- aggregation: sum
  dimensions:
  - tier
  name: overage_calls
  unit: request
- aggregation: max
  name: managed_onprem
  unit: month
name: Taxi Finops
provider_name: Taxi - Describe How Your APIs and Data Relate
provider_slug: taxi-describe-how-your-apis-and-data-relate
publisher_name: Orbital HQ
service_category: Data Integration
slug: taxi-finops
source_filename: taxi-finops.yml
source_heading: FinOps Profile
source_url: https://taxilang.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Taxi - Describe How Your APIs and Data Relate\nproviderId: taxi-describe-how-your-apis-and-data-relate\npublisherName: Orbital HQ\nserviceCategory: Data Integration\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Data Integration\n  - Federated Query\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for the commercial Orbital platform that executes TaxiQL\n  queries against the Taxi schema registry. Billing is a tiered subscription with monthly call\n  quotas, per-additional-user fees, an AI Copilot add-on, and metered overage; the Taxi language\n  itself is Apache 2.0 open source and not\
  \ directly billed.\nsources:\n  - https://taxilang.org/\n  - https://orbitalhq.com/pricing\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Orbital\n  ServiceCategory: Data Integration\n  ProviderName: Orbital\n  PublisherName: Orbital HQ\n  InvoiceIssuerName: Orbital HQ\n  BillingCurrency: USD\n  PricingUnit: subscription-month\nmeters:\n  - name: subscription_tier\n    unit: month\n    aggregation: max\n    dimensions:\n      - tier\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - workspace\n      - tier\n  - name: workspaces\n    unit: workspace\n    aggregation: max\n    dimensions:\n      - tier\n  - name: endpoints\n    unit: endpoint\n    aggregation: max\n    dimensions:\n      - workspace\n  - name: admin_users\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tier\n  - name: additional_users\n\
  \    unit: seat\n    aggregation: max\n    dimensions:\n      - tier\n  - name: ai_copilot_seats\n    unit: seat\n    aggregation: max\n  - name: overage_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: managed_onprem\n    unit: month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Orbital monthly call consumption against the tier ceiling (100K / 1M /\n      10M / 100M / 1B) so overage at $200-$400 per 10M calls is forecast, not surprise. Workspace\n      and endpoint counts are visible in the Orbital console.\n  - name: Allocation\n    description: Allocate by Orbital workspace and tier so each consuming team's call volume,\n      additional-user seats, and AI Copilot seats can be charged back distinctly.\n  - name: Optimization\n    description: Right-size the tier against monthly call volume, push pure-OSS use of Taxi /\n      TaxiQL down into self-hosted environments where managed Orbital execution isn't required,\n\
  \      and consolidate endpoints inside fewer workspaces to stay within the per-tier endpoint cap.\n  - name: Accountability\n    description: The data integration / platform team that owns the Orbital workspace owns the\n      subscription tier choice, additional-user count, and AI Copilot seat allocation.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/taxi-describe-how-your-apis-and-data-relate/refs/heads/main/finops/taxi-finops.yml
sources:
- https://taxilang.org/
- https://orbitalhq.com/pricing
specification: FinOps Framework
tags:
- Data Integration
- Federated Query
- Open Source
- FinOps
- FOCUS
---
