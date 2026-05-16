---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: montran-global-payments-hub-openapi.yml
  format: yaml
  label: Montran Global Payments Hub
  slug: montran-global-payments-hub
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/openapi/montran-global-payments-hub-openapi.yml
- filename: montran-instant-payments-gateway-openapi.yml
  format: yaml
  label: Montran Instant Payments Gateway
  slug: montran-instant-payments-gateway
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/openapi/montran-instant-payments-gateway-openapi.yml
- filename: montran-payments-connectivity-openapi.yml
  format: yaml
  label: Montran Payments Connectivity
  slug: montran-payments-connectivity
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/openapi/montran-payments-connectivity-openapi.yml
- filename: montran-corporate-payments-portal-openapi.yml
  format: yaml
  label: Montran Corporate Payments Portal
  slug: montran-corporate-payments-portal
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/openapi/montran-corporate-payments-portal-openapi.yml
- filename: montran-virtual-accounts-openapi.yml
  format: yaml
  label: Montran Virtual Accounts
  slug: montran-virtual-accounts
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/openapi/montran-virtual-accounts-openapi.yml
- filename: montran-sanctions-screening-openapi.yml
  format: yaml
  label: Montran Sanctions Screening
  slug: montran-sanctions-screening
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/openapi/montran-sanctions-screening-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Enterprise License + Services
description: 'FOCUS-aligned FinOps profile for Montran: enterprise software licensed to central banks and banks. Costs are dominated by perpetual / term licenses, implementation services, and annual support rather than a metered cloud spend. No public usage API.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Montran Corporation
  ProviderName: Montran
  PublisherName: Montran Corporation
  ServiceCategory: Payments Software
  ServiceName: Montran
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  - environment
  name: license_fees
  unit: year
- aggregation: sum
  dimensions:
  - product
  - phase
  name: implementation_services
  unit: project
- aggregation: sum
  dimensions:
  - product
  - tier
  name: support_maintenance
  unit: year
name: Montran Finops
provider_name: Montran
provider_slug: montran
publisher_name: Montran Corporation
service_category: Payments / Capital Markets Software
slug: montran-finops
source_filename: montran-finops.yml
source_heading: FinOps Profile
source_url: https://www.montran.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Montran\nproviderId: montran\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Payments\n  - Banking\n  - Capital Markets\ndescription: 'FOCUS-aligned FinOps profile for Montran: enterprise software licensed to central banks\n  and banks. Costs are dominated by perpetual / term licenses, implementation services, and annual support\n  rather than a metered cloud spend. No public usage API.'\nsources:\n  - https://www.montran.com\nnotes: Reconciliation set to false absent a public billing surface. License-based cost model documented\n  per general industry practice for payments software.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Montran Corporation\nserviceCategory: Payments / Capital Markets Software\nbillingModel:\n  pricingCategory: Enterprise License + Services\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Montran\n  ServiceCategory: Payments Software\n  ProviderName: Montran\n  PublisherName: Montran Corporation\n  InvoiceIssuerName: Montran Corporation\n  BillingCurrency: USD\nmeters:\n  - name: license_fees\n    unit: year\n    aggregation: sum\n    dimensions:\n      - product\n      - environment\n  - name: implementation_services\n    unit: project\n    aggregation: sum\n    dimensions:\n      - product\n      - phase\n  - name: support_maintenance\n    unit: year\n    aggregation: sum\n    dimensions:\n      - product\n      - tier\nprinciples:\n  - name: Visibility\n    description: Track Montran license, implementation, and support invoices in the financial system; product-line\n      visibility comes from\
  \ the deployed Montran modules (Instant Payments Gateway, Corporate Payments Portal,\n      RTGS, etc.).\n  - name: Allocation\n    description: Allocate Montran spend by product line and operating environment (production, DR, sandbox)\n      so payments operations and IT each carry their share.\n  - name: Optimization\n    description: Optimization is realized through scope at procurement (which modules and environments\n      are licensed) and right-sizing the infrastructure footprint that hosts Montran.\n  - name: Accountability\n    description: Payments operations owns the business case; IT owns the hosting cost; procurement owns\n      the renewal calendar.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/finops/montran-finops.yml
sources:
- https://www.montran.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Payments
- Banking
- Capital Markets
---
