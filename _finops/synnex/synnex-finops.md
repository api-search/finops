---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: synnex-streamone-ion-openapi.yml
  format: yaml
  label: TD SYNNEX StreamOne ION API
  slug: streamone-ion
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/synnex/refs/heads/main/openapi/synnex-streamone-ion-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies by region)
  billingFrequency: Per-Order / Subscription Settlement
  chargeCategories:
  - Purchase
  - Adjustment
  - Refund
  pricingCategory: Reseller Pass-Through
description: TD SYNNEX's APIs (StreamOne ION, Digital Bridge) drive reseller order, subscription, and entitlement workflows; settlement happens through the distribution agreement (cost-plus on resold cloud and IT product), not as a per-API charge.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: TD SYNNEX Corporation
  ProviderName: TD SYNNEX
  PublisherName: TD SYNNEX Corporation
  ServiceCategory: IT Distribution / Cloud Marketplace
  ServiceName: TD SYNNEX APIs (StreamOne ION, Digital Bridge)
layout: finops
meters:
- aggregation: max
  description: Active resold cloud subscriptions managed via StreamOne ION (CSP seats, Google Workspace seats, etc.).
  dimensions:
  - vendor
  - end_customer
  name: cloud_subscriptions
  unit: subscription-month
- aggregation: sum
  description: Orders placed through the API (StreamOne ION orders, Digital Bridge product orders).
  dimensions:
  - vendor
  - end_customer
  name: orders
  unit: order
- aggregation: sum
  description: Product / pricing lookup calls; not separately billed but useful for capacity planning.
  name: catalog_lookups
  unit: request
name: Synnex Finops
provider_name: Synnex
provider_slug: synnex
publisher_name: TD SYNNEX Corporation
service_category: IT Distribution / Cloud Marketplace
slug: synnex-finops
source_filename: synnex-finops.yml
source_heading: FinOps Profile
source_url: https://www.tdsynnex.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Synnex\nproviderId: synnex\npublisherName: TD SYNNEX Corporation\nserviceCategory: IT Distribution / Cloud Marketplace\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - IT Distribution\n  - Cloud Marketplace\n  - FinOps\n  - FOCUS\ndescription: TD SYNNEX's APIs (StreamOne ION, Digital Bridge) drive reseller order, subscription, and entitlement workflows; settlement happens through the distribution agreement (cost-plus on resold cloud and IT product), not as a per-API charge.\nsources:\n  - https://www.tdsynnex.com\n  - https://docs.streamone.cloud/\nnotes: No FOCUS-aligned per-call billing surface. Cost / margin reconciles\
  \ at the resold-product level (Microsoft CSP, Google Workspace, hardware SKUs) through TD SYNNEX's reseller settlement.\nbillingModel:\n  pricingCategory: Reseller Pass-Through\n  billingFrequency: Per-Order / Subscription Settlement\n  billingCurrency: 'USD (settlement varies by region)'\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: TD SYNNEX APIs (StreamOne ION, Digital Bridge)\n  ServiceCategory: IT Distribution / Cloud Marketplace\n  ProviderName: TD SYNNEX\n  PublisherName: TD SYNNEX Corporation\n  InvoiceIssuerName: TD SYNNEX Corporation\n  BillingCurrency: USD\nmeters:\n  - name: cloud_subscriptions\n    description: Active resold cloud subscriptions managed via StreamOne ION (CSP seats, Google Workspace seats, etc.).\n    unit: subscription-month\n    aggregation: max\n    dimensions:\n      - vendor\n      - end_customer\n  - name: orders\n    description: Orders placed through the API (StreamOne ION orders, Digital Bridge\
  \ product orders).\n    unit: order\n    aggregation: sum\n    dimensions:\n      - vendor\n      - end_customer\n  - name: catalog_lookups\n    description: Product / pricing lookup calls; not separately billed but useful for capacity planning.\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Resellers reconcile API-driven activity against TD SYNNEX reseller reporting; subscription, order, and renewal data are exposed through the partner reporting endpoints.\n  - name: Allocation\n    description: Allocate by end-customer and vendor (Microsoft, Google, hardware OEM) - the same dimensions TD SYNNEX uses on the reseller statement.\n  - name: Optimization\n    description: Optimize by automating renewal and cancellation flows, batching catalog syncs, and using StreamOne ION reports to surface dormant subscriptions before settlement.\n  - name: Accountability\n    description: Reseller's commercial team owns end-customer P&L; TD SYNNEX partner-management\
  \ owns the distribution-agreement relationship and settlement timing.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/synnex/refs/heads/main/finops/synnex-finops.yml
sources:
- https://www.tdsynnex.com
- https://docs.streamone.cloud/
specification: FinOps Framework
tags:
- IT Distribution
- Cloud Marketplace
- FinOps
- FOCUS
---
