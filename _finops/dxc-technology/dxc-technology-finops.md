---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: dxc-developer-central-api-openapi.yml
  format: yaml
  label: DXC Developer Central API
  slug: developer-central-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dxc-technology/refs/heads/main/openapi/dxc-developer-central-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Custom Contract
description: FOCUS-aligned FinOps shell for DXC Technology API surface; pricing is contracted, not publicly metered, so meters and FOCUS columns are placeholders pending direct invoice review.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: DXC Technology Company
  ProviderName: DXC Technology
  PublisherName: DXC Technology Company
  ServiceCategory: IT Services
  ServiceName: DXC Developer Central
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - engagement
  - region
  name: managed_service_hours
  unit: hour
name: Dxc Technology Finops
provider_name: DXC Technology
provider_slug: dxc-technology
publisher_name: DXC Technology Company
service_category: IT Services
slug: dxc-technology-finops
source_filename: dxc-technology-finops.yml
source_heading: FinOps Profile
source_url: https://developer.dxc.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: DXC Technology\nproviderId: dxc-technology\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - IT Services\n  - Enterprise\ndescription: 'FOCUS-aligned FinOps shell for DXC Technology API surface; pricing is contracted, not\n  publicly metered, so meters and FOCUS columns are placeholders pending direct invoice review.'\nnotes: DXC Technology does not publish public API pricing. FinOps mapping should be reconciled against\n  the actual managed-services agreement and invoice line items.\nsources:\n  - https://developer.dxc.com/\n  - https://dxc.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: DXC Technology Company\nserviceCategory:\
  \ IT Services\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: DXC Developer Central\n  ServiceCategory: IT Services\n  ProviderName: DXC Technology\n  PublisherName: DXC Technology Company\n  InvoiceIssuerName: DXC Technology Company\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - consumer\n  - name: managed_service_hours\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - engagement\n      - region\nprinciples:\n  - name: Visibility\n    description: Request itemized usage reports from the DXC account team; integrate invoice line items\n      into FOCUS-formatted tables.\n  - name: Allocation\n    description: Tag API consumers by engagement/cost-center and reconcile against the master services\n      agreement.\n  - name: Optimization\n\
  \    description: Negotiate volume discounts at renewal; consolidate API consumers across business units\n      to qualify for tier discounts.\n  - name: Accountability\n    description: Engagement owner reviews the monthly DXC invoice; flag deviations from baseline run-rate.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dxc-technology/refs/heads/main/finops/dxc-technology-finops.yml
sources:
- https://developer.dxc.com/
- https://dxc.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- IT Services
- Enterprise
---
