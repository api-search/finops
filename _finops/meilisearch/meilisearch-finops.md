---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription with Usage or Resource Pricing
description: FOCUS-aligned FinOps for Meilisearch.
focus_columns:
  BillingCurrency: USD
  ProviderName: Meilisearch
  PublisherName: Meilisearch
  ServiceCategory: Search
  ServiceName: Meilisearch
layout: finops
meters:
- aggregation: sum
  name: search_queries
  unit: query
- aggregation: max
  name: stored_documents
  unit: document-month
- aggregation: sum
  name: compute_resources
  unit: resource-hour
- aggregation: max
  name: storage
  unit: GB-month
name: Meilisearch Finops
provider_name: Meilisearch
provider_slug: meilisearch
publisher_name: Meilisearch
service_category: Search
slug: meilisearch-finops
source_filename: meilisearch-finops.yml
source_heading: FinOps Profile
source_url: https://www.meilisearch.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Meilisearch\nproviderId: meilisearch\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Search\ndescription: FOCUS-aligned FinOps for Meilisearch.\nsources:\n  - https://www.meilisearch.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Meilisearch\nserviceCategory: Search\nbillingModel:\n  pricingCategory: Subscription with Usage or Resource Pricing\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Meilisearch\n  ServiceCategory: Search\n  ProviderName: Meilisearch\n  PublisherName: Meilisearch\n  BillingCurrency: USD\nmeters:\n  - name: search_queries\n    unit: query\n    aggregation:\
  \ sum\n  - name: stored_documents\n    unit: document-month\n    aggregation: max\n  - name: compute_resources\n    unit: resource-hour\n    aggregation: sum\n  - name: storage\n    unit: GB-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Meilisearch consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/meilisearch/refs/heads/main/finops/meilisearch-finops.yml
sources:
- https://www.meilisearch.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Search
---
