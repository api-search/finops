---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: webmethods-api-gateway-openapi.yml
  format: yaml
  label: webMethods API Gateway Service Management API
  slug: webmethods-api-gateway
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/software-ag/refs/heads/main/openapi/webmethods-api-gateway-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription (Contact Sales)
description: FOCUS-aligned FinOps placeholder for Software AG webMethods. Pricing is contact-sales only, and webMethods is typically customer-deployed software; meters here describe the consumption shape customers should track to allocate license cost.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Software AG
  ProviderName: Software AG
  PublisherName: Software AG
  ServiceCategory: Enterprise Integration
  ServiceName: webMethods Integration Suite
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - environment
  name: gateway_calls
  unit: request
- aggregation: max
  dimensions:
  - environment
  - cluster
  name: runtime_cores
  unit: core
- aggregation: count
  dimensions:
  - tier
  name: environments
  unit: environment
name: Software Ag Finops
provider_name: Software AG
provider_slug: software-ag
publisher_name: Software AG
service_category: Enterprise Integration
slug: software-ag-finops
source_filename: software-ag-finops.yml
source_heading: FinOps Profile
source_url: https://www.softwareag.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Software AG\nproviderId: software-ag\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - API Management\n  - webMethods\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Software AG webMethods. Pricing is contact-sales only,\n  and webMethods is typically customer-deployed software; meters here describe the consumption shape\n  customers should track to allocate license cost.'\nsources:\n  - https://www.softwareag.com/\nnotes: Software AG does not publish a public price sheet, so unit prices and FOCUS PricingUnit cannot\n  be reconciled. Meters listed reflect the consumption shape webMethods customers typically negotiate\n  against (runtime cores / nodes, calls passing the gateway, environments).\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Software AG\nserviceCategory: Enterprise Integration\nbillingModel:\n  pricingCategory: Subscription (Contact Sales)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: webMethods Integration Suite\n  ServiceCategory: Enterprise Integration\n  ProviderName: Software AG\n  PublisherName: Software AG\n  InvoiceIssuerName: Software AG\n  BillingCurrency: USD\nmeters:\n  - name: gateway_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n  - name: runtime_cores\n    unit: core\n    aggregation: max\n    dimensions:\n      - environment\n      - cluster\n  - name: environments\n    unit: environment\n    aggregation: count\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Use webMethods API Gateway analytics, the Service Management\
  \ API, and webMethods Integration\n      Server logs to surface call volume, latency, and runtime cluster utilization.\n  - name: Allocation\n    description: Tag APIs and integrations to consuming application teams; map webMethods environments\n      (dev/test/prod) to internal cost centers for license recharge.\n  - name: Optimization\n    description: Right-size Integration Server runtime cores per cluster, retire unused APIs in API Gateway,\n      and consolidate environments where contract terms allow.\n  - name: Accountability\n    description: Platform owner reconciles Software AG license cost against Gateway analytics and runtime\n      utilization at each renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/software-ag/refs/heads/main/finops/software-ag-finops.yml
sources:
- https://www.softwareag.com/
specification: FinOps Framework
tags:
- API Management
- webMethods
- FinOps
- FOCUS
---
