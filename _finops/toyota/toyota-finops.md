---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: toyota-telematics-openapi.yml
  format: yaml
  label: Toyota Telematics API
  slug: toyota-telematics
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/toyota/refs/heads/main/openapi/toyota-telematics-openapi.yml
- filename: toyota-connected-services-openapi.yml
  format: yaml
  label: Toyota Connected Services API
  slug: toyota-connected-services
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/toyota/refs/heads/main/openapi/toyota-connected-services-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Subscription + Contracted Data Sharing
description: 'FinOps shape for Toyota: consumer Connected Services subscriptions bundled with the vehicle, plus contracted B2B telematics agreements for fleet/insurance partners. No public per-API meter rates exist; this artifact describes structural billing categories only.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Toyota Motor Sales, U.S.A., Inc.
  ProviderName: Toyota
  PublisherName: Toyota Motor Sales, U.S.A., Inc.
  ServiceCategory: Connected Vehicle
  ServiceName: Toyota Connected
layout: finops
meters:
- aggregation: sum
  description: Per-vehicle Connected Services subscription (consumer-facing).
  dimensions:
  - service_package
  - region
  name: connected_services_subscription
  unit: vehicle-month
- aggregation: sum
  description: Contracted partner telematics data-sharing volume.
  dimensions:
  - partner
  - data_category
  name: telematics_data_feed
  unit: vehicle-month
name: Toyota Finops
provider_name: Toyota
provider_slug: toyota
publisher_name: Toyota Motor Sales, U.S.A., Inc.
service_category: Connected Vehicle / Telematics
slug: toyota-finops
source_filename: toyota-finops.yml
source_heading: FinOps Profile
source_url: https://www.toyota.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Toyota\nproviderId: toyota\npublisherName: Toyota Motor Sales, U.S.A., Inc.\nserviceCategory: Connected Vehicle / Telematics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Automobiles\n  - Connected Car\n  - Telematics\n  - FinOps\n  - FOCUS\ndescription: 'FinOps shape for Toyota: consumer Connected Services subscriptions bundled with the vehicle,\n  plus contracted B2B telematics agreements for fleet/insurance partners. No public per-API meter rates\n  exist; this artifact describes structural billing categories only.'\nsources:\n  - https://www.toyota.com/\nnotes: Pricing not publicly retrievable; meters are descriptive\
  \ and unpriced.\nbillingModel:\n  pricingCategory: Subscription + Contracted Data Sharing\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Toyota Connected\n  ServiceCategory: Connected Vehicle\n  ProviderName: Toyota\n  PublisherName: Toyota Motor Sales, U.S.A., Inc.\n  InvoiceIssuerName: Toyota Motor Sales, U.S.A., Inc.\n  BillingCurrency: USD\nmeters:\n  - name: connected_services_subscription\n    description: Per-vehicle Connected Services subscription (consumer-facing).\n    unit: vehicle-month\n    aggregation: sum\n    dimensions:\n      - service_package\n      - region\n  - name: telematics_data_feed\n    description: Contracted partner telematics data-sharing volume.\n    unit: vehicle-month\n    aggregation: sum\n    dimensions:\n      - partner\n      - data_category\nprinciples:\n  - name: Visibility\n    description: For consumer Connected Services,\
  \ statements are per-VIN through Toyota's account portal;\n      partner data feeds are reconciled monthly against the contracted vehicle population.\n  - name: Allocation\n    description: Allocate consumer subscriptions per VIN/owner; allocate B2B telematics fees per partner-program\n      and use case (insurance, fleet, infrastructure).\n  - name: Optimization\n    description: For fleets, prune the active-VIN list against actual operating vehicles each cycle; consumers\n      should match the Connected Services tier (Audio Plus, Remote Connect, Service Connect, Drive Connect)\n      to features they actually use.\n  - name: Accountability\n    description: Fleet manager owns the partner-feed reconciliation; consumer billing is per-driver.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/toyota/refs/heads/main/finops/toyota-finops.yml
sources:
- https://www.toyota.com/
specification: FinOps Framework
tags:
- Automobiles
- Connected Car
- Telematics
- FinOps
- FOCUS
---
