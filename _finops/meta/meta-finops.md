---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: meta-openapi.yml
  format: yaml
  label: Facebook Graph API - User
  slug: facebook-graph-api-user
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/meta/refs/heads/main/openapi/meta-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Meta (Facebook + Instagram + WhatsApp + Threads).
focus_columns:
  BillingCurrency: USD
  ProviderName: Meta (Facebook + Instagram + WhatsApp + Threads)
  PublisherName: Meta (Facebook + Instagram + WhatsApp + Threads)
  ServiceCategory: Social + Messaging + Ads
  ServiceName: Meta (Facebook + Instagram + WhatsApp + Threads)
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  - region
  - instance_type
  - tenant
  name: compute_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - service
  - tier
  name: storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - egress_type
  - region_pair
  name: data_transfer
  unit: GB
- aggregation: sum
  dimensions:
  - service
  - operation
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - service
  name: managed_services
  unit: varies
name: Meta Finops
provider_name: Meta
provider_slug: meta
publisher_name: Meta (Facebook + Instagram + WhatsApp + Threads)
service_category: Social + Messaging + Ads
slug: meta-finops
source_filename: meta-finops.yml
source_heading: FinOps Profile
source_url: https://developers.facebook.com/docs/marketing-api
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Meta (Facebook + Instagram + WhatsApp + Threads)\nproviderId: meta\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Social + Messaging + Ads\ndescription: FOCUS-aligned FinOps for Meta (Facebook + Instagram + WhatsApp + Threads).\nsources:\n  - https://developers.facebook.com/docs/marketing-api\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Meta (Facebook + Instagram + WhatsApp + Threads)\nserviceCategory: Social + Messaging + Ads\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Meta (Facebook + Instagram\
  \ + WhatsApp + Threads)\n  ServiceCategory: Social + Messaging + Ads\n  ProviderName: Meta (Facebook + Instagram + WhatsApp + Threads)\n  PublisherName: Meta (Facebook + Instagram + WhatsApp + Threads)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Meta (Facebook + Instagram + WhatsApp + Threads) consumption monthly.\n  - name: Allocation\n  \
  \  description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/meta/refs/heads/main/finops/meta-finops.yml
sources:
- https://developers.facebook.com/docs/marketing-api
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Social + Messaging + Ads
---
