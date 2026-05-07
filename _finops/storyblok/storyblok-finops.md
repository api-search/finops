---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: storyblok-content-delivery-api-v2-openapi.yml
  format: yaml
  label: Storyblok Content Delivery API
  slug: storyblok-content-delivery-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/storyblok/refs/heads/main/openapi/storyblok-content-delivery-api-v2-openapi.yml
- filename: storyblok-management-api-openapi.yml
  format: yaml
  label: Storyblok Management API
  slug: storyblok-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/storyblok/refs/heads/main/openapi/storyblok-management-api-openapi.yml
- filename: storyblok-image-service-openapi.yml
  format: yaml
  label: Storyblok Image Service
  slug: storyblok-image-service
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/storyblok/refs/heads/main/openapi/storyblok-image-service-openapi.yml
- filename: storyblok-webhooks-asyncapi.yml
  format: yaml
  label: Storyblok Webhooks
  slug: storyblok-webhooks
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/storyblok/refs/heads/main/asyncapi/storyblok-webhooks-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription + Usage Overages
description: FOCUS-aligned FinOps definition for Storyblok. Storyblok bills a tiered monthly or annual subscription with included quotas for traffic, API requests, AI credits, locales, and seats; overages on each meter are billed as separate line items at published per-unit rates.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Storyblok GmbH
  ProviderName: Storyblok
  PublisherName: Storyblok GmbH
  ServiceCategory: Content Management
  ServiceName: Storyblok
layout: finops
meters:
- aggregation: sum
  description: Monthly or annual base plan fee for the subscribed tier
  dimensions:
  - plan
  name: base_subscription
  unit: month
- aggregation: max
  description: Active user seats above the included count, billed at $15/seat/month
  dimensions:
  - plan
  - role
  name: user_seats
  unit: seat
- aggregation: sum
  description: Outbound traffic served above the included plan allotment, billed at $75 per 250GB
  dimensions:
  - region
  - space
  name: traffic_gb
  unit: GB
- aggregation: sum
  description: Content Delivery API requests above the included plan allotment, billed at $10 per 1M
  dimensions:
  - api
  - cache_status
  - space
  name: api_requests
  unit: request
- aggregation: max
  description: Locales above the included count, billed at $20/locale/month
  dimensions:
  - locale_code
  - space
  name: locales
  unit: locale
- aggregation: sum
  description: AI credits consumed above the included plan allotment, billed at $20 per 200k credits
  dimensions:
  - feature
  - space
  name: ai_credits
  unit: credit
name: Storyblok Finops
provider_name: Storyblok
provider_slug: storyblok
publisher_name: Storyblok GmbH
service_category: Headless CMS
slug: storyblok-finops
source_filename: storyblok-finops.yml
source_heading: FinOps Profile
source_url: https://www.storyblok.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Storyblok\nproviderId: storyblok\npublisherName: Storyblok GmbH\nserviceCategory: Headless CMS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - CMS\n  - Content Delivery\n  - Headless CMS\ndescription: FOCUS-aligned FinOps definition for Storyblok. Storyblok bills a tiered monthly or annual\n  subscription with included quotas for traffic, API requests, AI credits, locales, and seats; overages\n  on each meter are billed as separate line items at published per-unit rates.\nsources:\n  - https://www.storyblok.com/pricing\n  - https://www.storyblok.com/docs/api/content-delivery/v2\nbillingModel:\n\
  \  pricingCategory: Tiered Subscription + Usage Overages\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Storyblok\n  ServiceCategory: Content Management\n  ProviderName: Storyblok\n  PublisherName: Storyblok GmbH\n  InvoiceIssuerName: Storyblok GmbH\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: base_subscription\n    description: Monthly or annual base plan fee for the subscribed tier\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: user_seats\n    description: Active user seats above the included count, billed at $15/seat/month\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\n      - role\n  - name: traffic_gb\n    description: Outbound traffic served above the included plan allotment, billed at $75 per 250GB\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n\
  \      - space\n  - name: api_requests\n    description: Content Delivery API requests above the included plan allotment, billed at $10 per 1M\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - cache_status\n      - space\n  - name: locales\n    description: Locales above the included count, billed at $20/locale/month\n    unit: locale\n    aggregation: max\n    dimensions:\n      - locale_code\n      - space\n  - name: ai_credits\n    description: AI credits consumed above the included plan allotment, billed at $20 per 200k credits\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - feature\n      - space\nprinciples:\n  - name: Visibility\n    description: Use the Storyblok account dashboard usage views to track traffic GB, API requests,\n      AI credit consumption, seats, and locales against included plan allotments.\n  - name: Allocation\n    description: Allocate cost by space and locale; use Storyblok spaces as the primary attribution\n\
  \      boundary for multi-product tenants.\n  - name: Optimization\n    description: Maximize the use of cached CDN requests (1,000 RPS limit vs 50 RPS uncached) to stay\n      under the API request quota; consolidate locales onto fewer paid locales where possible; choose\n      annual billing for the published discount on Growth and Growth Plus.\n  - name: Accountability\n    description: Assign a Storyblok workspace owner per space; review monthly usage against included\n      limits to forecast overage spend; escalate to Premium/Elite when overages exceed roughly 1.5-2x\n      the next tier's base price.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/storyblok/refs/heads/main/finops/storyblok-finops.yml
sources:
- https://www.storyblok.com/pricing
- https://www.storyblok.com/docs/api/content-delivery/v2
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- CMS
- Content Delivery
- Headless CMS
---
