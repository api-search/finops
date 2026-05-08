---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: api-rest-api.html
  format: yaml
  label: Oracle Fusion ERP REST API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/22r3/farfa/api-rest-api.html
- filename: api-rest-api.html
  format: yaml
  label: Oracle Fusion HCM REST API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/human-resources/22r3/farws/api-rest-api.html
- filename: api-rest-api.html
  format: yaml
  label: Oracle Fusion SCM REST API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/supply-chain-management/22r3/fasrs/api-rest-api.html
- filename: rest-api.html
  format: yaml
  label: Oracle Fusion CX Sales and Fusion Service REST API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/cx-sales/rest-api.html
- filename: oracle-fusion-common-openapi.yml
  format: yaml
  label: Oracle Fusion Common Features REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-fusion/refs/heads/main/openapi/oracle-fusion-common-openapi.yml
- filename: oracle-fusion-project-management-openapi.yml
  format: yaml
  label: Oracle Fusion Project Management REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-fusion/refs/heads/main/openapi/oracle-fusion-project-management-openapi.yml
- filename: oracle-fusion-epm-openapi.yml
  format: yaml
  label: Oracle Fusion EPM REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-fusion/refs/heads/main/openapi/oracle-fusion-epm-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription (Per Pillar)
description: 'FOCUS-aligned FinOps view for Oracle Fusion Cloud Applications: per-pillar SaaS subscriptions billed monthly per Hosted Named User / Hosted Employee / Hosted Single-Sign-On Employee. REST API access is bundled with the pillar subscription. FinOps observation centres on per-pillar seat utilization rather than per-call consumption.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Oracle America, Inc.
  PricingCategory: Subscription
  ProviderName: Oracle
  PublisherName: Oracle America, Inc.
  ServiceCategory: SaaS Applications
  ServiceName: Oracle Fusion Cloud Applications
layout: finops
meters:
- aggregation: max
  description: Active Hosted Named User seats per pillar per month
  dimensions:
  - pillar
  - module
  - business_unit
  name: hosted_named_user_subscription
  unit: seat-month
- aggregation: max
  description: Hosted Employee seats per pillar per month
  dimensions:
  - pillar
  - module
  - business_unit
  name: hosted_employee_subscription
  unit: employee-month
- aggregation: max
  description: Hosted Single-Sign-On Employee seats per month
  dimensions:
  - pillar
  - module
  name: hosted_sso_employee_subscription
  unit: employee-month
- aggregation: sum
  description: REST API calls (informational; bundled in the subscription)
  dimensions:
  - pillar
  - api
  - endpoint
  - consumer
  name: rest_api_calls
  unit: request
name: Oracle Fusion Finops
provider_name: Oracle Fusion Cloud Applications
provider_slug: oracle-fusion
publisher_name: Oracle America, Inc.
service_category: SaaS Applications
slug: oracle-fusion-finops
source_filename: oracle-fusion-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/applications/cloud/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Fusion Cloud Applications\nproviderId: oracle-fusion\npublisherName: Oracle America, Inc.\nserviceCategory: SaaS Applications\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - ERP\n  - HCM\n  - SaaS\n  - Oracle Cloud\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view for Oracle Fusion Cloud Applications: per-pillar\n  SaaS subscriptions billed monthly per Hosted Named User / Hosted Employee /\n  Hosted Single-Sign-On Employee. REST API access is bundled with the\n  pillar subscription. FinOps observation centres on per-pillar seat\n  utilization rather than per-call consumption.\nsources:\n  -\
  \ https://www.oracle.com/applications/cloud/\n  - https://docs.oracle.com/en/cloud/saas/\nnotes: >-\n  No per-API meter exists. Track license seat utilization per pillar (ERP,\n  HCM, SCM, CX, EPM) through the Fusion Applications usage reports and\n  reconcile against the contractual seat counts on each pillar order document.\nbillingModel:\n  pricingCategory: Tiered Subscription (Per Pillar)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Oracle Fusion Cloud Applications\n  ServiceCategory: SaaS Applications\n  ProviderName: Oracle\n  PublisherName: Oracle America, Inc.\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\n  PricingCategory: Subscription\n  ChargeCategory: Purchase\nmeters:\n  - name: hosted_named_user_subscription\n    description: Active Hosted Named User seats per pillar per month\n    unit: seat-month\n    aggregation: max\n    dimensions:\n\
  \      - pillar\n      - module\n      - business_unit\n  - name: hosted_employee_subscription\n    description: Hosted Employee seats per pillar per month\n    unit: employee-month\n    aggregation: max\n    dimensions:\n      - pillar\n      - module\n      - business_unit\n  - name: hosted_sso_employee_subscription\n    description: Hosted Single-Sign-On Employee seats per month\n    unit: employee-month\n    aggregation: max\n    dimensions:\n      - pillar\n      - module\n  - name: rest_api_calls\n    description: REST API calls (informational; bundled in the subscription)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - pillar\n      - api\n      - endpoint\n      - consumer\nprinciples:\n  - name: Visibility\n    description: >-\n      Review per-pillar seat utilization through the Fusion Applications\n      Security Console and Manage Users area; reconcile monthly against the\n      contractual seat counts captured on each pillar's order document.\n  - name:\
  \ Allocation\n    description: >-\n      Tag user records with pillar, business unit, and cost center so seat\n      cost can be allocated back to consuming finance teams.\n  - name: Optimization\n    description: >-\n      Reclaim inactive seats, consolidate duplicate user records across\n      pillars, and use the lower-priced Hosted Employee or Hosted SSO\n      Employee metrics for light-touch users where the module supports them.\n  - name: Accountability\n    description: >-\n      Pair each pillar's applications administrator with a finance partner;\n      review seat growth and renewal scoping at quarterly business reviews.\napis:\n  - name: Oracle Fusion ERP REST API\n    serviceName: Oracle Fusion ERP REST API\n    serviceCategory: SaaS Applications\n  - name: Oracle Fusion HCM REST API\n    serviceName: Oracle Fusion HCM REST API\n    serviceCategory: SaaS Applications\n  - name: Oracle Fusion SCM REST API\n    serviceName: Oracle Fusion SCM REST API\n    serviceCategory: SaaS\
  \ Applications\n  - name: Oracle Fusion CX Sales and Fusion Service REST API\n    serviceName: Oracle Fusion CX Sales and Fusion Service REST API\n    serviceCategory: SaaS Applications\n  - name: Oracle Fusion Common Features REST API\n    serviceName: Oracle Fusion Common Features REST API\n    serviceCategory: SaaS Applications\n  - name: Oracle Fusion Project Management REST API\n    serviceName: Oracle Fusion Project Management REST API\n    serviceCategory: SaaS Applications\n  - name: Oracle Fusion EPM REST API\n    serviceName: Oracle Fusion EPM REST API\n    serviceCategory: SaaS Applications\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-fusion/refs/heads/main/finops/oracle-fusion-finops.yml
sources:
- https://www.oracle.com/applications/cloud/
- https://docs.oracle.com/en/cloud/saas/
specification: FinOps Framework
tags:
- ERP
- HCM
- SaaS
- Oracle Cloud
- FinOps
- FOCUS
---
