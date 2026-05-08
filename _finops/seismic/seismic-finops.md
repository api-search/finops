---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: seismic-content-openapi.yml
  format: yaml
  label: Seismic Content API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/seismic/refs/heads/main/openapi/seismic-content-openapi.yml
- filename: seismic-livedocs-openapi.yml
  format: yaml
  label: Seismic LiveDocs API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/seismic/refs/heads/main/openapi/seismic-livedocs-openapi.yml
- filename: seismic-analytics-openapi.yml
  format: yaml
  label: Seismic Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/seismic/refs/heads/main/openapi/seismic-analytics-openapi.yml
- filename: seismic-user-management-openapi.yml
  format: yaml
  label: Seismic User Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/seismic/refs/heads/main/openapi/seismic-user-management-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FinOps shape for Seismic — quote-based enterprise SaaS subscription. The provider does not publish per-API meters or pricing; cost is a negotiated annual subscription with seats and module add-ons. API rate limits are operational guards, not billable meters.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Seismic Software, Inc.
  ProviderName: Seismic
  PublisherName: Seismic Software, Inc.
  ServiceCategory: Sales Enablement SaaS
  ServiceName: Seismic
layout: finops
meters:
- aggregation: sum
  description: Per-seat annual subscription (sales reps, content authors, admins)
  dimensions:
  - role
  name: seat_subscription
  unit: seat
- aggregation: sum
  description: Negotiated module / add-on line items (LiveDocs, LiveSend, Reporting, etc.)
  dimensions:
  - module
  name: module_addons
  unit: module
name: Seismic Finops
provider_name: Seismic
provider_slug: seismic
publisher_name: Seismic Software, Inc.
service_category: Sales Enablement SaaS
slug: seismic-finops
source_filename: seismic-finops.yml
source_heading: FinOps Profile
source_url: https://seismic.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Seismic\nproviderId: seismic\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Sales Enablement\n  - Content Management\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Seismic — quote-based enterprise SaaS subscription. The provider does not\n  publish per-API meters or pricing; cost is a negotiated annual subscription with seats and module add-ons.\n  API rate limits are operational guards, not billable meters.\nsources:\n  - https://seismic.com/\n  - https://developer.seismic.com/seismicsoftware/reference/rate-limiting\nnotes: Pricing and per-meter billing are not publicly disclosed; reconciled to negotiated-subscription\n  shape only.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Seismic Software, Inc.\nserviceCategory: Sales Enablement SaaS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Seismic\n  ServiceCategory: Sales Enablement SaaS\n  ProviderName: Seismic\n  PublisherName: Seismic Software, Inc.\n  InvoiceIssuerName: Seismic Software, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: seat_subscription\n    description: Per-seat annual subscription (sales reps, content authors, admins)\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - role\n  - name: module_addons\n    description: Negotiated module / add-on line items (LiveDocs, LiveSend, Reporting, etc.)\n    unit: module\n    aggregation: sum\n    dimensions:\n      - module\nprinciples:\n  - name: Visibility\n    description: Visibility is limited to the Seismic invoice and the Reporting API for in-product activity.\n      Use the Reporting API to attribute\
  \ consumption (content opened, livesends created) back to teams.\n  - name: Allocation\n    description: Allocate the subscription across sales / marketing / enablement cost centers based on\n      seat counts; module add-ons should be allocated to the team that requested them.\n  - name: Optimization\n    description: Right-size seats annually based on Reporting API activity. Avoid hitting Tier 1 / 1.5\n      generation limits with bulk LiveDoc workflows — batch and schedule instead of bursting.\n  - name: Accountability\n    description: Sales / Revenue Operations typically owns the Seismic line. The integration team owns\n      API rate-limit health and exemption requests through Seismic support.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/seismic/refs/heads/main/finops/seismic-finops.yml
sources:
- https://seismic.com/
- https://developer.seismic.com/seismicsoftware/reference/rate-limiting
specification: FinOps Framework
tags:
- Sales Enablement
- Content Management
- FinOps
- FOCUS
---
