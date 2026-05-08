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
description: 'FOCUS-aligned FinOps for Delek US Holdings: a downstream energy company with no public developer API. No API invoice line exists. Commercial relationships flow through product-supply, terminaling, midstream-logistics, and retail-fuel agreements rather than per-call billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Delek US Holdings, Inc.
  PricingCategory: Contract
  ProviderName: Delek US Holdings
  PublisherName: Delek US Holdings, Inc.
  RegionId: US
  ServiceCategory: Energy
  ServiceName: Delek US Holdings
  ServiceSubcategory: Downstream Petroleum
layout: finops
meters:
- aggregation: max
  description: Active partner integrations (EDI feeds, terminal-automation links, ticketing bridges) across refining, logistics, and retail business lines.
  dimensions:
  - partner
  - business_line
  - integration_type
  name: bilateral_integrations
  unit: integration
name: Delek Us Holdings Finops
provider_name: Delek US Holdings
provider_slug: delek-us-holdings
publisher_name: Delek US Holdings, Inc.
service_category: Energy
slug: delek-us-holdings-finops
source_filename: delek-us-holdings-finops.yml
source_heading: FinOps Profile
source_url: https://www.delekus.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Delek US Holdings\nproviderId: delek-us-holdings\npublisherName: Delek US Holdings, Inc.\nserviceCategory: Energy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Logistics\n  - Petroleum\n  - Refining\n  - Retail\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Delek US Holdings: a downstream energy company with no\n  public developer API. No API invoice line exists. Commercial relationships flow through\n  product-supply, terminaling, midstream-logistics, and retail-fuel agreements rather than per-call\n  billing.'\nsources:\n  - https://www.delekus.com\n  - https://www.deleklogistics.com\n\
  notes: No API consumption to meter. FinOps artifact retained for parity across providers; meters\n  are illustrative of the bilateral-integration shape rather than a billable surface.\nbillingModel:\n  pricingCategory: Bilateral Contracts\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Delek US Holdings\n  ServiceCategory: Energy\n  ServiceSubcategory: Downstream Petroleum\n  ProviderName: Delek US Holdings\n  PublisherName: Delek US Holdings, Inc.\n  InvoiceIssuerName: Delek US Holdings, Inc.\n  PricingCategory: Contract\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  RegionId: US\nmeters:\n  - name: bilateral_integrations\n    description: Active partner integrations (EDI feeds, terminal-automation links, ticketing\n      bridges) across refining, logistics, and retail business lines.\n    unit: integration\n    aggregation: max\n    dimensions:\n      - partner\n      - business_line\n\
  \      - integration_type\nprinciples:\n  - name: Visibility\n    description: There is no API invoice. Track partner-integration spend through procurement,\n      logistics, and IT-services contracts rather than developer-portal usage.\n  - name: Allocation\n    description: Allocate any integration-related cost to the refining, logistics, or retail\n      business unit that owns the partner relationship.\n  - name: Optimization\n    description: Consolidate redundant EDI feeds across affiliates (Delek Logistics, retail\n      stores), prefer modern terminal-automation protocols, and retire legacy bridges to reduce\n      operational toil.\n  - name: Accountability\n    description: Designate a single integration owner per partner per business line so EDI map\n      maintenance and ticketing-bridge SLAs have a clear escalation path.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/delek-us-holdings/refs/heads/main/finops/delek-us-holdings-finops.yml
sources:
- https://www.delekus.com
- https://www.deleklogistics.com
specification: FinOps Framework
tags:
- Energy
- Logistics
- Petroleum
- Refining
- Retail
- FinOps
- FOCUS
---
