---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: xero-accounting-openapi.yml
  format: yaml
  label: Xero Accounting API
  slug: xero-accounting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xero/refs/heads/main/openapi/xero-accounting-openapi.yml
- filename: xero-assets-openapi.yml
  format: yaml
  label: Xero Assets API
  slug: xero-assets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xero/refs/heads/main/openapi/xero-assets-openapi.yml
- filename: xero-bankfeeds-openapi.yml
  format: yaml
  label: Xero Bank Feeds API
  slug: xero-bank-feeds-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xero/refs/heads/main/openapi/xero-bankfeeds-openapi.yml
- filename: xero-finance-openapi.yml
  format: yaml
  label: Xero Finance API
  slug: xero-finance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xero/refs/heads/main/openapi/xero-finance-openapi.yml
- filename: xero-identity-openapi.yml
  format: yaml
  label: Xero Identity API
  slug: xero-identity-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xero/refs/heads/main/openapi/xero-identity-openapi.yml
- filename: xero-payroll-au-openapi.yml
  format: yaml
  label: Xero Payroll Australia API
  slug: xero-payroll-australia-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xero/refs/heads/main/openapi/xero-payroll-au-openapi.yml
- filename: xero-payroll-nz-openapi.yml
  format: yaml
  label: Xero Payroll New Zealand API
  slug: xero-payroll-new-zealand-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xero/refs/heads/main/openapi/xero-payroll-nz-openapi.yml
- filename: xero-payroll-uk-openapi.yml
  format: yaml
  label: Xero Payroll United Kingdom API
  slug: xero-payroll-united-kingdom-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xero/refs/heads/main/openapi/xero-payroll-uk-openapi.yml
- filename: xero-projects-openapi.yml
  format: yaml
  label: Xero Projects API
  slug: xero-projects-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xero/refs/heads/main/openapi/xero-projects-openapi.yml
- filename: xero-files-openapi.yml
  format: yaml
  label: Xero Files API
  slug: xero-files-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xero/refs/heads/main/openapi/xero-files-openapi.yml
billing_model:
  billingCurrency: USD/EUR/GBP/AUD/NZD/CAD (region-specific)
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Xero: per-organisation tiered SaaS subscription with no per-API meter; spend is driven by organisation count and plan tier per region.'
focus_columns:
  BillingCurrency: USD/EUR/GBP/AUD/NZD/CAD
  InvoiceIssuerName: Xero Limited
  ProviderName: Xero
  PublisherName: Xero Limited
  ServiceCategory: Accounting / SMB SaaS
  ServiceName: Xero
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - plan
  - organisation
  name: organisation_subscription
  unit: month
- aggregation: max
  dimensions:
  - region
  - organisation
  name: payroll_employees
  unit: employee
name: Xero Finops
provider_name: Xero
provider_slug: xero
publisher_name: Xero Limited
service_category: Accounting / SMB SaaS
slug: xero-finops
source_filename: xero-finops.yml
source_heading: FinOps Profile
source_url: https://www.xero.com/us/pricing-plans/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Xero\nproviderId: xero\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Accounting\n  - Finance\n  - SaaS\ndescription: 'FOCUS-aligned FinOps for Xero: per-organisation tiered SaaS subscription with no\n  per-API meter; spend is driven by organisation count and plan tier per region.'\nsources:\n  - https://www.xero.com/us/pricing-plans/\n  - https://developer.xero.com/\nnotes: Pricing pages were unreachable (503/timeout) during reconciliation; tier names and\n  prices have not been refreshed. Meters reflect the per-organisation subscription billing\n  surface rather than per-API usage.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Xero Limited\nserviceCategory: Accounting / SMB SaaS\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD/EUR/GBP/AUD/NZD/CAD (region-specific)\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Xero\n  ServiceCategory: Accounting / SMB SaaS\n  ProviderName: Xero\n  PublisherName: Xero Limited\n  InvoiceIssuerName: Xero Limited\n  BillingCurrency: USD/EUR/GBP/AUD/NZD/CAD\nmeters:\n  - name: organisation_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - region\n      - plan\n      - organisation\n  - name: payroll_employees\n    unit: employee\n    aggregation: max\n    dimensions:\n      - region\n      - organisation\nprinciples:\n  - name: Visibility\n    description: Spend is visible per organisation in the Xero account billing area; API\n      consumption itself is not metered or billed, so no separate FOCUS export exists for API\n      usage.\n  - name: Allocation\n\
  \    description: Allocate by organisation and region; integration partners reselling Xero seats\n      typically allocate via their partner billing rather than direct Xero invoices.\n  - name: Optimization\n    description: Levers are right-sizing the organisation tier (e.g. dropping from Established\n      to Growing if features go unused), pruning inactive organisations, and consolidating\n      payroll subscriptions per region.\n  - name: Accountability\n    description: Finance owns the Xero subscription; integration teams own the OAuth app and\n      tenant authorisations that consume the API at no separate cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/xero/refs/heads/main/finops/xero-finops.yml
sources:
- https://www.xero.com/us/pricing-plans/
- https://developer.xero.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Accounting
- Finance
- SaaS
---
