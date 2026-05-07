---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spot-administration-api-openapi.yml
  format: yaml
  label: Spot Administration API
  slug: administration-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spot/refs/heads/main/openapi/spot-administration-api-openapi.yml
- filename: spot-elastigroup-api-openapi.yml
  format: yaml
  label: Spot Elastigroup API
  slug: elastigroup-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spot/refs/heads/main/openapi/spot-elastigroup-api-openapi.yml
- filename: spot-ocean-api-openapi.yml
  format: yaml
  label: Spot Ocean API
  slug: ocean-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spot/refs/heads/main/openapi/spot-ocean-api-openapi.yml
- filename: spot-eco-api-openapi.yml
  format: yaml
  label: Spot Eco API
  slug: eco-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spot/refs/heads/main/openapi/spot-eco-api-openapi.yml
- filename: spot-billing-engine-api-openapi.yml
  format: yaml
  label: Spot Billing Engine API
  slug: billing-engine-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spot/refs/heads/main/openapi/spot-billing-engine-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: FOCUS-aligned FinOps placeholder for Spot (Flexera). Spot is itself a FinOps tool, but its own commercial pricing is contracted via Flexera sales and not exposed as a self-serve, per-call billing surface.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Flexera Software LLC
  ProviderName: Spot (Flexera)
  PublisherName: Flexera Software LLC
  ServiceCategory: Cloud Cost Optimization
  ServiceName: Spot
layout: finops
meters:
- aggregation: sum
  description: Placeholder for the Spot license meter; historical Spot commercial models include percentage-of-savings and per-managed-resource subscription, both contract-defined.
  dimensions:
  - product
  - cloud_account
  name: contracted_license
  unit: varies
name: Spot Finops
provider_name: Spot
provider_slug: spot
publisher_name: Flexera Software LLC
service_category: Cloud Cost Optimization
slug: spot-finops
source_filename: spot-finops.yml
source_heading: FinOps Profile
source_url: https://spot.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Spot\nproviderId: spot\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cloud Infrastructure\n  - Cost Optimization\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Spot (Flexera). Spot is itself\n  a FinOps tool, but its own commercial pricing is contracted via Flexera sales\n  and not exposed as a self-serve, per-call billing surface.\nsources:\n  - https://spot.io/\n  - https://www.flexera.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Flexera Software LLC\nserviceCategory: Cloud Cost Optimization\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Purchase\nfocusColumns:\n  ServiceName: Spot\n  ServiceCategory: Cloud Cost Optimization\n  ProviderName: Spot (Flexera)\n  PublisherName: Flexera Software LLC\n  InvoiceIssuerName: Flexera Software LLC\n  BillingCurrency: USD\nmeters:\n  - name: contracted_license\n    description: Placeholder for the Spot license meter; historical Spot\n      commercial models include percentage-of-savings and per-managed-resource\n      subscription, both contract-defined.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - product\n      - cloud_account\nprinciples:\n  - name: Visibility\n    description: Spot's UI exposes savings and resource utilization for the\n      products it manages; the cost of Spot itself is invoiced by Flexera under\n      the master agreement.\n  - name: Allocation\n    description: Allocate Spot license cost against the platform / SRE team that\n      operates the Ocean, Elastigroup, or Eco surface; allocate the savings Spot\n      delivers against\
  \ the workload teams whose cloud accounts are managed.\n  - name: Optimization\n    description: Optimize the relationship by measuring net savings (cloud\n      reduction minus Spot license fee). Renegotiate at renewal based on the\n      realized savings ratio.\n  - name: Accountability\n    description: Owned by the FinOps / cloud platform team that contracts Spot\n      and runs the optimization workflows.\nnotes: No public per-call billing surface for Spot's own service; entry exists\n  for catalog completeness.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spot/refs/heads/main/finops/spot-finops.yml
sources:
- https://spot.io/
- https://www.flexera.com/
specification: FinOps Framework
tags:
- Cloud Infrastructure
- Cost Optimization
- FinOps
- FOCUS
---
