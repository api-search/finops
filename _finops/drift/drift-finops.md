---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: drift-openapi.yml
  format: yaml
  label: Drift
  slug: drift
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/drift/refs/heads/main/openapi/drift-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Annual Contract (Tiered)
description: FOCUS-aligned FinOps for Drift.
focus_columns:
  BillingCurrency: USD
  ProviderName: Drift
  PublisherName: Drift
  ServiceCategory: Conversational AI
  ServiceName: Drift
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: sum
  name: conversations
  unit: conversation
- aggregation: sum
  name: ai_messages
  unit: message
- aggregation: sum
  name: playbook_executions
  unit: execution
name: Drift Finops
provider_name: Drift
provider_slug: drift
publisher_name: Drift
service_category: Conversational AI
slug: drift-finops
source_filename: drift-finops.yml
source_heading: FinOps Profile
source_url: https://www.drift.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Drift\nproviderId: drift\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Conversational AI\ndescription: FOCUS-aligned FinOps for Drift.\nsources:\n  - https://www.drift.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Drift\nserviceCategory: Conversational AI\nbillingModel:\n  pricingCategory: Annual Contract (Tiered)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Drift\n  ServiceCategory: Conversational AI\n  ProviderName: Drift\n  PublisherName: Drift\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n\
  \  - name: conversations\n    unit: conversation\n    aggregation: sum\n  - name: ai_messages\n    unit: message\n    aggregation: sum\n  - name: playbook_executions\n    unit: execution\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Drift consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/drift/refs/heads/main/finops/drift-finops.yml
sources:
- https://www.drift.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Conversational AI
---
