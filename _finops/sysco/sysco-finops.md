---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sysco-food-distribution-api-openapi.yml
  format: yaml
  label: Sysco Food Distribution API
  slug: food-distribution-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sysco/refs/heads/main/openapi/sysco-food-distribution-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  pricingCategory: Custom / Contact Sales
description: FinOps placeholder for Sysco. No public API billing surface; consumption costs are reflected on customer invoices for goods and services rather than as metered API line items.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Sysco Corporation
  ProviderName: Sysco
  PublisherName: Sysco Corporation
  ServiceCategory: Foodservice Distribution
  ServiceName: Sysco
layout: finops
meters:
- aggregation: sum
  name: custom_engagement
  unit: varies
name: Sysco Finops
provider_name: Sysco
provider_slug: sysco
publisher_name: Sysco Corporation
service_category: Foodservice Distribution
slug: sysco-finops
source_filename: sysco-finops.yml
source_heading: FinOps Profile
source_url: https://www.sysco.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Sysco\nproviderId: sysco\npublisherName: Sysco Corporation\nserviceCategory: Foodservice Distribution\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Foodservice\n  - Distribution\n  - FinOps\n  - FOCUS\ndescription: FinOps placeholder for Sysco. No public API billing surface; consumption costs are\n  reflected on customer invoices for goods and services rather than as metered API line items.\nsources:\n  - https://www.sysco.com/\nnotes: No public billing telemetry surface documented for API consumption. Meter list collapsed\n  to custom-engagement pending direct provider confirmation.\nbillingModel:\n  pricingCategory:\
  \ Custom / Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Sysco\n  ServiceCategory: Foodservice Distribution\n  ProviderName: Sysco\n  PublisherName: Sysco Corporation\n  InvoiceIssuerName: Sysco Corporation\n  BillingCurrency: USD\nmeters:\n  - name: custom_engagement\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Customer order and invoice visibility is delivered through Sysco Shop and the\n      customer's account team, not a public usage API.\n  - name: Allocation\n    description: Cost allocation is performed in the customer's own AP and procurement systems\n      against Sysco invoices.\n  - name: Optimization\n    description: Optimization is addressed through Sysco's account managers, contract pricing,\n      and order-pattern reviews.\n  - name: Accountability\n    description: Spend accountability sits with the customer's procurement or foodservice\
  \ operations\n      team holding the Sysco account.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sysco/refs/heads/main/finops/sysco-finops.yml
sources:
- https://www.sysco.com/
specification: FinOps Framework
tags:
- Foodservice
- Distribution
- FinOps
- FOCUS
---
