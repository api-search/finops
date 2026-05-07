---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (per SOW)
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Custom Contract / Managed Services
description: 'FinOps view of ExlService Holdings: invoicing is contract-driven (managed-services retainers, FTE-based, T&M, or outcome-based) rather than usage-metered. The FOCUS shape is professional-services billing rather than a metered API.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: ExlService Holdings, Inc.
  ProviderName: ExlService Holdings
  PublisherName: ExlService Holdings, Inc.
  ServiceCategory: Analytics / Digital Operations / BPO
  ServiceName: ExlService Holdings
layout: finops
meters:
- aggregation: sum
  dimensions:
  - sow
  - cost_center
  name: managed_services_fees
  unit: month
- aggregation: max
  dimensions:
  - role
  - sow
  name: fte_count
  unit: fte
- aggregation: sum
  dimensions:
  - kpi
  - sow
  name: outcome_based_fees
  unit: USD
name: Exlservice Holdings Finops
provider_name: ExlService Holdings
provider_slug: exlservice-holdings
publisher_name: ExlService Holdings, Inc.
service_category: Analytics / Digital Operations / BPO
slug: exlservice-holdings-finops
source_filename: exlservice-holdings-finops.yml
source_heading: FinOps Profile
source_url: https://www.exlservice.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ExlService Holdings\nproviderId: exlservice-holdings\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Analytics\n  - Digital Operations\n  - BPO\ndescription: 'FinOps view of ExlService Holdings: invoicing is contract-driven (managed-services retainers,\n  FTE-based, T&M, or outcome-based) rather than usage-metered. The FOCUS shape is professional-services\n  billing rather than a metered API.'\nsources:\n  - https://www.exlservice.com\nnotes: No public pricing or metered billing. FinOps controls focus on engagement-level budget tracking.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: ExlService Holdings, Inc.\nserviceCategory:\
  \ Analytics / Digital Operations / BPO\nbillingModel:\n  pricingCategory: Custom Contract / Managed Services\n  billingFrequency: Monthly (per SOW)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: ExlService Holdings\n  ServiceCategory: Analytics / Digital Operations / BPO\n  ProviderName: ExlService Holdings\n  PublisherName: ExlService Holdings, Inc.\n  InvoiceIssuerName: ExlService Holdings, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: managed_services_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - sow\n      - cost_center\n  - name: fte_count\n    unit: fte\n    aggregation: max\n    dimensions:\n      - role\n      - sow\n  - name: outcome_based_fees\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - kpi\n      - sow\nprinciples:\n  - name: Visibility\n    description: Track EXL SOW spend in your AP system; reconcile invoices monthly against milestones\n      and FTE consumption reports.\n\
  \  - name: Allocation\n    description: Tag SOWs with consuming business unit/product so engagement spend is allocable.\n  - name: Optimization\n    description: Convert T&M to fixed-fee or outcome-based pricing once volume is predictable; rebadge\n      offshore where appropriate; renegotiate at renewal.\n  - name: Accountability\n    description: Engagement owner approves invoices; finance reviews variance from forecast monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/exlservice-holdings/refs/heads/main/finops/exlservice-holdings-finops.yml
sources:
- https://www.exlservice.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Analytics
- Digital Operations
- BPO
---
