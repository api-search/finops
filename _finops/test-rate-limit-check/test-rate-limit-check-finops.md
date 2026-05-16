---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Kong Gateway Admin API
  slug: kong-gateway-admin-api
  spec_type: OpenAPI
  url: https://docs.konghq.com/gateway/latest/admin-api/
- filename: x-tyk-gateway.json
  format: json
  label: Tyk API Management API
  slug: tyk-api-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/TykTechnologies/tyk/master/apidef/oas/schema/x-tyk-gateway.json
- filename: api-spec.json
  format: json
  label: Grafana API
  slug: grafana-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/grafana/grafana/main/public/api-spec.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Test Rate Limit Check API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Test Rate Limit Check
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Test Rate Limit Check
  PublisherName: Test Rate Limit Check
  ServiceCategory: Developer Tools / API
  ServiceName: Test Rate Limit Check
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Test Rate Limit Check Finops
provider_name: Test Rate Limit Check
provider_slug: test-rate-limit-check
publisher_name: Test Rate Limit Check
service_category: API
slug: test-rate-limit-check-finops
source_filename: test-rate-limit-check-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Test Rate Limit Check\nproviderId: test-rate-limit-check\npublisherName: Test Rate Limit Check\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - API Governance\n  - API Management\n  - API Testing\n  - Performance Testing\n  - Rate Limiting\n  - Testing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Test Rate Limit Check API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Test Rate Limit Check\n  ServiceCategory: Developer Tools / API\n  ProviderName: Test Rate Limit Check\n  PublisherName: Test Rate Limit Check\n  InvoiceIssuerName: Test Rate Limit Check\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Kong Gateway Admin API\n    baseURL: https://your-kong.example.com:8001\n    tags:\n      - API Gateway\n      - API Management\n      - Rate Limiting\n      - Traffic Control\n    serviceName: Kong Gateway Admin API\n    serviceCategory: API\n  - name: AWS API Gateway API\n    baseURL: https://apigateway.amazonaws.com\n    tags:\n      - AWS\n      - API Gateway\n      - Cloud\n      - Rate Limiting\n    serviceName: AWS API Gateway API\n    serviceCategory: API\n  - name: Apigee API\n    baseURL: https://apigee.googleapis.com/v1\n    tags:\n      - API Management\n      - Google\
  \ Cloud\n      - Quotas\n      - Rate Limiting\n    serviceName: Apigee API\n    serviceCategory: API\n  - name: Azure API Management API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ApiManagement/service/{serviceName}\n    tags:\n      - API Management\n      - Azure\n      - Microsoft\n      - Rate Limiting\n    serviceName: Azure API Management API\n    serviceCategory: API\n  - name: Tyk API Management API\n    baseURL: https://your-tyk.example.com/api\n    tags:\n      - API Gateway\n      - API Management\n      - Open Source\n      - Rate Limiting\n    serviceName: Tyk API Management API\n    serviceCategory: API\n  - name: Grafana API\n    baseURL: https://your-grafana.example.com/api\n    tags:\n      - Dashboards\n      - Metrics\n      - Monitoring\n      - Observability\n    serviceName: Grafana API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost\
  \ / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/test-rate-limit-check/refs/heads/main/finops/test-rate-limit-check-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Governance
- API Management
- API Testing
- Performance Testing
- Rate Limiting
- Testing
- FinOps
- Cost Management
- FOCUS
---
