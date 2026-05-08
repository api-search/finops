---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: thesports-football-openapi.yml
  format: yaml
  label: TheSports Football API
  slug: football-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/thesports/refs/heads/main/openapi/thesports-football-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Custom / Contact Sales
description: 'FOCUS-aligned FinOps placeholder for TheSports: contact-sales sports data feeds with no published rate card.'
focus_columns:
  BillingCurrency: USD
  ProviderName: TheSports
  PublisherName: TheSports
  ServiceCategory: Sports Data
  ServiceName: TheSports
layout: finops
meters:
- aggregation: sum
  dimensions:
  - sport
  - feed
  name: contracted_data_access
  unit: varies
name: Thesports Finops
provider_name: TheSports
provider_slug: thesports
publisher_name: TheSports
service_category: Sports Data
slug: thesports-finops
source_filename: thesports-finops.yml
source_heading: FinOps Profile
source_url: https://www.thesports.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TheSports\nproviderId: thesports\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Sports\n  - Data\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for TheSports: contact-sales sports data feeds with no\n  published rate card.'\nsources:\n  - https://www.thesports.com/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: TheSports publishes no public pricing or billing documentation; FinOps shape is inferred from\n  the contact-sales posture and cannot be reconciled until a contract is in hand.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TheSports\nserviceCategory: Sports Data\nbillingModel:\n  pricingCategory:\
  \ Custom / Contact Sales\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: TheSports\n  ServiceCategory: Sports Data\n  ProviderName: TheSports\n  PublisherName: TheSports\n  BillingCurrency: USD\nmeters:\n  - name: contracted_data_access\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - sport\n      - feed\nprinciples:\n  - name: Visibility\n    description: Track invoiced contract spend and any per-feed usage reports TheSports provides under\n      the negotiated agreement.\n  - name: Allocation\n    description: Allocate the contracted feed cost to the sports product/team consuming each feed (football,\n      basketball, tennis, esports).\n  - name: Optimization\n    description: Renegotiate or rescope feeds at renewal based on actual sport-by-sport consumption;\n      drop unused feeds.\n  - name: Accountability\n    description: Assign a single sports-data owner accountable for\
  \ the TheSports contract, renewal date,\n      and overage exposure.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/thesports/refs/heads/main/finops/thesports-finops.yml
sources:
- https://www.thesports.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Sports
- Data
- FinOps
- FOCUS
---
