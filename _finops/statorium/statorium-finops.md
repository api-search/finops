---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: statorium-football-api-openapi.yml
  format: yaml
  label: Statorium Football API
  slug: football-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/statorium/refs/heads/main/openapi/statorium-football-api-openapi.yml
- filename: statorium-basketball-api-openapi.yml
  format: yaml
  label: Statorium Basketball API
  slug: basketball-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/statorium/refs/heads/main/openapi/statorium-basketball-api-openapi.yml
- filename: statorium-american-football-api-openapi.yml
  format: yaml
  label: Statorium American Football API
  slug: american-football-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/statorium/refs/heads/main/openapi/statorium-american-football-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: Statorium is a quote-based sports-data API with no public price list. There is no metered pay-as-you-go surface; charges land as a fixed fee or volume contract negotiated per buyer, so the FOCUS-billable line is a single contracted-engagement meter until a quote is signed.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Statorium
  ProviderName: Statorium
  PublisherName: Statorium
  ServiceCategory: Sports Data
  ServiceName: Statorium
layout: finops
meters:
- aggregation: sum
  description: Placeholder for the line items defined in a Statorium buyer quote (sport coverage, refresh cadence, delivery format).
  name: contracted_engagement
  unit: varies
name: Statorium Finops
provider_name: Statorium
provider_slug: statorium
publisher_name: Statorium
service_category: Sports Data
slug: statorium-finops
source_filename: statorium-finops.yml
source_heading: FinOps Profile
source_url: https://www.statorium.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Statorium\nproviderId: statorium\npublisherName: Statorium\nserviceCategory: Sports Data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Sports Data\ndescription: Statorium is a quote-based sports-data API with no public price list. There is no metered\n  pay-as-you-go surface; charges land as a fixed fee or volume contract negotiated per buyer, so the\n  FOCUS-billable line is a single contracted-engagement meter until a quote is signed.\nsources:\n  - https://www.statorium.com/\nnotes: No public pricing; FinOps shape cannot be reconciled until a buyer quote defines tier, sport\n  coverage, refresh\
  \ rate, and unit price.\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Statorium\n  ServiceCategory: Sports Data\n  ProviderName: Statorium\n  PublisherName: Statorium\n  InvoiceIssuerName: Statorium\n  BillingCurrency: USD\nmeters:\n  - name: contracted_engagement\n    description: Placeholder for the line items defined in a Statorium buyer quote (sport coverage,\n      refresh cadence, delivery format).\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility is whatever delivery telemetry (feed health, delay, error rates) is set\n      in the quote — there is no public Statorium usage / billing API.\n  - name: Allocation\n    description: Allocate the Statorium subscription line in your own product / ERP cost system; tag\n      by sport or product surface so renewal trade-offs are visible.\n  - name: Optimization\n\
  \    description: Optimization happens at quote renewal — adjust covered sports, refresh cadence, and\n      delivery format (JSON / widget / plugin) to fit actual demand.\n  - name: Accountability\n    description: A named product / data owner should hold the Statorium subscription cost line and\n      renewal review.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/statorium/refs/heads/main/finops/statorium-finops.yml
sources:
- https://www.statorium.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Sports Data
---
