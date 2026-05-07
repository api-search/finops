---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: choreo-api-management-openapi.yml
  format: yaml
  label: Choreo API Management API
  slug: api-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/choreo/refs/heads/main/openapi/choreo-api-management-openapi.yml
- filename: choreo-developer-portal-openapi.yml
  format: yaml
  label: Choreo Developer Portal API
  slug: developer-portal
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/choreo/refs/heads/main/openapi/choreo-developer-portal-openapi.yml
- filename: choreo-insights-openapi.yml
  format: yaml
  label: Choreo Insights API
  slug: insights
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/choreo/refs/heads/main/openapi/choreo-insights-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Credit
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Choreo: tiered subscription (Developer / Team / Enterprise) combined with pass-through infrastructure billing once free credits are exhausted. Per-component Team pricing plus monthly resource credits creates a hybrid Subscription + Pay-As-You-Go shape on Team and Enterprise.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: WSO2 LLC
  PricingCategory: Subscription
  ProviderName: WSO2
  PublisherName: WSO2 LLC
  ServiceCategory: Internal Developer Platform
  ServiceName: Choreo
layout: finops
meters:
- aggregation: sum
  description: Number of components subscribed under the Team plan
  dimensions:
  - project
  - organization
  name: component_subscription
  unit: component-month
- aggregation: sum
  description: CI builds executed
  dimensions:
  - project
  - component
  name: builds
  unit: build
- aggregation: sum
  description: Deployments executed
  dimensions:
  - project
  - environment
  name: deployments
  unit: deployment
- aggregation: sum
  description: API requests served through Choreo gateways
  dimensions:
  - api
  - environment
  - subscription
  name: api_requests
  unit: request
- aggregation: sum
  description: Log MB ingested (per day, with retention by plan)
  dimensions:
  - component
  - environment
  name: log_volume
  unit: MB-day
- aggregation: sum
  description: vCPU, RAM, storage, and network consumed on the Choreo data plane (pass-through on Team and Enterprise)
  dimensions:
  - resource_type
  - environment
  - region
  name: infrastructure
  unit: varies
name: Choreo Finops
provider_name: Choreo
provider_slug: choreo
publisher_name: WSO2 LLC
service_category: Internal Developer Platform
slug: choreo-finops
source_filename: choreo-finops.yml
source_heading: FinOps Profile
source_url: https://wso2.com/choreo/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Choreo\nproviderId: choreo\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - API Management\n  - Cloud Native\n  - Internal Developer Platform\n  - Kubernetes\n  - Platform Engineering\n  - WSO2\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Choreo: tiered subscription (Developer / Team / Enterprise)\n  combined with pass-through infrastructure billing once free credits are exhausted. Per-component\n  Team pricing plus monthly resource credits creates a hybrid Subscription + Pay-As-You-Go shape on\n  Team and Enterprise.'\nsources:\n  - https://wso2.com/choreo/pricing/\n  - https://wso2.com/choreo/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ WSO2 LLC\nserviceCategory: Internal Developer Platform\nbillingModel:\n  pricingCategory: Tiered Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Credit\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Choreo\n  ServiceCategory: Internal Developer Platform\n  ProviderName: WSO2\n  PublisherName: WSO2 LLC\n  InvoiceIssuerName: WSO2 LLC\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingCategory: Subscription\nmeters:\n  - name: component_subscription\n    description: Number of components subscribed under the Team plan\n    unit: component-month\n    aggregation: sum\n    dimensions:\n      - project\n      - organization\n  - name: builds\n    description: CI builds executed\n    unit: build\n    aggregation: sum\n    dimensions:\n      - project\n      - component\n  - name: deployments\n    description: Deployments executed\n    unit: deployment\n    aggregation: sum\n    dimensions:\n\
  \      - project\n      - environment\n  - name: api_requests\n    description: API requests served through Choreo gateways\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n      - subscription\n  - name: log_volume\n    description: Log MB ingested (per day, with retention by plan)\n    unit: MB-day\n    aggregation: sum\n    dimensions:\n      - component\n      - environment\n  - name: infrastructure\n    description: vCPU, RAM, storage, and network consumed on the Choreo data plane (pass-through on\n      Team and Enterprise)\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - resource_type\n      - environment\n      - region\nprinciples:\n  - name: Visibility\n    description: Use the Choreo console's Cost Insights and consumption dashboards to track resource\n      credit burn-down, build / deployment counts, and request volumes per project.\n  - name: Allocation\n    description: Tag spend by Choreo project, environment,\
  \ and team — the per-component Team pricing\n      makes component ownership the natural showback boundary.\n  - name: Optimization\n    description: Right-size component CPU/RAM, scale to zero where possible, prune unused builds and\n      old logs, and consolidate components before crossing the next per-component price step.\n  - name: Accountability\n    description: Platform team owns the Choreo subscription tier; product engineering owns per-component\n      consumption; finance reconciles WSO2 invoices and the in-product credit ledger.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/choreo/refs/heads/main/finops/choreo-finops.yml
sources:
- https://wso2.com/choreo/pricing/
- https://wso2.com/choreo/
specification: FinOps Framework
tags:
- API Management
- Cloud Native
- Internal Developer Platform
- Kubernetes
- Platform Engineering
- WSO2
- FinOps
- FOCUS
---
