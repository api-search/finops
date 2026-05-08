---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fiserv-commercehub-openapi.yml
  format: yaml
  label: Fiserv CommerceHub API
  slug: commercehub
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fiserv/refs/heads/main/openapi/fiserv-commercehub-openapi.yml
- filename: fiserv-cardpointe-gateway-openapi.yml
  format: yaml
  label: Fiserv CardPointe Gateway API
  slug: cardpointe-gateway
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fiserv/refs/heads/main/openapi/fiserv-cardpointe-gateway-openapi.yml
- filename: fiserv-bankinghub-openapi.yml
  format: yaml
  label: Fiserv BankingHub API
  slug: bankinghub
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fiserv/refs/heads/main/openapi/fiserv-bankinghub-openapi.yml
- filename: fiserv-carddeveloper-openapi.yml
  format: yaml
  label: Fiserv CardDeveloper API
  slug: carddeveloper
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fiserv/refs/heads/main/openapi/fiserv-carddeveloper-openapi.yml
- filename: fiserv-payment-events-asyncapi.yml
  format: yaml
  label: Fiserv Payment Events
  slug: payment-events
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/fiserv/refs/heads/main/asyncapi/fiserv-payment-events-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom B2B Contract
description: FOCUS-aligned FinOps for Fiserv.
focus_columns:
  BillingCurrency: USD
  ProviderName: Fiserv
  PublisherName: Fiserv
  ServiceCategory: Payment Processing
  ServiceName: Fiserv
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
name: Fiserv Finops
provider_name: Fiserv
provider_slug: fiserv
publisher_name: Fiserv
service_category: Payment Processing
slug: fiserv-finops
source_filename: fiserv-finops.yml
source_heading: FinOps Profile
source_url: https://developer.fiserv.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Fiserv\nproviderId: fiserv\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Payment Processing\ndescription: FOCUS-aligned FinOps for Fiserv.\nsources:\n  - https://developer.fiserv.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Fiserv\nserviceCategory: Payment Processing\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Fiserv\n  ServiceCategory: Payment Processing\n  ProviderName: Fiserv\n  PublisherName: Fiserv\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n \
  \     - product\n  - name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Fiserv consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fiserv/refs/heads/main/finops/fiserv-finops.yml
sources:
- https://developer.fiserv.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Payment Processing
---
