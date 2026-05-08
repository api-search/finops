---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: snow-software-licenses-openapi.yml
  format: yaml
  label: Snow Atlas SAM Licenses API
  slug: snow-atlas-licenses-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snow-software/refs/heads/main/openapi/snow-software-licenses-openapi.yml
- filename: snow-software-saas-applications-openapi.yml
  format: yaml
  label: Snow Atlas SaaS Applications API
  slug: snow-atlas-saas-applications-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snow-software/refs/heads/main/openapi/snow-software-saas-applications-openapi.yml
- filename: snow-software-saas-subscriptions-openapi.yml
  format: yaml
  label: Snow Atlas SaaS Subscriptions API
  slug: snow-atlas-saas-subscriptions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snow-software/refs/heads/main/openapi/snow-software-saas-subscriptions-openapi.yml
- filename: snow-software-computers-openapi.json
  format: json
  label: Snow Atlas SAM Computers API
  slug: snow-atlas-computers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snow-software/refs/heads/main/openapi/snow-software-computers-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription (Contact Sales)
description: 'FOCUS-aligned FinOps placeholder for Snow Software (now Flexera): pricing is contact-sales, invoicing flows through Flexera, and meter detail depends on the customer''s Snow Atlas tenant.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Flexera Software LLC
  ProviderName: Snow (Flexera)
  PublisherName: Flexera Software LLC
  ServiceCategory: Software Asset Management
  ServiceName: Snow Software Asset Management
layout: finops
meters:
- aggregation: max
  dimensions:
  - asset_type
  name: managed_assets
  unit: device
- aggregation: max
  dimensions:
  - publisher
  name: saas_applications
  unit: application
- aggregation: max
  dimensions:
  - business_unit
  name: managed_users
  unit: user
name: Snow Software Finops
provider_name: Snow Software
provider_slug: snow-software
publisher_name: Flexera Software LLC
service_category: Software Asset Management
slug: snow-software-finops
source_filename: snow-software-finops.yml
source_heading: FinOps Profile
source_url: https://www.flexera.com/products/snow
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Snow Software\nproviderId: snow-software\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Software Asset Management\n  - SaaS Management\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Snow Software (now Flexera): pricing is contact-sales,\n  invoicing flows through Flexera, and meter detail depends on the customer''s Snow Atlas tenant.'\nsources:\n  - https://www.flexera.com/products/snow\nnotes: Snow Software was acquired by Flexera; flexera.com publishes no per-seat or per-asset price sheet\n  for the Snow product family. FOCUS columns and meters here describe the consumption shape (managed\n  assets, SaaS apps, users) but unit prices cannot be reconciled without a customer order form.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Flexera Software LLC\nserviceCategory: Software Asset Management\nbillingModel:\n  pricingCategory: Subscription (Contact Sales)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Snow Software Asset Management\n  ServiceCategory: Software Asset Management\n  ProviderName: Snow (Flexera)\n  PublisherName: Flexera Software LLC\n  InvoiceIssuerName: Flexera Software LLC\n  BillingCurrency: USD\nmeters:\n  - name: managed_assets\n    unit: device\n    aggregation: max\n    dimensions:\n      - asset_type\n  - name: saas_applications\n    unit: application\n    aggregation: max\n    dimensions:\n      - publisher\n  - name: managed_users\n    unit: user\n    aggregation: max\n    dimensions:\n      - business_unit\nprinciples:\n  - name: Visibility\n    description: Use Snow Atlas dashboards to surface installed\
  \ software, SaaS subscriptions, and entitlement\n      gaps per business unit.\n  - name: Allocation\n    description: Tag each managed asset / SaaS application to a cost center and contract to enable chargeback\n      and renewal-by-owner.\n  - name: Optimization\n    description: Reclaim unused SaaS seats, true-down over-licensed software, and consolidate redundant\n      applications surfaced by Snow Risk Monitor and the SaaS Management module.\n  - name: Accountability\n    description: Snow Atlas administrators review entitlement-vs-installed deltas and SaaS usage at each\n      renewal cycle with finance and procurement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/snow-software/refs/heads/main/finops/snow-software-finops.yml
sources:
- https://www.flexera.com/products/snow
specification: FinOps Framework
tags:
- Software Asset Management
- SaaS Management
- FinOps
- FOCUS
---
