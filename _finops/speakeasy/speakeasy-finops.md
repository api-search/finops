---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Speakeasy
  slug: speakeasy
  spec_type: OpenAPI
  url: https://www.speakeasy.com/openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Subscription + Usage-Based
description: FOCUS-aligned FinOps for Speakeasy — per-language SDK subscriptions, request-metered MCP tool calls, and resource-metered Terraform, all on a monthly invoicing cycle.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Speakeasy API, Inc.
  ProviderName: Speakeasy
  PublisherName: Speakeasy API, Inc.
  ServiceCategory: Developer Tools
  ServiceName: Speakeasy
layout: finops
meters:
- aggregation: sum
  description: Per-language seat for the SDKs & CLIs Business tier ($720/mo or $600/mo annual).
  dimensions:
  - language
  - plan
  name: language_subscription
  unit: language-month
- aggregation: count
  description: OpenAPI operations counted by unique operationId per licensed language; basis for tier sizing.
  dimensions:
  - language
  - plan
  name: operations
  unit: operation
- aggregation: sum
  description: Tool calls issued by LLMs to MCP servers under the AI Control Plane enterprise contract.
  dimensions:
  - server
  - tool
  name: mcp_tool_call_requests
  unit: request
- aggregation: max
  description: Resources managed by a generated Terraform provider; billing basis for the Terraform Enterprise plan.
  dimensions:
  - provider
  name: terraform_managed_resources
  unit: resource
name: Speakeasy Finops
provider_name: Speakeasy
provider_slug: speakeasy
publisher_name: Speakeasy API, Inc.
service_category: Developer Tools / SDK & MCP Generation
slug: speakeasy-finops
source_filename: speakeasy-finops.yml
source_heading: FinOps Profile
source_url: https://www.speakeasy.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Speakeasy\nproviderId: speakeasy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - AI\n  - Documentation\n  - MCP\n  - Platform\n  - SDKs\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Speakeasy — per-language SDK subscriptions,\n  request-metered MCP tool calls, and resource-metered Terraform, all on a\n  monthly invoicing cycle.\nsources:\n  - https://www.speakeasy.com/pricing\n  - https://www.speakeasy.com/docs\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Speakeasy API, Inc.\nserviceCategory: Developer Tools / SDK & MCP Generation\nbillingModel:\n  pricingCategory: Subscription + Usage-Based\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Speakeasy\n  ServiceCategory: Developer Tools\n  ProviderName: Speakeasy\n  PublisherName: Speakeasy API, Inc.\n  InvoiceIssuerName: Speakeasy API, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: language_subscription\n    description: Per-language seat for the SDKs & CLIs Business tier ($720/mo or\n      $600/mo annual).\n    unit: language-month\n    aggregation: sum\n    dimensions:\n      - language\n      - plan\n  - name: operations\n    description: OpenAPI operations counted by unique operationId per licensed\n      language; basis for tier sizing.\n    unit: operation\n    aggregation: count\n    dimensions:\n      - language\n      - plan\n  - name: mcp_tool_call_requests\n    description: Tool calls issued by LLMs to MCP servers under the AI Control\n      Plane enterprise contract.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - server\n      -\
  \ tool\n  - name: terraform_managed_resources\n    description: Resources managed by a generated Terraform provider; billing\n      basis for the Terraform Enterprise plan.\n    unit: resource\n    aggregation: max\n    dimensions:\n      - provider\nprinciples:\n  - name: Visibility\n    description: Workspace dashboards expose operations counts per language and\n      tier. Enterprise customers receive usage exports for MCP and Terraform\n      meters; consumers should reconcile these against monthly invoices.\n  - name: Allocation\n    description: Allocate cost by the language seat (each licensed language is\n      its own line) and, for AI Control Plane, by MCP server / consuming team.\n  - name: Optimization\n    description: Hold operationId growth flat where possible to stay under the\n      250-operation cap; consolidate duplicate operations in your OpenAPI spec\n      before licensing additional languages. Annual billing yields ~17% discount\n      versus monthly.\n  - name:\
  \ Accountability\n    description: Platform / DX team owns the language license footprint;\n      AI / agents team owns the MCP tool-call meter; product owners track\n      Terraform resource counts as part of provider design.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/speakeasy/refs/heads/main/finops/speakeasy-finops.yml
sources:
- https://www.speakeasy.com/pricing
- https://www.speakeasy.com/docs
specification: FinOps Framework
tags:
- AI
- Documentation
- MCP
- Platform
- SDKs
- FinOps
- FOCUS
---
