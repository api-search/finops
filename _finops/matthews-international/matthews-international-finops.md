---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Project / Solution Contract
description: 'FOCUS-aligned FinOps shape for Matthews International: solution / project-priced industrial and brand-workflow integrations. There is no per-API-call meter; cost lives at the contract / project level.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Matthews International Corporation
  ProviderName: Matthews International
  PublisherName: Matthews International Corporation
  ServiceCategory: Industrial / B2B Solutions
  ServiceName: Matthews International Solutions
layout: finops
meters:
- aggregation: max
  description: Per-solution license, billed under the customer contract.
  dimensions:
  - segment
  - product
  - site
  name: solution_license
  unit: month
- aggregation: sum
  description: Implementation / professional services hours billed against the SOW.
  dimensions:
  - project
  - site
  name: professional_services
  unit: hour
- aggregation: max
  description: Annual support / maintenance contract value.
  dimensions:
  - segment
  - product
  name: support_contract
  unit: year
name: Matthews International Finops
provider_name: Matthews International
provider_slug: matthews-international
publisher_name: Matthews International Corporation
service_category: Industrial / B2B Solutions
slug: matthews-international-finops
source_filename: matthews-international-finops.yml
source_heading: FinOps Profile
source_url: https://www.matw.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Matthews International\nproviderId: matthews-international\npublisherName: Matthews International Corporation\nserviceCategory: Industrial / B2B Solutions\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Memorialization\n  - Branding\n  - Industrial\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Matthews International: solution / project-priced industrial\n  and brand-workflow integrations. There is no per-API-call meter; cost lives at the contract / project\n  level.'\nnotes: |\n  No public per-API pricing. Meters track contract-level economics (license, project services, support)\n  rather than\
  \ API request volume.\nsources:\n  - https://www.matw.com/\nprinciples:\n  - name: Visibility\n    description: Track integration spend at the project / contract level via the underlying purchase\n      order and statement-of-work; aggregate by Matthews business segment (Memorialization, Industrial\n      Technologies, SGK).\n  - name: Allocation\n    description: Allocate by consuming business unit / facility / brand. For warehouse automation, allocate\n      by site; for SGK brand workflows, allocate by brand and packaging program.\n  - name: Optimization\n    description: Consolidate integrations across sites and brands to reuse a single connector, negotiate\n      multi-year support, and revisit feature usage at contract renewal.\n  - name: Accountability\n    description: Assign a contract owner per Matthews business segment who reviews invoice accuracy and\n      milestone delivery against the SOW.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n\
  \      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Licensing and SaaS\n      - Workload Optimization\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Project / Solution Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Matthews International Solutions\n  ServiceCategory: Industrial / B2B Solutions\n  ProviderName: Matthews International\n  PublisherName: Matthews International Corporation\n  InvoiceIssuerName: Matthews International Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: solution_license\n    description: Per-solution license, billed\
  \ under the customer contract.\n    unit: month\n    aggregation: max\n    dimensions:\n      - segment\n      - product\n      - site\n  - name: professional_services\n    description: Implementation / professional services hours billed against the SOW.\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - project\n      - site\n  - name: support_contract\n    description: Annual support / maintenance contract value.\n    unit: year\n    aggregation: max\n    dimensions:\n      - segment\n      - product\napis:\n  - name: Matthews International API\n    baseURL: https://api.matw.com\n    tags:\n      - Memorialization\n      - Branding\n      - Industrial\n    serviceName: Matthews International API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Site\n    metric: billed_cost / active_sites\n    target: TBD\n  - name: Cost per Brand Program\n    metric: billed_cost / brand_programs\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/matthews-international/refs/heads/main/finops/matthews-international-finops.yml
sources:
- https://www.matw.com/
specification: FinOps Framework
tags:
- Memorialization
- Branding
- Industrial
- FinOps
- FOCUS
---
