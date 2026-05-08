---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: apollo-io-openapi.yml
  format: yaml
  label: Apollo People Search API
  slug: apollo-people-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apollo-io/refs/heads/main/openapi/apollo-io-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  pricingCategory: Subscription Per Seat With Usage Credits
description: Apollo.io bills per-seat-per-month subscriptions with separate monthly credit pools for searches, enrichments, mobile-number reveals, exports, and dialer minutes. Heavy-usage workspaces purchase credit top-ups or upgrade tier. This artifact maps Apollo charges to FOCUS columns for FinOps allocation across go-to-market cost centers.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Apollo.io
  ProviderName: Apollo.io
  PublisherName: Apollo.io
  ServiceCategory: Sales Intelligence
  ServiceName: Apollo.io
layout: finops
meters:
- aggregation: sum
  description: Active seats on Free / Basic / Professional / Organization tiers.
  dimensions:
  - tier
  - team
  - cost_center
  name: apollo_seats
  unit: seat-month
- aggregation: sum
  description: Search credits consumed by people / organization search calls.
  dimensions:
  - integration
  - user
  name: apollo_search_credits
  unit: credits
- aggregation: sum
  description: Enrichment credits consumed by people / org enrichment calls.
  dimensions:
  - integration
  - user
  name: apollo_enrichment_credits
  unit: credits
- aggregation: sum
  description: Mobile-number-reveal credits consumed.
  dimensions:
  - user
  - cost_center
  name: apollo_mobile_credits
  unit: credits
- aggregation: sum
  description: Export credits consumed when exporting people / accounts.
  dimensions:
  - user
  - cost_center
  name: apollo_export_credits
  unit: credits
- aggregation: sum
  description: Dialer minutes used through Apollo's calling feature.
  dimensions:
  - user
  - country
  name: apollo_dialer_minutes
  unit: minutes
- aggregation: sum
  description: Outbound sequence emails sent.
  dimensions:
  - sequence
  - user
  name: apollo_email_sends
  unit: messages
name: Apollo Io Finops
provider_name: Apollo.io
provider_slug: apollo-io
publisher_name: Apollo.io
service_category: Sales Intelligence
slug: apollo-io-finops
source_filename: apollo-io-finops.yml
source_heading: FinOps Profile
source_url: https://www.apollo.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Apollo.io\nproviderId: apollo-io\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Sales Intelligence\n  - B2B Data\n  - FinOps\n  - FOCUS\ndescription: >-\n  Apollo.io bills per-seat-per-month subscriptions with separate monthly\n  credit pools for searches, enrichments, mobile-number reveals, exports,\n  and dialer minutes. Heavy-usage workspaces purchase credit top-ups or\n  upgrade tier. This artifact maps Apollo charges to FOCUS columns for\n  FinOps allocation across go-to-market cost centers.\nsources:\n  - https://www.apollo.io/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Apollo.io\n\
  serviceCategory: Sales Intelligence\nbillingModel:\n  pricingCategory: Subscription Per Seat With Usage Credits\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: Apollo.io\n  ServiceCategory: Sales Intelligence\n  ProviderName: Apollo.io\n  PublisherName: Apollo.io\n  InvoiceIssuerName: Apollo.io\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: apollo_seats\n    description: Active seats on Free / Basic / Professional / Organization tiers.\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tier\n      - team\n      - cost_center\n  - name: apollo_search_credits\n    description: Search credits consumed by people / organization search calls.\n    unit: credits\n    aggregation: sum\n    dimensions:\n      - integration\n      - user\n  - name: apollo_enrichment_credits\n    description: Enrichment credits consumed by people / org enrichment\
  \ calls.\n    unit: credits\n    aggregation: sum\n    dimensions:\n      - integration\n      - user\n  - name: apollo_mobile_credits\n    description: Mobile-number-reveal credits consumed.\n    unit: credits\n    aggregation: sum\n    dimensions:\n      - user\n      - cost_center\n  - name: apollo_export_credits\n    description: Export credits consumed when exporting people / accounts.\n    unit: credits\n    aggregation: sum\n    dimensions:\n      - user\n      - cost_center\n  - name: apollo_dialer_minutes\n    description: Dialer minutes used through Apollo's calling feature.\n    unit: minutes\n    aggregation: sum\n    dimensions:\n      - user\n      - country\n  - name: apollo_email_sends\n    description: Outbound sequence emails sent.\n    unit: messages\n    aggregation: sum\n    dimensions:\n      - sequence\n      - user\nprinciples:\n  - name: Visibility\n    description: >-\n      Track Apollo's API Usage endpoint to monitor remaining search /\n      enrichment / mobile\
  \ credits weekly; pull monthly invoices for seat\n      and credit-topup charges.\n  - name: Allocation\n    description: >-\n      Allocate seat costs by team; allocate credit consumption by\n      sourcing campaign or integration via tags and lists.\n  - name: Optimization\n    description: >-\n      Use bulk enrichment endpoints (up to 10 records per call) for the\n      best per-record price; cache enrichments to avoid double-paying;\n      audit unused seats monthly.\n  - name: Accountability\n    description: >-\n      Designate Sales Operations / Marketing Ops as contract owner;\n      review credit consumption monthly and right-size at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apollo-io/refs/heads/main/finops/apollo-io-finops.yml
sources:
- https://www.apollo.io/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Sales Intelligence
- B2B Data
- FinOps
- FOCUS
---
