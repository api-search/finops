---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: liberty-mutual-insurance-renters-insurance-api-openapi.yml
  format: yaml
  label: Liberty Mutual Renters Insurance API
  slug: renters-insurance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/liberty-mutual-insurance/refs/heads/main/openapi/liberty-mutual-insurance-renters-insurance-api-openapi.yml
- filename: liberty-mutual-insurance-solaria-labs-api-openapi.yml
  format: yaml
  label: Liberty Mutual Solaria Labs API
  slug: solaria-labs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/liberty-mutual-insurance/refs/heads/main/openapi/liberty-mutual-insurance-solaria-labs-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom Contract
description: 'FOCUS-aligned FinOps scaffold for Liberty Mutual Insurance: partner-only API access with no public per-call pricing. Consumer-side telemetry tracks against the partner agreement (commission, premium, claims-handling), not metered API invoices.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Liberty Mutual Insurance Company
  ProviderName: Liberty Mutual Insurance
  PublisherName: Liberty Mutual Insurance Company
  ServiceCategory: Insurance / API
  ServiceName: Liberty Mutual Insurance API
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
  - product
  - state
  name: quotes_issued
  unit: quote
- aggregation: sum
  dimensions:
  - product
  - state
  name: policies_bound
  unit: policy
name: Liberty Mutual Insurance Finops
provider_name: Liberty Mutual Insurance
provider_slug: liberty-mutual-insurance
publisher_name: Liberty Mutual Insurance Company
service_category: Insurance / API
slug: liberty-mutual-insurance-finops
source_filename: liberty-mutual-insurance-finops.yml
source_heading: FinOps Profile
source_url: https://business.libertymutual.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Liberty Mutual Insurance\nproviderId: liberty-mutual-insurance\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Insurance\n  - Casualty\n  - Commercial Lines\n  - Personal Lines\ndescription: 'FOCUS-aligned FinOps scaffold for Liberty Mutual Insurance: partner-only API access with\n  no public per-call pricing. Consumer-side telemetry tracks against the partner agreement (commission,\n  premium, claims-handling), not metered API invoices.'\nnotes: Pricing is partner-contract driven. Meters describe the consumer-side observation surface.\nsources:\n  - https://business.libertymutual.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Liberty Mutual Insurance Company\nserviceCategory: Insurance / API\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Liberty Mutual Insurance API\n  ServiceCategory: Insurance / API\n  ProviderName: Liberty Mutual Insurance\n  PublisherName: Liberty Mutual Insurance Company\n  InvoiceIssuerName: Liberty Mutual Insurance Company\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n      - partner\n  - name: quotes_issued\n    unit: quote\n    aggregation: sum\n    dimensions:\n      - product\n      - state\n  - name: policies_bound\n    unit: policy\n    aggregation: sum\n    dimensions:\n      - product\n      - state\nprinciples:\n  - name: Visibility\n    description: Track quote, bind, and claim event volumes through your gateway\
  \ / observability stack;\n      Liberty Mutual does not expose a public usage API.\n  - name: Allocation\n    description: Tag calls by product line (renters, auto, commercial) and channel partner so commission\n      and partner-contract spend can be charged back.\n  - name: Optimization\n    description: Cache rating reference data and quote artifacts within partner TOS; batch claim status\n      polling to reduce call volume.\n  - name: Accountability\n    description: Assign a Liberty Mutual partner contract owner who reviews quote-to-bind ratios, claim\n      volumes, and partner-contract performance monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/liberty-mutual-insurance/refs/heads/main/finops/liberty-mutual-insurance-finops.yml
sources:
- https://business.libertymutual.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Insurance
- Casualty
- Commercial Lines
- Personal Lines
---
