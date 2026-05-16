---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: adt-platform-api-openapi.yml
  format: yaml
  label: ADT+ Platform API
  slug: adt-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adt/refs/heads/main/openapi/adt-platform-api-openapi.yml
- filename: adt-business-api-openapi.yml
  format: yaml
  label: ADT Business API
  slug: adt-business-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adt/refs/heads/main/openapi/adt-business-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for ADT: contract-based partner billing for security and monitoring integrations.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: ADT LLC
  ProviderName: ADT
  PublisherName: ADT LLC
  ServiceCategory: Security and Monitoring
  ServiceName: ADT
layout: finops
meters:
- aggregation: max
  dimensions:
  - region
  - service_plan
  name: monitored_sites
  unit: site
- aggregation: sum
  dimensions:
  - partner
  - environment
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - product
  name: subscription_fees
  unit: month
name: Adt Finops
provider_name: ADT
provider_slug: adt
publisher_name: ADT LLC
service_category: Security and Monitoring
slug: adt-finops
source_filename: adt-finops.yml
source_heading: FinOps Profile
source_url: https://www.adt.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ADT\nproviderId: adt\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: ADT lacks a publicly-priced developer API. FinOps mapping is illustrative only and\n  assumes contract-based partner billing.\ntags:\n  - FinOps\n  - FOCUS\n  - Home Security\n  - IoT\ndescription: 'FOCUS-aligned FinOps for ADT: contract-based partner billing for security and\n  monitoring integrations.'\nsources:\n  - https://www.adt.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: ADT LLC\nserviceCategory: Security and Monitoring\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n\
  focusColumns:\n  ServiceName: ADT\n  ServiceCategory: Security and Monitoring\n  ProviderName: ADT\n  PublisherName: ADT LLC\n  InvoiceIssuerName: ADT LLC\n  BillingCurrency: USD\nmeters:\n  - name: monitored_sites\n    unit: site\n    aggregation: max\n    dimensions:\n      - region\n      - service_plan\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - environment\n  - name: subscription_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Reconcile partner usage reports against ADT-issued invoices for the integration.\n  - name: Allocation\n    description: Tag API calls and monitored sites with the consuming product/team for partner chargeback.\n  - name: Optimization\n    description: Cache device state; batch event subscriptions; renegotiate partner volume tiers\n      annually.\n  - name: Accountability\n    description: Assign partner-integration\
  \ budget owner; review monthly invoice variances.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adt/refs/heads/main/finops/adt-finops.yml
sources:
- https://www.adt.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Home Security
- IoT
---
