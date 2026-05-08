---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: yoast-rest-openapi.yml
  format: yaml
  label: Yoast REST API
  slug: yoast-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/yoast/refs/heads/main/openapi/yoast-rest-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps view for Yoast: a flat annual plugin licence (per WordPress site /

  Shopify store) rather than a metered API. Cost surface is dominated by Premium licence

  renewals plus optional add-on plugins.

  '
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Yoast B.V.
  ProviderName: Yoast
  PublisherName: Yoast B.V.
  ServiceCategory: SEO / Content
  ServiceName: Yoast SEO
layout: finops
meters:
- aggregation: count
  description: Count of active Yoast SEO Premium site licences renewed annually.
  dimensions:
  - product
  - site
  name: premium_site_licences
  unit: licence-year
- aggregation: count
  description: Add-on plugin licences (Local SEO, Video SEO, News SEO, WooCommerce SEO, Yoast SEO for Shopify) purchased separately or as part of bundles.
  dimensions:
  - product
  - site
  name: addon_licences
  unit: licence-year
name: Yoast Finops
provider_name: Yoast
provider_slug: yoast
publisher_name: Yoast B.V.
service_category: SEO / Content
slug: yoast-finops
source_filename: yoast-finops.yml
source_heading: FinOps Profile
source_url: https://yoast.com/wordpress/plugins/seo/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Yoast\nproviderId: yoast\npublisherName: Yoast B.V.\nserviceCategory: SEO / Content\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - SEO\n  - WordPress\n  - Plugin\n  - FinOps\n  - FOCUS\ndescription: |\n  FOCUS-aligned FinOps view for Yoast: a flat annual plugin licence (per WordPress site /\n  Shopify store) rather than a metered API. Cost surface is dominated by Premium licence\n  renewals plus optional add-on plugins.\nsources:\n  - https://yoast.com/wordpress/plugins/seo/pricing/\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n\
  \    - Tax\nfocusColumns:\n  ServiceName: Yoast SEO\n  ServiceCategory: SEO / Content\n  ProviderName: Yoast\n  PublisherName: Yoast B.V.\n  InvoiceIssuerName: Yoast B.V.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: premium_site_licences\n    description: Count of active Yoast SEO Premium site licences renewed annually.\n    unit: licence-year\n    aggregation: count\n    dimensions:\n      - product\n      - site\n  - name: addon_licences\n    description: Add-on plugin licences (Local SEO, Video SEO, News SEO, WooCommerce SEO,\n      Yoast SEO for Shopify) purchased separately or as part of bundles.\n    unit: licence-year\n    aggregation: count\n    dimensions:\n      - product\n      - site\nprinciples:\n  - name: Visibility\n    description: Visibility is invoice-driven via the my.yoast.com account; there is no\n      usage telemetry for the plugin itself.\n  - name: Allocation\n    description: Allocate Yoast spend per WordPress site / brand by tagging\
  \ each licence\n      to the owning site URL within my.yoast.com.\n  - name: Optimization\n    description: Cost levers are bundle selection (Premium vs Premium + add-ons), multi-site\n      packs, and choosing the free Yoast SEO where Premium features are not needed.\n  - name: Accountability\n    description: Marketing / web ops typically owns Yoast renewal; finance reconciles the\n      annual purchase line on the my.yoast.com invoice.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/yoast/refs/heads/main/finops/yoast-finops.yml
sources:
- https://yoast.com/wordpress/plugins/seo/pricing/
specification: FinOps Framework
tags:
- SEO
- WordPress
- Plugin
- FinOps
- FOCUS
---
