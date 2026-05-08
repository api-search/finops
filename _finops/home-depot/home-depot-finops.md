---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: home-depot-home-depot-api-openapi.yml
  format: yaml
  label: Home Depot API
  slug: home-depot-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/home-depot/refs/heads/main/openapi/home-depot-home-depot-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Refund
  pricingCategory: Partner Program / Supplier Agreement
description: FOCUS-aligned FinOps stub for Home Depot. Partner-program / supplier-agreement economics rather than public API billing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: The Home Depot, Inc.
  PricingCategory: Bilateral
  PricingUnit: varies
  ProviderName: The Home Depot, Inc.
  PublisherName: The Home Depot, Inc.
  ServiceCategory: Retail / E-Commerce
  ServiceName: Home Depot
layout: finops
meters:
- aggregation: sum
  description: Orders placed against the supplier through Home Depot channels
  dimensions:
  - partner_id
  - sku
  - channel
  - market
  name: orders
  unit: order
- aggregation: sum
  description: Gross merchandise value of orders
  dimensions:
  - partner_id
  - sku
  name: gmv
  unit: USD
- aggregation: sum
  description: Advertising / OneSource spend on Home Depot platforms
  dimensions:
  - partner_id
  - campaign
  name: ad_spend
  unit: USD
- aggregation: sum
  description: Return events
  dimensions:
  - partner_id
  - sku
  name: returns
  unit: event
name: Home Depot Finops
provider_name: home-depot
provider_slug: home-depot
publisher_name: The Home Depot, Inc.
service_category: Retail / E-Commerce
slug: home-depot-finops
source_filename: home-depot-finops.yml
source_heading: FinOps Profile
source_url: https://corporate.homedepot.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: home-depot\nproviderId: home-depot\npublisherName: The Home Depot, Inc.\nserviceCategory: Retail / E-Commerce\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Retail\n  - E-Commerce\n  - Home Improvement\n  - Supplier\n  - FinOps\n  - FOCUS\nnotes: The Home Depot does not bill suppliers or partners for API calls in a usage-meter shape; cost flows\n  through partner-program fees, advertising spend, vendor agreements, and Pro-Xtra economics. Meters below\n  capture the right shape for a supplier integration; pricing is bilateral.\ndescription: 'FOCUS-aligned FinOps stub for Home Depot. Partner-program / supplier-agreement economics\n  rather than public API billing.'\n\
  sources:\n  - https://corporate.homedepot.com/\n  - https://supplierhub.homedepot.com/\nbillingModel:\n  pricingCategory: Partner Program / Supplier Agreement\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Home Depot\n  ServiceCategory: Retail / E-Commerce\n  ProviderName: The Home Depot, Inc.\n  PublisherName: The Home Depot, Inc.\n  InvoiceIssuerName: The Home Depot, Inc.\n  PricingCategory: Bilateral\n  PricingUnit: varies\n  BillingCurrency: USD\n  ChargeCategory: Usage\nprinciples:\n  - name: Visibility\n    description: Reconcile orders, returns, and ad-spend events through Supplier Hub reports and the\n      consuming ERP / advertising platform.\n  - name: Allocation\n    description: Allocate fees by program (Supplier Hub catalog, OneSource ads, Pro Xtra B2B) and by\n      department / SKU within your own organization.\n  - name: Optimization\n    description:\
  \ Cost levers are negotiation of vendor terms, advertising bid optimization, and improving\n      content / data quality to reduce Supplier-Hub penalty fees.\n  - name: Accountability\n    description: Vendor-management owns the Home Depot relationship; e-commerce / advertising teams own\n      the operational programs.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nmeters:\n  - name: orders\n    description: Orders placed against the supplier through\
  \ Home Depot channels\n    unit: order\n    aggregation: sum\n    dimensions:\n      - partner_id\n      - sku\n      - channel\n      - market\n  - name: gmv\n    description: Gross merchandise value of orders\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - partner_id\n      - sku\n  - name: ad_spend\n    description: Advertising / OneSource spend on Home Depot platforms\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - partner_id\n      - campaign\n  - name: returns\n    description: Return events\n    unit: event\n    aggregation: sum\n    dimensions:\n      - partner_id\n      - sku\napis:\n  - name: Home Depot API\n    baseURL: https://api.homedepot.com\n    tags:\n      - Retail\n      - E-Commerce\n      - Supplier\n    serviceName: Home Depot API\n    serviceCategory: Retail / E-Commerce\nunitEconomics:\n  - name: Effective Take Rate\n    metric: home_depot_fees / gmv\n    target: per partner agreement\n  - name: Cost per Order\n    metric: home_depot_fees\
  \ / orders\n    target: per partner agreement\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/home-depot/refs/heads/main/finops/home-depot-finops.yml
sources:
- https://corporate.homedepot.com/
- https://supplierhub.homedepot.com/
specification: FinOps Framework
tags:
- Retail
- E-Commerce
- Home Improvement
- Supplier
- FinOps
- FOCUS
---
