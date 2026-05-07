---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract-Based
description: Rollins is a services company; any API integration is partner-contract driven, not usage-metered. FinOps shape is placeholder.
focus_columns:
  BillingCurrency: USD
  ProviderName: Rollins
  PublisherName: Rollins, Inc.
  ServiceCategory: Pest Control Services
  ServiceName: Rollins Services
layout: finops
meters:
- aggregation: sum
  description: Negotiated partner or service charges
  dimensions:
  - contract
  name: contract_charges
  unit: varies
name: Rollins Finops
provider_name: Rollins
provider_slug: rollins
publisher_name: Rollins, Inc.
service_category: Pest Control Services
slug: rollins-finops
source_filename: rollins-finops.yml
source_heading: FinOps Profile
source_url: https://www.rollins.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Rollins\nproviderId: rollins\npublisherName: Rollins, Inc.\nserviceCategory: Pest Control Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Pest Control\n  - Services\n  - FinOps\n  - FOCUS\ndescription: >-\n  Rollins is a services company; any API integration is partner-contract driven, not\n  usage-metered. FinOps shape is placeholder.\nnotes: >-\n  No public billing or usage API exists. Service costs are governed by service contracts and\n  billed through standard AR/AP, not as itemized API line items.\nsources:\n  - https://www.rollins.com/\nbillingModel:\n  pricingCategory: Contract-Based\n  billingFrequency:\
  \ Per Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Rollins Services\n  ServiceCategory: Pest Control Services\n  ProviderName: Rollins\n  PublisherName: Rollins, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_charges\n    description: Negotiated partner or service charges\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: >-\n      Track Rollins-related spend through the AP system and field-services contracts; no API\n      usage telemetry is available.\n  - name: Allocation\n    description: >-\n      Allocate Rollins service charges to the property or facility receiving service rather\n      than to a generic IT bucket.\n  - name: Optimization\n    description: >-\n      Negotiate multi-site or multi-year discounts at contract renewal; review service scope\n      against actual incident frequency.\n  - name: Accountability\n    description: >-\n\
  \      Facilities or property-management leads own the Rollins relationship and review service\n      contracts annually.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rollins/refs/heads/main/finops/rollins-finops.yml
sources:
- https://www.rollins.com/
specification: FinOps Framework
tags:
- Pest Control
- Services
- FinOps
- FOCUS
---
