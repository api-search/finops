---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Temenos Transact Core Banking API
  slug: temenos-transact-core-banking-api
  spec_type: OpenAPI
  url: https://developer.temenos.com/transact/openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps scaffold for Temenos Transact. Sold as on-prem licenses or SaaS subscriptions to banks; commercial terms are sales-led and there is no public usage-based price list to map to FOCUS columns until a deployment is in place.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Temenos AG
  ProviderName: Temenos
  PublisherName: Temenos AG
  ServiceCategory: Banking Software
  ServiceName: Temenos Transact
layout: finops
meters:
- aggregation: sum
  dimensions:
  - module
  - deployment_model
  name: license_fees
  unit: varies
name: Temenos Transact Finops
provider_name: Temenos Transact
provider_slug: temenos-transact
publisher_name: Temenos AG
service_category: Banking Software
slug: temenos-transact-finops
source_filename: temenos-transact-finops.yml
source_heading: FinOps Profile
source_url: https://www.temenos.com/products/core-banking/transact/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Temenos Transact\nproviderId: temenos-transact\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Core Banking\n  - Financial Services\ndescription: >-\n  FOCUS-aligned FinOps scaffold for Temenos Transact. Sold as on-prem licenses or SaaS subscriptions to\n  banks; commercial terms are sales-led and there is no public usage-based price list to map to FOCUS\n  columns until a deployment is in place.\nsources:\n  - https://www.temenos.com/products/core-banking/transact/\n  - https://www.temenos.com/contact/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: >-\n  No public usage telemetry or programmatic billing surface. Reconciliation is deployment-specific.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Temenos AG\nserviceCategory: Banking Software\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Temenos Transact\n  ServiceCategory: Banking Software\n  ProviderName: Temenos\n  PublisherName: Temenos AG\n  InvoiceIssuerName: Temenos AG\n  BillingCurrency: USD\nmeters:\n  - name: license_fees\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - module\n      - deployment_model\nprinciples:\n  - name: Visibility\n    description: Temenos invoices and the bank's internal cost-allocation systems are the primary visibility\n      surface; no shared multi-tenant Transact usage API exists.\n  - name: Allocation\n    description: Allocate Transact license / SaaS spend across bank business units based on the Transact\n      modules each consumes per the master agreement.\n\
  \  - name: Optimization\n    description: Right-size deployment topology, retire unused modules at renewal, and consolidate non-prod\n      environments to reduce license footprint.\n  - name: Accountability\n    description: Bank core-banking program owner is accountable for Transact spend and reviews growth against\n      contractual baselines at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/temenos-transact/refs/heads/main/finops/temenos-transact-finops.yml
sources:
- https://www.temenos.com/products/core-banking/transact/
- https://www.temenos.com/contact/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Core Banking
- Financial Services
---
