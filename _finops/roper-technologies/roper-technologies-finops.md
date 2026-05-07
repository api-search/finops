---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Varies
  chargeCategories:
  - Purchase
  pricingCategory: Varies by Subsidiary
description: Roper Technologies is a diversified holding company. FinOps treatment must be applied at the subsidiary level (Aderant, Deltek, Vertafore, etc.); no Roper-level billing surface exists.
focus_columns:
  BillingCurrency: USD
  ProviderName: Roper Technologies
  PublisherName: Roper Technologies, Inc.
  ServiceCategory: Vertical SaaS Holding
  ServiceName: Roper Technologies (multi-subsidiary)
layout: finops
meters:
- aggregation: sum
  description: Aggregate of charges from Roper operating subsidiaries
  dimensions:
  - subsidiary
  - product
  name: subsidiary_charges
  unit: varies
name: Roper Technologies Finops
provider_name: Roper Technologies
provider_slug: roper-technologies
publisher_name: Roper Technologies, Inc.
service_category: Vertical SaaS Holding
slug: roper-technologies-finops
source_filename: roper-technologies-finops.yml
source_heading: FinOps Profile
source_url: https://www.ropertech.com/businesses
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Roper Technologies\nproviderId: roper-technologies\npublisherName: Roper Technologies, Inc.\nserviceCategory: Vertical SaaS Holding\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Holding Company\n  - Vertical Software\n  - SaaS\n  - FinOps\n  - FOCUS\ndescription: >-\n  Roper Technologies is a diversified holding company. FinOps treatment must be applied at\n  the subsidiary level (Aderant, Deltek, Vertafore, etc.); no Roper-level billing surface\n  exists.\nnotes: >-\n  No unified billing model. Each subsidiary issues its own invoices under its own legal\n  entity.\nsources:\n  - https://www.ropertech.com/businesses\n\
  billingModel:\n  pricingCategory: Varies by Subsidiary\n  billingFrequency: Varies\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Roper Technologies (multi-subsidiary)\n  ServiceCategory: Vertical SaaS Holding\n  ProviderName: Roper Technologies\n  PublisherName: Roper Technologies, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subsidiary_charges\n    description: Aggregate of charges from Roper operating subsidiaries\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - subsidiary\n      - product\nprinciples:\n  - name: Visibility\n    description: >-\n      Roll up subsidiary-level invoices (Aderant, Deltek, Vertafore, Clinisys) into a single\n      Roper view; the parent does not publish an aggregated usage feed.\n  - name: Allocation\n    description: >-\n      Allocate each subsidiary's spend to the consuming vertical (legal, healthcare,\n      construction, insurance) rather than treating Roper as one bucket.\n  - name:\
  \ Optimization\n    description: >-\n      Negotiate at the subsidiary level; cross-subsidiary leverage is limited by the holding\n      company's decentralized model.\n  - name: Accountability\n    description: >-\n      Vertical leadership (legal, healthcare, construction, etc.) owns the corresponding\n      Roper-subsidiary contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/roper-technologies/refs/heads/main/finops/roper-technologies-finops.yml
sources:
- https://www.ropertech.com/businesses
specification: FinOps Framework
tags:
- Holding Company
- Vertical Software
- SaaS
- FinOps
- FOCUS
---
