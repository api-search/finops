---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: boltic-gateway-api-openapi.yml
  format: yaml
  label: Boltic Gateway API
  slug: gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/boltic/refs/heads/main/openapi/boltic-gateway-api-openapi.yml
- filename: boltic-workflow-api-openapi.yml
  format: yaml
  label: Boltic Workflow API
  slug: workflow-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/boltic/refs/heads/main/openapi/boltic-workflow-api-openapi.yml
- filename: boltic-tables-api-openapi.yml
  format: yaml
  label: Boltic Tables API
  slug: tables-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/boltic/refs/heads/main/openapi/boltic-tables-api-openapi.yml
- filename: boltic-pipes-api-openapi.yml
  format: yaml
  label: Boltic Pipes API
  slug: pipes-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/boltic/refs/heads/main/openapi/boltic-pipes-api-openapi.yml
- filename: boltic-streams-api-openapi.yml
  format: yaml
  label: Boltic Streams API
  slug: streams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/boltic/refs/heads/main/openapi/boltic-streams-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription + Credits
description: 'FOCUS-aligned FinOps for Boltic: tiered subscription with execution / seat / storage quotas per plan, plus pay-as-you-go credits at $1.25 per credit for premium AI integrations.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Boltic
  PricingCategory: Standard
  PricingUnit: subscription-month
  ProviderName: Boltic
  PublisherName: Boltic
  ServiceCategory: Workflow Automation
  ServiceName: Boltic
layout: finops
meters:
- aggregation: sum
  description: Plan subscription fee billed monthly per account.
  dimensions:
  - plan
  - billing_cycle
  name: subscription_month
  unit: month
- aggregation: sum
  description: Count of workflow runs charged against the plan's monthly execution allowance.
  dimensions:
  - workflow
  - plan
  - environment
  name: workflow_executions
  unit: execution
- aggregation: max
  description: Number of provisioned team members on the account.
  dimensions:
  - plan
  - role
  name: seats
  unit: seat
- aggregation: max
  description: Provisioned storage attached to the account.
  dimensions:
  - plan
  name: storage
  unit: GB-month
- aggregation: sum
  description: Pay-as-you-go credits consumed for premium AI integrations and advanced models.
  dimensions:
  - integration
  - model
  name: ai_credits
  unit: credit
name: Boltic Finops
provider_name: Boltic
provider_slug: boltic
publisher_name: Boltic
service_category: Workflow Automation
slug: boltic-finops
source_filename: boltic-finops.yml
source_heading: FinOps Profile
source_url: https://www.boltic.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Boltic\nproviderId: boltic\npublisherName: Boltic\nserviceCategory: Workflow Automation\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Automation\n  - DataSync\n  - Gateways\n  - NoCode\n  - Streaming\n  - Workflows\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Boltic: tiered subscription with execution / seat / storage quotas\n  per plan, plus pay-as-you-go credits at $1.25 per credit for premium AI integrations.'\nsources:\n  - https://www.boltic.io/pricing\n  - https://docs.boltic.io/\nbillingModel:\n  pricingCategory: Tiered Subscription + Credits\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Boltic\n  ServiceCategory: Workflow Automation\n  ProviderName: Boltic\n  PublisherName: Boltic\n  InvoiceIssuerName: Boltic\n  BillingCurrency: USD\n  PricingCategory: Standard\n  PricingUnit: subscription-month\nmeters:\n  - name: subscription_month\n    description: Plan subscription fee billed monthly per account.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - billing_cycle\n  - name: workflow_executions\n    description: Count of workflow runs charged against the plan's monthly execution allowance.\n    unit: execution\n    aggregation: sum\n    dimensions:\n      - workflow\n      - plan\n      - environment\n  - name: seats\n    description: Number of provisioned team members on the account.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\n      - role\n  - name: storage\n    description: Provisioned\
  \ storage attached to the account.\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - plan\n  - name: ai_credits\n    description: Pay-as-you-go credits consumed for premium AI integrations and advanced models.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - integration\n      - model\nprinciples:\n  - name: Visibility\n    description: Track workflow execution counts, seat usage, and credit consumption from the Boltic console;\n      monitor monthly execution headroom to avoid plan overage.\n  - name: Allocation\n    description: Tag workflows with the consuming team / business function and split credit consumption\n      by integration and AI model so spend can be attributed.\n  - name: Optimization\n    description: Right-size the subscription tier to the actual monthly execution profile, consolidate\n      duplicate workflows, prefer batch and webhook-triggered patterns over polling, and reserve credits\n      for high-value AI calls.\n  - name: Accountability\n\
  \    description: Designate a workflow owner per business function; review monthly execution and credit\n      burn against budget and renegotiate Enterprise capacity at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/boltic/refs/heads/main/finops/boltic-finops.yml
sources:
- https://www.boltic.io/pricing
- https://docs.boltic.io/
specification: FinOps Framework
tags:
- Automation
- DataSync
- Gateways
- NoCode
- Streaming
- Workflows
- FinOps
- FOCUS
---
