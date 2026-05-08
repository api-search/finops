---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: oracle-retail-merchandising-openapi.yml
  format: yaml
  label: Oracle Retail Merchandising Foundation Cloud Service API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-retail/refs/heads/main/openapi/oracle-retail-merchandising-openapi.yml
- filename: oracle-retail-order-management-openapi.yml
  format: yaml
  label: Oracle Retail Order Management Suite Cloud Service API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-retail/refs/heads/main/openapi/oracle-retail-order-management-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription (Per Application)
description: 'FOCUS-aligned FinOps view for Oracle Retail: per-application SaaS subscriptions billed against retail-specific metrics (Annual Subscriber Revenue, Hosted Named User, POS Lane / Store) on the Oracle Retail price list. REST API access is bundled with the subscription. FinOps observation centres on the per-application metric (revenue tier, seat count, lane / store count) rather than per-call consumption.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Oracle America, Inc.
  PricingCategory: Subscription
  ProviderName: Oracle
  PublisherName: Oracle America, Inc.
  ServiceCategory: Retail Applications
  ServiceName: Oracle Retail
layout: finops
meters:
- aggregation: max
  description: Annual Subscriber Revenue tier on metered Retail Cloud Services
  dimensions:
  - service
  - business_unit
  name: annual_subscriber_revenue_tier
  unit: usd-annual-revenue
- aggregation: max
  description: Hosted Named User seats per month
  dimensions:
  - service
  - role
  name: hosted_named_user_subscription
  unit: seat-month
- aggregation: max
  description: Active POS lanes per month for Xstore Point of Service
  dimensions:
  - banner
  - region
  name: pos_lane_subscription
  unit: lane-month
- aggregation: max
  description: Active stores per month for Xstore Point of Service
  dimensions:
  - banner
  - region
  name: store_subscription
  unit: store-month
- aggregation: sum
  description: REST API calls (informational; bundled in the subscription)
  dimensions:
  - service
  - api
  - endpoint
  name: rest_api_calls
  unit: request
name: Oracle Retail Finops
provider_name: Oracle Retail
provider_slug: oracle-retail
publisher_name: Oracle America, Inc.
service_category: Retail Applications
slug: oracle-retail-finops
source_filename: oracle-retail-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/industries/retail/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Retail\nproviderId: oracle-retail\npublisherName: Oracle America, Inc.\nserviceCategory: Retail Applications\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Retail\n  - Merchandising\n  - Omnichannel\n  - Oracle Cloud\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view for Oracle Retail: per-application SaaS\n  subscriptions billed against retail-specific metrics (Annual Subscriber\n  Revenue, Hosted Named User, POS Lane / Store) on the Oracle Retail price\n  list. REST API access is bundled with the subscription. FinOps observation\n  centres on the per-application metric (revenue tier, seat\
  \ count, lane /\n  store count) rather than per-call consumption.\nsources:\n  - https://www.oracle.com/industries/retail/\n  - https://docs.oracle.com/en/industries/retail/\nnotes: >-\n  No per-API meter exists. Track the contractual metric per Retail Cloud\n  Service (revenue tier, seat count, lane count) at each renewal cycle.\nbillingModel:\n  pricingCategory: Tiered Subscription (Per Application)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Oracle Retail\n  ServiceCategory: Retail Applications\n  ProviderName: Oracle\n  PublisherName: Oracle America, Inc.\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\n  PricingCategory: Subscription\n  ChargeCategory: Purchase\nmeters:\n  - name: annual_subscriber_revenue_tier\n    description: Annual Subscriber Revenue tier on metered Retail Cloud Services\n    unit: usd-annual-revenue\n    aggregation: max\n\
  \    dimensions:\n      - service\n      - business_unit\n  - name: hosted_named_user_subscription\n    description: Hosted Named User seats per month\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - service\n      - role\n  - name: pos_lane_subscription\n    description: Active POS lanes per month for Xstore Point of Service\n    unit: lane-month\n    aggregation: max\n    dimensions:\n      - banner\n      - region\n  - name: store_subscription\n    description: Active stores per month for Xstore Point of Service\n    unit: store-month\n    aggregation: max\n    dimensions:\n      - banner\n      - region\n  - name: rest_api_calls\n    description: REST API calls (informational; bundled in the subscription)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - api\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: >-\n      Maintain a tenancy-level inventory of Oracle Retail Cloud Service\n      subscriptions, contractual\
  \ metrics, and active lane / store counts;\n      reconcile annually against the Oracle order document.\n  - name: Allocation\n    description: >-\n      Tag each Retail subscription with the consuming banner, region, and\n      business unit so spend can be attributed back to the operating\n      business.\n  - name: Optimization\n    description: >-\n      Reclaim inactive seats, decommission lanes for closed stores at the\n      monthly snapshot, and prefer RICS bulk patterns over transactional\n      REST integrations to reduce capacity pressure on the Retail Cloud pod.\n  - name: Accountability\n    description: >-\n      Pair the Retail applications administrator with retail-finance and\n      store-operations owners; review metric utilization at quarterly\n      business reviews.\napis:\n  - name: Oracle Retail Merchandising Foundation Cloud Service API\n    serviceName: Oracle Retail Merchandising Foundation Cloud Service API\n    serviceCategory: Retail Applications\n  - name:\
  \ Oracle Retail Pricing Cloud Service API\n    serviceName: Oracle Retail Pricing Cloud Service API\n    serviceCategory: Retail Applications\n  - name: Oracle Retail Integration Cloud Service API\n    serviceName: Oracle Retail Integration Cloud Service API\n    serviceCategory: Retail Applications\n  - name: Oracle Retail Order Management Suite Cloud Service API\n    serviceName: Oracle Retail Order Management Suite Cloud Service API\n    serviceCategory: Retail Applications\n  - name: Oracle Retail Xstore Point of Service API\n    serviceName: Oracle Retail Xstore Point of Service API\n    serviceCategory: Retail Applications\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-retail/refs/heads/main/finops/oracle-retail-finops.yml
sources:
- https://www.oracle.com/industries/retail/
- https://docs.oracle.com/en/industries/retail/
specification: FinOps Framework
tags:
- Retail
- Merchandising
- Omnichannel
- Oracle Cloud
- FinOps
- FOCUS
---
