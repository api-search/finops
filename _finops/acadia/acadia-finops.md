---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: acadia-platform.yaml
  format: yaml
  label: Acadia Platform API
  slug: acadia-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/acadia/refs/heads/main/openapi/acadia-platform.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription
description: FOCUS-aligned FinOps scaffold for Acadia (now an Epicor product). Pricing is enterprise quote-based, so meters and FOCUS columns reflect a typical SaaS seat-and-tenant invoice rather than per-call usage.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Epicor Software Corporation
  ProviderName: Acadia
  PublisherName: Epicor Software Corporation
  ServiceCategory: Connected Worker / Workforce Enablement SaaS
  ServiceName: Acadia
layout: finops
meters:
- aggregation: max
  description: Named-user seat assigned to a frontline worker, supervisor, or admin.
  dimensions:
  - role
  - site
  - business_unit
  name: named_user_seat
  unit: seat
- aggregation: sum
  description: Annual platform subscription per tenant.
  dimensions:
  - environment
  name: tenant_subscription
  unit: year
- aggregation: sum
  description: Acadia Platform API call (when the API add-on is contracted).
  dimensions:
  - endpoint
  - integration
  name: api_request
  unit: request
name: Acadia Finops
provider_name: Acadia
provider_slug: acadia
publisher_name: Epicor Software Corporation
service_category: Connected Worker / Workforce Enablement SaaS
slug: acadia-finops
source_filename: acadia-finops.yml
source_heading: FinOps Profile
source_url: https://www.acadia-software.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Acadia\nproviderId: acadia\npublisherName: Epicor Software Corporation\nserviceCategory: Connected Worker / Workforce Enablement SaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Connected Worker\n  - Knowledge Management\n  - Manufacturing\n  - Skills Management\n  - Training\n  - Workforce Development\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for Acadia (now an Epicor product). Pricing is enterprise\n  quote-based, so meters and FOCUS columns reflect a typical SaaS seat-and-tenant invoice rather than\n  per-call usage.\nsources:\n  - https://www.acadia-software.com/\nnotes: No public pricing\
  \ or billing API. The FinOps shape below assumes a SaaS subscription with seat-based\n  metering, which is the canonical Acadia / Epicor commercial model; specific dollar amounts and committed-use\n  terms must be reconciled from the customer's order form.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Acadia\n  ServiceCategory: Connected Worker / Workforce Enablement SaaS\n  ProviderName: Acadia\n  PublisherName: Epicor Software Corporation\n  InvoiceIssuerName: Epicor Software Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: named_user_seat\n    description: Named-user seat assigned to a frontline worker, supervisor, or admin.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - role\n      - site\n      - business_unit\n  - name: tenant_subscription\n    description: Annual platform subscription per tenant.\n\
  \    unit: year\n    aggregation: sum\n    dimensions:\n      - environment\n  - name: api_request\n    description: Acadia Platform API call (when the API add-on is contracted).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - integration\nprinciples:\n  - name: Visibility\n    description: Acadia / Epicor invoices are line-item PDFs; pull seat counts and integration add-ons\n      from the order form into the cost dataset since there is no public usage API.\n  - name: Allocation\n    description: Allocate seats to the consuming site, plant, or business unit; tag platform-API calls\n      to the integrating system (ERP, HRIS, LMS).\n  - name: Optimization\n    description: Reconcile named-user seats annually against active workforce; reclaim seats from churned\n      employees and align tier (read-only vs authoring) to actual usage.\n  - name: Accountability\n    description: Operations leadership at the consuming site owns seat counts and renewal scope;\
  \ integrations\n      are owned by the IT integration lead.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/acadia/refs/heads/main/finops/acadia-finops.yml
sources:
- https://www.acadia-software.com/
specification: FinOps Framework
tags:
- Connected Worker
- Knowledge Management
- Manufacturing
- Skills Management
- Training
- Workforce Development
- FinOps
- FOCUS
---
