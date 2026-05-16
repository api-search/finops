---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: google-search-console-api-openapi.yml
  format: yaml
  label: Google Search Console API
  slug: google-search-console-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-search-console/refs/heads/main/openapi/google-search-console-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: On-Demand
  chargeCategories:
  - Usage
  pricingCategory: Free
description: 'FOCUS-aligned FinOps for the Google Search Console API: free-of-charge service whose FinOps cost is human / pipeline cost rather than per-call billing. Meters track quota consumption rather than invoice line items.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google LLC
  ProviderName: Google
  PublisherName: Google LLC
  ServiceCategory: SEO / Search Tools
  ServiceName: Google Search Console
layout: finops
meters:
- aggregation: sum
  description: Search Analytics queries against per-site / per-user / per-project quotas
  dimensions:
  - site
  - user
  - project
  name: search_analytics_queries
  unit: request
- aggregation: sum
  description: URL Inspection / index inspection queries against per-site / per-project quotas
  dimensions:
  - site
  - project
  name: url_inspection_queries
  unit: request
- aggregation: sum
  description: Calls to the Indexing API
  dimensions:
  - project
  name: indexing_api_calls
  unit: request
- aggregation: sum
  description: Sitemap submission and management calls
  dimensions:
  - site
  name: sitemap_submissions
  unit: request
name: Google Search Console Finops
provider_name: Google Search Console
provider_slug: google-search-console
publisher_name: Google LLC
service_category: SEO / Search Tools
slug: google-search-console-finops
source_filename: google-search-console-finops.yml
source_heading: FinOps Profile
source_url: https://developers.google.com/webmaster-tools/limits
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Search Console\nproviderId: google-search-console\npublisherName: Google LLC\nserviceCategory: SEO / Search Tools\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - SEO\n  - Search\n  - Webmaster Tools\ndescription: 'FOCUS-aligned FinOps for the Google Search Console API: free-of-charge service whose FinOps\n  cost is human / pipeline cost rather than per-call billing. Meters track quota consumption rather than\n  invoice line items.'\nsources:\n  - https://developers.google.com/webmaster-tools/limits\nbillingModel:\n  pricingCategory: Free\n  billingFrequency: On-Demand\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Google Search Console\n  ServiceCategory: SEO / Search Tools\n  ProviderName: Google\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: search_analytics_queries\n    description: Search Analytics queries against per-site / per-user / per-project quotas\n    unit: request\n    aggregation: sum\n    dimensions:\n      - site\n      - user\n      - project\n  - name: url_inspection_queries\n    description: URL Inspection / index inspection queries against per-site / per-project quotas\n    unit: request\n    aggregation: sum\n    dimensions:\n      - site\n      - project\n  - name: indexing_api_calls\n    description: Calls to the Indexing API\n    unit: request\n    aggregation: sum\n    dimensions:\n      - project\n  - name: sitemap_submissions\n    description: Sitemap submission and management calls\n    unit: request\n    aggregation:\
  \ sum\n    dimensions:\n      - site\nprinciples:\n  - name: Visibility\n    description: Track API quota consumption in the Google Cloud Console quota tab; export usage to\n      logging for trend analysis even though no charges accrue.\n  - name: Allocation\n    description: Use distinct Google Cloud projects per consuming team or workload so quota usage and\n      eventual rate-limit incidents map to owners.\n  - name: Optimization\n    description: Cache Search Analytics responses, batch URL inspection calls, and stagger Indexing\n      API submissions across the day to avoid hitting per-minute / per-day caps.\n  - name: Accountability\n    description: Designate an SEO / data-platform owner for quota raise requests and monitor 429 rates\n      so consumers throttle themselves before quota exhaustion.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-search-console/refs/heads/main/finops/google-search-console-finops.yml
sources:
- https://developers.google.com/webmaster-tools/limits
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- SEO
- Search
- Webmaster Tools
---
