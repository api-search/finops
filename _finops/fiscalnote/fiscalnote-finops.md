---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fiscalnote-policynote-openapi.yml
  format: yaml
  label: FiscalNote PolicyNote API
  slug: policynote-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fiscalnote/refs/heads/main/openapi/fiscalnote-policynote-openapi.yml
- filename: fiscalnote-appdata-openapi.yml
  format: yaml
  label: FiscalNote AppData API
  slug: appdata-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fiscalnote/refs/heads/main/openapi/fiscalnote-appdata-openapi.yml
- filename: fiscalnote-people-openapi.yml
  format: yaml
  label: FiscalNote People API
  slug: people-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fiscalnote/refs/heads/main/openapi/fiscalnote-people-openapi.yml
- filename: fiscalnote-organization-openapi.yml
  format: yaml
  label: FiscalNote Organization API
  slug: organization-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fiscalnote/refs/heads/main/openapi/fiscalnote-organization-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps mapping for FiscalNote — annual subscription SaaS with seat-based and tier-gated pricing across PolicyNote, CQ, and Roll Call products. API access is bundled with the subscription rather than separately metered.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: FiscalNote, Inc.
  ProviderName: FiscalNote, Inc.
  PublisherName: FiscalNote, Inc.
  ServiceCategory: Government / Policy Intelligence
  ServiceName: FiscalNote
layout: finops
meters:
- aggregation: max
  description: Named-user seats on PolicyNote / CQ / Roll Call
  dimensions:
  - product
  - tier
  - team
  name: seats
  unit: seat-month
- aggregation: max
  description: Tier license fee (Platform Only / Essential / Advanced) on PolicyNote
  dimensions:
  - product
  - tier
  name: tier_license
  unit: month
- aggregation: sum
  description: Hands-on analyst curation hours bundled with Essential / Advanced tiers
  dimensions:
  - product
  - tier
  name: analyst_services
  unit: hour
- aggregation: sum
  description: Optional API usage where contract specifies a metered API add-on
  dimensions:
  - api
  - endpoint
  name: api_calls
  unit: request
name: Fiscalnote Finops
provider_name: FiscalNote
provider_slug: fiscalnote
publisher_name: FiscalNote, Inc.
service_category: Government / Policy Intelligence
slug: fiscalnote-finops
source_filename: fiscalnote-finops.yml
source_heading: FinOps Profile
source_url: https://www.fiscalnote.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: FiscalNote\nproviderId: fiscalnote\npublisherName: FiscalNote, Inc.\nserviceCategory: Government / Policy Intelligence\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Government\n  - Legislation\n  - Policy\n  - Political Intelligence\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps mapping for FiscalNote — annual subscription SaaS with seat-based and tier-gated pricing across PolicyNote, CQ, and Roll Call products. API access is bundled with the subscription rather than separately metered.\nnotes: No public pricing or invoice schema; meters reflect the expected invoice lines (seat-month, tier license, professional-services\
  \ analyst hours).\nsources:\n  - https://www.fiscalnote.com/products\n  - https://fiscalnote.com/policynote-plans\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: FiscalNote\n  ServiceCategory: Government / Policy Intelligence\n  ProviderName: FiscalNote, Inc.\n  PublisherName: FiscalNote, Inc.\n  InvoiceIssuerName: FiscalNote, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: seats\n    description: Named-user seats on PolicyNote / CQ / Roll Call\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - product\n      - tier\n      - team\n  - name: tier_license\n    description: Tier license fee (Platform Only / Essential / Advanced) on PolicyNote\n    unit: month\n    aggregation: max\n    dimensions:\n      - product\n      - tier\n  - name: analyst_services\n    description:\
  \ Hands-on analyst curation hours bundled with Essential / Advanced tiers\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - product\n      - tier\n  - name: api_calls\n    description: Optional API usage where contract specifies a metered API add-on\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: Pull seat-utilization reports from FiscalNote admin to track license waste; reconcile against the annual invoice.\n  - name: Allocation\n    description: Allocate seats by team/issue area in the FiscalNote admin so chargeback is unambiguous.\n  - name: Optimization\n    description: Right-size tier (Platform Only vs Essential) based on whether analyst curation is actually consumed; consolidate seats from departing employees promptly.\n  - name: Accountability\n    description: Government-affairs leader owns the contract; finance reviews seat utilization and tier appropriateness ahead of\
  \ each annual renewal.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fiscalnote/refs/heads/main/finops/fiscalnote-finops.yml
sources:
- https://www.fiscalnote.com/products
- https://fiscalnote.com/policynote-plans
specification: FinOps Framework
tags:
- Government
- Legislation
- Policy
- Political Intelligence
- FinOps
- FOCUS
---
