---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: lincoln-national-openapi.yml
  format: yaml
  label: Lincoln Financial LincSmart Enrollment API
  slug: lincsmart-enrollment-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lincoln-national/refs/heads/main/openapi/lincoln-national-openapi.yml
- filename: lincoln-national-openapi.yml
  format: yaml
  label: Lincoln Financial LincSmart EOI Solution API
  slug: lincsmart-eoi-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lincoln-national/refs/heads/main/openapi/lincoln-national-openapi.yml
- filename: lincoln-national-openapi.yml
  format: yaml
  label: Lincoln Financial LincSmart Plan Design API
  slug: lincsmart-plan-design-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lincoln-national/refs/heads/main/openapi/lincoln-national-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom Contract
description: 'FOCUS-aligned FinOps scaffold for Lincoln Financial / Lincoln National: partner-only LincSmart API access with no public per-call pricing. Consumer-side telemetry tracks against the LincSmart partner agreement, not metered API invoices.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Lincoln National Corporation
  ProviderName: Lincoln Financial
  PublisherName: Lincoln National Corporation
  ServiceCategory: Insurance / Retirement / API
  ServiceName: Lincoln Financial LincSmart API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - environment
  - partner
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - employer
  - product
  name: enrollment_events
  unit: event
- aggregation: sum
  name: eoi_decisions
  unit: decision
name: Lincoln National Finops
provider_name: Lincoln National
provider_slug: lincoln-national
publisher_name: Lincoln National Corporation
service_category: Insurance / Retirement / API
slug: lincoln-national-finops
source_filename: lincoln-national-finops.yml
source_heading: FinOps Profile
source_url: https://www.lincolnfinancial.com/public/static/digitalbrochure/gp/lincsmart/index.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lincoln National\nproviderId: lincoln-national\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Annuities\n  - Benefits\n  - Insurance\n  - Retirement\ndescription: 'FOCUS-aligned FinOps scaffold for Lincoln Financial / Lincoln National: partner-only LincSmart\n  API access with no public per-call pricing. Consumer-side telemetry tracks against the LincSmart partner\n  agreement, not metered API invoices.'\nnotes: Pricing is partner-contract driven. Meters describe the consumer-side observation surface.\nsources:\n  - https://www.lincolnfinancial.com/public/static/digitalbrochure/gp/lincsmart/index.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Lincoln National Corporation\nserviceCategory: Insurance / Retirement / API\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Lincoln Financial LincSmart API\n  ServiceCategory: Insurance / Retirement / API\n  ProviderName: Lincoln Financial\n  PublisherName: Lincoln National Corporation\n  InvoiceIssuerName: Lincoln National Corporation\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n      - partner\n  - name: enrollment_events\n    unit: event\n    aggregation: sum\n    dimensions:\n      - employer\n      - product\n  - name: eoi_decisions\n    unit: decision\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use the LincSmart real-time sync events plus your own observability stack to track\
  \ enrollment,\n      EOI, and leave activity volumes; Lincoln does not expose a public usage API.\n  - name: Allocation\n    description: Tag calls by employer group, product (life, disability, retirement), and benefits platform\n      partner so the LincSmart contract draw can be allocated correctly.\n  - name: Optimization\n    description: Replace weekly batch files with LincSmart real-time sync; throttle annual-enrollment\n      bursts via partner-coordinated windows.\n  - name: Accountability\n    description: Assign a LincSmart partner owner who reviews enrollment-event throughput and contract\n      consumption against quarterly benefit cycles.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lincoln-national/refs/heads/main/finops/lincoln-national-finops.yml
sources:
- https://www.lincolnfinancial.com/public/static/digitalbrochure/gp/lincsmart/index.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Annuities
- Benefits
- Insurance
- Retirement
---
