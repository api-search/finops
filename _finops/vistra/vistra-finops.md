---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: vistra-incorporations-openapi.yml
  format: yaml
  label: Vistra Incorporations API
  slug: incorporations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vistra/refs/heads/main/openapi/vistra-incorporations-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Tax
  pricingCategory: Energy Supply Contract
description: Vistra Corp is an integrated electricity retailer and generator. The FinOps surface is electricity supply (kWh delivered, capacity, transmission) rather than metered API consumption; this artifact is a Contact Sales placeholder and should not be confused with cloud- service FinOps.
focus_columns:
  BillingCurrency: USD
  ProviderName: Vistra Corp.
  PublisherName: Vistra Corp.
  ServiceCategory: Energy / Electricity
  ServiceName: Vistra
layout: finops
meters:
- aggregation: sum
  dimensions:
  - retail_brand
  - rate_plan
  name: kwh_delivered
  unit: kWh
- aggregation: max
  dimensions:
  - retail_brand
  name: demand_charges
  unit: kW
name: Vistra Finops
provider_name: Vistra
provider_slug: vistra
publisher_name: Vistra Corp.
service_category: Energy / Electricity
slug: vistra-finops
source_filename: vistra-finops.yml
source_heading: FinOps Profile
source_url: https://www.vistracorp.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Vistra\nproviderId: vistra\npublisherName: Vistra Corp.\nserviceCategory: Energy / Electricity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Energy\n  - Electricity\n  - Retail Energy\ndescription: Vistra Corp is an integrated electricity retailer and generator. The FinOps surface\n  is electricity supply (kWh delivered, capacity, transmission) rather than metered API\n  consumption; this artifact is a Contact Sales placeholder and should not be confused with cloud-\n  service FinOps.\nsources:\n  - https://www.vistracorp.com/\nnotes: No public unit prices for an API surface; meters reflect electricity-supply categories that\n  would\
  \ appear on a Vistra retail invoice.\nbillingModel:\n  pricingCategory: Energy Supply Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Vistra\n  ServiceCategory: Energy / Electricity\n  ProviderName: Vistra Corp.\n  PublisherName: Vistra Corp.\n  BillingCurrency: USD\nmeters:\n  - name: kwh_delivered\n    unit: kWh\n    aggregation: sum\n    dimensions:\n      - retail_brand\n      - rate_plan\n  - name: demand_charges\n    unit: kW\n    aggregation: max\n    dimensions:\n      - retail_brand\nprinciples:\n  - name: Visibility\n    description: Visibility is provided by the smart-meter / utility billing data feed and the\n      retail brand's customer portal (TXU, Homefield, etc.); there is no developer billing API.\n  - name: Allocation\n    description: Allocate spend by service-address / facility against the consuming business unit.\n  - name: Optimization\n    description: Optimization levers are\
  \ commercial - rate-plan selection, demand-response\n      participation, on-site generation / storage, and contract term negotiation.\n  - name: Accountability\n    description: Facilities / energy management owns electricity spend; finance reconciles against\n      monthly utility statements.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vistra/refs/heads/main/finops/vistra-finops.yml
sources:
- https://www.vistracorp.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Energy
- Electricity
- Retail Energy
---
