---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: oracle-primavera-p6-eppm-openapi.yml
  format: yaml
  label: Oracle Primavera P6 EPPM REST API
  slug: oracle-primavera-p6-eppm-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-primavera/refs/heads/main/openapi/oracle-primavera-p6-eppm-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription + BYOL (On-Premises)
description: 'FOCUS-aligned FinOps view for Oracle Primavera: Primavera Cloud is billed as a SaaS subscription per Hosted Named User per month (with role tiers for full-use vs viewer); on-premises P6 EPPM is billed against the contractual Oracle Technology license. REST API access is bundled with the subscription / license. FinOps observation focuses on user-license utilization per role and on the underlying infrastructure costs for on-premises deployments.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Oracle America, Inc.
  PricingCategory: Subscription
  ProviderName: Oracle
  PublisherName: Oracle America, Inc.
  ServiceCategory: Project Management
  ServiceName: Oracle Primavera
layout: finops
meters:
- aggregation: max
  description: Active Hosted Named User (full-use) seats per month
  dimensions:
  - role
  - business_unit
  name: primavera_cloud_full_user_subscription
  unit: seat-month
- aggregation: max
  description: Active Hosted Named User (viewer) seats per month
  dimensions:
  - role
  - business_unit
  name: primavera_cloud_viewer_subscription
  unit: seat-month
- aggregation: max
  description: Contractual Oracle Technology license for on-premises P6 EPPM
  dimensions:
  - license_type
  name: primavera_p6_on_prem_license
  unit: license
- aggregation: sum
  description: REST API calls (informational; bundled in the subscription / license)
  dimensions:
  - api
  - endpoint
  - consumer
  name: rest_api_calls
  unit: request
name: Oracle Primavera Finops
provider_name: Oracle Primavera
provider_slug: oracle-primavera
publisher_name: Oracle America, Inc.
service_category: Project Management
slug: oracle-primavera-finops
source_filename: oracle-primavera-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/construction-engineering/primavera/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Primavera\nproviderId: oracle-primavera\npublisherName: Oracle America, Inc.\nserviceCategory: Project Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Project Management\n  - Construction\n  - Engineering\n  - Oracle Cloud\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view for Oracle Primavera: Primavera Cloud is billed as\n  a SaaS subscription per Hosted Named User per month (with role tiers for\n  full-use vs viewer); on-premises P6 EPPM is billed against the contractual\n  Oracle Technology license. REST API access is bundled with the subscription\n  / license. FinOps observation\
  \ focuses on user-license utilization per role\n  and on the underlying infrastructure costs for on-premises deployments.\nsources:\n  - https://www.oracle.com/construction-engineering/primavera/\n  - https://docs.oracle.com/cd/F37125_01/\n  - https://www.oracle.com/cloud/price-list/\nnotes: >-\n  No per-API meter exists. Track license seat utilization per role through\n  the Primavera Cloud admin console, plus underlying OCI / on-premises\n  infrastructure cost for on-premises P6 EPPM deployments.\nbillingModel:\n  pricingCategory: Tiered Subscription + BYOL (On-Premises)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Oracle Primavera\n  ServiceCategory: Project Management\n  ProviderName: Oracle\n  PublisherName: Oracle America, Inc.\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\n  PricingCategory: Subscription\n  ChargeCategory: Purchase\n\
  meters:\n  - name: primavera_cloud_full_user_subscription\n    description: Active Hosted Named User (full-use) seats per month\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - role\n      - business_unit\n  - name: primavera_cloud_viewer_subscription\n    description: Active Hosted Named User (viewer) seats per month\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - role\n      - business_unit\n  - name: primavera_p6_on_prem_license\n    description: Contractual Oracle Technology license for on-premises P6 EPPM\n    unit: license\n    aggregation: max\n    dimensions:\n      - license_type\n  - name: rest_api_calls\n    description: REST API calls (informational; bundled in the subscription / license)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - consumer\nprinciples:\n  - name: Visibility\n    description: >-\n      Review per-role seat utilization in the Primavera Cloud admin console\n     \
  \ and reconcile monthly against the contractual seat count; for\n      on-premises P6 EPPM track the underlying WebLogic / database\n      infrastructure cost separately.\n  - name: Allocation\n    description: >-\n      Tag user records with project, business unit, and cost center so\n      Primavera seats can be attributed back to the consuming portfolio.\n  - name: Optimization\n    description: >-\n      Move occasional reviewers from full-use to viewer seats, reclaim\n      inactive accounts, and consolidate small project portfolios onto a\n      single Primavera Cloud tenant where governance permits.\n  - name: Accountability\n    description: >-\n      Pair the Primavera applications administrator with a portfolio /\n      construction-controls owner; review seat growth and renewal scoping at\n      portfolio gate reviews.\napis:\n  - name: Oracle Primavera P6 EPPM REST API\n    serviceName: Oracle Primavera P6 EPPM REST API\n    serviceCategory: Project Management\n  - name: Oracle\
  \ Primavera Gateway Integration API\n    serviceName: Oracle Primavera Gateway Integration API\n    serviceCategory: Project Management\n  - name: Oracle Primavera Analytics API\n    serviceName: Oracle Primavera Analytics API\n    serviceCategory: Project Management\n  - name: Oracle Primavera P6 Scheduling API\n    serviceName: Oracle Primavera P6 Scheduling API\n    serviceCategory: Project Management\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-primavera/refs/heads/main/finops/oracle-primavera-finops.yml
sources:
- https://www.oracle.com/construction-engineering/primavera/
- https://docs.oracle.com/cd/F37125_01/
- https://www.oracle.com/cloud/price-list/
specification: FinOps Framework
tags:
- Project Management
- Construction
- Engineering
- Oracle Cloud
- FinOps
- FOCUS
---
