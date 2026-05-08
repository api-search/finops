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
  - Usage
  pricingCategory: Custom / Contact Sales
description: FinOps placeholder for Synovus Financial. Pricing and billing meters are not publicly disclosed; consumption-cost mapping is established per commercial banking integration contract.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Synovus Financial Corp.
  ProviderName: Synovus Financial
  PublisherName: Synovus Financial Corp.
  ServiceCategory: Banking
  ServiceName: Synovus Financial
layout: finops
meters:
- aggregation: sum
  name: custom_engagement
  unit: varies
name: Synovus Financial Finops
provider_name: Synovus Financial
provider_slug: synovus-financial
publisher_name: Synovus Financial Corp.
service_category: Banking
slug: synovus-financial-finops
source_filename: synovus-financial-finops.yml
source_heading: FinOps Profile
source_url: https://www.synovus.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Synovus Financial\nproviderId: synovus-financial\npublisherName: Synovus Financial Corp.\nserviceCategory: Banking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Financial Services\n  - FinOps\n  - FOCUS\ndescription: FinOps placeholder for Synovus Financial. Pricing and billing meters are not publicly\n  disclosed; consumption-cost mapping is established per commercial banking integration contract.\nsources:\n  - https://www.synovus.com/\nnotes: No public billing or usage telemetry surface documented. Meter list collapsed to a single\n  custom-engagement line pending direct provider confirmation.\nbillingModel:\n\
  \  pricingCategory: Custom / Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Synovus Financial\n  ServiceCategory: Banking\n  ProviderName: Synovus Financial\n  PublisherName: Synovus Financial Corp.\n  InvoiceIssuerName: Synovus Financial Corp.\n  BillingCurrency: USD\nmeters:\n  - name: custom_engagement\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Consumption visibility is provided through statements and reports negotiated\n      under the Synovus commercial banking agreement; no public usage API is documented.\n  - name: Allocation\n    description: Cost allocation is handled through the customer's own accounts-payable and\n      treasury reconciliation against Synovus invoices.\n  - name: Optimization\n    description: Optimization levers (transaction routing, account structure, fee tiers) are\n      addressed through the Synovus relationship manager.\n\
  \  - name: Accountability\n    description: Spend accountability sits with the treasury or finance team holding the Synovus\n      banking relationship.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/synovus-financial/refs/heads/main/finops/synovus-financial-finops.yml
sources:
- https://www.synovus.com/
specification: FinOps Framework
tags:
- Banking
- Financial Services
- FinOps
- FOCUS
---
