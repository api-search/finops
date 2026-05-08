---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: idex-onsite-full-feed-api-openapi.yml
  format: yaml
  label: IDEX Onsite Full Feed API
  slug: idex-onsite-full-feed-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/diamond-search/refs/heads/main/openapi/idex-onsite-full-feed-api-openapi.yml
- filename: idex-lab-grown-file-api-openapi.yml
  format: yaml
  label: IDEX Lab Grown File API
  slug: idex-lab-grown-file-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/diamond-search/refs/heads/main/openapi/idex-lab-grown-file-api-openapi.yml
- filename: idex-data-report-api-openapi.yml
  format: yaml
  label: IDEX Data Report API
  slug: idex-data-report-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/diamond-search/refs/heads/main/openapi/idex-data-report-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Refund
  pricingCategory: Subscription
description: FOCUS-aligned FinOps shape for IDEX Online Diamond Search. Billing is annual subscription per IDEX tier (Direct / Premium / Pro / Onsite); API access is bundled with the subscription rather than metered per request.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: IDEX Online Ltd.
  ProviderName: IDEX Online
  PublisherName: IDEX Online Ltd.
  ServiceCategory: Market Data / Diamond Trading
  ServiceName: IDEX Diamond Search
layout: finops
meters:
- aggregation: count
  description: Active IDEX subscriptions by tier
  dimensions:
  - tier
  name: subscription_seats
  unit: seat
- aggregation: sum
  description: Feed pulls / API calls by subscriber (informational, not invoiced)
  dimensions:
  - api
  - subscription_tier
  name: feed_pulls
  unit: request
name: Diamond Search Finops
provider_name: Diamond Search
provider_slug: diamond-search
publisher_name: IDEX Online Ltd.
service_category: Market Data / Diamond Trading
slug: diamond-search-finops
source_filename: diamond-search-finops.yml
source_heading: FinOps Profile
source_url: https://www.idexonline.com/Subscribe
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Diamond Search\nproviderId: diamond-search\npublisherName: IDEX Online Ltd.\nserviceCategory: Market Data / Diamond Trading\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Diamonds\n  - Lab Grown\n  - Pricing\n  - Trading\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for IDEX Online Diamond Search. Billing is annual subscription\n  per IDEX tier (Direct / Premium / Pro / Onsite); API access is bundled with the subscription rather\n  than metered per request.\nsources:\n  - https://www.idexonline.com/Subscribe\n  - https://www.idexonline.com/OurServices\nbillingModel:\n  pricingCategory: Subscription\n\
  \  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Refund\nfocusColumns:\n  ServiceName: IDEX Diamond Search\n  ServiceCategory: Market Data / Diamond Trading\n  ProviderName: IDEX Online\n  PublisherName: IDEX Online Ltd.\n  InvoiceIssuerName: IDEX Online Ltd.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_seats\n    description: Active IDEX subscriptions by tier\n    unit: seat\n    aggregation: count\n    dimensions:\n      - tier\n  - name: feed_pulls\n    description: Feed pulls / API calls by subscriber (informational, not invoiced)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - subscription_tier\nprinciples:\n  - name: Visibility\n    description: Reconcile annual IDEX invoices against the contracted tier and seat count; the API itself\n      does not produce a usage invoice.\n  - name: Allocation\n    description: Allocate IDEX subscription cost to the\
  \ trading desk or storefront product that consumes\n      the Onsite/Data Report feeds.\n  - name: Optimization\n    description: Choose the lowest tier that includes required entitlements (Onsite vs. Pro vs. Premium);\n      cache feed snapshots to reduce repeated pulls and shared infrastructure load.\n  - name: Accountability\n    description: Subscription owner is responsible for renewal terms and ensuring API integrations stay\n      within fair-use polling cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/diamond-search/refs/heads/main/finops/diamond-search-finops.yml
sources:
- https://www.idexonline.com/Subscribe
- https://www.idexonline.com/OurServices
specification: FinOps Framework
tags:
- Diamonds
- Lab Grown
- Pricing
- Trading
- FinOps
- FOCUS
---
