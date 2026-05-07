---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: dnv-class-status-openapi.yml
  format: yaml
  label: DNV Class Status API
  slug: dnv-class-status-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dnv/refs/heads/main/openapi/dnv-class-status-openapi.yml
billing_model:
  billingCurrency: USD/EUR/NOK
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Tax
  pricingCategory: Enterprise Contract
description: FOCUS-aligned FinOps shape for DNV Maritime APIs. DNV does not publish a per-call meter; cost is governed by the negotiated API contract (often bundled with classification or advisory services).
focus_columns:
  BillingCurrency: USD/EUR/NOK
  ChargeCategory: Purchase
  InvoiceIssuerName: DNV AS
  ProviderName: DNV
  PublisherName: DNV AS
  ServiceCategory: Maritime Classification / Data Platform
  ServiceName: DNV Maritime APIs
layout: finops
meters:
- aggregation: sum
  description: Internal observability of calls against DNV APIs
  dimensions:
  - api
  - vessel_imo
  name: api_requests
  unit: request
- aggregation: count
  description: Active named technical contacts under the API contract
  dimensions:
  - contract
  name: contract_seats
  unit: seat
name: Dnv Finops
provider_name: DNV
provider_slug: dnv
publisher_name: DNV AS
service_category: Maritime Classification / Data Platform
slug: dnv-finops
source_filename: dnv-finops.yml
source_heading: FinOps Profile
source_url: https://maritime.dnv.com/api/cs-iacs-customer
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: DNV\nproviderId: dnv\npublisherName: DNV AS\nserviceCategory: Maritime Classification / Data Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Maritime\n  - Classification\n  - Vessel\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for DNV Maritime APIs. DNV does not publish a per-call meter;\n  cost is governed by the negotiated API contract (often bundled with classification or advisory services).\nnotes: No public pricing or per-meter billing is published; reconciled=false. Meters below describe the\n  consumption surface that a customer would observe internally.\nsources:\n  - https://maritime.dnv.com/api/cs-iacs-customer\n\
  \  - https://www.dnv.com/maritime/\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD/EUR/NOK\n  chargeCategories:\n    - Purchase\n    - Tax\nfocusColumns:\n  ServiceName: DNV Maritime APIs\n  ServiceCategory: Maritime Classification / Data Platform\n  ProviderName: DNV\n  PublisherName: DNV AS\n  InvoiceIssuerName: DNV AS\n  BillingCurrency: USD/EUR/NOK\n  ChargeCategory: Purchase\nmeters:\n  - name: api_requests\n    description: Internal observability of calls against DNV APIs\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - vessel_imo\n  - name: contract_seats\n    description: Active named technical contacts under the API contract\n    unit: seat\n    aggregation: count\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: DNV invoices are issued under the API/classification contract; reconcile against contracted\n      services rather than per-call usage.\n\
  \  - name: Allocation\n    description: Allocate DNV cost to the fleet/vessel program that consumes class-status and IACS-75 data.\n  - name: Optimization\n    description: Cache class-status responses; reuse OAuth tokens (~20 min validity) across requests; coalesce\n      vessel-IMO lookups.\n  - name: Accountability\n    description: The named technical contact on the API contract is accountable for credential security\n      and adherence to the contracted scope.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dnv/refs/heads/main/finops/dnv-finops.yml
sources:
- https://maritime.dnv.com/api/cs-iacs-customer
- https://www.dnv.com/maritime/
specification: FinOps Framework
tags:
- Maritime
- Classification
- Vessel
- FinOps
- FOCUS
---
