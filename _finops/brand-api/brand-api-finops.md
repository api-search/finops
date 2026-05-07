---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: brandfetch-brand-api.yml
  format: yaml
  label: Brandfetch Brand API
  slug: brandfetch-brand-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/brand-api/refs/heads/main/openapi/brandfetch-brand-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Brandfetch: a free Logo API with a soft 500K-monthly fair-use ceiling, plus a flat $99/month Brand API subscription capped at 2,500 calls and Enterprise custom plans for higher volume and SLA.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Brandfetch
  PricingCategory: Standard
  PricingUnit: subscription-month
  ProviderName: Brandfetch
  PublisherName: Brandfetch
  ServiceCategory: Brand Data API
  ServiceName: Brandfetch
layout: finops
meters:
- aggregation: sum
  description: Calls to the Logo API; metered for fair-use review against the 500K monthly soft cap.
  dimensions:
  - domain
  - api_key
  name: logo_api_requests
  unit: request
- aggregation: sum
  description: Calls to the Brand API; counted against the 2,500/month subscription cap.
  dimensions:
  - domain
  - api_key
  name: brand_api_calls
  unit: request
- aggregation: sum
  description: Brand API subscription fee billed monthly ($99/month, ~20% off annual).
  dimensions:
  - plan
  - billing_cycle
  name: subscription_month
  unit: month
name: Brand Api Finops
provider_name: Brand API (Brandfetch)
provider_slug: brand-api
publisher_name: Brandfetch
service_category: Brand Data API
slug: brand-api-finops
source_filename: brand-api-finops.yml
source_heading: FinOps Profile
source_url: https://brandfetch.com/developers/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Brand API (Brandfetch)\nproviderId: brand-api\npublisherName: Brandfetch\nserviceCategory: Brand Data API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Brands\n  - Logos\n  - Brand Assets\n  - Company Data\n  - Firmographics\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Brandfetch: a free Logo API with a soft 500K-monthly fair-use\n  ceiling, plus a flat $99/month Brand API subscription capped at 2,500 calls and Enterprise custom\n  plans for higher volume and SLA.'\nsources:\n  - https://brandfetch.com/developers/pricing\n  - https://docs.brandfetch.com/logo-api/rate-limits\nbillingModel:\n  pricingCategory:\
  \ Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Brandfetch\n  ServiceCategory: Brand Data API\n  ProviderName: Brandfetch\n  PublisherName: Brandfetch\n  InvoiceIssuerName: Brandfetch\n  BillingCurrency: USD\n  PricingCategory: Standard\n  PricingUnit: subscription-month\nmeters:\n  - name: logo_api_requests\n    description: Calls to the Logo API; metered for fair-use review against the 500K monthly soft cap.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - domain\n      - api_key\n  - name: brand_api_calls\n    description: Calls to the Brand API; counted against the 2,500/month subscription cap.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - domain\n      - api_key\n  - name: subscription_month\n    description: Brand API subscription fee billed monthly ($99/month, ~20% off annual).\n    unit: month\n    aggregation: sum\n    dimensions:\n\
  \      - plan\n      - billing_cycle\nprinciples:\n  - name: Visibility\n    description: Track Logo API request volume per consumer / domain and reconcile against the 500K\n      soft monthly ceiling and the 2,500 hard Brand API cap; pull invoices from the Brandfetch dashboard.\n  - name: Allocation\n    description: Issue separate API keys per consuming product or surface so logo and brand-data spend\n      can be attributed cleanly.\n  - name: Optimization\n    description: Cache logo URLs and brand records aggressively at the CDN / edge to stay within per-IP\n      and per-customer 5-minute throughput windows; reserve Brand API calls for surfaces that need rich\n      brand metadata; switch to Enterprise when sustained volume exceeds the Brand API hard cap.\n  - name: Accountability\n    description: Designate a brand-platform owner; alert when 5-minute or monthly thresholds approach\n      exhaustion; budget annual billing for the 20% discount on Brand API.\nmaintainers:\n  - FN:\
  \ Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/brand-api/refs/heads/main/finops/brand-api-finops.yml
sources:
- https://brandfetch.com/developers/pricing
- https://docs.brandfetch.com/logo-api/rate-limits
specification: FinOps Framework
tags:
- Brands
- Logos
- Brand Assets
- Company Data
- Firmographics
- FinOps
- FOCUS
---
