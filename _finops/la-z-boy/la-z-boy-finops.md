---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Contract / Partner
description: La-Z-Boy publishes no public API pricing or billing documentation. This artifact is a placeholder FOCUS-aligned scaffold for any future private partner integration; meters are illustrative.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: La-Z-Boy Incorporated
  ProviderName: La-Z-Boy
  PublisherName: La-Z-Boy Incorporated
  ServiceCategory: Retail / Furniture
  ServiceName: La-Z-Boy
layout: finops
meters:
- aggregation: sum
  dimensions:
  - integration
  - environment
  name: api_requests
  unit: request
name: La Z Boy Finops
provider_name: La-Z-Boy
provider_slug: la-z-boy
publisher_name: La-Z-Boy Incorporated
service_category: Retail / Furniture
slug: la-z-boy-finops
source_filename: la-z-boy-finops.yml
source_heading: FinOps Profile
source_url: https://www.la-z-boy.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: La-Z-Boy\nproviderId: la-z-boy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Furniture\n  - Retail\ndescription: La-Z-Boy publishes no public API pricing or billing documentation. This artifact is a placeholder\n  FOCUS-aligned scaffold for any future private partner integration; meters are illustrative.\nsources:\n  - https://www.la-z-boy.com/\nnotes: No public pricing or billing model. FinOps shape can only be filled in once a partner agreement\n  exists.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: La-Z-Boy Incorporated\nserviceCategory: Retail / Furniture\nbillingModel:\n  pricingCategory: Contract / Partner\n  billingFrequency:\
  \ Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: La-Z-Boy\n  ServiceCategory: Retail / Furniture\n  ProviderName: La-Z-Boy\n  PublisherName: La-Z-Boy Incorporated\n  InvoiceIssuerName: La-Z-Boy Incorporated\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - integration\n      - environment\nprinciples:\n  - name: Visibility\n    description: No public consumption telemetry; integrators must capture client-side request volumes\n      themselves.\n  - name: Allocation\n    description: Tag any private API calls with the consuming program/business unit to enable internal\n      chargeback against the partner agreement.\n  - name: Optimization\n    description: Cache catalog/dealer data; coordinate batch workflows to reduce request volume on shared\n      partner endpoints.\n  - name: Accountability\n    description: Partnership owner reviews integration\
  \ metrics against the partner agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/la-z-boy/refs/heads/main/finops/la-z-boy-finops.yml
sources:
- https://www.la-z-boy.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Furniture
- Retail
---
