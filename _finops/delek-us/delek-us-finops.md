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
  - Purchase
  - Adjustment
  pricingCategory: Bilateral Contracts
description: 'FOCUS-aligned FinOps for Delek US: Delek US is a downstream energy company without a public developer API. There is no API invoice line. Commercial relationships flow through product-supply, terminaling, and retail-fuel agreements rather than per-call billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Delek US Holdings, Inc.
  PricingCategory: Contract
  ProviderName: Delek US
  PublisherName: Delek US Holdings, Inc.
  RegionId: US
  ServiceCategory: Energy
  ServiceName: Delek US
  ServiceSubcategory: Downstream Petroleum
layout: finops
meters:
- aggregation: max
  description: Active partner integrations (EDI feeds, terminal-automation links, ticketing bridges).
  dimensions:
  - partner
  - integration_type
  name: bilateral_integrations
  unit: integration
name: Delek Us Finops
provider_name: Delek US
provider_slug: delek-us
publisher_name: Delek US Holdings, Inc.
service_category: Energy
slug: delek-us-finops
source_filename: delek-us-finops.yml
source_heading: FinOps Profile
source_url: https://www.delekus.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Delek US\nproviderId: delek-us\npublisherName: Delek US Holdings, Inc.\nserviceCategory: Energy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Petroleum\n  - Refining\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Delek US: Delek US is a downstream energy company without a\n  public developer API. There is no API invoice line. Commercial relationships flow through\n  product-supply, terminaling, and retail-fuel agreements rather than per-call billing.'\nsources:\n  - https://www.delekus.com\nnotes: No API consumption to meter. FinOps artifact retained for parity across providers; meters\n\
  \  are illustrative of the bilateral-integration shape rather than a billable surface.\nbillingModel:\n  pricingCategory: Bilateral Contracts\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Delek US\n  ServiceCategory: Energy\n  ServiceSubcategory: Downstream Petroleum\n  ProviderName: Delek US\n  PublisherName: Delek US Holdings, Inc.\n  InvoiceIssuerName: Delek US Holdings, Inc.\n  PricingCategory: Contract\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  RegionId: US\nmeters:\n  - name: bilateral_integrations\n    description: Active partner integrations (EDI feeds, terminal-automation links, ticketing\n      bridges).\n    unit: integration\n    aggregation: max\n    dimensions:\n      - partner\n      - integration_type\nprinciples:\n  - name: Visibility\n    description: There is no API invoice. Track partner-integration spend through procurement and\n      logistics contracts rather\
  \ than developer-portal usage.\n  - name: Allocation\n    description: Allocate any integration-related cost to the trading or logistics business unit\n      that owns the partner relationship.\n  - name: Optimization\n    description: Consolidate redundant EDI feeds and prefer modern terminal-automation protocols\n      where retiring legacy bridges reduces operational toil.\n  - name: Accountability\n    description: Designate a single integration owner per partner so EDI map maintenance and\n      ticketing-bridge SLAs have a clear escalation path.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/delek-us/refs/heads/main/finops/delek-us-finops.yml
sources:
- https://www.delekus.com
specification: FinOps Framework
tags:
- Energy
- Petroleum
- Refining
- FinOps
- FOCUS
---
