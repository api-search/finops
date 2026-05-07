---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: expedia-rapid-openapi-original.yml
  format: yaml
  label: Expedia Rapid API
  slug: rapid
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/expedia-group/refs/heads/main/openapi/expedia-rapid-openapi-original.yml
- filename: expedia-fraud-protection-openapi-original.yml
  format: yaml
  label: Expedia Fraud Protection API
  slug: fraud-protection
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/expedia-group/refs/heads/main/openapi/expedia-fraud-protection-openapi-original.yml
- filename: expedia-lodging-product-openapi-original.yml
  format: yaml
  label: Expedia Lodging API
  slug: lodging
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/expedia-group/refs/heads/main/openapi/expedia-lodging-product-openapi-original.yml
- filename: expedia-deposit-openapi-original.yml
  format: yaml
  label: Expedia EPS Deposit API
  slug: deposit
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/expedia-group/refs/heads/main/openapi/expedia-deposit-openapi-original.yml
- filename: expedia-loyalty-openapi-original.yml
  format: yaml
  label: Expedia Loyalty Earn API
  slug: loyalty
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/expedia-group/refs/heads/main/openapi/expedia-loyalty-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom B2B Contract
description: FOCUS-aligned FinOps for Expedia Group.
focus_columns:
  BillingCurrency: USD
  ProviderName: Expedia Group
  PublisherName: Expedia Group
  ServiceCategory: Travel / Hospitality
  ServiceName: Expedia Group
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
name: Expedia Group Finops
provider_name: Expedia Group
provider_slug: expedia-group
publisher_name: Expedia Group
service_category: Travel / Hospitality
slug: expedia-group-finops
source_filename: expedia-group-finops.yml
source_heading: FinOps Profile
source_url: https://developers.expediagroup.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Expedia Group\nproviderId: expedia-group\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Travel / Hospitality\ndescription: FOCUS-aligned FinOps for Expedia Group.\nsources:\n  - https://developers.expediagroup.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Expedia Group\nserviceCategory: Travel / Hospitality\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Expedia Group\n  ServiceCategory: Travel / Hospitality\n  ProviderName: Expedia Group\n  PublisherName: Expedia Group\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n \
  \   unit: transaction\n    aggregation: sum\n    dimensions:\n      - product\n  - name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Expedia Group consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/expedia-group/refs/heads/main/finops/expedia-group-finops.yml
sources:
- https://developers.expediagroup.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Travel / Hospitality
---
