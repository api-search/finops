---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: atandt-wireless-apis.yaml
  format: yaml
  label: AT&T Wireless APIs
  slug: att-wireless-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/atandt/refs/heads/main/openapi/atandt-wireless-apis.yaml
- filename: atandt-network-apis.yaml
  format: yaml
  label: AT&T 5G Network APIs
  slug: att-network-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/atandt/refs/heads/main/openapi/atandt-network-apis.yaml
- filename: atandt-enterprise-connectivity-apis.yaml
  format: yaml
  label: AT&T Enterprise Connectivity APIs
  slug: att-enterprise-connectivity-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/atandt/refs/heads/main/openapi/atandt-enterprise-connectivity-apis.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom B2B Contract
description: FOCUS-aligned FinOps for AT&T.
focus_columns:
  BillingCurrency: USD
  ProviderName: AT&T
  PublisherName: AT&T
  ServiceCategory: Telecommunications
  ServiceName: AT&T
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
name: Atandt Finops
provider_name: AT&T
provider_slug: atandt
publisher_name: AT&T
service_category: Telecommunications
slug: atandt-finops
source_filename: atandt-finops.yml
source_heading: FinOps Profile
source_url: https://developer.att.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AT&T\nproviderId: atandt\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Telecommunications\ndescription: FOCUS-aligned FinOps for AT&T.\nsources:\n  - https://developer.att.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: AT&T\nserviceCategory: Telecommunications\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: AT&T\n  ServiceCategory: Telecommunications\n  ProviderName: AT&T\n  PublisherName: AT&T\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - product\n\
  \  - name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track AT&T consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/atandt/refs/heads/main/finops/atandt-finops.yml
sources:
- https://developer.att.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Telecommunications
---
