---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: gravitee-management-api-openapi.yml
  format: yaml
  label: Gravitee Management API
  slug: gravitee-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gravitee/refs/heads/main/openapi/gravitee-management-api-openapi.yml
- filename: gravitee-access-management-api-openapi.yml
  format: yaml
  label: Gravitee Access Management API
  slug: gravitee-access-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gravitee/refs/heads/main/openapi/gravitee-access-management-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Gravitee: flat-rate monthly subscription per platform tier (with included gateways, brokers, and unlimited API calls / events) plus optional add-on packages. Cost grows with platform tier and add-ons, not with per-call traffic.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Gravitee.io, Inc.
  ProviderName: Gravitee
  PublisherName: Gravitee.io, Inc.
  ServiceCategory: API Management
  ServiceName: Gravitee
layout: finops
meters:
- aggregation: sum
  description: Monthly Gravitee platform subscription fee per tier
  dimensions:
  - product
  - tier
  name: platform_subscription
  unit: month
- aggregation: max
  description: Production gateway count consumed per subscription
  dimensions:
  - product
  - tier
  name: production_gateways
  unit: gateway
- aggregation: max
  description: Third-party federated event brokers consumed (Event Management tiers)
  dimensions:
  - tier
  name: federated_brokers
  unit: broker
- aggregation: max
  description: Optional Agent Management / Enterprise Auth add-on packages
  dimensions:
  - addon_name
  name: addon_packages
  unit: package
- aggregation: max
  description: APIs managed in the platform (operational metric — unlimited per subscription)
  name: managed_apis
  unit: api
name: Gravitee Finops
provider_name: Gravitee
provider_slug: gravitee
publisher_name: Gravitee.io, Inc.
service_category: API Management
slug: gravitee-finops
source_filename: gravitee-finops.yml
source_heading: FinOps Profile
source_url: https://www.gravitee.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Gravitee\nproviderId: gravitee\npublisherName: Gravitee.io, Inc.\nserviceCategory: API Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - API Management\n  - API Gateway\n  - Event Streaming\ndescription: 'FOCUS-aligned FinOps for Gravitee: flat-rate monthly subscription per platform tier\n  (with included gateways, brokers, and unlimited API calls / events) plus optional add-on packages.\n  Cost grows with platform tier and add-ons, not with per-call traffic.'\nsources:\n  - https://www.gravitee.io/pricing\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Gravitee\n  ServiceCategory: API Management\n  ProviderName: Gravitee\n  PublisherName: Gravitee.io, Inc.\n  InvoiceIssuerName: Gravitee.io, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: platform_subscription\n    description: Monthly Gravitee platform subscription fee per tier\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n      - tier\n  - name: production_gateways\n    description: Production gateway count consumed per subscription\n    unit: gateway\n    aggregation: max\n    dimensions:\n      - product\n      - tier\n  - name: federated_brokers\n    description: Third-party federated event brokers consumed (Event Management tiers)\n    unit: broker\n    aggregation: max\n    dimensions:\n      - tier\n  - name: addon_packages\n    description: Optional Agent Management / Enterprise Auth add-on packages\n\
  \    unit: package\n    aggregation: max\n    dimensions:\n      - addon_name\n  - name: managed_apis\n    description: APIs managed in the platform (operational metric — unlimited per subscription)\n    unit: api\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Use Gravitee's Analytics / Monitoring views and the Management API to track gateway\n      utilization, API call volume, and consumer growth even though calls are not directly billed.\n  - name: Allocation\n    description: Map Gravitee environments / organizations to consuming business units; allocate the\n      flat subscription fee proportionally based on managed-API count or gateway-traffic share.\n  - name: Optimization\n    description: Right-size the subscription tier (Planet vs Galaxy vs Universe) to gateway and\n      broker need; consolidate dev / test environments into a single non-prod tier; defer\n      Agent / Enterprise Auth add-ons until adoption justifies them.\n  - name: Accountability\n\
  \    description: Designate a platform owner for the Gravitee contract and review tier-fit annually\n      against actual gateway / broker usage and feature consumption.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gravitee/refs/heads/main/finops/gravitee-finops.yml
sources:
- https://www.gravitee.io/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- API Management
- API Gateway
- Event Streaming
---
