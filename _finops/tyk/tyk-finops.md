---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tyk-gateway-api-openapi.yml
  format: yaml
  label: Tyk Gateway API
  slug: tyk-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tyk/refs/heads/main/openapi/tyk-gateway-api-openapi.yml
- filename: tyk-dashboard-api-openapi.yml
  format: yaml
  label: Tyk Dashboard API
  slug: tyk-dashboard-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tyk/refs/heads/main/openapi/tyk-dashboard-api-openapi.yml
- filename: tyk-dashboard-admin-api-openapi.yml
  format: yaml
  label: Tyk Dashboard Admin API
  slug: tyk-dashboard-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tyk/refs/heads/main/openapi/tyk-dashboard-admin-api-openapi.yml
- filename: tyk-mdcb-api-openapi.yml
  format: yaml
  label: Tyk MDCB API
  slug: tyk-mdcb-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tyk/refs/heads/main/openapi/tyk-mdcb-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription + Usage-Based
description: 'FOCUS-aligned FinOps for Tyk: hybrid model combining a free open-source gateway, a usage-based Core SaaS tier, a flat-rate Professional subscription, and a custom-contract Enterprise tier.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Tyk Technologies Ltd
  ProviderName: Tyk
  PublisherName: Tyk Technologies Ltd
  ServiceCategory: API Management
  ServiceName: Tyk
layout: finops
meters:
- aggregation: sum
  description: Requests proxied through the Tyk gateway (Core / consumption-based tier)
  dimensions:
  - api
  - environment
  - deployment_mode
  name: gateway_requests
  unit: request
- aggregation: sum
  description: Flat Professional / Enterprise subscription term
  dimensions:
  - tier
  name: subscription_period
  unit: month
- aggregation: max
  description: Number of distinct gateway environments (cloud, hybrid, self-managed)
  dimensions:
  - deployment_mode
  name: deployment_environments
  unit: environment
name: Tyk Finops
provider_name: Tyk
provider_slug: tyk
publisher_name: Tyk Technologies Ltd
service_category: API Management
slug: tyk-finops
source_filename: tyk-finops.yml
source_heading: FinOps Profile
source_url: https://tyk.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tyk\nproviderId: tyk\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - API Gateway\n  - API Management\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Tyk: hybrid model combining a free open-source gateway, a usage-based\n  Core SaaS tier, a flat-rate Professional subscription, and a custom-contract Enterprise tier.'\nsources:\n  - https://tyk.io/pricing/\n  - https://tyk.io/docs/api-management/rate-limit/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tyk Technologies Ltd\nserviceCategory: API Management\nbillingModel:\n  pricingCategory: Tiered Subscription + Usage-Based\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Tyk\n  ServiceCategory: API Management\n  ProviderName: Tyk\n  PublisherName: Tyk Technologies Ltd\n  InvoiceIssuerName: Tyk Technologies Ltd\n  BillingCurrency: USD\nmeters:\n  - name: gateway_requests\n    description: Requests proxied through the Tyk gateway (Core / consumption-based tier)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n      - deployment_mode\n  - name: subscription_period\n    description: Flat Professional / Enterprise subscription term\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: deployment_environments\n    description: Number of distinct gateway environments (cloud, hybrid, self-managed)\n    unit: environment\n    aggregation: max\n    dimensions:\n      - deployment_mode\nprinciples:\n  - name: Visibility\n    description: Use Tyk Dashboard\
  \ analytics and the gateway's exported metrics (Prometheus, OpenTelemetry)\n      to surface request volume and tier consumption per API.\n  - name: Allocation\n    description: Tag API definitions and policies with consuming team / product so gateway-level usage\n      can be attributed back to internal cost centers.\n  - name: Optimization\n    description: Choose the lowest-cost deployment mode (open-source self-managed vs Tyk Cloud) per workload;\n      use rate-limit smoothing and caching policies to avoid pushing upstream usage beyond Core thresholds.\n  - name: Accountability\n    description: Assign API and gateway environment owners; review consumption against the chosen tier\n      (Core vs Professional vs Enterprise) at each renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tyk/refs/heads/main/finops/tyk-finops.yml
sources:
- https://tyk.io/pricing/
- https://tyk.io/docs/api-management/rate-limit/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- API Gateway
- API Management
- FinOps
- FOCUS
---
