---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: truto-admin-openapi.yml
  format: yaml
  label: Truto Admin API
  slug: truto-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/truto/refs/heads/main/openapi/truto-admin-openapi.yml
- filename: truto-unified-hris-openapi.yml
  format: yaml
  label: Truto Unified HRIS API
  slug: truto-unified-hris-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/truto/refs/heads/main/openapi/truto-unified-hris-openapi.yml
- filename: truto-unified-ats-openapi.yml
  format: yaml
  label: Truto Unified ATS API
  slug: truto-unified-ats-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/truto/refs/heads/main/openapi/truto-unified-ats-openapi.yml
- filename: truto-unified-crm-openapi.yml
  format: yaml
  label: Truto Unified CRM API
  slug: truto-unified-crm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/truto/refs/heads/main/openapi/truto-unified-crm-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Per-Connector Subscription
description: FOCUS-aligned FinOps for Truto's per-connector unified-API subscription — billed annually per connector ($999 Expansion, $1,999 Enterprise) with active-account-based billing, unlimited API calls, and tier-based environment / log-retention caps.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Truto
  ProviderName: Truto
  PublisherName: Truto
  ServiceCategory: Unified API / Integration Platform
  ServiceName: Truto Unified API
layout: finops
meters:
- aggregation: sum
  description: Annual per-connector subscription line (Expansion $999, Enterprise $1,999).
  dimensions:
  - tier
  - connector
  name: connector_subscription
  unit: connector
- aggregation: max
  description: Active customer/company accounts on the platform; the basis for billing visibility (not separately metered, but drives subscription scope).
  dimensions:
  - tier
  name: active_accounts
  unit: account
- aggregation: max
  description: Configured environments (5 included on Expansion, unlimited on Enterprise).
  dimensions:
  - tier
  name: environments
  unit: environment
name: Truto Finops
provider_name: Truto
provider_slug: truto
publisher_name: Truto
service_category: Unified API / Integration Platform
slug: truto-finops
source_filename: truto-finops.yml
source_heading: FinOps Profile
source_url: https://truto.one/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Truto\nproviderId: truto\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Unified API\n  - Integrations\n  - iPaaS\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Truto's per-connector unified-API subscription — billed annually\n  per connector ($999 Expansion, $1,999 Enterprise) with active-account-based billing, unlimited API calls,\n  and tier-based environment / log-retention caps.\nsources:\n  - https://truto.one/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Truto\nserviceCategory: Unified API / Integration Platform\nbillingModel:\n  pricingCategory: Per-Connector Subscription\n  billingFrequency: Annual\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Truto Unified API\n  ServiceCategory: Unified API / Integration Platform\n  ProviderName: Truto\n  PublisherName: Truto\n  InvoiceIssuerName: Truto\n  BillingCurrency: USD\nmeters:\n  - name: connector_subscription\n    description: Annual per-connector subscription line (Expansion $999, Enterprise $1,999).\n    unit: connector\n    aggregation: sum\n    dimensions:\n      - tier\n      - connector\n  - name: active_accounts\n    description: Active customer/company accounts on the platform; the basis for billing visibility (not\n      separately metered, but drives subscription scope).\n    unit: account\n    aggregation: max\n    dimensions:\n      - tier\n  - name: environments\n    description: Configured environments (5 included on Expansion, unlimited on Enterprise).\n    unit: environment\n    aggregation: max\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Visibility is\
  \ per-connector — track which connectors are active and how many accounts\n      they cover via the Truto dashboard; the invoice line maps directly to connector count.\n  - name: Allocation\n    description: Allocate cost per connector to the product or feature that consumes it (e.g. CRM connector\n      to RevOps, ATS connector to People Ops); active-account billing means deactivating unused accounts\n      reduces effective cost.\n  - name: Optimization\n    description: Cost levers are connector-count discipline (do not enable connectors you do not actively\n      use), tier downgrade where Enterprise-only features (single tenant, on-prem, 90-day logs) are not\n      required, and consolidating environments within the 5-environment Expansion cap.\n  - name: Accountability\n    description: Each connector should have an engineering or product owner responsible for justifying\n      its renewal; finance reviews the annual per-connector roster at contract anniversary.\nmaintainers:\n \
  \ - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/truto/refs/heads/main/finops/truto-finops.yml
sources:
- https://truto.one/pricing
specification: FinOps Framework
tags:
- Unified API
- Integrations
- iPaaS
- FinOps
- FOCUS
---
