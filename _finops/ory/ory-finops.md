---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ory-hydra-openapi.json
  format: json
  label: Ory Hydra
  slug: hydra
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ory/refs/heads/main/openapi/ory-hydra-openapi.json
- filename: ory-kratos-openapi.json
  format: json
  label: Ory Kratos
  slug: kratos
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ory/refs/heads/main/openapi/ory-kratos-openapi.json
- filename: ory-keto-openapi.json
  format: json
  label: Ory Keto
  slug: keto
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ory/refs/heads/main/openapi/ory-keto-openapi.json
- filename: ory-oathkeeper-openapi.json
  format: json
  label: Ory Oathkeeper
  slug: oathkeeper
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ory/refs/heads/main/openapi/ory-oathkeeper-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual subscription with monthly usage settlement
  chargeCategories:
  - Purchase
  - Usage
  - Credit
  - Tax
  pricingCategory: Subscription + Pay-As-You-Go
description: FOCUS-aligned FinOps definition for Ory Network. Combines an annual subscription fee per project plan with usage-based metering on aDAU, M2M tokens, and permission checks net of a fixed monthly credit.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Ory Corp.
  ProviderName: Ory
  PublisherName: Ory Corp.
  ServiceCategory: Identity
  ServiceName: Ory Network
layout: finops
meters:
- aggregation: sum
  description: Active Daily Active Users measured per project per month, net of monthly credit
  dimensions:
  - project
  - environment
  - plan
  name: adau
  unit: aDAU
- aggregation: sum
  description: Machine-to-machine OAuth2 tokens issued per project per month
  dimensions:
  - project
  - environment
  - plan
  name: m2m_tokens
  unit: token
- aggregation: sum
  description: Ory Keto permission check evaluations per project per month
  dimensions:
  - project
  - environment
  - plan
  name: permission_checks
  unit: check
- aggregation: count
  description: Annual subscription fee per project at the chosen plan level
  dimensions:
  - project
  - plan
  name: project_subscription
  unit: project-year
- aggregation: sum
  description: Included monthly usage credit applied against meters before billable usage accrues
  dimensions:
  - project
  - plan
  name: monthly_credit
  unit: USD
name: Ory Finops
provider_name: Ory
provider_slug: ory
publisher_name: Ory Corp.
service_category: Identity
slug: ory-finops
source_filename: ory-finops.yml
source_heading: FinOps Profile
source_url: https://www.ory.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ory\nproviderId: ory\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Identity\n  - CIAM\n  - OAuth2\ndescription: FOCUS-aligned FinOps definition for Ory Network. Combines an annual subscription\n  fee per project plan with usage-based metering on aDAU, M2M tokens, and permission checks\n  net of a fixed monthly credit.\nsources:\n  - https://www.ory.com/pricing\n  - https://www.ory.com/docs/guides/rate-limits\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Ory Corp.\nserviceCategory: Identity\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency:\
  \ Annual subscription with monthly usage settlement\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Credit\n    - Tax\nfocusColumns:\n  ServiceName: Ory Network\n  ServiceCategory: Identity\n  ProviderName: Ory\n  PublisherName: Ory Corp.\n  InvoiceIssuerName: Ory Corp.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: adau\n    description: Active Daily Active Users measured per project per month, net of monthly\n      credit\n    unit: aDAU\n    aggregation: sum\n    dimensions:\n      - project\n      - environment\n      - plan\n  - name: m2m_tokens\n    description: Machine-to-machine OAuth2 tokens issued per project per month\n    unit: token\n    aggregation: sum\n    dimensions:\n      - project\n      - environment\n      - plan\n  - name: permission_checks\n    description: Ory Keto permission check evaluations per project per month\n    unit: check\n    aggregation: sum\n    dimensions:\n      - project\n      - environment\n\
  \      - plan\n  - name: project_subscription\n    description: Annual subscription fee per project at the chosen plan level\n    unit: project-year\n    aggregation: count\n    dimensions:\n      - project\n      - plan\n  - name: monthly_credit\n    description: Included monthly usage credit applied against meters before billable usage\n      accrues\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - project\n      - plan\nprinciples:\n  - name: Visibility\n    description: Use the Ory Console usage dashboards to monitor aDAU, M2M token issuance,\n      and permission check counts per project; reconcile against the monthly invoice and\n      credit consumption.\n  - name: Allocation\n    description: Allocate by Ory project (one project per app/tenant is a common pattern)\n      and by environment (production vs staging). Tag identity flows by client_id to attribute\n      M2M token spend to consuming services.\n  - name: Optimization\n    description: Reduce aDAU by aligning\
  \ session lifetime to user behavior, prefer long-lived\n      sessions over re-authentication where appropriate, batch permission checks via Keto\n      check requests, and right-size plan tier so the included monthly credit covers steady-state\n      usage.\n  - name: Accountability\n    description: Each Ory project should have a named owner who reviews monthly usage versus\n      the included credit and decides when to escalate from Production to Growth or Enterprise.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ory/refs/heads/main/finops/ory-finops.yml
sources:
- https://www.ory.com/pricing
- https://www.ory.com/docs/guides/rate-limits
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Identity
- CIAM
- OAuth2
---
