---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: orion-fhir-openapi.yml
  format: yaml
  label: Orion Health FHIR API
  slug: orion-health-fhir-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/orion/refs/heads/main/openapi/orion-fhir-openapi.yml
- filename: orion-population-health-openapi.yml
  format: yaml
  label: Orion Health Population Health API
  slug: orion-health-population-health-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/orion/refs/heads/main/openapi/orion-population-health-openapi.yml
- filename: orion-hie-openapi.yml
  format: yaml
  label: Orion Health HIE API
  slug: orion-health-hie-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/orion/refs/heads/main/openapi/orion-hie-openapi.yml
- filename: orion-rhapsody-openapi.yml
  format: yaml
  label: Orion Health Rhapsody Integration API
  slug: orion-health-rhapsody-integration-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/orion/refs/heads/main/openapi/orion-rhapsody-openapi.yml
billing_model:
  billingCurrency: USD/NZD/AUD/GBP/EUR
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Enterprise Subscription (Population-Scoped)
description: 'FOCUS-aligned FinOps view for Orion Health: negotiated enterprise license scoped by population size and product bundle (Amadeus DCR, Virtuoso DFD, Orchestral HIP, Communicate, Rhapsody), plus the underlying infrastructure cost when self-hosted (on-premises hardware or customer cloud compute, storage, and egress). API access is bundled with the license.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Orion Health Limited
  PricingCategory: Subscription
  ProviderName: Orion Health
  PublisherName: Orion Health Limited
  ServiceCategory: Healthcare Interoperability
  ServiceName: Orion Health
layout: finops
meters:
- aggregation: max
  description: Contracted population coverage (lives) under the Orion Health agreement
  dimensions:
  - product
  - region
  name: orion_population_subscription
  unit: lives
- aggregation: max
  description: Active Orion Health products under the agreement
  dimensions:
  - product
  name: orion_product_bundle
  unit: bundle
- aggregation: sum
  description: Underlying infrastructure compute cost when Orion Health is self-hosted
  dimensions:
  - environment
  - region
  name: hosting_compute
  unit: hour
- aggregation: sum
  description: Underlying infrastructure storage cost when Orion Health is self-hosted
  dimensions:
  - environment
  - region
  name: hosting_storage
  unit: GB-month
name: Orion Finops
provider_name: Orion Health
provider_slug: orion
publisher_name: Orion Health Limited
service_category: Healthcare Interoperability
slug: orion-finops
source_filename: orion-finops.yml
source_heading: FinOps Profile
source_url: https://www.orionhealth.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Orion Health\nproviderId: orion\npublisherName: Orion Health Limited\nserviceCategory: Healthcare Interoperability\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare\n  - FHIR\n  - HIE\n  - Interoperability\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view for Orion Health: negotiated enterprise license\n  scoped by population size and product bundle (Amadeus DCR, Virtuoso DFD,\n  Orchestral HIP, Communicate, Rhapsody), plus the underlying infrastructure\n  cost when self-hosted (on-premises hardware or customer cloud compute,\n  storage, and egress). API access is bundled with the license.\n\
  sources:\n  - https://www.orionhealth.com/\n  - https://www.orionhealth.com/global/products/\nnotes: >-\n  No public per-API meter exists. FinOps observation focuses on the\n  contractual population / product-bundle terms plus the underlying\n  self-hosted infrastructure cost where applicable.\nbillingModel:\n  pricingCategory: Enterprise Subscription (Population-Scoped)\n  billingFrequency: Annual\n  billingCurrency: USD/NZD/AUD/GBP/EUR\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Orion Health\n  ServiceCategory: Healthcare Interoperability\n  ProviderName: Orion Health\n  PublisherName: Orion Health Limited\n  InvoiceIssuerName: Orion Health Limited\n  BillingCurrency: USD\n  PricingCategory: Subscription\n  ChargeCategory: Purchase\nmeters:\n  - name: orion_population_subscription\n    description: Contracted population coverage (lives) under the Orion Health agreement\n    unit: lives\n    aggregation: max\n\
  \    dimensions:\n      - product\n      - region\n  - name: orion_product_bundle\n    description: Active Orion Health products under the agreement\n    unit: bundle\n    aggregation: max\n    dimensions:\n      - product\n  - name: hosting_compute\n    description: Underlying infrastructure compute cost when Orion Health is self-hosted\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - environment\n      - region\n  - name: hosting_storage\n    description: Underlying infrastructure storage cost when Orion Health is self-hosted\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - environment\n      - region\nprinciples:\n  - name: Visibility\n    description: >-\n      Track contracted population size, product bundle, and deployment\n      model in a contract-management ledger; for self-hosted deployments\n      track the underlying infrastructure cost in the hosting cloud's\n      cost-management tooling.\n  - name: Allocation\n    description: >-\n     \
  \ Allocate Orion Health subscription cost across the participating\n      health systems, payers, or government health authorities by\n      contributing population.\n  - name: Optimization\n    description: >-\n      Right-size the deployment (Rhapsody engine count, FHIR repository\n      sizing) to actual message and population volume; consolidate\n      participating organizations onto a shared HIE deployment where\n      governance permits to reduce per-organization overhead.\n  - name: Accountability\n    description: >-\n      Pair the Orion Health platform owner with a healthcare-finance\n      partner; review contracted population coverage and deployment\n      capacity at each renewal and at participating-organization onboarding.\napis:\n  - name: Orion Health FHIR API\n    serviceName: Orion Health FHIR API\n    serviceCategory: Healthcare Interoperability\n  - name: Orion Health Population Health API\n    serviceName: Orion Health Population Health API\n    serviceCategory:\
  \ Healthcare Interoperability\n  - name: Orion Health HIE API\n    serviceName: Orion Health HIE API\n    serviceCategory: Healthcare Interoperability\n  - name: Orion Health Rhapsody Integration API\n    serviceName: Orion Health Rhapsody Integration API\n    serviceCategory: Healthcare Interoperability\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/orion/refs/heads/main/finops/orion-finops.yml
sources:
- https://www.orionhealth.com/
- https://www.orionhealth.com/global/products/
specification: FinOps Framework
tags:
- Healthcare
- FHIR
- HIE
- Interoperability
- FinOps
- FOCUS
---
