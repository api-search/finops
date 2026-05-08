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
  - Purchase
  pricingCategory: Contract-Negotiated
description: FinOps shape for Western & Southern Financial Group is contract-driven; the holding company does not publish a public API pricing surface, so meters and FOCUS columns are minimum placeholders.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Western and Southern Life Insurance Company
  ProviderName: Western & Southern Financial Group
  PublisherName: The Western and Southern Life Insurance Company
  ServiceCategory: Insurance
  ServiceName: Western & Southern Financial Group
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  - subsidiary
  name: contracted_service
  unit: varies
name: Western And Southern Financial Finops
provider_name: western-and-southern-financial
provider_slug: western-and-southern-financial
publisher_name: The Western and Southern Life Insurance Company
service_category: Insurance
slug: western-and-southern-financial-finops
source_filename: western-and-southern-financial-finops.yml
source_heading: FinOps Profile
source_url: https://www.westernsouthern.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Western & Southern Financial Group\nproviderId: western-and-southern-financial\npublisherName: The Western and Southern Life Insurance Company\nserviceCategory: Insurance\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Insurance\n  - Financial Services\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps shape for Western & Southern Financial Group is contract-driven; the holding company does not publish a public API pricing surface, so meters and FOCUS columns are minimum placeholders.\nsources:\n  - https://www.westernsouthern.com\nnotes: No public pricing/billing pages exist. Populate meters and chargeCategories\
  \ from an actual producer / institutional contract once one exists.\nbillingModel:\n  pricingCategory: Contract-Negotiated\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Western & Southern Financial Group\n  ServiceCategory: Insurance\n  ProviderName: Western & Southern Financial Group\n  PublisherName: The Western and Southern Life Insurance Company\n  InvoiceIssuerName: The Western and Southern Life Insurance Company\n  BillingCurrency: USD\nmeters:\n  - name: contracted_service\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - subsidiary\nprinciples:\n  - name: Visibility\n    description: Consumption signal comes from contracted producer / distribution reporting; no public usage API.\n  - name: Allocation\n    description: Spend is allocated by subsidiary brand (Western & Southern Life, Gerber Life, Touchstone, Fort Washington) and contract.\n  - name: Optimization\n\
  \    description: Optimization is commercial - distribution mix, product selection, contract renegotiation.\n  - name: Accountability\n    description: Owned by the integrating partner's finance / treasury function; technical teams own only the integration surface.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/western-and-southern-financial/refs/heads/main/finops/western-and-southern-financial-finops.yml
sources:
- https://www.westernsouthern.com
specification: FinOps Framework
tags:
- Insurance
- Financial Services
- FinOps
- FOCUS
- Contact Sales
---
