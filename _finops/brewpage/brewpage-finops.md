---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: brewpage-openapi.yml
  format: yaml
  label: BrewPage API
  slug: api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/brewpage/refs/heads/main/openapi/brewpage-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Free
description: Capacity-oriented FinOps shape for BrewPage. Because the platform is free, the meters track consumption against published structural caps rather than $-denominated charges. Consumers can use these meters for internal allocation (e.g., per-agent or per-team hosting footprint) and for forecasting when migrating to a self-hosted alternative.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: N/A
  ProviderName: BrewPage
  PublisherName: BrewPage
  RegionId: global
  ServiceCategory: Web Hosting and Storage
  ServiceName: BrewPage
layout: finops
meters:
- aggregation: count
  dimensions:
  - namespace
  - format
  - owner_token
  name: html_pages_hosted
  unit: page
- aggregation: count
  dimensions:
  - namespace
  - content_type
  - owner_token
  name: files_hosted
  unit: file
- aggregation: sum
  dimensions:
  - namespace
  - owner_token
  name: file_bytes_stored
  unit: byte
- aggregation: count
  dimensions:
  - namespace
  - owner_token
  name: sites_hosted
  unit: site
- aggregation: count
  dimensions:
  - site_id
  name: site_files
  unit: file
- aggregation: count
  dimensions:
  - store_id
  - owner_token
  name: kv_keys
  unit: key
- aggregation: count
  dimensions:
  - namespace
  - owner_token
  name: json_documents
  unit: document
- aggregation: count
  dimensions:
  - resource_type
  - namespace
  name: views_served
  unit: request
- aggregation: max
  dimensions:
  - resource_type
  name: ttl_days
  unit: day
name: Brewpage Finops
provider_name: BrewPage
provider_slug: brewpage
publisher_name: BrewPage
service_category: Web Hosting and Storage
slug: brewpage-finops
source_filename: brewpage-finops.yml
source_heading: FinOps Profile
source_url: https://brewpage.app/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: BrewPage\nproviderId: brewpage\ncreated: '2026-05-16'\nmodified: '2026-05-16'\nreconciled: false\nnotes: >-\n  BrewPage is a free service with no commercial billing surface. There is no\n  invoice, no metered price, no subscription, and no customer agreement. The\n  FinOps shape below documents the platform's *capacity* meters (file count,\n  KV keys, document count, storage size, TTL) so that consumers can map\n  BrewPage usage to internal allocation/showback, not so that BrewPage itself\n  can be charged. Set reconciled to true if BrewPage introduces paid tiers.\ntags:\n  - FinOps\n  - FOCUS\n  - Free\n  - Hosting\ndescription: >-\n  Capacity-oriented FinOps shape for BrewPage. Because the platform is free,\n  the meters track consumption against published structural caps rather than\n  $-denominated charges. Consumers can use these meters for internal\n  allocation\
  \ (e.g., per-agent or per-team hosting footprint) and for\n  forecasting when migrating to a self-hosted alternative.\nsources:\n  - https://brewpage.app/\n  - https://brewpage.app/llms.txt\n  - https://brewpage.app/llms-full.txt\n  - https://brewpage.app/api/openapi.yaml\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: BrewPage\nserviceCategory: Web Hosting and Storage\nbillingModel:\n  pricingCategory: Free\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nmeters:\n  - name: html_pages_hosted\n    unit: page\n    aggregation: count\n    dimensions:\n      - namespace\n      - format\n      - owner_token\n  - name: files_hosted\n    unit: file\n    aggregation: count\n    dimensions:\n      - namespace\n      - content_type\n      - owner_token\n  - name: file_bytes_stored\n\
  \    unit: byte\n    aggregation: sum\n    dimensions:\n      - namespace\n      - owner_token\n  - name: sites_hosted\n    unit: site\n    aggregation: count\n    dimensions:\n      - namespace\n      - owner_token\n  - name: site_files\n    unit: file\n    aggregation: count\n    dimensions:\n      - site_id\n  - name: kv_keys\n    unit: key\n    aggregation: count\n    dimensions:\n      - store_id\n      - owner_token\n  - name: json_documents\n    unit: document\n    aggregation: count\n    dimensions:\n      - namespace\n      - owner_token\n  - name: views_served\n    unit: request\n    aggregation: count\n    dimensions:\n      - resource_type\n      - namespace\n  - name: ttl_days\n    unit: day\n    aggregation: max\n    dimensions:\n      - resource_type\nfocusColumns:\n  ServiceName: BrewPage\n  ServiceCategory: Web Hosting and Storage\n  ProviderName: BrewPage\n  PublisherName: BrewPage\n  InvoiceIssuerName: N/A\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  RegionId:\
  \ global\nprinciples:\n  - name: Visibility\n    description: Use GET /api/stats for platform-wide usage, and pass X-Owner-Token to the list endpoints (GET /api/kv, /api/json, /api/files) to see only the caller's resources. The Gallery endpoint surfaces public content.\n  - name: Allocation\n    description: Tag resources by namespace at creation (`ns` query param) and by owner-token group across creates to attribute hosting footprint to a team, agent, or feature.\n  - name: Optimization\n    description: Use PUT to iterate on a stable short URL instead of re-POSTing (saves IndexNow quota and avoids duplicate gallery entries). Set TTL as low as the use case allows (1..30 days). For binary artifacts, prefer /api/files over re-encoding into HTML.\n  - name: Accountability\n    description: Every request is logged with IP, User-Agent, method, path, status, and timestamp for 30 days; abuse reports are posted to /api/reports. Owners control deletion via DELETE with X-Owner-Token.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/brewpage/refs/heads/main/finops/brewpage-finops.yml
sources:
- https://brewpage.app/
- https://brewpage.app/llms.txt
- https://brewpage.app/llms-full.txt
- https://brewpage.app/api/openapi.yaml
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Free
- Hosting
---
