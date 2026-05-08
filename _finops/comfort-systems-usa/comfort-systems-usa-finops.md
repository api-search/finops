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
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Project / Service Contract
description: 'FOCUS-aligned FinOps for Comfort Systems USA: project- and contract-priced mechanical/HVAC services. No public API or recurring SaaS spend; meters cover invoice-line abstractions for capital projects and recurring service contracts.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Comfort Systems USA, Inc.
  ProviderName: Comfort Systems USA
  PublisherName: Comfort Systems USA, Inc.
  ServiceCategory: Construction Services
  ServiceName: Comfort Systems USA
layout: finops
meters:
- aggregation: sum
  dimensions:
  - project
  - subsidiary
  name: project_milestones
  unit: milestone
- aggregation: sum
  dimensions:
  - site
  - scope
  name: service_contract
  unit: month
- aggregation: sum
  dimensions:
  - trade
  - region
  name: time_and_materials
  unit: hour
name: Comfort Systems Usa Finops
provider_name: Comfort Systems USA
provider_slug: comfort-systems-usa
publisher_name: Comfort Systems USA, Inc.
service_category: Construction Services
slug: comfort-systems-usa-finops
source_filename: comfort-systems-usa-finops.yml
source_heading: FinOps Profile
source_url: https://www.comfortsystemsusa.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Comfort Systems USA\nproviderId: comfort-systems-usa\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Construction\n  - HVAC\ndescription: 'FOCUS-aligned FinOps for Comfort Systems USA: project- and contract-priced mechanical/HVAC\n  services. No public API or recurring SaaS spend; meters cover invoice-line abstractions for capital\n  projects and recurring service contracts.'\nsources:\n  - https://www.comfortsystemsusa.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Comfort Systems USA, Inc.\nserviceCategory: Construction Services\nbillingModel:\n  pricingCategory: Project / Service Contract\n  billingFrequency: Per-Invoice\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Comfort Systems USA\n  ServiceCategory: Construction Services\n  ProviderName: Comfort Systems USA\n  PublisherName: Comfort Systems USA, Inc.\n  InvoiceIssuerName: Comfort Systems USA, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: project_milestones\n    unit: milestone\n    aggregation: sum\n    dimensions:\n      - project\n      - subsidiary\n  - name: service_contract\n    unit: month\n    aggregation: sum\n    dimensions:\n      - site\n      - scope\n  - name: time_and_materials\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - trade\n      - region\nprinciples:\n  - name: Visibility\n    description: Reconcile project invoices against the schedule of values and change orders; track service-contract\n      utilization.\n  - name: Allocation\n    description: Tag invoices to building, site, or capital project for chargeback.\n  -\
  \ name: Optimization\n    description: Bundle service work; renegotiate multi-site service contracts at renewal; compare bids\n      across Comfort Systems subsidiaries.\n  - name: Accountability\n    description: Facilities/PMO owns project scope; finance owns capital approvals and AP.\nnotes: No public API/SaaS pricing.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/comfort-systems-usa/refs/heads/main/finops/comfort-systems-usa-finops.yml
sources:
- https://www.comfortsystemsusa.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Construction
- HVAC
---
