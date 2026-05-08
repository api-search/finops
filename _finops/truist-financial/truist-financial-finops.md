---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: truist-personal-small-business-accounts-openapi.yml
  format: yaml
  label: Truist Personal and Small Business Accounts API
  slug: truist-personal-small-business-accounts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/truist-financial/refs/heads/main/openapi/truist-personal-small-business-accounts-openapi.yml
- filename: truist-personal-small-business-transactions-openapi.yml
  format: yaml
  label: Truist Personal and Small Business Transactions API
  slug: truist-personal-small-business-transactions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/truist-financial/refs/heads/main/openapi/truist-personal-small-business-transactions-openapi.yml
- filename: truist-commercial-accounts-openapi.yml
  format: yaml
  label: Truist Commercial Accounts API
  slug: truist-commercial-accounts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/truist-financial/refs/heads/main/openapi/truist-commercial-accounts-openapi.yml
- filename: truist-commercial-account-transactions-openapi.yml
  format: yaml
  label: Truist Commercial Account Transactions API
  slug: truist-commercial-account-transactions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/truist-financial/refs/heads/main/openapi/truist-commercial-account-transactions-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom B2B Contract
description: FOCUS-aligned FinOps for Truist Financial.
focus_columns:
  BillingCurrency: USD
  ProviderName: Truist Financial
  PublisherName: Truist Financial
  ServiceCategory: Banking
  ServiceName: Truist Financial
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  name: transactions
  unit: transaction
- aggregation: sum
  name: api_calls
  unit: call
- aggregation: max
  name: annual_contract
  unit: year
name: Truist Financial Finops
provider_name: Truist Financial
provider_slug: truist-financial
publisher_name: Truist Financial
service_category: Banking
slug: truist-financial-finops
source_filename: truist-financial-finops.yml
source_heading: FinOps Profile
source_url: https://www.truist.com/business/treasury-management
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Truist Financial\nproviderId: truist-financial\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Banking\ndescription: FOCUS-aligned FinOps for Truist Financial.\nsources:\n  - https://www.truist.com/business/treasury-management\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Truist Financial\nserviceCategory: Banking\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Truist Financial\n  ServiceCategory: Banking\n  ProviderName: Truist Financial\n  PublisherName: Truist Financial\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n    unit:\
  \ transaction\n    aggregation: sum\n    dimensions:\n      - product\n  - name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Truist Financial consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/truist-financial/refs/heads/main/finops/truist-financial-finops.yml
sources:
- https://www.truist.com/business/treasury-management
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking
---
