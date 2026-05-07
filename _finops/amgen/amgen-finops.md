---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories:
  - Purchase
  pricingCategory: Not Applicable
description: FOCUS-aligned FinOps placeholder for Amgen. Amgen has no public API metered billing surface; commercial spend on Amgen relates to therapy procurement through GPOs, distributors, and payers, which sits outside API FinOps.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Amgen Inc.
  ProviderName: Amgen
  PublisherName: Amgen Inc.
  ServiceCategory: Biopharmaceutical
  ServiceName: Amgen
layout: finops
meters:
- aggregation: sum
  description: Placeholder; not billed as a developer line item
  dimensions:
  - consumer
  name: api_requests
  unit: request
name: Amgen Finops
provider_name: Amgen
provider_slug: amgen
publisher_name: Amgen Inc.
service_category: Biopharmaceutical
slug: amgen-finops
source_filename: amgen-finops.yml
source_heading: FinOps Profile
source_url: https://www.amgen.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Amgen\nproviderId: amgen\npublisherName: Amgen Inc.\nserviceCategory: Biopharmaceutical\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Biotechnology\n  - Biopharmaceutical\ndescription: >-\n  FOCUS-aligned FinOps placeholder for Amgen. Amgen has no public API metered\n  billing surface; commercial spend on Amgen relates to therapy procurement\n  through GPOs, distributors, and payers, which sits outside API FinOps.\nnotes: >-\n  No public API billing surface.\nsources:\n  - https://www.amgen.com\nbillingModel:\n  pricingCategory: Not Applicable\n  billingFrequency: Not Applicable\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Amgen\n  ServiceCategory: Biopharmaceutical\n  ProviderName: Amgen\n  PublisherName: Amgen Inc.\n  InvoiceIssuerName: Amgen Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    description: Placeholder; not billed as a developer line item\n    unit: request\n    aggregation: sum\n    dimensions:\n      - consumer\nprinciples:\n  - name: Visibility\n    description: >-\n      No Amgen-issued developer telemetry. Therapy spend visibility lives in\n      payer / distributor systems.\n  - name: Allocation\n    description: >-\n      Allocate Amgen-related costs through procurement and clinical operations,\n      not API consumer tags.\n  - name: Optimization\n    description: >-\n      Optimization levers (formulary, prior auth, biosimilar substitution) are\n      outside developer scope.\n  - name: Accountability\n    description: >-\n      Budget ownership sits with pharmacy, clinical, and procurement\
  \ leaders.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amgen/refs/heads/main/finops/amgen-finops.yml
sources:
- https://www.amgen.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Biotechnology
- Biopharmaceutical
---
