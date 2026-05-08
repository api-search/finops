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
  label: Temenos Transact API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.temenos.com/transact/openapi.json
- filename: openapi.json
  format: json
  label: Temenos Infinity API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.temenos.com/infinity/openapi.json
- filename: openapi.json
  format: json
  label: Temenos Payments API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.temenos.com/payments/openapi.json
- filename: openapi.json
  format: json
  label: Temenos Fund Administration API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.temenos.com/funds/openapi.json
- filename: openapi.json
  format: json
  label: Temenos Financial Crime Mitigation API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.temenos.com/fcm/openapi.json
- filename: temenos-data-hub-openapi.yml
  format: yaml
  label: Temenos Transact Data Hub API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-data-hub-openapi.yml
- filename: temenos-wealth-openapi.yml
  format: yaml
  label: Temenos Wealth API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-wealth-openapi.yml
- filename: temenos-enterprise-product-pricing-openapi.yml
  format: yaml
  label: Temenos Enterprise Product and Pricing API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-enterprise-product-pricing-openapi.yml
- filename: temenos-cloud-banking-openapi.yml
  format: yaml
  label: Temenos Cloud Banking (CMB) API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-cloud-banking-openapi.yml
- filename: temenos-journey-manager-openapi.yml
  format: yaml
  label: Temenos Journey Manager API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-journey-manager-openapi.yml
- filename: temenos-microservices-openapi.yml
  format: yaml
  label: Temenos Transact Microservices API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-microservices-openapi.yml
- filename: temenos-bnpl-openapi.yml
  format: yaml
  label: Temenos Buy Now Pay Later API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-bnpl-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps scaffold for Temenos. Temenos sells software licenses and SaaS subscriptions to financial institutions; commercial terms are sales-led and there is no public usage-based price list to map to FOCUS columns until a deployment is in place.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Temenos AG
  ProviderName: Temenos
  PublisherName: Temenos AG
  ServiceCategory: Banking Software
  ServiceName: Temenos
layout: finops
meters:
- aggregation: sum
  dimensions:
  - module
  - deployment_model
  name: license_fees
  unit: varies
name: Temenos Finops
provider_name: Temenos
provider_slug: temenos
publisher_name: Temenos AG
service_category: Banking Software
slug: temenos-finops
source_filename: temenos-finops.yml
source_heading: FinOps Profile
source_url: https://www.temenos.com/products/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Temenos\nproviderId: temenos\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Core Banking\n  - Financial Services\ndescription: >-\n  FOCUS-aligned FinOps scaffold for Temenos. Temenos sells software licenses and SaaS subscriptions to\n  financial institutions; commercial terms are sales-led and there is no public usage-based price list\n  to map to FOCUS columns until a deployment is in place.\nsources:\n  - https://www.temenos.com/products/\n  - https://www.temenos.com/contact/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: >-\n  No public usage telemetry or programmatic billing surface. Reconciliation is deployment-specific.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: Temenos AG\nserviceCategory: Banking Software\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Temenos\n  ServiceCategory: Banking Software\n  ProviderName: Temenos\n  PublisherName: Temenos AG\n  InvoiceIssuerName: Temenos AG\n  BillingCurrency: USD\nmeters:\n  - name: license_fees\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - module\n      - deployment_model\nprinciples:\n  - name: Visibility\n    description: Temenos invoices and the bank's internal cost-allocation systems are the primary visibility\n      surface; no shared multi-tenant usage API is published.\n  - name: Allocation\n    description: Allocate license / SaaS spend across bank business units (retail, corporate, wealth) based\n      on the modules each unit consumes per the master agreement.\n  - name: Optimization\n\
  \    description: Right-size deployment topology, retire unused modules at renewal, and consolidate environments\n      to reduce non-prod license footprint.\n  - name: Accountability\n    description: Bank CIO / core banking program owner is accountable for Temenos spend and reviews growth\n      against the contractual baseline at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/finops/temenos-finops.yml
sources:
- https://www.temenos.com/products/
- https://www.temenos.com/contact/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Core Banking
- Financial Services
---
