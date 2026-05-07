---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: blue-yonder-warehouse-management-openapi.yml
  format: yaml
  label: Blue Yonder Warehouse Management API
  slug: blue-yonder-warehouse-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/blue-yonder/refs/heads/main/openapi/blue-yonder-warehouse-management-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise Subscription (Negotiated)
description: 'FOCUS-aligned FinOps placeholder for Blue Yonder: enterprise supply-chain SaaS billed under a contract-negotiated annual subscription combined with module add-ons (WMS, TMS, OMS, Planning, Workforce) and Blue Yonder Network connectivity.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Blue Yonder Group, Inc.
  ProviderName: Blue Yonder
  PublisherName: Blue Yonder Group, Inc.
  ServiceCategory: Supply Chain SaaS
  ServiceName: Blue Yonder
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  - environment
  name: platform_subscription
  unit: year
- aggregation: sum
  dimensions:
  - module
  - tenant
  name: module_subscriptions
  unit: year
- aggregation: max
  dimensions:
  - tenant
  - role
  name: named_users
  unit: seat
- aggregation: sum
  dimensions:
  - partner
  - document_type
  name: network_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - module
  name: predictions_consumed
  unit: prediction
name: Blue Yonder Finops
provider_name: blue-yonder
provider_slug: blue-yonder
publisher_name: Blue Yonder Group, Inc.
service_category: Supply Chain SaaS
slug: blue-yonder-finops
source_filename: blue-yonder-finops.yml
source_heading: FinOps Profile
source_url: https://www.blueyonder.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Blue Yonder\nproviderId: blue-yonder\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Supply Chain\n  - SaaS\ndescription: 'FOCUS-aligned FinOps placeholder for Blue Yonder: enterprise supply-chain SaaS billed\n  under a contract-negotiated annual subscription combined with module add-ons (WMS, TMS, OMS,\n  Planning, Workforce) and Blue Yonder Network connectivity.'\nsources:\n  - https://www.blueyonder.com\nnotes: Blue Yonder commercial terms are private; reconcile against the active enterprise contract\n  for actual fee structure.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Blue Yonder Group, Inc.\nserviceCategory: Supply\
  \ Chain SaaS\nbillingModel:\n  pricingCategory: Enterprise Subscription (Negotiated)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Blue Yonder\n  ServiceCategory: Supply Chain SaaS\n  ProviderName: Blue Yonder\n  PublisherName: Blue Yonder Group, Inc.\n  InvoiceIssuerName: Blue Yonder Group, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: platform_subscription\n    unit: year\n    aggregation: sum\n    dimensions:\n      - tenant\n      - environment\n  - name: module_subscriptions\n    unit: year\n    aggregation: sum\n    dimensions:\n      - module\n      - tenant\n  - name: named_users\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tenant\n      - role\n  - name: network_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - partner\n      - document_type\n  - name: predictions_consumed\n    unit: prediction\n\
  \    aggregation: sum\n    dimensions:\n      - module\nprinciples:\n  - name: Visibility\n    description: Use Blue Yonder Platform tenant administration and customer-success usage reports\n      to track module activation, named-user counts, and Network transaction volume.\n  - name: Allocation\n    description: Map Blue Yonder modules and tenants to consuming business units (planning, retail,\n      logistics) for chargeback against the bundled enterprise invoice.\n  - name: Optimization\n    description: Reclaim unused module activations and seats during annual renewal; consolidate\n      Network connectivity across business units; align AI prediction consumption with business\n      cadence.\n  - name: Accountability\n    description: Designate a Blue Yonder contract owner per legal entity; review utilization and\n      realized supply-chain savings quarterly with the Blue Yonder customer success team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/blue-yonder/refs/heads/main/finops/blue-yonder-finops.yml
sources:
- https://www.blueyonder.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Supply Chain
- SaaS
---
