---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ryder-fleet-management-api-openapi.yml
  format: yaml
  label: Ryder Fleet Management API
  slug: fleet-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ryder-system/refs/heads/main/openapi/ryder-fleet-management-api-openapi.yml
- filename: ryder-carrier-api-openapi.yml
  format: yaml
  label: Ryder Carrier API
  slug: carrier-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ryder-system/refs/heads/main/openapi/ryder-carrier-api-openapi.yml
- filename: ryder-tm-shipment-api-openapi.yml
  format: yaml
  label: Ryder TM Shipment Management API
  slug: tm-shipment-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ryder-system/refs/heads/main/openapi/ryder-tm-shipment-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom B2B Contract
description: FOCUS-aligned FinOps for Ryder System.
focus_columns:
  BillingCurrency: USD
  ProviderName: Ryder System
  PublisherName: Ryder System
  ServiceCategory: Logistics / Fleet Management
  ServiceName: Ryder System
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
name: Ryder System Finops
provider_name: Ryder System
provider_slug: ryder-system
publisher_name: Ryder System
service_category: Logistics / Fleet Management
slug: ryder-system-finops
source_filename: ryder-system-finops.yml
source_heading: FinOps Profile
source_url: https://ryder.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ryder System\nproviderId: ryder-system\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Logistics / Fleet Management\ndescription: FOCUS-aligned FinOps for Ryder System.\nsources:\n  - https://ryder.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Ryder System\nserviceCategory: Logistics / Fleet Management\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Ryder System\n  ServiceCategory: Logistics / Fleet Management\n  ProviderName: Ryder System\n  PublisherName: Ryder System\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n  \
  \  unit: transaction\n    aggregation: sum\n    dimensions:\n      - product\n  - name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Ryder System consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ryder-system/refs/heads/main/finops/ryder-system-finops.yml
sources:
- https://ryder.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Logistics / Fleet Management
---
