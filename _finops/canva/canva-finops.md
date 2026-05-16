---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Canva Connect API
  slug: canva-connect-api
  spec_type: OpenAPI
  url: https://www.canva.com/developers/docs/connect-api/openapi/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Refund
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Canva: per-seat SaaS subscriptions (Free, Pro, Teams, Enterprise) with API access tied to the underlying Canva account; private integrations require Canva Enterprise.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Canva Pty Ltd
  ProviderName: Canva
  PublisherName: Canva Pty Ltd
  ServiceCategory: Design SaaS
  ServiceName: Canva
layout: finops
meters:
- aggregation: sum
  dimensions:
  - plan
  - team
  name: seat_subscription
  unit: seat-month
- aggregation: sum
  dimensions:
  - api
  - integration
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - format
  name: design_exports
  unit: export
- aggregation: sum
  dimensions:
  - product
  - region
  name: print_orders
  unit: order
name: Canva Finops
provider_name: Canva
provider_slug: canva
publisher_name: Canva Pty Ltd
service_category: Design SaaS
slug: canva-finops
source_filename: canva-finops.yml
source_heading: FinOps Profile
source_url: https://www.canva.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Canva\nproviderId: canva\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Cost Management\n  - Design\n  - SaaS\ndescription: 'FOCUS-aligned FinOps for Canva: per-seat SaaS subscriptions (Free, Pro, Teams, Enterprise)\n  with API access tied to the underlying Canva account; private integrations require Canva Enterprise.'\nnotes: Canva does not bill the Connect API as a separate SKU. API access is included with a Canva account;\n  private/Enterprise integrations are negotiated. Reconcile if Canva publishes a usage-priced API tier.\nsources:\n  - https://www.canva.com/pricing/\n  - https://www.canva.dev/docs/connect/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Canva Pty Ltd\nserviceCategory: Design SaaS\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Canva\n  ServiceCategory: Design SaaS\n  ProviderName: Canva\n  PublisherName: Canva Pty Ltd\n  InvoiceIssuerName: Canva Pty Ltd\n  BillingCurrency: USD\nmeters:\n  - name: seat_subscription\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - plan\n      - team\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - integration\n  - name: design_exports\n    unit: export\n    aggregation: sum\n    dimensions:\n      - format\n  - name: print_orders\n    unit: order\n    aggregation: sum\n    dimensions:\n      - product\n      - region\nprinciples:\n  - name: Visibility\n    description: Use the Canva admin console for seat utilization and\
  \ billing exports; the Connect API\n      itself does not emit a usage-cost stream.\n  - name: Allocation\n    description: Use Canva Teams workspace structure to attribute seat costs to departments; tag Connect\n      API integrations with consuming application IDs upstream of Canva.\n  - name: Optimization\n    description: Right-size paid seats by reviewing inactive users; reuse brand templates and bulk-create\n      via Connect API to reduce per-design overhead.\n  - name: Accountability\n    description: Workspace owners hold the bill; Enterprise contracts add named account management. Review\n      seat count quarterly and renegotiate at renewal.\nmaintainers:\n  - FN: Canva\n    email: developers@canva.com\n    url: https://www.canva.com/developers/\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/canva/refs/heads/main/finops/canva-finops.yml
sources:
- https://www.canva.com/pricing/
- https://www.canva.dev/docs/connect/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cost Management
- Design
- SaaS
---
