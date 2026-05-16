---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: advance-auto-parts-catalog-api-openapi.yml
  format: yaml
  label: Advance Auto Parts Catalog API
  slug: advance-auto-parts-catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/advance-auto-parts/refs/heads/main/openapi/advance-auto-parts-catalog-api-openapi.yml
- filename: advance-auto-parts-commerce-api-openapi.yml
  format: yaml
  label: Advance Auto Parts Commerce API
  slug: advance-auto-parts-commerce-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/advance-auto-parts/refs/heads/main/openapi/advance-auto-parts-commerce-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Advance Auto Parts: B2B partnership billing for catalog and commerce integrations.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Advance Auto Parts, Inc.
  ProviderName: Advance Auto Parts
  PublisherName: Advance Auto Parts, Inc.
  ServiceCategory: Automotive Retail
  ServiceName: Advance Auto Parts
layout: finops
meters:
- aggregation: sum
  dimensions:
  - partner
  - environment
  name: catalog_lookups
  unit: request
- aggregation: sum
  dimensions:
  - partner
  - region
  name: orders_placed
  unit: order
- aggregation: sum
  name: subscription_fees
  unit: month
name: Advance Auto Parts Finops
provider_name: Advance Auto Parts
provider_slug: advance-auto-parts
publisher_name: Advance Auto Parts, Inc.
service_category: Automotive Retail
slug: advance-auto-parts-finops
source_filename: advance-auto-parts-finops.yml
source_heading: FinOps Profile
source_url: https://shop.advanceautoparts.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Advance Auto Parts\nproviderId: advance-auto-parts\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: No public API pricing. FinOps mapping reflects assumed B2B partnership billing.\ntags:\n  - FinOps\n  - FOCUS\n  - Automotive\n  - Retail\ndescription: 'FOCUS-aligned FinOps for Advance Auto Parts: B2B partnership billing for catalog\n  and commerce integrations.'\nsources:\n  - https://shop.advanceautoparts.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Advance Auto Parts, Inc.\nserviceCategory: Automotive Retail\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n\
  \    - Usage\nfocusColumns:\n  ServiceName: Advance Auto Parts\n  ServiceCategory: Automotive Retail\n  ProviderName: Advance Auto Parts\n  PublisherName: Advance Auto Parts, Inc.\n  InvoiceIssuerName: Advance Auto Parts, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: catalog_lookups\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - environment\n  - name: orders_placed\n    unit: order\n    aggregation: sum\n    dimensions:\n      - partner\n      - region\n  - name: subscription_fees\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Reconcile partner-scoped usage reports against monthly Advance Auto Parts invoices.\n  - name: Allocation\n    description: Tag catalog lookups and orders with the consuming product/team.\n  - name: Optimization\n    description: Cache product reference data; batch inventory polls; consolidate orders to lower\n      per-order fees.\n  - name: Accountability\n    description: Assign\
  \ B2B integration budget owner; review monthly variance.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/advance-auto-parts/refs/heads/main/finops/advance-auto-parts-finops.yml
sources:
- https://shop.advanceautoparts.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Automotive
- Retail
---
