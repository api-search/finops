---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: veritas-infoscale-rest-api.yaml
  format: yaml
  label: Veritas InfoScale REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/openapi/veritas-infoscale-rest-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps stub for Veritas InfoScale: enterprise software license (per-node / per-capacity) with no public pricing or usage/billing API.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Veritas Technologies LLC
  ProviderName: Veritas
  PublisherName: Veritas Technologies LLC
  ServiceCategory: Storage / High Availability
  ServiceName: Veritas InfoScale
layout: finops
meters:
- aggregation: sum
  description: Annual InfoScale license line; sizing dimensions (nodes, sockets, capacity) negotiated in the order form.
  name: software_license
  unit: varies
name: Veritas Infoscale Finops
provider_name: Veritas InfoScale
provider_slug: veritas-infoscale
publisher_name: Veritas Technologies LLC
service_category: Storage / High Availability
slug: veritas-infoscale-finops
source_filename: veritas-infoscale-finops.yml
source_heading: FinOps Profile
source_url: https://www.veritas.com/protection/infoscale
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Veritas InfoScale\nproviderId: veritas-infoscale\npublisherName: Veritas Technologies LLC\nserviceCategory: Storage / High Availability\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Storage Management\n  - High Availability\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps stub for Veritas InfoScale: enterprise software license (per-node /\n  per-capacity) with no public pricing or usage/billing API.'\nsources:\n  - https://www.veritas.com/protection/infoscale\nnotes: No public pricing or billing API; product page returned 403 to crawlers. Meters are not invented;\n  reconciliation deferred.\nbillingModel:\n\
  \  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Veritas InfoScale\n  ServiceCategory: Storage / High Availability\n  ProviderName: Veritas\n  PublisherName: Veritas Technologies LLC\n  InvoiceIssuerName: Veritas Technologies LLC\n  BillingCurrency: USD\nmeters:\n  - name: software_license\n    description: Annual InfoScale license line; sizing dimensions (nodes, sockets, capacity) negotiated\n      in the order form.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility into InfoScale usage is local to the customer's deployment via the InfoScale\n      Operations Manager / CLI; there is no public cost API.\n  - name: Allocation\n    description: Allocation is per-cluster / per-node based on entitlement records held by the customer\n      and validated by Veritas at audit time.\n  - name: Optimization\n    description: Optimization levers\
  \ are right-sizing nodes / sockets at renewal and consolidating clusters\n      to reduce entitlement count.\n  - name: Accountability\n    description: Accountability sits with the platform / infrastructure team that operates the InfoScale\n      clusters; finance owns the annual subscription line.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/finops/veritas-infoscale-finops.yml
sources:
- https://www.veritas.com/protection/infoscale
specification: FinOps Framework
tags:
- Storage Management
- High Availability
- FinOps
- FOCUS
---
