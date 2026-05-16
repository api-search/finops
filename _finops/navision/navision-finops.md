---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nav-webservices.yaml
  format: yaml
  label: Dynamics NAV Web Services API
  slug: dynamics-nav-web-services-api
  spec_type: OpenAPI
  url: https://example.com/openapi/nav-webservices.yaml
- filename: nav-odata.yaml
  format: yaml
  label: Dynamics NAV OData API
  slug: dynamics-nav-odata-api
  spec_type: OpenAPI
  url: https://example.com/openapi/nav-odata.yaml
- filename: business-central-api-v2.yml
  format: yaml
  label: Business Central API v2.0
  slug: business-central-api-v20
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/navision/refs/heads/main/openapi/business-central-api-v2.yml
- filename: admin-center-api.yml
  format: yaml
  label: Business Central Administration Center API
  slug: business-central-administration-center-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/navision/refs/heads/main/openapi/admin-center-api.yml
- filename: automation-api.yml
  format: yaml
  label: Business Central Automation API
  slug: business-central-automation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/navision/refs/heads/main/openapi/automation-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Microsoft Dynamics NAV / Dynamics 365 Business Central: per-seat subscription billing across Essentials, Premium, and Team Members SKUs with annual commitment, plus metered Microsoft Copilot Credits.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Subscription
  PricingUnit: seat-month
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: ERP
  ServiceName: Microsoft Dynamics 365 Business Central
  ServiceSubcategory: Business Management
layout: finops
meters:
- aggregation: sum
  description: Number of Essentials full-user seats licensed.
  dimensions:
  - tenant
  - environment
  name: essentials_seats
  unit: seat-month
- aggregation: sum
  description: Number of Premium full-user seats licensed.
  dimensions:
  - tenant
  - environment
  name: premium_seats
  unit: seat-month
- aggregation: sum
  description: Number of limited-access Team Members seats licensed.
  dimensions:
  - tenant
  - environment
  name: team_member_seats
  unit: seat-month
- aggregation: sum
  description: Microsoft Copilot Credits consumed by AI agents inside Business Central.
  dimensions:
  - tenant
  - agent
  name: copilot_credits
  unit: credit
- aggregation: avg
  description: Provisioned production and sandbox environments per tenant.
  dimensions:
  - tenant
  - type
  name: environments
  unit: environment-month
- aggregation: avg
  description: Compressed environment database storage (cap 3 TB per environment).
  dimensions:
  - tenant
  - environment
  name: storage
  unit: GB-month
name: Navision Finops
provider_name: Microsoft Dynamics NAV
provider_slug: navision
publisher_name: Microsoft Corporation
service_category: ERP
slug: navision-finops
source_filename: navision-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/dynamics-365/products/business-central/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Dynamics NAV\nproviderId: navision\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - ERP\n  - Microsoft\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Microsoft Dynamics NAV / Dynamics 365 Business Central: per-seat\n  subscription billing across Essentials, Premium, and Team Members SKUs with annual commitment, plus\n  metered Microsoft Copilot Credits.'\nsources:\n  - https://www.microsoft.com/en-us/dynamics-365/products/business-central/pricing\n  - https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/operational-limits-online\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Microsoft Corporation\nserviceCategory: ERP\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Microsoft Dynamics 365 Business Central\n  ServiceCategory: ERP\n  ServiceSubcategory: Business Management\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  PricingCategory: Subscription\n  PricingUnit: seat-month\nmeters:\n  - name: essentials_seats\n    description: Number of Essentials full-user seats licensed.\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - environment\n  - name: premium_seats\n    description: Number of Premium full-user seats licensed.\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - environment\n  - name: team_member_seats\n    description:\
  \ Number of limited-access Team Members seats licensed.\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - environment\n  - name: copilot_credits\n    description: Microsoft Copilot Credits consumed by AI agents inside Business Central.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - tenant\n      - agent\n  - name: environments\n    description: Provisioned production and sandbox environments per tenant.\n    unit: environment-month\n    aggregation: avg\n    dimensions:\n      - tenant\n      - type\n  - name: storage\n    description: Compressed environment database storage (cap 3 TB per environment).\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - tenant\n      - environment\nprinciples:\n  - name: Visibility\n    description: Use the Microsoft 365 admin center, Dynamics 365 admin center, and the Business Central\n      Telemetry data in Application Insights to attribute seat consumption, environment counts, and\
  \ Copilot\n      Credit burn.\n  - name: Allocation\n    description: Map seat assignments and environments to cost centers via Microsoft Entra (Azure AD)\n      groups and license assignment policies; tag custom AL extensions and integrations by department.\n  - name: Optimization\n    description: Right-size SKU mix — use Team Members ($8) for read/approval-only users instead of full\n      Essentials/Premium seats; consolidate environments where possible; meter Copilot adoption before\n      committing credit packs; spread API load across multiple users to avoid throttling-driven retries.\n  - name: Accountability\n    description: Tie annual seat commitments to department headcount forecasts; set Copilot Credit budget\n      alerts; review unused seats quarterly; review API throttling telemetry to ensure integrations stay\n      within per-user limits.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/navision/refs/heads/main/finops/navision-finops.yml
sources:
- https://www.microsoft.com/en-us/dynamics-365/products/business-central/pricing
- https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/operational-limits-online
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- ERP
- Microsoft
- Cost Management
---
