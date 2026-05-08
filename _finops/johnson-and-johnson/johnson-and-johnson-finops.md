---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: johnson-and-johnson-lifescan-api-openapi.yml
  format: yaml
  label: Johnson & Johnson LifeScan API
  slug: lifescan-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/johnson-and-johnson/refs/heads/main/openapi/johnson-and-johnson-lifescan-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Enterprise / Negotiated
description: FOCUS-aligned FinOps scaffold for Johnson & Johnson integration surfaces. Treated as negotiated enterprise; no first-party billing API.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Johnson & Johnson
  ProviderName: Johnson & Johnson
  PublisherName: Johnson & Johnson
  ServiceCategory: Healthcare / Enterprise Integration
  ServiceName: Johnson & Johnson Integration APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - integration
  - business_segment
  - partner
  name: api_requests
  unit: request
- aggregation: count
  dimensions:
  - integration
  - business_segment
  name: file_transfers
  unit: file
name: Johnson And Johnson Finops
provider_name: Johnson & Johnson
provider_slug: johnson-and-johnson
publisher_name: Johnson & Johnson
service_category: Healthcare / Enterprise Integration
slug: johnson-and-johnson-finops
source_filename: johnson-and-johnson-finops.yml
source_heading: FinOps Profile
source_url: https://www.jnj.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Johnson & Johnson\nproviderId: johnson-and-johnson\npublisherName: Johnson & Johnson\nserviceCategory: Healthcare / Enterprise Integration\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: J&J does not expose a public usage-billing surface. FinOps shape is inferred from a\n  negotiated-enterprise model. Meters listed reflect typical integration line items (API\n  calls, file transfers) and should be re-modeled against the actual contract once available.\ntags:\n  - Healthcare\n  - Medical Devices\n  - Pharmaceuticals\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for Johnson & Johnson integration surfaces.\n\
  \  Treated as negotiated enterprise; no first-party billing API.\nsources:\n  - https://www.jnj.com/\n  - https://www.finops.org/framework/\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Enterprise / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Johnson & Johnson Integration APIs\n  ServiceCategory: Healthcare / Enterprise Integration\n  ProviderName: Johnson & Johnson\n  PublisherName: Johnson & Johnson\n  InvoiceIssuerName: Johnson & Johnson\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - integration\n      - business_segment\n      - partner\n  - name: file_transfers\n    unit: file\n    aggregation: count\n    dimensions:\n      - integration\n      - business_segment\nprinciples:\n  - name: Visibility\n    description: Track usage at the integration-contract\
  \ level since J&J does not expose\n      first-party usage telemetry; instrument calls on the consumer side.\n  - name: Allocation\n    description: Allocate by business_segment (Innovative Medicine vs MedTech vs Supply\n      Chain) and by integration_id to reflect the multi-OpCo structure.\n  - name: Optimization\n    description: Use bulk / batch interfaces where contracts permit, and reconcile usage\n      against contract minimums periodically.\n  - name: Accountability\n    description: Each integration has a J&J relationship owner; pair with an internal API\n      product manager who owns the consumer-side cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/johnson-and-johnson/refs/heads/main/finops/johnson-and-johnson-finops.yml
sources:
- https://www.jnj.com/
- https://www.finops.org/framework/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Healthcare
- Medical Devices
- Pharmaceuticals
- FinOps
- FOCUS
---
