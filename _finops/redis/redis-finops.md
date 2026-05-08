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
  pricingCategory: Per-Shard-Hour with Minimums
description: FOCUS-aligned FinOps for Redis Cloud.
focus_columns:
  BillingCurrency: USD
  ProviderName: Redis Cloud
  PublisherName: Redis Cloud
  ServiceCategory: Database / Cache
  ServiceName: Redis Cloud
layout: finops
meters:
- aggregation: sum
  dimensions:
  - plan
  - region
  - cloud
  name: shard_hours
  unit: shard-hour
- aggregation: max
  name: memory
  unit: GB-month
- aggregation: sum
  name: data_transfer
  unit: GB
- aggregation: max
  name: backup_storage
  unit: GB-month
name: Redis Finops
provider_name: Redis
provider_slug: redis
publisher_name: Redis Cloud
service_category: Database / Cache
slug: redis-finops
source_filename: redis-finops.yml
source_heading: FinOps Profile
source_url: https://redis.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Redis Cloud\nproviderId: redis\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Database / Cache\ndescription: FOCUS-aligned FinOps for Redis Cloud.\nsources:\n  - https://redis.io/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Redis Cloud\nserviceCategory: Database / Cache\nbillingModel:\n  pricingCategory: Per-Shard-Hour with Minimums\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Redis Cloud\n  ServiceCategory: Database / Cache\n  ProviderName: Redis Cloud\n  PublisherName: Redis Cloud\n  BillingCurrency: USD\nmeters:\n  - name: shard_hours\n    unit: shard-hour\n    aggregation:\
  \ sum\n    dimensions:\n      - plan\n      - region\n      - cloud\n  - name: memory\n    unit: GB-month\n    aggregation: max\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n  - name: backup_storage\n    unit: GB-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Redis Cloud consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/redis/refs/heads/main/finops/redis-finops.yml
sources:
- https://redis.io/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Database / Cache
---
