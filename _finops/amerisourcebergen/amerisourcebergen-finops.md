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
  - Usage
  pricingCategory: Not Applicable
description: FOCUS-aligned FinOps placeholder for AmerisourceBergen / Cencora. There is no developer API metered billing surface; pharmaceutical distribution is invoiced as cost-of-goods plus distribution fees under master agreements, outside the scope of API FinOps.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Cencora, Inc.
  ProviderName: AmerisourceBergen
  PublisherName: Cencora, Inc.
  ServiceCategory: Pharmaceutical Distribution
  ServiceName: AmerisourceBergen
layout: finops
meters:
- aggregation: sum
  description: Placeholder; not currently billed by Cencora as a developer line item
  dimensions:
  - consumer
  name: api_requests
  unit: request
name: Amerisourcebergen Finops
provider_name: AmerisourceBergen
provider_slug: amerisourcebergen
publisher_name: Cencora, Inc.
service_category: Pharmaceutical Distribution
slug: amerisourcebergen-finops
source_filename: amerisourcebergen-finops.yml
source_heading: FinOps Profile
source_url: https://www.cencora.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: AmerisourceBergen\nproviderId: amerisourcebergen\npublisherName: Cencora, Inc.\nserviceCategory: Pharmaceutical Distribution\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Pharmaceutical Distribution\n  - Healthcare\ndescription: >-\n  FOCUS-aligned FinOps placeholder for AmerisourceBergen / Cencora. There is no\n  developer API metered billing surface; pharmaceutical distribution is\n  invoiced as cost-of-goods plus distribution fees under master agreements,\n  outside the scope of API FinOps.\nnotes: >-\n  No public API billing surface. Charges flow through distribution agreements\n  rather\
  \ than per-request invoices.\nsources:\n  - https://www.cencora.com\nbillingModel:\n  pricingCategory: Not Applicable\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: AmerisourceBergen\n  ServiceCategory: Pharmaceutical Distribution\n  ProviderName: AmerisourceBergen\n  PublisherName: Cencora, Inc.\n  InvoiceIssuerName: Cencora, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    description: Placeholder; not currently billed by Cencora as a developer line item\n    unit: request\n    aggregation: sum\n    dimensions:\n      - consumer\nprinciples:\n  - name: Visibility\n    description: >-\n      Cencora customers see consumption through EDI usage reporting and\n      ordering portals, not through a public usage API.\n  - name: Allocation\n    description: >-\n      Allocate any integration costs to the supply-chain or procurement\n      function that owns the Cencora relationship.\n  - name: Optimization\n\
  \    description: >-\n      Cost levers are batching of EDI documents, order consolidation, and\n      contract pricing tiers, not API request optimization.\n  - name: Accountability\n    description: >-\n      Budget ownership sits with procurement and supply-chain leadership; FinOps\n      practitioners should partner with them rather than treat this as an API\n      spend line.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amerisourcebergen/refs/heads/main/finops/amerisourcebergen-finops.yml
sources:
- https://www.cencora.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Pharmaceutical Distribution
- Healthcare
---
