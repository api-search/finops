---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: wso2-publisher-api.yaml
  format: yaml
  label: WSO2 Publisher API
  slug: publisher-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wso2/refs/heads/main/openapi/wso2-publisher-api.yaml
- filename: wso2-devportal-api.yaml
  format: yaml
  label: WSO2 Developer Portal API
  slug: devportal-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wso2/refs/heads/main/openapi/wso2-devportal-api.yaml
- filename: wso2-admin-api.yaml
  format: yaml
  label: WSO2 Admin Portal API
  slug: admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wso2/refs/heads/main/openapi/wso2-admin-api.yaml
- filename: wso2-gateway-api.yaml
  format: yaml
  label: WSO2 Gateway API
  slug: gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wso2/refs/heads/main/openapi/wso2-gateway-api.yaml
- filename: wso2-service-catalog-api.yaml
  format: yaml
  label: WSO2 Service Catalog API
  slug: service-catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wso2/refs/heads/main/openapi/wso2-service-catalog-api.yaml
- filename: wso2-devops-api.yaml
  format: yaml
  label: WSO2 DevOps API
  slug: devops-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wso2/refs/heads/main/openapi/wso2-devops-api.yaml
- filename: wso2-dcr-api.yaml
  format: yaml
  label: WSO2 DCR API
  slug: dcr-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wso2/refs/heads/main/openapi/wso2-dcr-api.yaml
- filename: wso2-governance-api.yaml
  format: yaml
  label: WSO2 Governance API
  slug: governance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wso2/refs/heads/main/openapi/wso2-governance-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Pay-As-You-Go + Subscription
description: 'FOCUS-aligned FinOps for WSO2: open-source product (no software cost) plus two SaaS cost surfaces - Choreo, billed per-component-month with infrastructure resource credits, and Asgardeo, billed per monthly-active-user across B2C / B2B / B2E. Enterprise on-prem support contracts are quote-based.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: WSO2 LLC
  ProviderName: WSO2
  PublisherName: WSO2 LLC
  ServiceCategory: API Management / Identity SaaS
  ServiceName: WSO2
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  - component
  - organization
  name: choreo_component_month
  unit: month
- aggregation: sum
  dimensions:
  - organization
  - resource_type
  name: choreo_resource_credits
  unit: USD
- aggregation: sum
  dimensions:
  - tier
  - organization
  name: choreo_builds
  unit: build
- aggregation: sum
  dimensions:
  - tier
  - organization
  name: choreo_deployments
  unit: deployment
- aggregation: sum
  dimensions:
  - tier
  - component
  name: choreo_api_requests
  unit: request
- aggregation: max
  dimensions:
  - flavor
  - tier
  - organization
  name: asgardeo_mau
  unit: mau
- aggregation: sum
  dimensions:
  - product
  - environment
  name: enterprise_subscription
  unit: month
name: Wso2 Finops
provider_name: WSO2
provider_slug: wso2
publisher_name: WSO2 LLC
service_category: API Management / Identity SaaS + Open Source
slug: wso2-finops
source_filename: wso2-finops.yml
source_heading: FinOps Profile
source_url: https://wso2.com/choreo/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: WSO2\nproviderId: wso2\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - API Management\n  - Identity\n  - Open Source\ndescription: 'FOCUS-aligned FinOps for WSO2: open-source product (no software cost) plus two SaaS\n  cost surfaces - Choreo, billed per-component-month with infrastructure resource credits, and\n  Asgardeo, billed per monthly-active-user across B2C / B2B / B2E. Enterprise on-prem support\n  contracts are quote-based.'\nsources:\n  - https://wso2.com/choreo/pricing/\n  - https://wso2.com/asgardeo/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: WSO2 LLC\nserviceCategory: API Management / Identity SaaS +\
  \ Open Source\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: WSO2\n  ServiceCategory: API Management / Identity SaaS\n  ProviderName: WSO2\n  PublisherName: WSO2 LLC\n  InvoiceIssuerName: WSO2 LLC\n  BillingCurrency: USD\nmeters:\n  - name: choreo_component_month\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - component\n      - organization\n  - name: choreo_resource_credits\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - organization\n      - resource_type\n  - name: choreo_builds\n    unit: build\n    aggregation: sum\n    dimensions:\n      - tier\n      - organization\n  - name: choreo_deployments\n    unit: deployment\n    aggregation: sum\n    dimensions:\n      - tier\n      - organization\n  - name: choreo_api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - tier\n      - component\n  - name: asgardeo_mau\n    unit: mau\n    aggregation: max\n    dimensions:\n      - flavor\n      - tier\n      - organization\n  - name: enterprise_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n      - environment\nprinciples:\n  - name: Visibility\n    description: Choreo exposes per-organization resource-credit and component-usage dashboards;\n      Asgardeo exposes MAU dashboards per flavor (B2C / B2B / B2E). On-prem WSO2 has no vendor\n      bill - operators meter their own infrastructure costs.\n  - name: Allocation\n    description: Allocate Choreo by component and organization; allocate Asgardeo by tenant /\n      sub-organization and MAU flavor. On-prem allocates by deployment environment and\n      subscription contract.\n  - name: Optimization\n    description: For Choreo, levers are right-sizing component count, scaling-to-zero unused\n      services, and managing build/deployment frequency. For Asgardeo,\
  \ MAU pruning and selecting\n      the appropriate flavor (B2C vs B2B vs B2E) are the main levers. For on-prem, throttling-\n      tier policy tuning is the operator's lever.\n  - name: Accountability\n    description: Choreo cost owned by the engineering team running components; Asgardeo cost\n      owned by the IAM team or product team owning the customer-facing app; on-prem subscription\n      cost owned by the platform team renewing the WSO2 contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wso2/refs/heads/main/finops/wso2-finops.yml
sources:
- https://wso2.com/choreo/pricing/
- https://wso2.com/asgardeo/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- API Management
- Identity
- Open Source
---
