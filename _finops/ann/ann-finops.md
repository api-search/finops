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
  chargeCategories:
  - Adjustment
  - Credit
  pricingCategory: Take Rate
description: FOCUS-aligned FinOps placeholder for Ann Taylor's affiliate program. The cash flow is reverse-direction (publisher earns commission, not pays a fee); the publisher's FinOps cost surface is the affiliate-network platform fee plus revenue-share, not Ann Taylor's API.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: FlexOffers (or CJ Affiliate, depending on network)
  ProviderName: Ann Taylor
  PublisherName: Ann Taylor / Sycamore Partners
  ServiceCategory: Affiliate Marketing
  ServiceName: Ann Taylor Affiliate Program
layout: finops
meters:
- aggregation: sum
  description: Gross sales attributed via affiliate links
  dimensions:
  - publisher
  - sub_id
  - channel
  name: attributed_sales
  unit: USD
- aggregation: sum
  description: Commission paid out to publisher (negative cost / revenue from FinOps view)
  dimensions:
  - publisher
  - period
  name: commissions_earned
  unit: USD
- aggregation: count
  description: Affiliate link click volume
  dimensions:
  - publisher
  - link
  name: clicks
  unit: click
name: Ann Finops
provider_name: ANN Inc.
provider_slug: ann
publisher_name: Ann Taylor (operated by Sycamore Partners portfolio companies)
service_category: Affiliate Marketing
slug: ann-finops
source_filename: ann-finops.yml
source_heading: FinOps Profile
source_url: https://www.flexoffers.com/affiliate-programs/ann-taylor-affiliate-program/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: ANN Inc.\nproviderId: ann\npublisherName: Ann Taylor (operated by Sycamore Partners portfolio companies)\nserviceCategory: Affiliate Marketing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Affiliate Marketing\n  - Retail\ndescription: >-\n  FOCUS-aligned FinOps placeholder for Ann Taylor's affiliate program. The\n  cash flow is reverse-direction (publisher earns commission, not pays a\n  fee); the publisher's FinOps cost surface is the affiliate-network platform\n  fee plus revenue-share, not Ann Taylor's API.\nnotes: >-\n  Affiliate revenue is not an API charge category in the conventional FinOps\n\
  \  sense; it is a marketing channel commission settled via FlexOffers / CJ.\nsources:\n  - https://www.flexoffers.com/affiliate-programs/ann-taylor-affiliate-program/\nbillingModel:\n  pricingCategory: Take Rate\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Ann Taylor Affiliate Program\n  ServiceCategory: Affiliate Marketing\n  ProviderName: Ann Taylor\n  PublisherName: Ann Taylor / Sycamore Partners\n  InvoiceIssuerName: FlexOffers (or CJ Affiliate, depending on network)\n  BillingCurrency: USD\nmeters:\n  - name: attributed_sales\n    description: Gross sales attributed via affiliate links\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - publisher\n      - sub_id\n      - channel\n  - name: commissions_earned\n    description: Commission paid out to publisher (negative cost / revenue from FinOps view)\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - publisher\n     \
  \ - period\n  - name: clicks\n    description: Affiliate link click volume\n    unit: click\n    aggregation: count\n    dimensions:\n      - publisher\n      - link\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the FlexOffers / CJ publisher dashboard for click, conversion, and\n      payout reporting. Ann Taylor itself does not expose publisher-level\n      telemetry.\n  - name: Allocation\n    description: >-\n      Allocate affiliate revenue and any platform fees to the marketing\n      sub-channel and content team that owns the link.\n  - name: Optimization\n    description: >-\n      Optimization levers are creative selection, deep-link strategy, and\n      catalog feed freshness; not request-rate tuning.\n  - name: Accountability\n    description: >-\n      Marketing and content teams own this revenue line; finance / FinOps\n      handles 1099 reconciliation through the network.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ann/refs/heads/main/finops/ann-finops.yml
sources:
- https://www.flexoffers.com/affiliate-programs/ann-taylor-affiliate-program/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Affiliate Marketing
- Retail
---
