---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Agreement
  chargeCategories:
  - Adjustment
  - Tax
  pricingCategory: Research Collaboration
description: 'FOCUS-aligned FinOps for Bristol Myers Squibb: not a commercial API publisher. Programmatic surfaces (Medical Information portal, BMS Study Connect, Business Development, data sharing) are accessed under research and partnership agreements. Cost is governed by the underlying collaboration contract, not metered API spend.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Bristol-Myers Squibb Company
  PricingCategory: Other
  PricingUnit: agreement
  ProviderName: Bristol Myers Squibb
  PublisherName: Bristol-Myers Squibb Company
  ServiceCategory: Pharmaceutical
  ServiceName: Bristol Myers Squibb
layout: finops
meters:
- aggregation: count
  description: Active research / partnership / data sharing agreement between BMS and the consuming organization.
  dimensions:
  - program
  - therapeutic_area
  name: collaboration_agreement
  unit: agreement
- aggregation: sum
  description: Independent researcher data sharing requests submitted and approved.
  dimensions:
  - therapeutic_area
  - study
  name: data_sharing_request
  unit: request
name: Bristol Myers Squibb Finops
provider_name: Bristol Myers Squibb
provider_slug: bristol-myers-squibb
publisher_name: Bristol-Myers Squibb Company
service_category: Pharmaceutical
slug: bristol-myers-squibb-finops
source_filename: bristol-myers-squibb-finops.yml
source_heading: FinOps Profile
source_url: https://www.bms.com/researchers-and-partners.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Bristol Myers Squibb\nproviderId: bristol-myers-squibb\npublisherName: Bristol-Myers Squibb Company\nserviceCategory: Pharmaceutical\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Pharmaceutical\n  - Biopharmaceutical\n  - Clinical Trials\n  - Digital Health\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Bristol Myers Squibb: not a commercial API publisher. Programmatic\n  surfaces (Medical Information portal, BMS Study Connect, Business Development, data sharing) are accessed\n  under research and partnership agreements. Cost is governed by the underlying collaboration contract,\n  not metered API spend.'\n\
  sources:\n  - https://www.bms.com/researchers-and-partners.html\nnotes: BMS is not billed as an API service. Reconcile against the relevant research collaboration / partnership\n  agreement for any cost or commitment terms.\nbillingModel:\n  pricingCategory: Research Collaboration\n  billingFrequency: Per-Agreement\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: Bristol Myers Squibb\n  ServiceCategory: Pharmaceutical\n  ProviderName: Bristol Myers Squibb\n  PublisherName: Bristol-Myers Squibb Company\n  InvoiceIssuerName: Bristol-Myers Squibb Company\n  BillingCurrency: USD\n  PricingCategory: Other\n  PricingUnit: agreement\nmeters:\n  - name: collaboration_agreement\n    description: Active research / partnership / data sharing agreement between BMS and the consuming\n      organization.\n    unit: agreement\n    aggregation: count\n    dimensions:\n      - program\n      - therapeutic_area\n  - name: data_sharing_request\n   \
  \ description: Independent researcher data sharing requests submitted and approved.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - therapeutic_area\n      - study\nprinciples:\n  - name: Visibility\n    description: Track active collaboration agreements, scope of data shared, and reporting deliverables\n      under each agreement; reconcile internal usage against contract terms.\n  - name: Allocation\n    description: Allocate program costs to therapeutic-area research budgets and to the partnerships /\n      business development function rather than to engineering platform cost.\n  - name: Optimization\n    description: Consolidate data sharing requests across teams, reuse anonymized study data where contract\n      terms allow, and align renewal cadence with research milestones.\n  - name: Accountability\n    description: Designate a research / partnership owner for each BMS agreement; track deliverables,\n      data-sharing scope, and contractual obligations on a\
  \ defined cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bristol-myers-squibb/refs/heads/main/finops/bristol-myers-squibb-finops.yml
sources:
- https://www.bms.com/researchers-and-partners.html
specification: FinOps Framework
tags:
- Pharmaceutical
- Biopharmaceutical
- Clinical Trials
- Digital Health
- FinOps
- FOCUS
---
