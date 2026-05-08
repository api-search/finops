---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: biogen-developer-api-openapi.yml
  format: yaml
  label: Biogen Developer API
  slug: developer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/biogen/refs/heads/main/openapi/biogen-developer-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Enterprise / Contract Negotiated
description: 'FOCUS-aligned FinOps placeholder for Biogen: no public developer pricing surface identified, so spend is modeled as B2B partner / commercial contract activity rather than per-call metered usage.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Biogen Inc.
  ProviderName: Biogen
  PublisherName: Biogen Inc.
  ServiceCategory: Life Sciences
  ServiceName: Biogen
layout: finops
meters:
- aggregation: count
  dimensions:
  - partner_type
  - region
  name: partner_contract
  unit: contract
- aggregation: sum
  dimensions:
  - partner
  - dataset
  name: data_access_requests
  unit: request
name: Biogen Finops
provider_name: Biogen
provider_slug: biogen
publisher_name: Biogen Inc.
service_category: Life Sciences / Pharmaceuticals
slug: biogen-finops
source_filename: biogen-finops.yml
source_heading: FinOps Profile
source_url: https://www.biogen.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Biogen\nproviderId: biogen\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Biotechnology\n  - Healthcare\n  - Life Sciences\ndescription: 'FOCUS-aligned FinOps placeholder for Biogen: no public developer pricing surface\n  identified, so spend is modeled as B2B partner / commercial contract activity rather than per-call\n  metered usage.'\nsources:\n  - https://www.biogen.com\nnotes: No public Biogen API pricing or billing documentation found; reconcile if/when a developer\n  portal launches.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Biogen Inc.\nserviceCategory: Life Sciences / Pharmaceuticals\nbillingModel:\n  pricingCategory:\
  \ Enterprise / Contract Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Biogen\n  ServiceCategory: Life Sciences\n  ProviderName: Biogen\n  PublisherName: Biogen Inc.\n  InvoiceIssuerName: Biogen Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: partner_contract\n    unit: contract\n    aggregation: count\n    dimensions:\n      - partner_type\n      - region\n  - name: data_access_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - dataset\nprinciples:\n  - name: Visibility\n    description: No public usage telemetry; rely on contractual reporting clauses with the Biogen\n      partner contact.\n  - name: Allocation\n    description: Attribute partner agreement spend to the consuming therapeutic area / clinical\n      program through the contract repository.\n  - name: Optimization\n    description: Consolidate partner\
  \ agreements at the enterprise level to lift volume-tier\n      thresholds where Biogen offers them.\n  - name: Accountability\n    description: Assign a contract owner per Biogen agreement; review quarterly against business\n      outcomes for the program being supported.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/biogen/refs/heads/main/finops/biogen-finops.yml
sources:
- https://www.biogen.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Biotechnology
- Healthcare
- Life Sciences
---
