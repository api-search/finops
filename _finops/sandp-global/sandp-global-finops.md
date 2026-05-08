---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sandp-global-capital-iq-openapi.yml
  format: yaml
  label: S&P Capital IQ API
  slug: sandp-global-capital-iq-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sandp-global/refs/heads/main/openapi/sandp-global-capital-iq-openapi.yml
- filename: sandp-global-commodity-insights-openapi.yml
  format: yaml
  label: S&P Global Commodity Insights API
  slug: sandp-global-commodity-insights-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sandp-global/refs/heads/main/openapi/sandp-global-commodity-insights-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Subscription / Licensed
description: FOCUS-aligned FinOps artifact for S&P Global. Pricing is gated; meters and principles describe the expected billing surface. S&P Global APIs and data feeds (Market Intelligence, Capital IQ, Indices, Ratings, Platts) are sold under enterprise data licenses. There is no public price list; access is via contract with S&P Global sales.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: S&P Global Inc.
  ProviderName: S&P Global
  PublisherName: S&P Global Inc.
  ServiceCategory: Financial Market Data
  ServiceName: S&P Global
  ServiceSubcategory: Market Data / Indices
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  - user_count
  name: data_license
  unit: month
- aggregation: sum
  dimensions:
  - product
  - feed
  - client_id
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - product
  - feed
  name: data_volume
  unit: GB
name: Sandp Global Finops
provider_name: S&P Global
provider_slug: sandp-global
publisher_name: S&P Global Inc.
service_category: Financial Market Data
slug: sandp-global-finops
source_filename: sandp-global-finops.yml
source_heading: FinOps Profile
source_url: https://www.spglobal.com/marketintelligence/en/solutions/marketplace
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: S&P Global\nproviderId: sandp-global\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- Capital Markets\n- Financial Data\n- Indices\n- Market Intelligence\n- Ratings\n- FinOps\n- FOCUS\ndescription: FOCUS-aligned FinOps artifact for S&P Global. Pricing is gated; meters and principles describe\n  the expected billing surface. S&P Global APIs and data feeds (Market Intelligence, Capital IQ, Indices,\n  Ratings, Platts) are sold under enterprise data licenses. There is no public price list; access is via\n  contract with S&P Global sales.\nsources:\n- https://www.spglobal.com/marketintelligence/en/solutions/marketplace\n- https://focus.finops.org/focus-specification/v1-3/\n- https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: S&P Global Inc.\nserviceCategory: Financial Market Data\nbillingModel:\n  pricingCategory: Subscription / Licensed\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Tax\n  - Adjustment\nfocusColumns:\n  ServiceName: S&P Global\n  ServiceCategory: Financial Market Data\n  ServiceSubcategory: Market Data / Indices\n  ProviderName: S&P Global\n  PublisherName: S&P Global Inc.\n  InvoiceIssuerName: S&P Global Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: data_license\n  unit: month\n  aggregation: max\n  dimensions:\n  - product\n  - user_count\n- name: api_requests\n  unit: request\n  aggregation: sum\n  dimensions:\n  - product\n  - feed\n  - client_id\n- name: data_volume\n  unit: GB\n  aggregation: sum\n  dimensions:\n  - product\n  - feed\nprinciples:\n- name: Visibility\n  description: Track consumption per data feed (Capital\
  \ IQ, Xpressfeed, Marketplace, Indices) using S&P\n    Global's customer portal; reconcile against the negotiated user / record / redistribution caps in\n    your contract.\n- name: Allocation\n  description: Tag every downstream consumer (desk, application, fund) so usage caps and redistribution\n    clauses can be attributed; required for audit response.\n- name: Optimization\n  description: Right-size feed scope at renewal — drop unused universes / regions; use delta files (Xpressfeed)\n    instead of full snapshots to cut data-volume charges; consolidate users under enterprise licenses\n    where it lowers per-seat cost.\n- name: Accountability\n  description: Market-data manager owns S&P Global vendor relationship, audit responses, and license-cap\n    monitoring.\nnotes: S&P Global APIs and data feeds (Market Intelligence, Capital IQ, Indices, Ratings, Platts) are\n  sold under enterprise data licenses. There is no public price list; access is via contract with S&P\n  Global sales.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sandp-global/refs/heads/main/finops/sandp-global-finops.yml
sources:
- https://www.spglobal.com/marketintelligence/en/solutions/marketplace
- https://focus.finops.org/focus-specification/v1-3/
- https://www.finops.org/framework/
specification: FinOps Framework
tags:
- Capital Markets
- Financial Data
- Indices
- Market Intelligence
- Ratings
- FinOps
- FOCUS
---
