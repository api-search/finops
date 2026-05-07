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
description: FOCUS-aligned FinOps placeholder for Amphenol. Amphenol has no public API metered billing surface; spend on Amphenol parts flows as direct material cost through ERP systems and distributor invoices, outside API FinOps scope.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Amphenol Corporation
  ProviderName: Amphenol
  PublisherName: Amphenol Corporation
  ServiceCategory: Electronic Components
  ServiceName: Amphenol
layout: finops
meters:
- aggregation: sum
  description: Placeholder; not billed as a developer line item
  dimensions:
  - consumer
  name: api_requests
  unit: request
name: Amphenol Finops
provider_name: Amphenol
provider_slug: amphenol
publisher_name: Amphenol Corporation
service_category: Electronic Components
slug: amphenol-finops
source_filename: amphenol-finops.yml
source_heading: FinOps Profile
source_url: https://www.amphenol.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Amphenol\nproviderId: amphenol\npublisherName: Amphenol Corporation\nserviceCategory: Electronic Components\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Electronic Connectors\n  - Interconnect Systems\ndescription: >-\n  FOCUS-aligned FinOps placeholder for Amphenol. Amphenol has no public API\n  metered billing surface; spend on Amphenol parts flows as direct material\n  cost through ERP systems and distributor invoices, outside API FinOps scope.\nnotes: >-\n  No public API billing surface. Costs are component direct material.\nsources:\n  - https://www.amphenol.com\nbillingModel:\n  pricingCategory:\
  \ Not Applicable\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Amphenol\n  ServiceCategory: Electronic Components\n  ProviderName: Amphenol\n  PublisherName: Amphenol Corporation\n  InvoiceIssuerName: Amphenol Corporation\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    description: Placeholder; not billed as a developer line item\n    unit: request\n    aggregation: sum\n    dimensions:\n      - consumer\nprinciples:\n  - name: Visibility\n    description: >-\n      Visibility into Amphenol spend is via ERP material ledgers and\n      distributor invoices, not API telemetry.\n  - name: Allocation\n    description: >-\n      Allocate to BOMs / product lines rather than to API consumers.\n  - name: Optimization\n    description: >-\n      Optimization levers are part consolidation, alternates, and volume\n      contracts, not request optimization.\n  - name: Accountability\n    description: >-\n\
  \      Procurement and operations own this spend, not the developer / FinOps API\n      practice.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amphenol/refs/heads/main/finops/amphenol-finops.yml
sources:
- https://www.amphenol.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Electronic Connectors
- Interconnect Systems
---
