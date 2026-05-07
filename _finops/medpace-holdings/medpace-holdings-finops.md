---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Per-Milestone / Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Credit
  pricingCategory: Per-Study SOW (Fixed + Per-Subject + Pass-Through)
description: 'FOCUS-aligned FinOps shape for Medpace Holdings: clinical trial services priced per study via SOW with fixed-price service fees, per-subject / per-visit unit pricing, and pass-through costs. FinOps focus is study-level financial management rather than per-API-call billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Medpace Holdings, Inc.
  ProviderName: Medpace
  PublisherName: Medpace Holdings, Inc.
  ServiceCategory: Contract Research Organization (CRO)
  ServiceName: Medpace Clinical Trial Services
layout: finops
meters:
- aggregation: sum
  description: Fixed-price service fee per study, recognized against milestones.
  dimensions:
  - study
  - phase
  - therapeutic_area
  name: study_service_fee
  unit: study-milestone
- aggregation: sum
  description: Subjects enrolled / randomized in the study.
  dimensions:
  - study
  - site
  - country
  name: subjects_enrolled
  unit: subject
- aggregation: sum
  description: Protocol-defined visits completed.
  dimensions:
  - study
  - visit_type
  - site
  name: subject_visits
  unit: visit
- aggregation: sum
  description: Pass-through costs (investigator grants, central labs, IRB / EC, courier).
  dimensions:
  - study
  - cost_type
  - vendor
  name: pass_through_costs
  unit: USD
- aggregation: sum
  description: Approved change orders amending the SOW.
  dimensions:
  - study
  - reason_code
  name: change_orders
  unit: USD
name: Medpace Holdings Finops
provider_name: Medpace Holdings
provider_slug: medpace-holdings
publisher_name: Medpace Holdings, Inc.
service_category: Contract Research Organization (CRO)
slug: medpace-holdings-finops
source_filename: medpace-holdings-finops.yml
source_heading: FinOps Profile
source_url: https://www.medpace.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Medpace Holdings\nproviderId: medpace-holdings\npublisherName: Medpace Holdings, Inc.\nserviceCategory: Contract Research Organization (CRO)\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Clinical Research\n  - CRO\n  - Biotech\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Medpace Holdings: clinical trial services priced per study\n  via SOW with fixed-price service fees, per-subject / per-visit unit pricing, and pass-through costs.\n  FinOps focus is study-level financial management rather than per-API-call billing.'\nnotes: |\n  No public per-API pricing. Cost is allocated per study / protocol;\
  \ meters represent clinical-trial\n  economic units (subjects enrolled, visits, sites, deliverable milestones).\nsources:\n  - https://www.medpace.com/\nprinciples:\n  - name: Visibility\n    description: Track study burn against budget via the SOW and PM dashboard; reconcile invoices to\n      enrollment milestones (first patient in, last patient last visit) and pass-through receipts.\n  - name: Allocation\n    description: Allocate by study / protocol / phase / therapeutic area. For sponsors with multi-study\n      portfolios, allocate to clinical program and indication, and break out pass-through (investigator\n      grants, central labs, courier) from service fees.\n  - name: Optimization\n    description: Optimize protocol design (visit count, complexity), select sites by historical enrollment\n      and quality data, and choose appropriate Medpace service modules (full-service vs functional service\n      provision) per study.\n  - name: Accountability\n    description: Assign a\
  \ sponsor study lead per protocol who reviews monthly burn, change orders, and\n      milestone delivery with the Medpace project manager.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Per-Study SOW (Fixed + Per-Subject + Pass-Through)\n  billingFrequency: Per-Milestone / Monthly\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Medpace Clinical Trial Services\n  ServiceCategory:\
  \ Contract Research Organization (CRO)\n  ProviderName: Medpace\n  PublisherName: Medpace Holdings, Inc.\n  InvoiceIssuerName: Medpace Holdings, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: study_service_fee\n    description: Fixed-price service fee per study, recognized against milestones.\n    unit: study-milestone\n    aggregation: sum\n    dimensions:\n      - study\n      - phase\n      - therapeutic_area\n  - name: subjects_enrolled\n    description: Subjects enrolled / randomized in the study.\n    unit: subject\n    aggregation: sum\n    dimensions:\n      - study\n      - site\n      - country\n  - name: subject_visits\n    description: Protocol-defined visits completed.\n    unit: visit\n    aggregation: sum\n    dimensions:\n      - study\n      - visit_type\n      - site\n  - name: pass_through_costs\n    description: Pass-through costs (investigator grants, central labs, IRB / EC, courier).\n    unit: USD\n    aggregation: sum\n    dimensions:\n\
  \      - study\n      - cost_type\n      - vendor\n  - name: change_orders\n    description: Approved change orders amending the SOW.\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - study\n      - reason_code\napis:\n  - name: Medpace Holdings API\n    baseURL: https://api.medpace.com\n    tags:\n      - Clinical Research\n      - CRO\n      - Biotech\n    serviceName: Medpace Holdings API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Enrolled Subject\n    metric: billed_cost / subjects_enrolled\n    target: TBD\n  - name: Cost per Visit\n    metric: billed_cost / subject_visits\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/medpace-holdings/refs/heads/main/finops/medpace-holdings-finops.yml
sources:
- https://www.medpace.com/
specification: FinOps Framework
tags:
- Clinical Research
- CRO
- Biotech
- FinOps
- FOCUS
---
