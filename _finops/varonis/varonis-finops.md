---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: varonis-datalert-openapi.yml
  format: yaml
  label: Varonis DatAlert API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/varonis/refs/heads/main/openapi/varonis-datalert-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps stub for Varonis: enterprise platform subscription with no public pricing, no published meters, and no public usage/billing API. Customers receive an annual platform invoice negotiated through sales.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Varonis Systems, Inc.
  ProviderName: Varonis
  PublisherName: Varonis Systems, Inc.
  ServiceCategory: Data Security
  ServiceName: Varonis Data Security Platform
layout: finops
meters:
- aggregation: sum
  description: Annual platform subscription line; sub-meters not publicly documented.
  name: platform_subscription
  unit: varies
name: Varonis Finops
provider_name: Varonis
provider_slug: varonis
publisher_name: Varonis Systems, Inc.
service_category: Data Security
slug: varonis-finops
source_filename: varonis-finops.yml
source_heading: FinOps Profile
source_url: https://www.varonis.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Varonis\nproviderId: varonis\npublisherName: Varonis Systems, Inc.\nserviceCategory: Data Security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Data Security\n  - Cloud Security\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps stub for Varonis: enterprise platform subscription with no public pricing,\n  no published meters, and no public usage/billing API. Customers receive an annual platform invoice negotiated\n  through sales.'\nsources:\n  - https://www.varonis.com/pricing\nnotes: No public pricing or billing API. FinOps shape inferred from the enterprise subscription model;\n  meters are not invented.\
  \ Reconciliation pending customer-portal access.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Varonis Data Security Platform\n  ServiceCategory: Data Security\n  ProviderName: Varonis\n  PublisherName: Varonis Systems, Inc.\n  InvoiceIssuerName: Varonis Systems, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: platform_subscription\n    description: Annual platform subscription line; sub-meters not publicly documented.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Varonis exposes consumption inside the platform UI (events, alerts, classification scans)\n      but does not publish a customer-facing usage/cost API. Track license utilization via the customer\n      success engagement.\n  - name: Allocation\n    description: Allocation is contract-level. Internal chargeback typically rides on data-source coverage\n      (file\
  \ shares, M365 tenants, IaaS accounts) negotiated in the order form.\n  - name: Optimization\n    description: Optimization levers are scope-driven (which data sources / modules are licensed) rather\n      than usage-rate. Renewal time is the primary optimization checkpoint.\n  - name: Accountability\n    description: Accountability sits with the security team that owns the Varonis tenant; finance owns\n      the annual subscription line.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/varonis/refs/heads/main/finops/varonis-finops.yml
sources:
- https://www.varonis.com/pricing
specification: FinOps Framework
tags:
- Data Security
- Cloud Security
- FinOps
- FOCUS
---
