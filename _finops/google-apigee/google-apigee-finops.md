---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yml
  format: yaml
  label: Google Apigee Management API
  slug: google-apigee-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-apigee/refs/heads/main/openapi/openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (PAYG) / Annual (Subscription)
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go + Subscription
description: 'FOCUS-aligned FinOps for Apigee: PAYG bills hourly per environment (Base/Intermediate/Comprehensive) plus API call volume; subscription tiers (Standard/Enterprise/Enterprise Plus) bill annually with negotiated caps. Apigee invoices flow through the standard Google Cloud billing surface so spend appears in the Cloud Billing export alongside other GCP services.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google LLC
  ProviderName: Google Cloud
  PublisherName: Google LLC
  ServiceCategory: API Management
  ServiceName: Apigee API Management
layout: finops
meters:
- aggregation: sum
  description: Hours that an Apigee environment is provisioned
  dimensions:
  - environment_type
  - region
  - organization
  name: environment_hours
  unit: environment-hour
- aggregation: sum
  description: API calls processed by Apigee proxies
  dimensions:
  - organization
  - environment
  - api_proxy
  - api_product
  name: api_calls
  unit: request
- aggregation: sum
  description: Provisioned gateway capacity above included environment baseline
  dimensions:
  - region
  - environment
  name: gateway_nodes
  unit: node-hour
- aggregation: sum
  description: Annual subscription seat (Standard / Enterprise / Enterprise Plus)
  dimensions:
  - tier
  name: subscription_fee
  unit: contract-year
- aggregation: sum
  description: Advanced API Security add-on volume
  dimensions:
  - environment
  name: advanced_api_security
  unit: request
- aggregation: sum
  description: API Hub catalog and discovery usage
  dimensions:
  - organization
  name: api_hub_usage
  unit: request
name: Google Apigee Finops
provider_name: Google Apigee
provider_slug: google-apigee
publisher_name: Google LLC
service_category: API Management
slug: google-apigee-finops
source_filename: google-apigee-finops.yml
source_heading: FinOps Profile
source_url: https://cloud.google.com/apigee/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Apigee\nproviderId: google-apigee\npublisherName: Google LLC\nserviceCategory: API Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - API Management\n  - API Gateway\n  - Google Cloud\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Apigee: PAYG bills hourly per environment (Base/Intermediate/Comprehensive)\n  plus API call volume; subscription tiers (Standard/Enterprise/Enterprise Plus) bill annually with negotiated\n  caps. Apigee invoices flow through the standard Google Cloud billing surface so spend appears in the\n  Cloud Billing export alongside other GCP services.'\nsources:\n  - https://cloud.google.com/apigee/pricing\n\
  \  - https://docs.cloud.google.com/apigee/docs/api-platform/reference/limits\n  - https://cloud.google.com/billing/docs\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Subscription\n  billingFrequency: Monthly (PAYG) / Annual (Subscription)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Apigee API Management\n  ServiceCategory: API Management\n  ProviderName: Google Cloud\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: environment_hours\n    description: Hours that an Apigee environment is provisioned\n    unit: environment-hour\n    aggregation: sum\n    dimensions:\n      - environment_type\n      - region\n      - organization\n  - name: api_calls\n    description: API calls processed by Apigee proxies\n    unit: request\n    aggregation: sum\n    dimensions:\n      - organization\n      - environment\n\
  \      - api_proxy\n      - api_product\n  - name: gateway_nodes\n    description: Provisioned gateway capacity above included environment baseline\n    unit: node-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - environment\n  - name: subscription_fee\n    description: Annual subscription seat (Standard / Enterprise / Enterprise Plus)\n    unit: contract-year\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: advanced_api_security\n    description: Advanced API Security add-on volume\n    unit: request\n    aggregation: sum\n    dimensions:\n      - environment\n  - name: api_hub_usage\n    description: API Hub catalog and discovery usage\n    unit: request\n    aggregation: sum\n    dimensions:\n      - organization\napis:\n  - name: Apigee API\n    baseURL: https://apigee.googleapis.com\n    serviceName: Apigee API\n    serviceCategory: API Management\n  - name: Apigee Connect API\n    baseURL: https://apigeeconnect.googleapis.com\n    serviceName: Apigee\
  \ Connect API\n    serviceCategory: API Management\n  - name: Apigee Hub API\n    baseURL: https://apihub.googleapis.com\n    serviceName: Apigee Hub API\n    serviceCategory: API Catalog\nprinciples:\n  - name: Visibility\n    description: Enable the Cloud Billing detailed export to BigQuery; filter to service `apigee.googleapis.com`\n      to see per-environment hourly cost and API call charges. Use Apigee Analytics for proxy-level traffic.\n  - name: Allocation\n    description: Tag API proxies, products, and environments with org/team labels; pivot the Cloud Billing\n      export by these labels to chargeback to consuming product teams.\n  - name: Optimization\n    description: Right-size environment type (Base vs Intermediate vs Comprehensive); collapse non-prod\n      environments outside business hours; cache responses with the ResponseCache policy to cut backend\n      and Apigee throughput cost; commit to a Subscription tier when annual run-rate exceeds PAYG break-even.\n  - name:\
  \ Accountability\n    description: Assign each Apigee environment and API product to a budget owner; configure Cloud Billing\n      budget alerts at 50/80/100% of monthly forecast and route to the owner.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-apigee/refs/heads/main/finops/google-apigee-finops.yml
sources:
- https://cloud.google.com/apigee/pricing
- https://docs.cloud.google.com/apigee/docs/api-platform/reference/limits
- https://cloud.google.com/billing/docs
specification: FinOps Framework
tags:
- API Management
- API Gateway
- Google Cloud
- FinOps
- FOCUS
---
