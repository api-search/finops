---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: regal-cinema-openapi.yml
  format: yaml
  label: Regal Cinema API
  slug: regal-cinema-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/regal-entertainment-group/refs/heads/main/openapi/regal-cinema-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: FinOps shape for Regal Cinemas partner data feeds. No self-serve API, no published meters; spend is governed by the partner contract.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Regal Cinemas, Inc.
  ProviderName: Regal Cinemas
  PublisherName: Regal Cinemas, Inc.
  ServiceCategory: Entertainment
  ServiceName: Regal Cinemas
layout: finops
meters:
- aggregation: sum
  name: contract_term
  unit: month
name: Regal Entertainment Group Finops
provider_name: regal-entertainment-group
provider_slug: regal-entertainment-group
publisher_name: Regal Cinemas, Inc.
service_category: Entertainment
slug: regal-entertainment-group-finops
source_filename: regal-entertainment-group-finops.yml
source_heading: FinOps Profile
source_url: https://www.regmovies.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: regal-entertainment-group\nproviderId: regal-entertainment-group\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Cinema\n  - Ticketing\ndescription: FinOps shape for Regal Cinemas partner data feeds. No self-serve API, no published meters;\n  spend is governed by the partner contract.\nsources:\n  - https://www.regmovies.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Regal Cinemas, Inc.\nserviceCategory: Entertainment\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Regal Cinemas\n  ServiceCategory:\
  \ Entertainment\n  ProviderName: Regal Cinemas\n  PublisherName: Regal Cinemas, Inc.\n  InvoiceIssuerName: Regal Cinemas, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_term\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility relies on the Regal / Cineworld partner invoice; there is no programmatic\n      usage feed.\n  - name: Allocation\n    description: Allocate to the marketing or ticketing-aggregation product line that signed the partnership.\n  - name: Optimization\n    description: Optimization is contractual — renegotiate scope at renewal rather than tuning request\n      volume.\n  - name: Accountability\n    description: Owner is the partnership lead who manages the Regal contract.\nnotes: No public pricing or usage API; FinOps shape is a contract-driven partnership. Generic per-request\n  meters and FOCUS columns removed.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/regal-entertainment-group/refs/heads/main/finops/regal-entertainment-group-finops.yml
sources:
- https://www.regmovies.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cinema
- Ticketing
---
