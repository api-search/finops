---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: regions-open-banking-openapi.yml
  format: yaml
  label: Regions Open Banking API
  slug: regions-open-banking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/regions-financial/refs/heads/main/openapi/regions-open-banking-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: FinOps shape for Regions Financial banking integrations. Spend is invoiced under treasury-management or aggregator contracts; there is no metered self-serve API to reconcile.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Regions Bank
  ProviderName: Regions Financial
  PublisherName: Regions Bank
  ServiceCategory: Banking
  ServiceName: Regions Bank
layout: finops
meters:
- aggregation: sum
  name: contract_term
  unit: month
name: Regions Financial Finops
provider_name: regions-financial
provider_slug: regions-financial
publisher_name: Regions Bank
service_category: Banking
slug: regions-financial-finops
source_filename: regions-financial-finops.yml
source_heading: FinOps Profile
source_url: https://www.regions.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: regions-financial\nproviderId: regions-financial\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Banking\n  - FDX\ndescription: FinOps shape for Regions Financial banking integrations. Spend is invoiced under treasury-management\n  or aggregator contracts; there is no metered self-serve API to reconcile.\nsources:\n  - https://www.regions.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Regions Bank\nserviceCategory: Banking\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Regions Bank\n  ServiceCategory:\
  \ Banking\n  ProviderName: Regions Financial\n  PublisherName: Regions Bank\n  InvoiceIssuerName: Regions Bank\n  BillingCurrency: USD\nmeters:\n  - name: contract_term\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the Regions treasury-management or aggregator invoice; no programmatic\n      usage feed for FDX or commercial APIs is published.\n  - name: Allocation\n    description: Allocate to the corporate treasury function (commercial APIs) or to the aggregator product\n      that consumes the FDX feed.\n  - name: Optimization\n    description: Optimization is contractual — bundle treasury services, renegotiate aggregator scope,\n      and consolidate authentication endpoints under one agreement.\n  - name: Accountability\n    description: Owner is the corporate-treasury or aggregator-management function that holds the Regions\n      contract.\nnotes: Bank integrations are contractual and aggregator-mediated; no metered\
  \ API. Generic FOCUS request\n  meters removed.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/regions-financial/refs/heads/main/finops/regions-financial-finops.yml
sources:
- https://www.regions.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking
- FDX
---
