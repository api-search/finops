---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Purchase
  pricingCategory: N/A
description: FinOps view for Apogee Enterprises is illustrative only. The company is an architectural products manufacturer with no published commercial developer API, so there is no API billing model to align with FOCUS at this time.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Apogee Enterprises, Inc.
  ProviderName: Apogee Enterprises
  PublisherName: Apogee Enterprises, Inc.
  ServiceCategory: Architectural Products
  ServiceName: Apogee Enterprises Partner Integration
layout: finops
meters:
- aggregation: sum
  description: Per-contract value of a partner / customer integration agreement
  dimensions:
  - partner
  name: integration_contract
  unit: contract
name: Apog Enterprises Finops
provider_name: Apogee Enterprises
provider_slug: apog-enterprises
publisher_name: Apogee Enterprises, Inc.
service_category: Architectural Products
slug: apog-enterprises-finops
source_filename: apog-enterprises-finops.yml
source_heading: FinOps Profile
source_url: https://www.apog.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Apogee Enterprises\nproviderId: apog-enterprises\npublisherName: Apogee Enterprises, Inc.\nserviceCategory: Architectural Products\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Architectural\n  - Glass\ndescription: FinOps view for Apogee Enterprises is illustrative only. The company is an architectural\n  products manufacturer with no published commercial developer API, so there is no API billing model to\n  align with FOCUS at this time.\nnotes: No public API billing exists. Placeholder structure retained for schema completeness.\nsources:\n  - https://www.apog.com\nbillingModel:\n  pricingCategory:\
  \ N/A\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Apogee Enterprises Partner Integration\n  ServiceCategory: Architectural Products\n  ProviderName: Apogee Enterprises\n  PublisherName: Apogee Enterprises, Inc.\n  InvoiceIssuerName: Apogee Enterprises, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: integration_contract\n    description: Per-contract value of a partner / customer integration agreement\n    unit: contract\n    aggregation: sum\n    dimensions:\n      - partner\nprinciples:\n  - name: Visibility\n    description: Track partner integration usage via private B2B contract reporting; no public telemetry\n      surface exists.\n  - name: Allocation\n    description: Allocate any integration cost back to the operating segment (Framing, Glass, Services,\n      Optical) consuming it.\n  - name: Optimization\n    description: Consolidate partner integrations to shared interfaces\
  \ where possible; renegotiate at\n      contract renewal.\n  - name: Accountability\n    description: IT or operating-segment business owner owns each partner integration contract and renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apog-enterprises/refs/heads/main/finops/apog-enterprises-finops.yml
sources:
- https://www.apog.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Architectural
- Glass
---
