---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: vessel-platform-openapi.yml
  format: yaml
  label: Vessel Platform API
  slug: platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vessel/refs/heads/main/openapi/vessel-platform-openapi.yml
- filename: vessel-crm-openapi.yml
  format: yaml
  label: Vessel CRM API
  slug: crm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vessel/refs/heads/main/openapi/vessel-crm-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: Vessel bills on a connection-tier subscription model (Start, Launch, Custom) rather than per API call. Cost scales with the number of customer SaaS integrations active, not request volume; Launch and Custom are quoted directly.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Vessel
  ProviderName: Vessel
  PublisherName: Vessel
  ServiceCategory: Integration Platform
  ServiceName: Vessel Unified API
layout: finops
meters:
- aggregation: max
  dimensions:
  - environment
  - integration_provider
  name: connections_active
  unit: connection
- aggregation: max
  dimensions:
  - plan_tier
  name: plan_subscription
  unit: month
name: Vessel Finops
provider_name: Vessel
provider_slug: vessel
publisher_name: Vessel
service_category: Unified API / Integrations
slug: vessel-finops
source_filename: vessel-finops.yml
source_heading: FinOps Profile
source_url: https://www.vessel.dev/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Vessel\nproviderId: vessel\npublisherName: Vessel\nserviceCategory: Unified API / Integrations\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Unified API\n  - Integrations\ndescription: Vessel bills on a connection-tier subscription model (Start, Launch, Custom) rather\n  than per API call. Cost scales with the number of customer SaaS integrations active, not request\n  volume; Launch and Custom are quoted directly.\nsources:\n  - https://www.vessel.dev/pricing\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n\
  \  ServiceName: Vessel Unified API\n  ServiceCategory: Integration Platform\n  ProviderName: Vessel\n  PublisherName: Vessel\n  InvoiceIssuerName: Vessel\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: connections_active\n    unit: connection\n    aggregation: max\n    dimensions:\n      - environment\n      - integration_provider\n  - name: plan_subscription\n    unit: month\n    aggregation: max\n    dimensions:\n      - plan_tier\nprinciples:\n  - name: Visibility\n    description: Track active connections in the Vessel dashboard against the plan ceiling (5 / 20\n      / unlimited); since billing is plan-tier based, dashboard connection count is the leading\n      cost indicator.\n  - name: Allocation\n    description: Tag each Vessel connection with the consuming customer / tenant and the destination\n      SaaS provider; allocate the plan fee across active connections for showback.\n  - name: Optimization\n    description: Decommission stale connections; promote\
  \ prototypes from Start to Launch only when\n      they cross the 5-connection ceiling; consolidate to Custom when whitelabeling or unlimited\n      connections is required to avoid per-tenant escalations.\n  - name: Accountability\n    description: The integrating product team owns the Vessel plan and connection lifecycle; finance\n      reconciles the monthly subscription against the contracted Launch / Custom rate.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vessel/refs/heads/main/finops/vessel-finops.yml
sources:
- https://www.vessel.dev/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Unified API
- Integrations
---
