---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: instacart-developer-platform-api-openapi.yml
  format: yaml
  label: Instacart Developer Platform API
  slug: developer-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/instacart/refs/heads/main/openapi/instacart-developer-platform-api-openapi.yml
- filename: instacart-connect-fulfillment-api-openapi.yml
  format: yaml
  label: Instacart Connect Fulfillment API
  slug: connect-fulfillment-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/instacart/refs/heads/main/openapi/instacart-connect-fulfillment-api-openapi.yml
- filename: instacart-connect-post-checkout-api-openapi.yml
  format: yaml
  label: Instacart Connect Post-Checkout API
  slug: connect-post-checkout-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/instacart/refs/heads/main/openapi/instacart-connect-post-checkout-api-openapi.yml
- filename: instacart-catalog-api-openapi.yml
  format: yaml
  label: Instacart Catalog API
  slug: catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/instacart/refs/heads/main/openapi/instacart-catalog-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Tax
  - Adjustment
  - Refund
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Take Rate + Ads
description: FOCUS-aligned FinOps shape for Instacart. The dominant cost line for retailer and brand partners is the marketplace take rate (per-order percentage and fees) plus optional advertising spend, not API call fees - APIs are bundled into the partner agreement. FinOps practice for Instacart focuses on per-order economics and ad-spend ROAS rather than per-call accounting.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Maplebear Inc. d/b/a Instacart
  PricingCategory: Take Rate
  PricingUnit: order
  ProviderName: Instacart
  PublisherName: Maplebear Inc. d/b/a Instacart
  ServiceCategory: Marketplace + Logistics
  ServiceName: Instacart Connect
layout: finops
meters:
- aggregation: sum
  description: Completed orders processed through the Instacart marketplace
  dimensions:
  - retailer
  - region
  - delivery_type
  name: orders_fulfilled
  unit: order
- aggregation: sum
  description: Take-rate revenue attributable to the partner
  dimensions:
  - retailer
  - category
  name: take_rate_revenue
  unit: USD
- aggregation: sum
  description: Spend on Instacart Ads (sponsored products, display)
  dimensions:
  - campaign
  - sku
  - brand
  name: ads_spend
  unit: USD
name: Instacart Finops
provider_name: instacart
provider_slug: instacart
publisher_name: Maplebear Inc. d/b/a Instacart
service_category: Marketplace + Logistics
slug: instacart-finops
source_filename: instacart-finops.yml
source_heading: FinOps Profile
source_url: https://docs.instacart.com/connect/api
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Instacart\nproviderId: instacart\npublisherName: Maplebear Inc. d/b/a Instacart\nserviceCategory: Marketplace + Logistics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Grocery\n  - E-Commerce\n  - Marketplace\n  - Logistics\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Instacart. The dominant cost line for retailer and brand\n  partners is the marketplace take rate (per-order percentage and fees) plus optional advertising spend,\n  not API call fees - APIs are bundled into the partner agreement. FinOps practice for Instacart focuses\n  on per-order economics and ad-spend ROAS rather than per-call\
  \ accounting.\nnotes: API access itself is not separately metered. The meaningful FinOps surface is the per-order take-rate\n  invoice and the Instacart Ads spend.\nsources:\n  - https://docs.instacart.com/connect/api\nprinciples:\n  - name: Visibility\n    description: Use partner reporting (orders, GMV, take-rate) and Instacart Ads dashboards to surface\n      per-order economics and ad spend.\n  - name: Allocation\n    description: Tag campaigns and SKUs by brand / category so ad spend allocates to product lines; map\n      take-rate fees to the originating retailer storefront.\n  - name: Optimization\n    description: Tune ad bids and daily budgets, retire low-performing SKUs from sponsored placements,\n      and align fulfillment options to lower delivery-cost-to-serve.\n  - name: Accountability\n    description: Designate a Connect / Ads owner with monthly Instacart-spend budget; review per-order\n      contribution margin and ROAS in monthly reviews.\ndomains:\n  - name: Understand\
  \ Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Take Rate + Ads\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Instacart Connect\n  ServiceCategory: Marketplace + Logistics\n  ProviderName: Instacart\n  PublisherName: Maplebear Inc. d/b/a Instacart\n  InvoiceIssuerName: Maplebear Inc. d/b/a Instacart\n  PricingCategory:\
  \ Take Rate\n  PricingUnit: order\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: orders_fulfilled\n    description: Completed orders processed through the Instacart marketplace\n    unit: order\n    aggregation: sum\n    dimensions:\n      - retailer\n      - region\n      - delivery_type\n  - name: take_rate_revenue\n    description: Take-rate revenue attributable to the partner\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - retailer\n      - category\n  - name: ads_spend\n    description: Spend on Instacart Ads (sponsored products, display)\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - campaign\n      - sku\n      - brand\napis:\n  - name: Instacart Connect API\n    baseURL: https://{instacart_domain}/v2\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Order\n    metric: take_rate_revenue / orders_fulfilled\n    target: TBD\n  - name: Return on Ad Spend\n    metric: attributed_revenue / ads_spend\n    target: TBD\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/instacart/refs/heads/main/finops/instacart-finops.yml
sources:
- https://docs.instacart.com/connect/api
specification: FinOps Framework
tags:
- Grocery
- E-Commerce
- Marketplace
- Logistics
- FinOps
- FOCUS
---
