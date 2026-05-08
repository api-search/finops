---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: reddit-data-api-openapi.yml
  format: yaml
  label: Reddit Data API
  slug: data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/reddit/refs/heads/main/openapi/reddit-data-api-openapi.yml
- filename: reddit-ads-api-openapi.yml
  format: yaml
  label: Reddit Ads API
  slug: ads-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/reddit/refs/heads/main/openapi/reddit-ads-api-openapi.yml
- filename: reddit-embeds-openapi.yml
  format: yaml
  label: Reddit Embeds (oEmbed)
  slug: embeds
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/reddit/refs/heads/main/openapi/reddit-embeds-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps shape for the Reddit Data API. Free tier carries no FinOps signal; the commercial tier is contact-sales and produces a contract-level invoice rather than a granular usage feed.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Reddit, Inc.
  ProviderName: Reddit
  PublisherName: Reddit, Inc.
  ServiceCategory: Social Media Data
  ServiceName: Reddit Data API
layout: finops
meters:
- aggregation: count
  description: Non-billable OAuth client calls under the free non-commercial tier
  dimensions:
  - oauth_client
  name: free_tier_calls
  unit: request
- aggregation: sum
  description: Annual Reddit Data API commercial agreement
  dimensions:
  - contract_term
  name: commercial_contract
  unit: contract
name: Reddit Finops
provider_name: Reddit
provider_slug: reddit
publisher_name: Reddit, Inc.
service_category: Social Media Data
slug: reddit-finops
source_filename: reddit-finops.yml
source_heading: FinOps Profile
source_url: https://www.reddit.com/wiki/api
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Reddit\nproviderId: reddit\npublisherName: Reddit, Inc.\nserviceCategory: Social Media Data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Social Media\n  - Content\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for the Reddit Data API. Free tier carries no FinOps\n  signal; the commercial tier is contact-sales and produces a contract-level invoice rather\n  than a granular usage feed.\nsources:\n  - https://www.reddit.com/wiki/api\nnotes: Reddit developer/billing pages are gated against automated fetch; the meter list reflects\n  the assumed free + contract shape rather than a fetched billing surface.\n\
  billingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Reddit Data API\n  ServiceCategory: Social Media Data\n  ProviderName: Reddit\n  PublisherName: Reddit, Inc.\n  InvoiceIssuerName: Reddit, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: free_tier_calls\n    description: Non-billable OAuth client calls under the free non-commercial tier\n    unit: request\n    aggregation: count\n    dimensions:\n      - oauth_client\n  - name: commercial_contract\n    description: Annual Reddit Data API commercial agreement\n    unit: contract\n    aggregation: sum\n    dimensions:\n      - contract_term\nprinciples:\n  - name: Visibility\n    description: Reddit's OAuth dashboard exposes per-client request counters; pair with internal\n      logging on your client side to attribute spend to consuming products before invoice time.\n  - name: Allocation\n    description: Allocate the Reddit\
  \ commercial contract to the consuming product / data team;\n      tag client_ids by use-case so each call can be attributed.\n  - name: Optimization\n    description: Cache responses aggressively, use the listing endpoints' after/before pagination\n      rather than polling, and confine commercial ingestion to the minimum subreddit / endpoint\n      surface to keep call ceilings tight at renewal.\n  - name: Accountability\n    description: The data / research team consuming Reddit content owns the contract; engineering\n      owns OAuth client hygiene.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/reddit/refs/heads/main/finops/reddit-finops.yml
sources:
- https://www.reddit.com/wiki/api
specification: FinOps Framework
tags:
- Social Media
- Content
- FinOps
- FOCUS
---
