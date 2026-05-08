---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: scrapfly-scrape-openapi.yml
  format: yaml
  label: Scrapfly Scrape API
  slug: scrape-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scrapfly/refs/heads/main/openapi/scrapfly-scrape-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription + Pay-As-You-Go
description: FOCUS-aligned FinOps shape for Scrapfly — credit-based subscription with optional pay-as-you-go overflow. A single credit pool meters all products (Scrape, Cloud Browser, Screenshot, Extraction, Crawler). Per-request credit cost varies by enabled features (JS rendering, residential proxy, country targeting).
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Scrapfly Inc.
  ProviderName: Scrapfly
  PublisherName: Scrapfly Inc.
  ServiceCategory: Web Scraping / Data Extraction
  ServiceName: Scrapfly
layout: finops
meters:
- aggregation: sum
  description: Recurring monthly plan fee (Discovery, Pro, Startup, Enterprise, Custom)
  dimensions:
  - plan
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Credits consumed per Scrape API request, varying by features enabled
  dimensions:
  - product
  - render_js
  - proxy_pool
  - country
  name: scrape_credits
  unit: credit
- aggregation: sum
  description: Credits consumed by Cloud Browser sessions
  dimensions:
  - product
  - session_duration
  name: cloud_browser_credits
  unit: credit
- aggregation: sum
  description: Credits consumed by Screenshot API requests
  dimensions:
  - product
  - render_js
  name: screenshot_credits
  unit: credit
- aggregation: sum
  description: Credits consumed by Extraction API requests
  dimensions:
  - product
  - extraction_model
  name: extraction_credits
  unit: credit
- aggregation: sum
  description: Credits consumed by Crawler API requests
  dimensions:
  - product
  name: crawler_credits
  unit: credit
- aggregation: sum
  description: Pay-as-you-go credit blocks billed when subscription credits are exhausted (Pro and above)
  dimensions:
  - plan
  name: extra_credit_blocks
  unit: 10000-credit-block
name: Scrapfly Finops
provider_name: Scrapfly
provider_slug: scrapfly
publisher_name: Scrapfly Inc.
service_category: Web Scraping / Data Extraction
slug: scrapfly-finops
source_filename: scrapfly-finops.yml
source_heading: FinOps Profile
source_url: https://scrapfly.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Scrapfly\nproviderId: scrapfly\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Web Scraping\n  - Data Extraction\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Scrapfly — credit-based subscription with optional pay-as-you-go\n  overflow. A single credit pool meters all products (Scrape, Cloud Browser, Screenshot, Extraction, Crawler).\n  Per-request credit cost varies by enabled features (JS rendering, residential proxy, country targeting).\nsources:\n  - https://scrapfly.io/pricing\n  - https://scrapfly.io/docs/scrape-api/getting-started\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Scrapfly Inc.\nserviceCategory: Web Scraping\
  \ / Data Extraction\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Scrapfly\n  ServiceCategory: Web Scraping / Data Extraction\n  ProviderName: Scrapfly\n  PublisherName: Scrapfly Inc.\n  InvoiceIssuerName: Scrapfly Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subscription_fee\n    description: Recurring monthly plan fee (Discovery, Pro, Startup, Enterprise, Custom)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: scrape_credits\n    description: Credits consumed per Scrape API request, varying by features enabled\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - product\n      - render_js\n      - proxy_pool\n      - country\n  - name: cloud_browser_credits\n    description: Credits consumed by Cloud Browser sessions\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - product\n\
  \      - session_duration\n  - name: screenshot_credits\n    description: Credits consumed by Screenshot API requests\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - product\n      - render_js\n  - name: extraction_credits\n    description: Credits consumed by Extraction API requests\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - product\n      - extraction_model\n  - name: crawler_credits\n    description: Credits consumed by Crawler API requests\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - product\n  - name: extra_credit_blocks\n    description: Pay-as-you-go credit blocks billed when subscription credits are exhausted (Pro and above)\n    unit: 10000-credit-block\n    aggregation: sum\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n    description: Inspect X-Scrapfly-Api-Cost on every response to attribute credit cost per call. Use\n      the Scrapfly dashboard's usage analytics, the cost estimator, and per-project\
  \ usage views to monitor\n      consumption.\n  - name: Allocation\n    description: Use Scrapfly Projects to split credit consumption by application, team, or environment.\n      Project-scoped concurrency and credit usage feed back via X-Scrapfly-Project-* headers.\n  - name: Optimization\n    description: Disable JS rendering and residential proxies when not required (each adds credit cost),\n      cache successful responses, and right-size the plan against observed monthly credit burn. Use the\n      pricing estimator to model feature toggles before changes.\n  - name: Accountability\n    description: Engineering owners of each Project hold accountability for their credit budget. Free\n      and Discovery plans hard-cap at quota; Pro+ owners must monitor overflow billing to avoid surprise\n      pay-as-you-go charges.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scrapfly/refs/heads/main/finops/scrapfly-finops.yml
sources:
- https://scrapfly.io/pricing
- https://scrapfly.io/docs/scrape-api/getting-started
specification: FinOps Framework
tags:
- Web Scraping
- Data Extraction
- FinOps
- FOCUS
---
