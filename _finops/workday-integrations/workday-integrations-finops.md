---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Workday REST API
  slug: ''
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/restapi/openapi.json
- filename: workday-integrations-raas-openapi.yml
  format: yaml
  label: Workday RaaS (Report-as-a-Service)
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-integrations/refs/heads/main/openapi/workday-integrations-raas-openapi.yml
- filename: workday-integrations-prism-analytics-openapi.yml
  format: yaml
  label: Workday Prism Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-integrations/refs/heads/main/openapi/workday-integrations-prism-analytics-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps stub for the Workday Integrations capability. Integration entitlement is bundled into the Workday tenant subscription; per-integration-run pricing and a public usage API are not exposed, so meters describe contractual entitlement rather than runtime billing.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Workday, Inc.
  ProviderName: Workday
  PublisherName: Workday, Inc.
  ServiceCategory: Integration / iPaaS
  ServiceName: Workday Integrations
layout: finops
meters:
- aggregation: max
  description: Annual Workday Integrations entitlement attached to the tenant subscription; covers Studio runtime and bundled Cloud Connect packs.
  dimensions:
  - tenant
  name: integrations_entitlement
  unit: month
- aggregation: max
  description: Count of customer-built and Cloud Connect integrations active in the tenant; used for governance and renewal sizing rather than per-run billing.
  dimensions:
  - tenant
  - integration_type
  name: active_integrations
  unit: integration
name: Workday Integrations Finops
provider_name: Workday Integrations
provider_slug: workday-integrations
publisher_name: Workday, Inc.
service_category: Integration / iPaaS
slug: workday-integrations-finops
source_filename: workday-integrations-finops.yml
source_heading: FinOps Profile
source_url: https://www.workday.com/en-us/enterprise-resource-planning.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workday Integrations\nproviderId: workday-integrations\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Integration\n  - iPaaS\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps stub for the Workday Integrations capability. Integration entitlement is bundled into the Workday tenant subscription; per-integration-run pricing and a public usage API are not exposed, so meters describe contractual entitlement rather than runtime billing.\nsources:\n  - https://www.workday.com/en-us/enterprise-resource-planning.html\nnotes: Duplicates the workday-integration finops surface under the alternate slug. Generic api_request / data_egress / compute_seconds meters from the scaffold have been removed.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Workday, Inc.\nserviceCategory: Integration / iPaaS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Workday Integrations\n  ServiceCategory: Integration / iPaaS\n  ProviderName: Workday\n  PublisherName: Workday, Inc.\n  InvoiceIssuerName: Workday, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: integrations_entitlement\n    description: Annual Workday Integrations entitlement attached to the tenant subscription; covers Studio runtime and bundled Cloud Connect packs.\n    unit: month\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: active_integrations\n    description: Count of customer-built and Cloud Connect integrations active in the tenant; used for governance and renewal sizing rather than per-run billing.\n    unit: integration\n    aggregation: max\n   \
  \ dimensions:\n      - tenant\n      - integration_type\nprinciples:\n  - name: Visibility\n    description: Maintain an integration inventory (owner, source / target, cadence) and reconcile it against tenant integration event reports; invoice line items don't break out integration runs, so visibility comes from the catalog plus utilization telemetry.\n  - name: Allocation\n    description: Allocate integration spend back to the systems-of-record on each side of the integration; require a business case linking each new integration to a downstream consumer.\n  - name: Optimization\n    description: Retire dead integrations at renewal, prefer EIB over custom Studio when data shape allows, schedule batch runs in low-load windows, and consolidate point-to-point flows into reusable Studio templates.\n  - name: Accountability\n    description: An Integration Center of Excellence lead approves new integrations, runs quarterly inventory reviews, and represents the integration backlog at Workday\
  \ renewal conversations.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday-integrations/refs/heads/main/finops/workday-integrations-finops.yml
sources:
- https://www.workday.com/en-us/enterprise-resource-planning.html
specification: FinOps Framework
tags:
- Integration
- iPaaS
- FinOps
- FOCUS
---
