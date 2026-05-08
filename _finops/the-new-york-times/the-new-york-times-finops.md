---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: new-york-times-archive-openapi-original.yml
  format: yaml
  label: The New York Times Archive API
  slug: archive-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-archive-openapi-original.yml
- filename: new-york-times-article-search-openapi-original.yml
  format: yaml
  label: The New York Times Article Search API
  slug: article-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-article-search-openapi-original.yml
- filename: new-york-times-books-openapi-original.yml
  format: yaml
  label: The New York Times Books API
  slug: books-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-books-openapi-original.yml
- filename: new-york-times-most-popular-openapi-original.yml
  format: yaml
  label: The New York Times Most Popular API
  slug: most-popular
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-most-popular-openapi-original.yml
- filename: new-york-times-movie-review-openapi-original.yml
  format: yaml
  label: The New York Times Movie Reviews API
  slug: movie-reviews-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-movie-review-openapi-original.yml
- filename: new-york-times-semantic-openapi-original.yml
  format: yaml
  label: The New York Times Semantic API
  slug: semantic-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-semantic-openapi-original.yml
- filename: new-york-times-times-tags-openapi-original.yml
  format: yaml
  label: The New York Times TimesTags API
  slug: timestags-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-times-tags-openapi-original.yml
- filename: new-york-times-times-newswire-openapi-original.yml
  format: yaml
  label: The New York Times Times Newswire API
  slug: times-newswire-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-times-newswire-openapi-original.yml
- filename: new-york-times-top-stories-openapi-original.yml
  format: yaml
  label: The New York Times Top Stories API
  slug: top-stories
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-top-stories-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: On-Demand
  chargeCategories:
  - Usage
  pricingCategory: Free (Non-Commercial)
description: FOCUS-aligned FinOps scaffold for The New York Times Developer Network. The public APIs are free for non-commercial use under a developer key, so there is no FOCUS-billable usage line for general developers; any commercial / syndication use is invoiced under a separate negotiated agreement with The New York Times.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The New York Times Company
  ProviderName: The New York Times
  PublisherName: The New York Times Company
  ServiceCategory: News / Media
  ServiceName: NYT Developer Network
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - app_id
  name: api_requests
  unit: request
name: The New York Times Finops
provider_name: The New York Times
provider_slug: the-new-york-times
publisher_name: The New York Times Company
service_category: News / Media
slug: the-new-york-times-finops
source_filename: the-new-york-times-finops.yml
source_heading: FinOps Profile
source_url: https://developer.nytimes.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: The New York Times\nproviderId: the-new-york-times\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - News\n  - Media\ndescription: >-\n  FOCUS-aligned FinOps scaffold for The New York Times Developer Network. The public APIs are free for\n  non-commercial use under a developer key, so there is no FOCUS-billable usage line for general developers;\n  any commercial / syndication use is invoiced under a separate negotiated agreement with The New York\n  Times.\nsources:\n  - https://developer.nytimes.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: >-\n  Free non-commercial use means no FOCUS Usage line items. Commercial agreements are invoiced separately\n  by The New York Times Company and are not described publicly.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The New York Times Company\nserviceCategory: News / Media\nbillingModel:\n  pricingCategory: Free (Non-Commercial)\n  billingFrequency: On-Demand\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: NYT Developer Network\n  ServiceCategory: News / Media\n  ProviderName: The New York Times\n  PublisherName: The New York Times Company\n  InvoiceIssuerName: The New York Times Company\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - app_id\nprinciples:\n  - name: Visibility\n    description: Per-app usage is visible inside the NYT Developer Network portal; no programmatic FOCUS-grade\n      cost export exists for the free tier.\n  - name: Allocation\n    description: Allocate usage by registered NYT app per consuming product / team so quota headroom\
  \ is\n      tracked even though there is no monetary charge.\n  - name: Optimization\n    description: Cache responses, prefer Top Stories or Times Wire over Article Search where possible to\n      stay within per-app quotas, and consolidate apps to reduce key sprawl.\n  - name: Accountability\n    description: App owner inside the consuming organization is accountable for staying within the developer\n      key's quota and for upgrading to a commercial agreement when use crosses the non-commercial line.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/finops/the-new-york-times-finops.yml
sources:
- https://developer.nytimes.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- News
- Media
---
