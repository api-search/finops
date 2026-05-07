---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fabric-openapi-original.yml
  format: yaml
  label: Equinix Fabric API
  slug: fabric
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/equinix/refs/heads/main/openapi/fabric-openapi-original.yml
- filename: metal-openapi-original.yml
  format: yaml
  label: Equinix Metal API
  slug: metal
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/equinix/refs/heads/main/openapi/metal-openapi-original.yml
- filename: eia-openapi-original.yml
  format: yaml
  label: Equinix Internet Access API
  slug: internet-access
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/equinix/refs/heads/main/openapi/eia-openapi-original.yml
- filename: lookup-openapi-original.yml
  format: yaml
  label: Equinix Lookup API
  slug: lookup
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/equinix/refs/heads/main/openapi/lookup-openapi-original.yml
- filename: orders-openapi-original.yml
  format: yaml
  label: Equinix Orders API
  slug: orders
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/equinix/refs/heads/main/openapi/orders-openapi-original.yml
- filename: orderhistory-openapi-original.yml
  format: yaml
  label: Equinix Order History API
  slug: order-history
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/equinix/refs/heads/main/openapi/orderhistory-openapi-original.yml
- filename: securecabinet-openapi-original.yml
  format: yaml
  label: Equinix Secure Cabinet API
  slug: secure-cabinet
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/equinix/refs/heads/main/openapi/securecabinet-openapi-original.yml
- filename: smarthands-openapi-original.yml
  format: yaml
  label: Equinix Smart Hands API
  slug: smart-hands
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/equinix/refs/heads/main/openapi/smarthands-openapi-original.yml
- filename: accesstoken-openapi-original.yml
  format: yaml
  label: Equinix API Authentication
  slug: access-token
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/equinix/refs/heads/main/openapi/accesstoken-openapi-original.yml
- filename: sts-openapi-original.yml
  format: yaml
  label: Equinix Security Token Service
  slug: sts
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/equinix/refs/heads/main/openapi/sts-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom B2B Contract
description: FOCUS-aligned FinOps for Equinix.
focus_columns:
  BillingCurrency: USD
  ProviderName: Equinix
  PublisherName: Equinix
  ServiceCategory: Data Center / Interconnect
  ServiceName: Equinix
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
name: Equinix Finops
provider_name: Equinix
provider_slug: equinix
publisher_name: Equinix
service_category: Data Center / Interconnect
slug: equinix-finops
source_filename: equinix-finops.yml
source_heading: FinOps Profile
source_url: https://developer.equinix.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Equinix\nproviderId: equinix\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Data Center / Interconnect\ndescription: FOCUS-aligned FinOps for Equinix.\nsources:\n  - https://developer.equinix.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Equinix\nserviceCategory: Data Center / Interconnect\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Equinix\n  ServiceCategory: Data Center / Interconnect\n  ProviderName: Equinix\n  PublisherName: Equinix\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n    unit: transaction\n    aggregation:\
  \ sum\n    dimensions:\n      - product\n  - name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Equinix consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/equinix/refs/heads/main/finops/equinix-finops.yml
sources:
- https://developer.equinix.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Data Center / Interconnect
---
