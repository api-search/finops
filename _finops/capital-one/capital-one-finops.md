---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Custom Partner Agreement
description: 'FOCUS-aligned FinOps for Capital One DevExchange: partner-negotiated banking APIs billed through bilateral agreements rather than self-service usage tariffs.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Capital One Services, LLC
  ProviderName: Capital One
  PublisherName: Capital One Services, LLC
  ServiceCategory: Banking API
  ServiceName: Capital One DevExchange
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - partner
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - partner
  - product
  name: contract_fee
  unit: month
name: Capital One Finops
provider_name: Capital One
provider_slug: capital-one
publisher_name: Capital One Services, LLC
service_category: Banking API
slug: capital-one-finops
source_filename: capital-one-finops.yml
source_heading: FinOps Profile
source_url: https://developer.capitalone.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Capital One\nproviderId: capital-one\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Banking\n  - Financial Services\n  - DevExchange\ndescription: 'FOCUS-aligned FinOps for Capital One DevExchange: partner-negotiated banking APIs billed\n  through bilateral agreements rather than self-service usage tariffs.'\nnotes: Capital One does not publish a public API pricing or billing surface. Treat all billing as opaque\n  partner-contract terms; reconcile against partnership invoice line items when available.\nsources:\n  - https://developer.capitalone.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Capital One Services, LLC\n\
  serviceCategory: Banking API\nbillingModel:\n  pricingCategory: Custom Partner Agreement\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Capital One DevExchange\n  ServiceCategory: Banking API\n  ProviderName: Capital One\n  PublisherName: Capital One Services, LLC\n  InvoiceIssuerName: Capital One Services, LLC\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - partner\n  - name: contract_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - partner\n      - product\nprinciples:\n  - name: Visibility\n    description: Visibility into request counts is provided through the partner DevExchange dashboard\n      or bilateral reporting; no public usage API.\n  - name: Allocation\n    description: Allocation is by client_id (partner OAuth credential); for multi-product partners, tag\n\
  \      requests with internal correlation IDs upstream.\n  - name: Optimization\n    description: Optimize by batching authorizations, caching reference data (e.g. credit offers), and\n      negotiating volume terms at renewal.\n  - name: Accountability\n    description: Partnership owner holds the budget; quarterly business reviews with Capital One are typical.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/capital-one/refs/heads/main/finops/capital-one-finops.yml
sources:
- https://developer.capitalone.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking
- Financial Services
- DevExchange
---
