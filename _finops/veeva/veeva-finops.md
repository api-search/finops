---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: veeva-vault-openapi.yml
  format: yaml
  label: Veeva Vault Platform API
  slug: veeva-vault-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veeva/refs/heads/main/openapi/veeva-vault-openapi.yml
- filename: veeva-vault-openapi.yml
  format: yaml
  label: Veeva Vault Query Language (VQL) API
  slug: veeva-vault-query-language
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veeva/refs/heads/main/openapi/veeva-vault-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps stub for Veeva: enterprise life-sciences SaaS subscription with no public pricing or usage/billing API. API access is bundled with the Vault / CRM subscription.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Veeva Systems Inc.
  ProviderName: Veeva
  PublisherName: Veeva Systems Inc.
  ServiceCategory: Life Sciences SaaS
  ServiceName: Veeva Vault / CRM
layout: finops
meters:
- aggregation: sum
  description: Annual Vault / CRM tenant subscription line; sub-meters not publicly published.
  name: tenant_subscription
  unit: varies
- aggregation: sum
  description: Observed API call count from in-product API Usage Logs. Not a billable meter; provided for capacity tracking and rate-limit insight.
  name: api_usage_observed
  unit: request
name: Veeva Finops
provider_name: veeva
provider_slug: veeva
publisher_name: Veeva Systems Inc.
service_category: Life Sciences SaaS
slug: veeva-finops
source_filename: veeva-finops.yml
source_heading: FinOps Profile
source_url: https://www.veeva.com/products/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: veeva\nproviderId: veeva\npublisherName: Veeva Systems Inc.\nserviceCategory: Life Sciences SaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Life Sciences\n  - SaaS\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps stub for Veeva: enterprise life-sciences SaaS subscription with no public\n  pricing or usage/billing API. API access is bundled with the Vault / CRM subscription.'\nsources:\n  - https://www.veeva.com/products/\n  - https://developer.veevavault.com/api/26.1/\nnotes: No public pricing. Meters not invented; API usage is observable per-tenant via API Usage Logs but\n  is not a billable line. Reconciliation\
  \ deferred pending customer-portal billing API discovery.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Veeva Vault / CRM\n  ServiceCategory: Life Sciences SaaS\n  ProviderName: Veeva\n  PublisherName: Veeva Systems Inc.\n  InvoiceIssuerName: Veeva Systems Inc.\n  BillingCurrency: USD\nmeters:\n  - name: tenant_subscription\n    description: Annual Vault / CRM tenant subscription line; sub-meters not publicly published.\n    unit: varies\n    aggregation: sum\n  - name: api_usage_observed\n    description: Observed API call count from in-product API Usage Logs. Not a billable meter; provided\n      for capacity tracking and rate-limit insight.\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Veeva exposes per-tenant API call telemetry through Admin > Settings > Logs > API Usage\n      Logs and rate-limit response headers;\
  \ cost telemetry is invoice-level only.\n  - name: Allocation\n    description: Allocation is contract-level (per Vault / CRM tenant); internal chargeback rides on\n      seat / module / data-volume scoping in the order form.\n  - name: Optimization\n    description: 'Optimization levers are scope-driven: which Vaults are licensed, seat counts, and integration\n      patterns (batch vs interactive). Renewal is the primary optimization checkpoint.'\n  - name: Accountability\n    description: Accountability sits with the platform owner team that holds the Veeva tenant agreement;\n      finance owns the annual subscription line.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veeva/refs/heads/main/finops/veeva-finops.yml
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
