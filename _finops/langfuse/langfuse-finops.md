---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Tracing API
  slug: langfuse-tracing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Observations API
  slug: langfuse-observations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Metrics API
  slug: langfuse-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Prompt Management API
  slug: langfuse-prompts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Datasets API
  slug: langfuse-datasets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Evaluations API
  slug: langfuse-evaluations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Scores API
  slug: langfuse-scores-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Organizations & Projects API
  slug: langfuse-organizations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Instance Management API
  slug: langfuse-instance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: FOCUS-aligned FinOps profile for Langfuse Cloud. Cloud billing combines a flat-rate monthly subscription per plan tier with usage-based overage on units (a unified metric covering traces, observations, and scores). Self-hosted has no platform fees.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Langfuse GmbH
  ProviderName: Langfuse
  PublisherName: Langfuse GmbH
  ServiceCategory: AI
  ServiceName: Langfuse Cloud
layout: finops
meters:
- aggregation: sum
  description: Monthly plan subscription (Core $29, Pro $199, Enterprise $2,499).
  dimensions:
  - account
  - plan
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Billable units (traces, observations, scores). Each plan includes a baseline; overage at $8/100k with volume discounts.
  dimensions:
  - organization
  - project
  name: units
  unit: unit
- aggregation: sum
  description: Optional Pro Teams add-on ($300/month) for SSO and fine-grained RBAC.
  dimensions:
  - organization
  name: teams_addon
  unit: month
name: Langfuse Finops
provider_name: Langfuse
provider_slug: langfuse
publisher_name: Langfuse GmbH
service_category: AI
slug: langfuse-finops
source_filename: langfuse-finops.yml
source_heading: FinOps Profile
source_url: https://langfuse.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Langfuse\nproviderId: langfuse\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- LLM\n- Observability\n- Open Source\n- Evaluations\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for Langfuse Cloud. Cloud billing combines a\n  flat-rate monthly subscription per plan tier with usage-based overage on units (a unified\n  metric covering traces, observations, and scores). Self-hosted has no platform fees.\nsources:\n- https://langfuse.com/pricing\n- https://langfuse.com/docs\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Langfuse GmbH\nserviceCategory: AI\nbillingModel:\n\
  \  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Langfuse Cloud\n  ServiceCategory: AI\n  ProviderName: Langfuse\n  PublisherName: Langfuse GmbH\n  InvoiceIssuerName: Langfuse GmbH\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: subscription_fee\n  description: Monthly plan subscription (Core $29, Pro $199, Enterprise $2,499).\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n  - plan\n- name: units\n  description: Billable units (traces, observations, scores). Each plan includes a baseline;\n    overage at $8/100k with volume discounts.\n  unit: unit\n  aggregation: sum\n  dimensions:\n  - organization\n  - project\n- name: teams_addon\n  description: Optional Pro Teams add-on ($300/month) for SSO and fine-grained RBAC.\n  unit: month\n  aggregation: sum\n  dimensions:\n  - organization\nprinciples:\n- name: Visibility\n\
  \  description: Use Langfuse usage dashboards and invoices to map unit consumption to\n    organizations and projects.\n- name: Allocation\n  description: Tag traces by environment and product to allocate units to consuming services.\n- name: Optimization\n  description: Sample low-value traces, choose appropriate retention tier, and consider\n    self-hosting for high-volume workloads.\n- name: Accountability\n  description: Assign each project to a budget owner and review monthly unit consumption\n    against forecast.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/finops/langfuse-finops.yml
sources:
- https://langfuse.com/pricing
- https://langfuse.com/docs
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- Observability
- Open Source
- Evaluations
- FinOps
- Cost Management
- FOCUS
---
