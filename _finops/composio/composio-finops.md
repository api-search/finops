---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: composio-openapi-original.yml
  format: yaml
  label: Composio Tool Router API
  slug: tool-router-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/composio/refs/heads/main/openapi/composio-openapi-original.yml
- filename: composio-openapi-original.yml
  format: yaml
  label: Composio Tools API
  slug: tools-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/composio/refs/heads/main/openapi/composio-openapi-original.yml
- filename: composio-openapi-original.yml
  format: yaml
  label: Composio Connected Accounts API
  slug: connected-accounts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/composio/refs/heads/main/openapi/composio-openapi-original.yml
- filename: composio-openapi-original.yml
  format: yaml
  label: Composio Auth Configs API
  slug: auth-configs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/composio/refs/heads/main/openapi/composio-openapi-original.yml
- filename: composio-openapi-original.yml
  format: yaml
  label: Composio Triggers API
  slug: triggers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/composio/refs/heads/main/openapi/composio-openapi-original.yml
- filename: composio-openapi-original.yml
  format: yaml
  label: Composio Toolkits API
  slug: toolkits-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/composio/refs/heads/main/openapi/composio-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Tiered Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Composio: tiered subscription with monthly tool-call quotas plus per-1K overage billing for AI-agent integration calls.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Composio Inc.
  PricingUnit: tool_call
  ProviderName: Composio
  PublisherName: Composio Inc.
  ServiceCategory: AI Tooling / Integrations
  ServiceName: Composio
layout: finops
meters:
- aggregation: sum
  description: Count of billable tool-call invocations executed through Composio
  dimensions:
  - tier
  - toolkit
  - account
  - environment
  name: tool_calls
  unit: tool_call
- aggregation: max
  description: Monthly subscription per account/workspace
  dimensions:
  - tier
  - account
  name: subscription_seat
  unit: month
- aggregation: sum
  description: Tool calls exceeding the included monthly quota, billed per 1,000
  dimensions:
  - tier
  - account
  name: tool_call_overage
  unit: tool_calls_per_1000
name: Composio Finops
provider_name: Composio
provider_slug: composio
publisher_name: Composio Inc.
service_category: AI Tooling / Integrations
slug: composio-finops
source_filename: composio-finops.yml
source_heading: FinOps Profile
source_url: https://composio.dev/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Composio\nproviderId: composio\npublisherName: Composio Inc.\nserviceCategory: AI Tooling / Integrations\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - AI Agents\n  - Authentication\n  - Integrations\n  - OAuth\n  - Tools\n  - Unified_API\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Composio: tiered subscription with monthly tool-call quotas plus\n  per-1K overage billing for AI-agent integration calls.'\nsources:\n  - https://composio.dev/pricing\n  - https://docs.composio.dev/\nbillingModel:\n  pricingCategory: Tiered Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n\
  \  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Composio\n  ServiceCategory: AI Tooling / Integrations\n  ProviderName: Composio\n  PublisherName: Composio Inc.\n  InvoiceIssuerName: Composio Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: tool_call\nmeters:\n  - name: tool_calls\n    description: Count of billable tool-call invocations executed through Composio\n    unit: tool_call\n    aggregation: sum\n    dimensions:\n      - tier\n      - toolkit\n      - account\n      - environment\n  - name: subscription_seat\n    description: Monthly subscription per account/workspace\n    unit: month\n    aggregation: max\n    dimensions:\n      - tier\n      - account\n  - name: tool_call_overage\n    description: Tool calls exceeding the included monthly quota, billed per 1,000\n    unit: tool_calls_per_1000\n    aggregation: sum\n    dimensions:\n      - tier\n      - account\nprinciples:\n  -\
  \ name: Visibility\n    description: Use the Composio dashboard's usage views to track tool-call consumption per workspace\n      and toolkit; export usage to internal data warehouses for unified FinOps reporting.\n  - name: Allocation\n    description: Tag tool calls by Composio entity ID (the per-end-user identifier) and toolkit so consumption\n      can be attributed to consuming team, product, or end-customer.\n  - name: Optimization\n    description: Reduce per-tool-call cost by caching deterministic tool outputs, batching agent steps,\n      using the Tool Router to short-circuit unnecessary calls, and right-sizing the subscription tier\n      against included quota.\n  - name: Accountability\n    description: Set quota alerts before the included tool-call ceiling is reached on Starter and Professional\n      to control overage spend; assign workspace owners as budget holders.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/composio/refs/heads/main/finops/composio-finops.yml
sources:
- https://composio.dev/pricing
- https://docs.composio.dev/
specification: FinOps Framework
tags:
- AI Agents
- Authentication
- Integrations
- OAuth
- Tools
- Unified_API
- FinOps
- FOCUS
---
