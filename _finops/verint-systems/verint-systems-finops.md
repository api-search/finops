---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps stub for Verint Systems: enterprise customer-engagement SaaS subscription with no public pricing or usage/billing API.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Verint Systems Inc.
  ProviderName: Verint Systems
  PublisherName: Verint Systems Inc.
  ServiceCategory: Customer Engagement
  ServiceName: Verint Open CCaaS / WEM
layout: finops
meters:
- aggregation: sum
  description: Annual Verint platform subscription line; sub-meters not publicly published.
  name: platform_subscription
  unit: varies
name: Verint Systems Finops
provider_name: Verint Systems
provider_slug: verint-systems
publisher_name: Verint Systems Inc.
service_category: Customer Engagement
slug: verint-systems-finops
source_filename: verint-systems-finops.yml
source_heading: FinOps Profile
source_url: https://www.verint.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Verint Systems\nproviderId: verint-systems\npublisherName: Verint Systems Inc.\nserviceCategory: Customer Engagement\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Customer Engagement\n  - Analytics\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps stub for Verint Systems: enterprise customer-engagement SaaS subscription\n  with no public pricing or usage/billing API.'\nsources:\n  - https://www.verint.com/\nnotes: No public pricing or billing API. Meters are not invented; reconciliation deferred pending customer-portal\n  access.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Verint Open CCaaS / WEM\n  ServiceCategory: Customer Engagement\n  ProviderName: Verint Systems\n  PublisherName: Verint Systems Inc.\n  InvoiceIssuerName: Verint Systems Inc.\n  BillingCurrency: USD\nmeters:\n  - name: platform_subscription\n    description: Annual Verint platform subscription line; sub-meters not publicly published.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Verint exposes consumption telemetry inside the platform UI; no public usage/cost API\n      is documented. Track license utilization through the customer success engagement.\n  - name: Allocation\n    description: Allocation is contract-level (per Verint product, seat / channel scoping in the order\n      form).\n  - name: Optimization\n    description: 'Optimization is scope-driven: which channels and modules are licensed, agent / seat\n      counts. Renewal is the primary\
  \ optimization checkpoint.'\n  - name: Accountability\n    description: Accountability sits with the contact-center / WEM platform owner; finance owns the\n      annual subscription line.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/verint-systems/refs/heads/main/finops/verint-systems-finops.yml
sources:
- https://www.verint.com/
specification: FinOps Framework
tags:
- Customer Engagement
- Analytics
- FinOps
- FOCUS
---
