---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: stackone-openapi.yml
  format: yaml
  label: StackOne
  slug: stackone
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stackone/refs/heads/main/openapi/stackone-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription + Pay-As-You-Go
description: FOCUS-aligned FinOps for StackOne - subscription base (Starter free, Core and Enterprise contact-sales) plus action-call metering ($0.003 per call on Starter overage, $0.30 per 1,000 on Core / Enterprise). The action call is the unit meter; cost dimensions include connector, project, and tenant.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: StackOne
  ProviderName: StackOne
  PublisherName: StackOne
  ServiceCategory: Integration Platform
  ServiceName: StackOne Unified API
layout: finops
meters:
- aggregation: count
  dimensions:
  - connector
  - linked_account
  - project
  - tenant
  name: action_calls
  unit: action
- aggregation: sum
  dimensions:
  - plan_tier
  name: subscription_seat
  unit: month
- aggregation: count
  dimensions:
  - project
  name: custom_connectors
  unit: connector
- aggregation: count
  dimensions:
  - plan_tier
  name: projects
  unit: project
name: Stackone Finops
provider_name: StackOne
provider_slug: stackone
publisher_name: StackOne
service_category: Integration Platform
slug: stackone-finops
source_filename: stackone-finops.yml
source_heading: FinOps Profile
source_url: https://www.stackone.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: StackOne\nproviderId: stackone\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Integrations\n  - iPaaS\n  - Unified API\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for StackOne - subscription base (Starter free, Core and Enterprise contact-sales) plus action-call metering ($0.003 per call on Starter overage, $0.30 per 1,000 on Core / Enterprise). The action call is the unit meter; cost dimensions include connector, project, and tenant.\nsources:\n  - https://www.stackone.com/pricing\n  - https://docs.stackone.com/\nnotes: Per-call rates are public; base subscription for Core / Enterprise is contact-sales and not modeled here as a fixed line.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: StackOne\nserviceCategory: Integration Platform\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: StackOne Unified API\n  ServiceCategory: Integration Platform\n  ProviderName: StackOne\n  PublisherName: StackOne\n  InvoiceIssuerName: StackOne\n  BillingCurrency: USD\nmeters:\n  - name: action_calls\n    unit: action\n    aggregation: count\n    dimensions:\n      - connector\n      - linked_account\n      - project\n      - tenant\n  - name: subscription_seat\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan_tier\n  - name: custom_connectors\n    unit: connector\n    aggregation: count\n    dimensions:\n      - project\n  - name: projects\n    unit: project\n    aggregation: count\n    dimensions:\n      - plan_tier\nprinciples:\n  - name: Visibility\n    description: StackOne's dashboard reports action-call\
  \ counts per linked account, connector, and project; export these via the platform API to attribute spend back to the tenant or feature consuming the call.\n  - name: Allocation\n    description: Tag every linked account with the consuming product, tenant, and environment so the action-call meter can roll up by team. StackOne's project abstraction is the natural allocation boundary - one project per consuming product or workspace keeps cost lines clean.\n  - name: Optimization\n    description: Cache idempotent reads (employee lookups, candidate metadata) at the consumer side, batch list endpoints with cursoring rather than re-fetching, and prefer the Unified API over per-vendor connectors to amortize action-call cost across providers. Negotiate volume discounts on action-call rate at Core or Enterprise tier.\n  - name: Accountability\n    description: Platform / integrations team owns the StackOne contract and tier choice; consuming product teams own the action-call volume their workflows\
  \ generate and review monthly meter exports.\nmaintainers:\n  - name: StackOne\n    url: https://www.stackone.com/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stackone/refs/heads/main/finops/stackone-finops.yml
sources:
- https://www.stackone.com/pricing
- https://docs.stackone.com/
specification: FinOps Framework
tags:
- Integrations
- iPaaS
- Unified API
- FinOps
- FOCUS
---
