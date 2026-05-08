---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mulesoft-anypoint-platform-openapi.yml
  format: yaml
  label: MuleSoft Anypoint Platform Management API
  slug: mulesoft-anypoint-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mulesoft/refs/heads/main/openapi/mulesoft-anypoint-platform-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  - Tax
  pricingCategory: Capacity-Based Subscription + Add-Ons
description: 'FOCUS-aligned FinOps for MuleSoft Anypoint Platform: capacity-based subscription billing measured in Mule Flow / Mule Message capacity (vCores), with a layered support tier (Gold / Platinum / Titanium) and optional add-on modules. Invoiced by Salesforce Inc. as the publisher; consumption observability comes from the Anypoint Usage Reports.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Salesforce, Inc.
  ProviderName: MuleSoft
  PublisherName: Salesforce, Inc.
  ServiceCategory: Integration Platform / API Management
  ServiceName: MuleSoft Anypoint Platform
layout: finops
meters:
- aggregation: max
  dimensions:
  - environment
  - region
  - runtime
  name: vcore_capacity
  unit: vCore
- aggregation: max
  dimensions:
  - api
  - environment
  name: mule_flows
  unit: flow
- aggregation: sum
  dimensions:
  - api
  - environment
  - runtime
  name: mule_messages
  unit: message
- aggregation: sum
  dimensions:
  - api
  - environment
  - client_application
  name: api_calls
  unit: request
- aggregation: max
  dimensions:
  - addon
  name: addon_seats
  unit: month
name: Mulesoft Finops
provider_name: MuleSoft
provider_slug: mulesoft
publisher_name: Salesforce, Inc.
service_category: Integration Platform / API Management
slug: mulesoft-finops
source_filename: mulesoft-finops.yml
source_heading: FinOps Profile
source_url: https://www.mulesoft.com/anypoint-pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: MuleSoft\nproviderId: mulesoft\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - API Management\n  - Integration Platform\n  - Anypoint Platform\ndescription: 'FOCUS-aligned FinOps for MuleSoft Anypoint Platform: capacity-based subscription billing\n  measured in Mule Flow / Mule Message capacity (vCores), with a layered support tier (Gold / Platinum\n  / Titanium) and optional add-on modules. Invoiced by Salesforce Inc. as the publisher; consumption observability\n  comes from the Anypoint Usage Reports.'\nsources:\n  - https://www.mulesoft.com/anypoint-pricing\n  - https://www.salesforce.com/mulesoft/anypoint-platform/pricing/\n  - https://docs.mulesoft.com/general/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Salesforce, Inc.\nserviceCategory: Integration Platform / API Management\nbillingModel:\n  pricingCategory: Capacity-Based Subscription + Add-Ons\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: MuleSoft Anypoint Platform\n  ServiceCategory: Integration Platform / API Management\n  ProviderName: MuleSoft\n  PublisherName: Salesforce, Inc.\n  InvoiceIssuerName: Salesforce, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: vcore_capacity\n    unit: vCore\n    aggregation: max\n    dimensions:\n      - environment\n      - region\n      - runtime\n  - name: mule_flows\n    unit: flow\n    aggregation: max\n    dimensions:\n      - api\n      - environment\n  - name: mule_messages\n    unit: message\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n      - runtime\n  - name: api_calls\n\
  \    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n      - client_application\n  - name: addon_seats\n    unit: month\n    aggregation: max\n    dimensions:\n      - addon\nprinciples:\n  - name: Visibility\n    description: Use Anypoint Usage Reports for vCore / flow / message consumption against the contracted\n      capacity; expose API Manager X-Ratelimit-* headers to client teams for self-service awareness.\n  - name: Allocation\n    description: Tag APIs and Mule applications with consuming line-of-business, environment, and product\n      owner; aggregate Anypoint Usage Reports by these tags for chargeback.\n  - name: Optimization\n    description: Right-size vCore capacity per environment, prune low-throughput APIs, lean on Flex Gateway\n      replicas before adding capacity, and consolidate add-ons (Monitoring, Security, DataGraph) only\n      where the LOB benefits.\n  - name: Accountability\n    description: The platform owner runs renewal\
  \ sizing against Anypoint Usage Reports; LOB API owners\n      own their per-API throughput SLAs and Rate-Limiting SLA contract definitions; procurement aligns\n      add-on renewals with the master Salesforce contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mulesoft/refs/heads/main/finops/mulesoft-finops.yml
sources:
- https://www.mulesoft.com/anypoint-pricing
- https://www.salesforce.com/mulesoft/anypoint-platform/pricing/
- https://docs.mulesoft.com/general/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- API Management
- Integration Platform
- Anypoint Platform
---
