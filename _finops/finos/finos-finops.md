---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: finos-symphony-pod-api-openapi.yml
  format: yaml
  label: Symphony API Spec
  slug: symphony-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/finos/refs/heads/main/openapi/finos-symphony-pod-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (membership only)
  chargeCategories:
  - Purchase
  pricingCategory: Free Open Source + Optional Annual Membership
description: 'FOCUS-aligned FinOps for FINOS: the standards (FDC3, CDM, CCC, Morphir, Symphony API Spec) are open source and free at the API/spec layer; FINOS itself is funded through corporate membership fees ($200K Platinum / $50K Gold / $10K-$30K Silver / Free Associate) plus Linux Foundation membership. FinOps for a FINOS consumer therefore tracks (a) implementation cost of adopting the standards and (b) optional membership spend if the organization wants governance influence; there is no per-call API meter.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: The Linux Foundation
  PricingCategory: Free Open Source + Membership
  PricingUnit: membership-year
  ProviderName: FINOS
  PublisherName: Fintech Open Source Foundation (FINOS)
  ServiceCategory: Open Source Foundation / Standards Body
  ServiceName: FINOS
layout: finops
meters:
- aggregation: max
  description: FINOS membership tier (Platinum / Gold / Silver / Associate).
  dimensions:
  - tier
  - company_size
  name: membership_tier
  unit: membership-year
- aggregation: sum
  description: Engineering / committer hours contributed upstream to FINOS projects.
  dimensions:
  - project
  - team
  name: contribution_hours
  unit: hour
name: Finos Finops
provider_name: FINOS
provider_slug: finos
publisher_name: Fintech Open Source Foundation (FINOS) — a Linux Foundation project
service_category: Open Source Foundation / Standards Body
slug: finos-finops
source_filename: finos-finops.yml
source_heading: FinOps Profile
source_url: https://www.finos.org/membership
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: FINOS\nproviderId: finos\npublisherName: Fintech Open Source Foundation (FINOS) — a Linux Foundation project\nserviceCategory: Open Source Foundation / Standards Body\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Financial Services\n  - Fintech\n  - Linux Foundation\n  - Open Source\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for FINOS: the standards (FDC3, CDM, CCC, Morphir, Symphony API Spec)\n  are open source and free at the API/spec layer; FINOS itself is funded through corporate membership\n  fees ($200K Platinum / $50K Gold / $10K-$30K Silver / Free Associate) plus Linux Foundation membership.\n  FinOps for a FINOS\
  \ consumer therefore tracks (a) implementation cost of adopting the standards and\n  (b) optional membership spend if the organization wants governance influence; there is no per-call\n  API meter.'\nsources:\n  - https://www.finos.org/membership\n  - https://www.finos.org/projects\nprinciples:\n  - name: Visibility\n    description: Track FINOS membership invoice (annual) and Linux Foundation corporate membership invoice;\n      track engineering effort spent adopting / contributing to FINOS standards (FDC3, CDM, CCC, Morphir).\n  - name: Allocation\n    description: Allocate membership cost to corporate-strategy / open-source-program-office budget; allocate\n      adoption engineering time to the consuming product line (e.g. trading desktop adopting FDC3).\n  - name: Optimization\n    description: Combine FINOS Silver/Gold tiers with Linux Foundation membership to maximize governance\n      voice for the spend; contribute upstream to standards your firm depends on (reduces in-house maintenance\n\
  \      burden); reuse existing FINOS reference implementations rather than building proprietary equivalents.\n  - name: Accountability\n    description: Open-source program office / corporate strategy owns membership tier; engineering leads\n      on each implementing product own adoption and contribution decisions; annual review of membership\n      ROI.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Budgeting\n      - Benchmarking\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\nbillingModel:\n  pricingCategory: Free Open Source + Optional Annual Membership\n  billingFrequency: Annual (membership only)\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: FINOS\n  ServiceCategory: Open Source Foundation / Standards Body\n  ProviderName: FINOS\n  PublisherName: Fintech Open Source Foundation (FINOS)\n  InvoiceIssuerName: The Linux Foundation\n  PricingCategory: Free Open Source + Membership\n  PricingUnit: membership-year\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: membership_tier\n    description: FINOS membership tier (Platinum / Gold / Silver / Associate).\n    unit: membership-year\n    aggregation: max\n    dimensions:\n      - tier\n      - company_size\n  - name: contribution_hours\n    description: Engineering / committer hours contributed upstream to FINOS projects.\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - project\n      - team\napis:\n  - name: FDC3\n    serviceName: FDC3\n    serviceCategory: Standard\n  - name: Common Domain Model\n    serviceName: Common Domain Model\n    serviceCategory: Standard\n  -\
  \ name: Common Cloud Controls\n    serviceName: Common Cloud Controls\n    serviceCategory: Standard\n  - name: Morphir\n    serviceName: Morphir\n    serviceCategory: Standard\n  - name: Symphony API Spec\n    serviceName: Symphony API Spec\n    serviceCategory: Specification\nunitEconomics:\n  - name: Cost per Implementing Product\n    metric: (membership_fee + adoption_engineering_cost) / implementing_products\n    target: organization-dependent\n  - name: Contribution / Membership ROI\n    metric: contribution_hours / membership_fee\n    target: maximize meaningful contribution\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/finos/refs/heads/main/finops/finos-finops.yml
sources:
- https://www.finos.org/membership
- https://www.finos.org/projects
specification: FinOps Framework
tags:
- Financial Services
- Fintech
- Linux Foundation
- Open Source
- FinOps
- Cost Management
- FOCUS
---
