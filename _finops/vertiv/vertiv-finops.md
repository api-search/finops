---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: vertiv-environet-alert-openapi.yml
  format: yaml
  label: Vertiv Environet Alert REST API
  slug: environet-alert-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vertiv/refs/heads/main/openapi/vertiv-environet-alert-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Hardware + Service Contract
description: Vertiv is a hardware + service provider for data-center power and thermal management. Spend is dominated by capex (hardware purchase) and service contracts rather than metered API billing, so the FinOps surface is a Contact Sales placeholder.
focus_columns:
  BillingCurrency: USD
  ProviderName: Vertiv
  PublisherName: Vertiv Group Corporation
  ServiceCategory: Data Center Infrastructure
  ServiceName: Vertiv
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product_family
  name: hardware_purchase
  unit: unit
- aggregation: sum
  dimensions:
  - contract_type
  - site
  name: service_contract
  unit: month
name: Vertiv Finops
provider_name: Vertiv
provider_slug: vertiv
publisher_name: Vertiv Group Corporation
service_category: Data Center Infrastructure
slug: vertiv-finops
source_filename: vertiv-finops.yml
source_heading: FinOps Profile
source_url: https://www.vertiv.com/en-us/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Vertiv\nproviderId: vertiv\npublisherName: Vertiv Group Corporation\nserviceCategory: Data Center Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Data Center\n  - Power Management\n  - Hardware\ndescription: Vertiv is a hardware + service provider for data-center power and thermal management.\n  Spend is dominated by capex (hardware purchase) and service contracts rather than metered API\n  billing, so the FinOps surface is a Contact Sales placeholder.\nsources:\n  - https://www.vertiv.com/en-us/\nnotes: No metered API billing or FOCUS-aligned cost-and-usage feed is published; meters describe\n  the categories typical Vertiv\
  \ invoices contain.\nbillingModel:\n  pricingCategory: Hardware + Service Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Vertiv\n  ServiceCategory: Data Center Infrastructure\n  ProviderName: Vertiv\n  PublisherName: Vertiv Group Corporation\n  BillingCurrency: USD\nmeters:\n  - name: hardware_purchase\n    unit: unit\n    aggregation: sum\n    dimensions:\n      - product_family\n  - name: service_contract\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract_type\n      - site\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the Vertiv invoice and any deployed Vertiv management software\n      (Environet, Trellis, Avocent) for asset and incident telemetry; there is no hosted billing API.\n  - name: Allocation\n    description: Spend is allocated by site / facility against the equipment install base; tag the\n      asset register\
  \ with cost-center on the consumer side.\n  - name: Optimization\n    description: Cost levers are right-sizing UPS / cooling capacity, multi-year service contracts,\n      and refreshing aging units to lower-PUE families.\n  - name: Accountability\n    description: Facilities / data-center operations typically own Vertiv spend; finance reconciles\n      against multi-year service agreements.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vertiv/refs/heads/main/finops/vertiv-finops.yml
sources:
- https://www.vertiv.com/en-us/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Data Center
- Power Management
- Hardware
---
