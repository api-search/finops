---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: veeva-systems-openapi.yml
  format: yaml
  label: Veeva Systems API
  slug: veeva-systems-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veeva-systems/refs/heads/main/openapi/veeva-systems-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps stub for Veeva Systems: enterprise life-sciences SaaS subscription with no public pricing or usage/billing API.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Veeva Systems Inc.
  ProviderName: Veeva Systems
  PublisherName: Veeva Systems Inc.
  ServiceCategory: Life Sciences SaaS
  ServiceName: Veeva Vault / CRM / Crossix / Network
layout: finops
meters:
- aggregation: sum
  description: Annual Vault / CRM / Crossix / Network subscription line; sub-meters not publicly published.
  name: tenant_subscription
  unit: varies
- aggregation: sum
  description: Observed API call count from in-product API Usage Logs. Not a billable meter.
  name: api_usage_observed
  unit: request
name: Veeva Systems Finops
provider_name: Veeva Systems
provider_slug: veeva-systems
publisher_name: Veeva Systems Inc.
service_category: Life Sciences SaaS
slug: veeva-systems-finops
source_filename: veeva-systems-finops.yml
source_heading: FinOps Profile
source_url: https://www.veeva.com/products/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Veeva Systems\nproviderId: veeva-systems\npublisherName: Veeva Systems Inc.\nserviceCategory: Life Sciences SaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Life Sciences\n  - SaaS\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps stub for Veeva Systems: enterprise life-sciences SaaS subscription with\n  no public pricing or usage/billing API.'\nsources:\n  - https://www.veeva.com/products/\n  - https://developer.veevavault.com/api/26.1/\nnotes: No public pricing or billing API. Meters are not invented; API call counts are observable per-tenant\n  via API Usage Logs but are not a billable line.\nbillingModel:\n\
  \  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Veeva Vault / CRM / Crossix / Network\n  ServiceCategory: Life Sciences SaaS\n  ProviderName: Veeva Systems\n  PublisherName: Veeva Systems Inc.\n  InvoiceIssuerName: Veeva Systems Inc.\n  BillingCurrency: USD\nmeters:\n  - name: tenant_subscription\n    description: Annual Vault / CRM / Crossix / Network subscription line; sub-meters not publicly published.\n    unit: varies\n    aggregation: sum\n  - name: api_usage_observed\n    description: Observed API call count from in-product API Usage Logs. Not a billable meter.\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Per-tenant API telemetry is exposed through Admin > Settings > Logs > API Usage Logs\n      and rate-limit response headers; cost is invoice-level only.\n  - name: Allocation\n    description: Allocation is contract-level per\
  \ Veeva product / tenant; chargeback rides on seat / module\n      scoping negotiated in the order form.\n  - name: Optimization\n    description: 'Optimization is scope-driven: which Vault / CRM modules are licensed, seat counts, and\n      integration patterns (batch vs interactive). Renewal is the primary optimization checkpoint.'\n  - name: Accountability\n    description: Accountability sits with the platform owner team that holds the Veeva tenant agreement;\n      finance owns the annual subscription line.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veeva-systems/refs/heads/main/finops/veeva-systems-finops.yml
sources:
- https://www.veeva.com/products/
- https://developer.veevavault.com/api/26.1/
specification: FinOps Framework
tags:
- Life Sciences
- SaaS
- FinOps
- FOCUS
---
