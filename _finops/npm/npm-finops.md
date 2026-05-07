---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: npm-registry-api-openapi.yml
  format: yaml
  label: npm Registry API
  slug: registry
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/npm/refs/heads/main/openapi/npm-registry-api-openapi.yml
- filename: npm-public-api-openapi.yml
  format: yaml
  label: npm Public API
  slug: public
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/npm/refs/heads/main/openapi/npm-public-api-openapi.yml
- filename: npm-hooks-api-openapi.yml
  format: yaml
  label: npm Hooks API
  slug: hooks
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/npm/refs/heads/main/openapi/npm-hooks-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Subscription + Usage
description: 'FOCUS-aligned FinOps for npm: the public registry is free; commercial spend is on GitHub seats and Packages storage/egress, billed per user per month with usage overages.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: GitHub, Inc.
  PricingCategory: Subscription + Usage
  PricingUnit: seat
  ProviderName: npm
  PublisherName: GitHub, Inc.
  ServiceCategory: Developer Tools / Package Registry
  ServiceName: npm
layout: finops
meters:
- aggregation: sum
  description: Per-user GitHub plan seat (Team or Enterprise) granting private npm package access
  dimensions:
  - plan
  - org
  name: github_seats
  unit: seat
- aggregation: avg
  description: GitHub Packages storage consumed by private npm packages
  dimensions:
  - org
  - visibility
  name: packages_storage
  unit: GB-month
- aggregation: sum
  description: Outbound data transfer from the GitHub Packages registry
  dimensions:
  - org
  name: packages_data_transfer
  unit: GB
- aggregation: sum
  description: GitHub Actions minutes consumed by npm publish/CI workflows
  dimensions:
  - runner_os
  - org
  name: actions_minutes
  unit: minute
name: Npm Finops
provider_name: npm
provider_slug: npm
publisher_name: GitHub, Inc.
service_category: Developer Tools / Package Registry
slug: npm-finops
source_filename: npm-finops.yml
source_heading: FinOps Profile
source_url: https://github.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: npm\nproviderId: npm\npublisherName: GitHub, Inc.\nserviceCategory: Developer Tools / Package Registry\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Packages\n  - JavaScript\n  - Node.js\n  - Package Management\n  - Registry\n  - Security\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for npm: the public registry is free; commercial spend is on GitHub\n  seats and Packages storage/egress, billed per user per month with usage overages.'\nsources:\n  - https://github.com/pricing\n  - https://docs.github.com/en/billing\n  - https://www.npmjs.com/products\nprinciples:\n  - name: Visibility\n\
  \    description: Use the GitHub billing dashboard and Billing Platform API to see per-org Packages storage,\n      data transfer, and Actions minutes. Public registry consumption is free and not metered.\n  - name: Allocation\n    description: Tag spend by GitHub organization and team; private npm packages roll up under the publishing\n      org's GitHub Packages line items.\n  - name: Optimization\n    description: Use the public npm registry for OSS dependencies (zero cost). Mirror or proxy via Verdaccio/JFrog\n      for high-volume bulk reads. Use replicate.npmjs.com instead of scraping for indexing workloads.\n  - name: Accountability\n    description: Org admins manage seats and Packages overage policies. Set Actions/Packages spending\n      limits and alerts in GitHub billing settings; reconcile monthly invoices against per-team chargeback.\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n\
  \    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: npm\n  ServiceCategory: Developer Tools / Package Registry\n  ProviderName: npm\n  PublisherName: GitHub, Inc.\n  InvoiceIssuerName: GitHub, Inc.\n  PricingCategory: Subscription + Usage\n  PricingUnit: seat\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: github_seats\n    description: Per-user GitHub plan seat (Team or Enterprise) granting private npm package access\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - plan\n      - org\n  - name: packages_storage\n    description: GitHub Packages storage consumed by private npm packages\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - org\n      - visibility\n  - name: packages_data_transfer\n    description: Outbound data transfer from the GitHub Packages registry\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - org\n  - name: actions_minutes\n    description:\
  \ GitHub Actions minutes consumed by npm publish/CI workflows\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - runner_os\n      - org\napis:\n  - name: npm Registry API\n    baseURL: https://registry.npmjs.org\n    tags:\n      - Packages\n      - JavaScript\n      - Registry\n      - Package Management\n      - Node.js\n    serviceName: npm Registry API\n    serviceCategory: Package Registry\n  - name: npm Public API\n    baseURL: https://npm.pkg.github.com\n    tags:\n      - Packages\n      - Tokens\n      - Authentication\n    serviceName: GitHub Packages npm\n    serviceCategory: Package Registry\n  - name: npm Hooks API\n    baseURL: ''\n    tags:\n      - Webhooks\n      - Notifications\n      - Events\n    serviceName: npm Hooks API\n    serviceCategory: Package Registry\n  - name: npm CLI\n    baseURL: ''\n    tags:\n      - Command Line\n      - Package Management\n    serviceName: npm CLI\n    serviceCategory: Package Registry\n  - name: npm Provenance\n   \
  \ baseURL: ''\n    tags:\n      - Security\n      - Supply Chain\n      - Sigstore\n    serviceName: npm Provenance\n    serviceCategory: Package Registry\nunitEconomics:\n  - name: Cost per private package GB-month\n    metric: packages_storage_cost / packages_storage_GB\n    target: minimize via cleanup of stale package versions\n  - name: Cost per developer-month\n    metric: github_seat_cost + packages_overage / active_developers\n    target: monitor against GitHub Team baseline\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/npm/refs/heads/main/finops/npm-finops.yml
sources:
- https://github.com/pricing
- https://docs.github.com/en/billing
- https://www.npmjs.com/products
specification: FinOps Framework
tags:
- Packages
- JavaScript
- Node.js
- Package Management
- Registry
- Security
- FinOps
- Cost Management
- FOCUS
---
