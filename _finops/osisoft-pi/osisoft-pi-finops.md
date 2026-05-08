---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: osisoft-pi-web-api-openapi.yml
  format: yaml
  label: OSIsoft PI Web API
  slug: pi-web-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/osisoft-pi/refs/heads/main/openapi/osisoft-pi-web-api-openapi.yml
billing_model:
  billingCurrency: USD (varies by region)
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Subscription (Enterprise)
description: Structural FinOps definition for AVEVA PI System (OSIsoft PI). Pricing is enterprise-subscription only with no public meter rates; this artifact captures the FOCUS-shaped fields available from the public product page only.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: AVEVA Group plc
  ProviderName: AVEVA
  PublisherName: AVEVA Group plc
  ServiceCategory: Industrial Software
  ServiceName: AVEVA PI System
layout: finops
meters:
- aggregation: count
  description: Annual PI System subscription, sized per deployment
  dimensions:
  - module
  - deployment
  name: pi_subscription
  unit: subscription-year
- aggregation: sum
  description: AVEVA CONNECT Data Services data volume (where applicable)
  dimensions:
  - tenant
  - service
  name: connect_data_volume
  unit: varies
name: Osisoft Pi Finops
provider_name: osisoft-pi
provider_slug: osisoft-pi
publisher_name: AVEVA Group plc
service_category: Industrial Software
slug: osisoft-pi-finops
source_filename: osisoft-pi-finops.yml
source_heading: FinOps Profile
source_url: https://www.aveva.com/en/products/aveva-pi-system/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: osisoft-pi\nproviderId: osisoft-pi\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: No public pricing or usage API. AVEVA PI System is sold under enterprise subscription\n  agreements; FinOps mapping below is a structural placeholder pending contractual disclosure.\ntags:\n  - FinOps\n  - FOCUS\n  - Industrial\n  - Time Series\n  - Process Historian\ndescription: Structural FinOps definition for AVEVA PI System (OSIsoft PI). Pricing is enterprise-subscription\n  only with no public meter rates; this artifact captures the FOCUS-shaped fields available\n  from the public product page only.\nsources:\n  - https://www.aveva.com/en/products/aveva-pi-system/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: AVEVA Group plc\nserviceCategory: Industrial Software\nbillingModel:\n  pricingCategory: Subscription (Enterprise)\n  billingFrequency: Annual\n  billingCurrency: USD (varies by region)\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: AVEVA PI System\n  ServiceCategory: Industrial Software\n  ProviderName: AVEVA\n  PublisherName: AVEVA Group plc\n  InvoiceIssuerName: AVEVA Group plc\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: pi_subscription\n    description: Annual PI System subscription, sized per deployment\n    unit: subscription-year\n    aggregation: count\n    dimensions:\n      - module\n      - deployment\n  - name: connect_data_volume\n    description: AVEVA CONNECT Data Services data volume (where applicable)\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - tenant\n      - service\nprinciples:\n  -\
  \ name: Visibility\n    description: PI System usage visibility comes from the customer's own monitoring of PI\n      Server, PI Web API, and CONNECT tenant dashboards; AVEVA does not provide a public\n      cost API.\n  - name: Allocation\n    description: Allocate by module (PI Server, PI Vision, AF SDK, CONNECT) and by site/business\n      unit using the deployment topology; tag PI assets in the AF hierarchy by cost center.\n  - name: Optimization\n    description: Right-size PI Server tag counts and CONNECT data ingestion. Negotiate at\n      renewal based on actual asset/tag growth rather than initial estimates.\n  - name: Accountability\n    description: Designate a PI System owner per site responsible for renewal forecasting\n      and license utilization tracking against the AVEVA contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/osisoft-pi/refs/heads/main/finops/osisoft-pi-finops.yml
sources:
- https://www.aveva.com/en/products/aveva-pi-system/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Industrial
- Time Series
- Process Historian
---
