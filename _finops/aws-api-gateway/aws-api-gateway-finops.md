---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: aws-api-gateway-v1-openapi.yml
  format: yaml
  label: Amazon API Gateway V1 (REST)
  slug: aws-api-gateway-v1
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aws-api-gateway/refs/heads/main/openapi/aws-api-gateway-v1-openapi.yml
- filename: aws-api-gateway-v2-openapi.yml
  format: yaml
  label: Amazon API Gateway V2 (HTTP and WebSocket)
  slug: aws-api-gateway-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aws-api-gateway/refs/heads/main/openapi/aws-api-gateway-v2-openapi.yml
- filename: aws-api-gateway-management-openapi.yml
  format: yaml
  label: Amazon API Gateway Management API
  slug: aws-api-gateway-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aws-api-gateway/refs/heads/main/openapi/aws-api-gateway-management-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Pay-As-You-Go
description: 'FOCUS-aligned FinOps for AWS API Gateway: pay-as-you-go per-million-call pricing per API type, plus data transfer out, optional cache hours, optional portal subscription, and a 12-month free tier. Cost is driven by call volume and the chosen API type (HTTP cheaper than REST).'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Amazon Web Services, Inc.
  ProviderName: AWS
  PublisherName: Amazon Web Services, Inc.
  RegionId: varies
  ServiceCategory: API Management
  ServiceName: Amazon API Gateway
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - api_id
  - stage
  name: rest_api_calls
  unit: request
- aggregation: sum
  dimensions:
  - region
  - api_id
  - stage
  name: http_api_calls
  unit: request
- aggregation: sum
  dimensions:
  - region
  - api_id
  name: websocket_messages
  unit: message
- aggregation: sum
  dimensions:
  - region
  - api_id
  name: websocket_connection_minutes
  unit: minute
- aggregation: sum
  dimensions:
  - region
  name: data_transfer_out
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - cache_size
  name: cache_hours
  unit: hour
- aggregation: sum
  dimensions:
  - portal_id
  name: portal_subscription
  unit: month
- aggregation: sum
  name: portal_product_addon
  unit: product-month
name: Aws Api Gateway Finops
provider_name: Amazon API Gateway
provider_slug: aws-api-gateway
publisher_name: Amazon Web Services, Inc.
service_category: API Management / Serverless
slug: aws-api-gateway-finops
source_filename: aws-api-gateway-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/api-gateway/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AWS API Gateway\nproviderId: aws-api-gateway\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - API Management\n  - Serverless\n  - AWS\ndescription: 'FOCUS-aligned FinOps for AWS API Gateway: pay-as-you-go per-million-call pricing per\n  API type, plus data transfer out, optional cache hours, optional portal subscription, and a\n  12-month free tier. Cost is driven by call volume and the chosen API type (HTTP cheaper than REST).'\nsources:\n  - https://aws.amazon.com/api-gateway/pricing/\n  - https://docs.aws.amazon.com/apigateway/latest/developerguide/limits.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon Web Services,\
  \ Inc.\nserviceCategory: API Management / Serverless\nbillingModel:\n  pricingCategory: Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Amazon API Gateway\n  ServiceCategory: API Management\n  ProviderName: AWS\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  RegionId: varies\nmeters:\n  - name: rest_api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - region\n      - api_id\n      - stage\n  - name: http_api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - region\n      - api_id\n      - stage\n  - name: websocket_messages\n    unit: message\n    aggregation: sum\n    dimensions:\n      - region\n      - api_id\n  - name: websocket_connection_minutes\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - region\n      -\
  \ api_id\n  - name: data_transfer_out\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n  - name: cache_hours\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - region\n      - cache_size\n  - name: portal_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - portal_id\n  - name: portal_product_addon\n    unit: product-month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use CloudWatch Metrics (Count, IntegrationLatency, 4XXError, 5XXError, CacheHitCount)\n      per APIName + Stage; the Cost Explorer \"Amazon API Gateway\" service shows usage-type breakdown.\n      Tag stages with cost allocation tags for FOCUS-aligned reporting.\n  - name: Allocation\n    description: Tag REST API stages and HTTP APIs with team / product / environment cost allocation\n      tags; Cost & Usage Reports map UsageType (e.g. ApiGatewayRequest, ApiGatewayHttpApiRequest)\n      to FOCUS ServiceSubcategory.\n  - name: Optimization\n\
  \    description: Migrate suitable workloads from REST API ($3.50/M) to HTTP API ($1.00/M) for ~70%\n      savings; turn off caching where hit rate is low; right-size cache to the smallest tier that\n      yields useful hit rate; avoid edge-optimized for in-region traffic.\n  - name: Accountability\n    description: Platform team typically owns API Gateway; product teams own per-API cost via tags and\n      usage-plan-bound API keys for chargeback.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aws-api-gateway/refs/heads/main/finops/aws-api-gateway-finops.yml
sources:
- https://aws.amazon.com/api-gateway/pricing/
- https://docs.aws.amazon.com/apigateway/latest/developerguide/limits.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- API Management
- Serverless
---
