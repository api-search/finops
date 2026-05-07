---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cyberark-conjur-openapi.yml
  format: yaml
  label: CyberArk Conjur Secrets Manager API
  slug: conjur
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cyberark/refs/heads/main/openapi/cyberark-conjur-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Enterprise Subscription
description: 'FOCUS-aligned FinOps for CyberArk: enterprise per-seat / per-machine-identity subscriptions across PAM, Workforce Access, Secrets Management, and Identity Governance. APIs are entitlements of the product license rather than separately metered.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: CyberArk Software Ltd.
  PricingCategory: Subscription
  PricingUnit: seat-year
  ProviderName: CyberArk
  PublisherName: CyberArk Software Ltd.
  ServiceCategory: Identity Security
  ServiceName: CyberArk
layout: finops
meters:
- aggregation: max
  description: Licensed privileged users / endpoints under PAM coverage
  dimensions:
  - product
  - business_unit
  name: privileged_users
  unit: seat-year
- aggregation: max
  description: Licensed workforce identity seats (SSO / MFA / passwordless)
  dimensions:
  - product
  - business_unit
  name: workforce_users
  unit: seat-year
- aggregation: max
  description: Licensed machine identities / secrets / certificates
  dimensions:
  - product
  - environment
  name: machine_identities
  unit: machine-year
- aggregation: sum
  description: API calls against CyberArk REST APIs (not separately billed; observed for capacity)
  dimensions:
  - api
  - tenant
  name: api_requests
  unit: request
name: Cyberark Finops
provider_name: CyberArk
provider_slug: cyberark
publisher_name: CyberArk Software Ltd.
service_category: Identity Security
slug: cyberark-finops
source_filename: cyberark-finops.yml
source_heading: FinOps Profile
source_url: https://www.cyberark.com/products/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CyberArk\nproviderId: cyberark\npublisherName: CyberArk Software Ltd.\nserviceCategory: Identity Security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Identity Security\n  - Privileged Access Management\n  - Secrets Management\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for CyberArk: enterprise per-seat / per-machine-identity subscriptions\n  across PAM, Workforce Access, Secrets Management, and Identity Governance. APIs are entitlements of\n  the product license rather than separately metered.'\nsources:\n  - https://www.cyberark.com/products/\nnotes: No public pricing. Replace meter targets with contract-derived\
  \ values (per-privileged-user, per-machine-identity,\n  per-workforce-user).\nprinciples:\n  - name: Visibility\n    description: Use CyberArk Identity Security Intelligence and the per-product admin consoles to count\n      privileged users, machine identities, and workforce seats; export to your CMDB / FinOps store.\n  - name: Allocation\n    description: Tag Safes (PAM), platforms, and Conjur policy branches by business unit / application\n      to attribute identity spend; use Identity Flows for joiner/mover/leaver attribution.\n  - name: Optimization\n    description: Decommission unused privileged / workforce seats at quarterly access reviews; consolidate\n      Conjur secrets across applications; right-size Privilege Cloud vs Self-Hosted PAM by deployment\n      density.\n  - name: Accountability\n    description: Identity / security org owns the CyberArk contract; coordinate with finance for chargeback\n      based on Safe ownership and identity governance rollups.\ndomains:\n\
  \  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Forecasting\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Enterprise Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CyberArk\n  ServiceCategory: Identity Security\n  ProviderName: CyberArk\n  PublisherName: CyberArk Software Ltd.\n  InvoiceIssuerName: CyberArk Software Ltd.\n  PricingCategory: Subscription\n  PricingUnit: seat-year\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name:\
  \ privileged_users\n    description: Licensed privileged users / endpoints under PAM coverage\n    unit: seat-year\n    aggregation: max\n    dimensions:\n      - product\n      - business_unit\n  - name: workforce_users\n    description: Licensed workforce identity seats (SSO / MFA / passwordless)\n    unit: seat-year\n    aggregation: max\n    dimensions:\n      - product\n      - business_unit\n  - name: machine_identities\n    description: Licensed machine identities / secrets / certificates\n    unit: machine-year\n    aggregation: max\n    dimensions:\n      - product\n      - environment\n  - name: api_requests\n    description: API calls against CyberArk REST APIs (not separately billed; observed for capacity)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - tenant\napis:\n  - name: CyberArk Conjur Secrets Manager API\n    baseURL: https://conjur.example.com\n    tags:\n      - Authentication\n      - Conjur\n      - DevOps Secrets\n      - Machine\
  \ Identity\n      - Policies\n      - Resources\n      - Roles\n      - Secrets\n      - Vault\n    serviceName: CyberArk Conjur Secrets Manager API\n    serviceCategory: API\n  - name: CyberArk PAM Self-Hosted REST API\n    baseURL: ''\n    tags:\n      - Accounts\n      - PAM\n      - Privileged Access\n      - REST\n      - Safes\n      - Sessions\n      - Vault\n    serviceName: CyberArk PAM Self-Hosted REST API\n    serviceCategory: API\n  - name: CyberArk Privilege Cloud REST API\n    baseURL: ''\n    tags:\n      - Accounts\n      - PAM\n      - Privilege Cloud\n      - Safes\n      - SaaS\n      - Vault\n    serviceName: CyberArk Privilege Cloud REST API\n    serviceCategory: API\n  - name: CyberArk Identity REST API\n    baseURL: ''\n    tags:\n      - Identity\n      - MFA\n      - OAuth2\n      - SCIM\n      - SSO\n      - Workforce Identity\n    serviceName: CyberArk Identity REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Privileged User\n    metric:\
  \ billed_cost / privileged_users\n    target: TBD\n  - name: Cost per Machine Identity\n    metric: billed_cost / machine_identities\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cyberark/refs/heads/main/finops/cyberark-finops.yml
sources:
- https://www.cyberark.com/products/
specification: FinOps Framework
tags:
- Identity Security
- Privileged Access Management
- Secrets Management
- FinOps
- FOCUS
---
