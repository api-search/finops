---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: state-street-alpha-data-platform-openapi.yml
  format: yaml
  label: Alpha Data Platform API
  slug: alpha-data-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/state-street/refs/heads/main/openapi/state-street-alpha-data-platform-openapi.yml
- filename: state-street-fund-connect-openapi.yml
  format: yaml
  label: Fund Connect API
  slug: fund-connect-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/state-street/refs/heads/main/openapi/state-street-fund-connect-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: State Street has a developer portal for institutional API products but no public, metered billing surface. Costs land inside the broader institutional client agreement; there is no FOCUS-billable per-call price list to reconcile.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: State Street Corporation
  ProviderName: State Street
  PublisherName: State Street Corporation
  ServiceCategory: Financial Services / Asset Servicing
  ServiceName: State Street
layout: finops
meters:
- aggregation: sum
  description: Placeholder for line items defined in a State Street institutional / partner contract.
  name: contracted_engagement
  unit: varies
name: State Street Finops
provider_name: State Street
provider_slug: state-street
publisher_name: State Street Corporation
service_category: Financial Services / Asset Servicing
slug: state-street-finops
source_filename: state-street-finops.yml
source_heading: FinOps Profile
source_url: https://developer.statestreet.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: State Street\nproviderId: state-street\npublisherName: State Street Corporation\nserviceCategory: Financial Services / Asset Servicing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Financial Services\n  - Asset Servicing\ndescription: State Street has a developer portal for institutional API products but no public, metered\n  billing surface. Costs land inside the broader institutional client agreement; there is no FOCUS-billable\n  per-call price list to reconcile.\nsources:\n  - https://developer.statestreet.com/\nnotes: No public State Street API pricing or invoice surface. Meters and FOCUS\
  \ columns are placeholders\n  pending a contracted engagement.\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: State Street\n  ServiceCategory: Financial Services / Asset Servicing\n  ProviderName: State Street\n  PublisherName: State Street Corporation\n  InvoiceIssuerName: State Street Corporation\n  BillingCurrency: USD\nmeters:\n  - name: contracted_engagement\n    description: Placeholder for line items defined in a State Street institutional / partner contract.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the State Street client reporting workflow tied to the underlying\n      asset-servicing contract — there is no public usage / billing API.\n  - name: Allocation\n    description: Allocate the institutional engagement cost in your own ERP; State Street does not\n      surface a self-serve cost\
  \ breakdown for API consumption.\n  - name: Optimization\n    description: Optimization happens via contract review, scope renegotiation, or product-mix changes\n      with the API Platform Management team.\n  - name: Accountability\n    description: A named institutional client owner should hold the State Street engagement cost line\n      and renewal cycle.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/state-street/refs/heads/main/finops/state-street-finops.yml
sources:
- https://developer.statestreet.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Financial Services
- Asset Servicing
---
