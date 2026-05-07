---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-azure-api-management-rest-api-openapi.yaml
  format: yaml
  label: Azure API Management REST API
  slug: azure-api-management-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-api-management/refs/heads/main/openapi/microsoft-azure-api-management-rest-api-openapi.yaml
- filename: microsoft-azure-api-management-gateway-openapi.yaml
  format: yaml
  label: Azure API Management Gateway
  slug: azure-api-management-gateway
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-api-management/refs/heads/main/openapi/microsoft-azure-api-management-gateway-openapi.yaml
- filename: microsoft-azure-api-management-self-hosted-gateway-openapi.yaml
  format: yaml
  label: Azure API Management Self-Hosted Gateway
  slug: azure-api-management-self-hosted-gateway
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-api-management/refs/heads/main/openapi/microsoft-azure-api-management-self-hosted-gateway-openapi.yaml
- filename: microsoft-azure-api-management-ai-gateway-openapi.yaml
  format: yaml
  label: Azure API Management AI Gateway
  slug: azure-api-management-ai-gateway
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-api-management/refs/heads/main/openapi/microsoft-azure-api-management-ai-gateway-openapi.yaml
- filename: microsoft-azure-api-management-developer-portal-openapi.yaml
  format: yaml
  label: Azure API Management Developer Portal
  slug: azure-api-management-developer-portal
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-api-management/refs/heads/main/openapi/microsoft-azure-api-management-developer-portal-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Azure API Management: hourly per-scale-unit billing on classic and v2 tiers, plus per-million-call metering on the Consumption tier.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Integration / API Gateway
  ServiceName: Azure API Management
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  - region
  - resource
  name: scale_unit_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - region
  - api
  name: consumption_calls
  unit: call
- aggregation: max
  dimensions:
  - tier
  name: cache_storage
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - direction
  name: data_transfer
  unit: GB
name: Microsoft Azure Api Management Finops
provider_name: Microsoft Azure API Management
provider_slug: microsoft-azure-api-management
publisher_name: Microsoft Corporation
service_category: Integration / API Gateway
slug: microsoft-azure-api-management-finops
source_filename: microsoft-azure-api-management-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/api-management/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Azure API Management\nproviderId: microsoft-azure-api-management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - API Management\n  - Microsoft Azure\ndescription: 'FOCUS-aligned FinOps for Azure API Management: hourly per-scale-unit billing on classic\n  and v2 tiers, plus per-million-call metering on the Consumption tier.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/api-management/\n  - https://learn.microsoft.com/en-us/azure/api-management/plan-manage-costs\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Integration / API Gateway\nbillingModel:\n  pricingCategory:\
  \ Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Azure API Management\n  ServiceCategory: Integration / API Gateway\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: scale_unit_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - tier\n      - region\n      - resource\n  - name: consumption_calls\n    unit: call\n    aggregation: sum\n    dimensions:\n      - region\n      - api\n  - name: cache_storage\n    unit: GB\n    aggregation: max\n    dimensions:\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - direction\nprinciples:\n  - name: Visibility\n    description: Use Azure Cost Management cost analysis filtered\
  \ on resource type 'Microsoft.ApiManagement/service'\n      and the service's diagnostic logs to break down per-API and per-product call volume.\n  - name: Allocation\n    description: Tag API Management instances with cost-center and product tags; group APIs into\n      Products with subscription keys per consumer team for chargeback.\n  - name: Optimization\n    description: Right-size scale units; use Consumption tier for spiky workloads; consolidate dev/test\n      onto Developer tier; use Premium multi-region only where required; apply caching policies to\n      reduce backend cost.\n  - name: Accountability\n    description: Assign API product owners as cost owners; alert on scale-unit count drift; review\n      autoscale settings on v2 tiers to avoid runaway scale-out.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-api-management/refs/heads/main/finops/microsoft-azure-api-management-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/api-management/
- https://learn.microsoft.com/en-us/azure/api-management/plan-manage-costs
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- API Management
- Microsoft Azure
---
