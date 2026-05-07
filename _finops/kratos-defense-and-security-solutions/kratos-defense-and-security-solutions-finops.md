---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice / Milestone
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Government Contract (FFP / CPFF / T&M / OTA)
description: 'FinOps shape for Kratos: defense-contractor billing under government / commercial-defense contract vehicles. No public API tariff; cost lines are program-specific and follow contract type (FFP, CPFF, T&M, OTA, GSA schedule).'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Kratos Defense & Security Solutions, Inc.
  ProviderName: Kratos Defense & Security Solutions
  PublisherName: Kratos Defense & Security Solutions, Inc.
  ServiceCategory: Defense
  ServiceName: Kratos Defense & Security Solutions
layout: finops
meters:
- aggregation: count
  dimensions:
  - program
  - clin
  name: program_milestones
  unit: milestone
- aggregation: sum
  dimensions:
  - labor_category
  - program
  name: labor_hours
  unit: hour
- aggregation: sum
  dimensions:
  - endpoint
  - program
  name: api_calls
  unit: request
- aggregation: max
  dimensions:
  - product
  - program
  name: license_seats
  unit: seat
- aggregation: max
  dimensions:
  - product
  name: managed_assets
  unit: asset
name: Kratos Defense And Security Solutions Finops
provider_name: Kratos Defense & Security Solutions
provider_slug: kratos-defense-and-security-solutions
publisher_name: Kratos Defense & Security Solutions, Inc.
service_category: Defense Technology
slug: kratos-defense-and-security-solutions-finops
source_filename: kratos-defense-and-security-solutions-finops.yml
source_heading: FinOps Profile
source_url: https://www.kratosdefense.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Kratos Defense & Security Solutions\nproviderId: kratos-defense-and-security-solutions\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Defense\n  - Government\n  - National Security\ndescription: 'FinOps shape for Kratos: defense-contractor billing under government / commercial-defense\n  contract vehicles. No public API tariff; cost lines are program-specific and follow contract type (FFP,\n  CPFF, T&M, OTA, GSA schedule).'\nsources:\n  - https://www.kratosdefense.com\n  - https://developer.kratosdefense.com\nnotes: Pricing is contract-specific and frequently sensitive / classified. Reconcile from program contract\n  documentation and DCAA-compliant cost reporting when authorized access is obtained.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n \
  \ dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Kratos Defense & Security Solutions, Inc.\nserviceCategory: Defense Technology\nbillingModel:\n  pricingCategory: Government Contract (FFP / CPFF / T&M / OTA)\n  billingFrequency: Per-Invoice / Milestone\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Kratos Defense & Security Solutions\n  ServiceCategory: Defense\n  ProviderName: Kratos Defense & Security Solutions\n  PublisherName: Kratos Defense & Security Solutions, Inc.\n  InvoiceIssuerName: Kratos Defense & Security Solutions, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: program_milestones\n    unit: milestone\n    aggregation: count\n    dimensions:\n      - program\n      - clin\n  - name: labor_hours\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - labor_category\n      - program\n  - name: api_calls\n    unit:\
  \ request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - program\n  - name: license_seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\n      - program\n  - name: managed_assets\n    unit: asset\n    aggregation: max\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Use program-specific cost reporting (DCAA-compliant CDRLs, DD250, monthly progress reports)\n      to surface labor, ODC, and material costs against each Contract Line Item Number (CLIN).\n  - name: Allocation\n    description: Charge labor and ODCs to the correct program/CLIN; tag API/platform usage by program\n      so cost rolls up to the responsible PM.\n  - name: Optimization\n    description: Use commercial-of-the-shelf (COTS) Kratos products where available to convert program-funded\n      development to a lower-cost license model; bundle multi-program enclaves where ATO permits.\n  - name: Accountability\n    description: Program managers\
  \ own the contract budget, EVM reporting, and milestone billing; finance\n      reconciles cost performance reports against funded ceiling.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kratos-defense-and-security-solutions/refs/heads/main/finops/kratos-defense-and-security-solutions-finops.yml
sources:
- https://www.kratosdefense.com
- https://developer.kratosdefense.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Defense
- Government
- National Security
---
