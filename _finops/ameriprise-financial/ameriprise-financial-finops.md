---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ameriprise.yml
  format: yaml
  label: Ameriprise Financial Website
  slug: website
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ameriprise-financial/refs/heads/main/openapi/ameriprise.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories:
  - Usage
  pricingCategory: Not Applicable
description: FOCUS-aligned FinOps placeholder for Ameriprise Financial. Ameriprise does not publish a developer API or metered billing surface, so there are no API meters, charge categories, or invoice issuer columns to reconcile. This document keeps the FinOps shape so downstream tooling can iterate, but the meters listed are nominal.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Ameriprise Financial, Inc.
  ProviderName: Ameriprise Financial
  PublisherName: Ameriprise Financial, Inc.
  ServiceCategory: Financial Services
  ServiceName: Ameriprise Financial
layout: finops
meters:
- aggregation: sum
  description: Placeholder; not currently billed by Ameriprise
  dimensions:
  - consumer
  name: api_requests
  unit: request
name: Ameriprise Financial Finops
provider_name: Ameriprise Financial
provider_slug: ameriprise-financial
publisher_name: Ameriprise Financial, Inc.
service_category: Financial Services
slug: ameriprise-financial-finops
source_filename: ameriprise-financial-finops.yml
source_heading: FinOps Profile
source_url: https://www.ameriprise.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Ameriprise Financial\nproviderId: ameriprise-financial\npublisherName: Ameriprise Financial, Inc.\nserviceCategory: Financial Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Financial Services\n  - Wealth Management\ndescription: >-\n  FOCUS-aligned FinOps placeholder for Ameriprise Financial. Ameriprise does\n  not publish a developer API or metered billing surface, so there are no API\n  meters, charge categories, or invoice issuer columns to reconcile. This\n  document keeps the FinOps shape so downstream tooling can iterate, but the\n  meters listed are nominal.\nnotes: >-\n  No public\
  \ API billing surface. Replace meters with provider-issued line items\n  if Ameriprise launches a developer program.\nsources:\n  - https://www.ameriprise.com\nbillingModel:\n  pricingCategory: Not Applicable\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Ameriprise Financial\n  ServiceCategory: Financial Services\n  ProviderName: Ameriprise Financial\n  PublisherName: Ameriprise Financial, Inc.\n  InvoiceIssuerName: Ameriprise Financial, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    description: Placeholder; not currently billed by Ameriprise\n    unit: request\n    aggregation: sum\n    dimensions:\n      - consumer\nprinciples:\n  - name: Visibility\n    description: >-\n      No Ameriprise-issued usage telemetry exists for developers. If integrating\n      via Plaid or similar aggregators, rely on the aggregator's usage dashboard.\n  - name: Allocation\n    description: >-\n      Allocate\
  \ any third-party aggregator costs to the consuming team or\n      product, since Ameriprise itself does not invoice for API consumption.\n  - name: Optimization\n    description: >-\n      The primary cost lever is aggregator selection and per-item pricing\n      (Plaid, MX, Finicity), not Ameriprise tariffs.\n  - name: Accountability\n    description: >-\n      Budget ownership sits with whichever team contracts the aggregator that\n      provides Ameriprise account connectivity.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ameriprise-financial/refs/heads/main/finops/ameriprise-financial-finops.yml
sources:
- https://www.ameriprise.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Financial Services
- Wealth Management
---
