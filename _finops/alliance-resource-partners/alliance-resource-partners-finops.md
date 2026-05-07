---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps shell for Alliance Resource Partners: no public API commercial surface. Data-feed and integration costs are governed by bilateral commercial agreements; reconcile against the contracted feed agreement.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Alliance Resource Partners, L.P.
  ProviderName: Alliance Resource Partners
  PublisherName: Alliance Resource Partners, L.P.
  ServiceCategory: Energy / Mining Data
  ServiceName: Alliance Resource Partners Data Feeds
layout: finops
meters:
- aggregation: sum
  description: Annual data-feed subscription value
  dimensions:
  - feed
  - partner
  name: data_feed_subscription
  unit: contract-year
name: Alliance Resource Partners Finops
provider_name: Alliance Resource Partners
provider_slug: alliance-resource-partners
publisher_name: Alliance Resource Partners, L.P.
service_category: Energy / Mining Data
slug: alliance-resource-partners-finops
source_filename: alliance-resource-partners-finops.yml
source_heading: FinOps Profile
source_url: https://www.arlp.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Alliance Resource Partners\nproviderId: alliance-resource-partners\npublisherName: Alliance Resource Partners, L.P.\nserviceCategory: Energy / Mining Data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Coal\n  - Mining\n  - Energy\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shell for Alliance Resource Partners: no public API commercial surface.\n  Data-feed and integration costs are governed by bilateral commercial agreements; reconcile against the\n  contracted feed agreement.'\nsources:\n  - https://www.arlp.com\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory:\
  \ Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Alliance Resource Partners Data Feeds\n  ServiceCategory: Energy / Mining Data\n  ProviderName: Alliance Resource Partners\n  PublisherName: Alliance Resource Partners, L.P.\n  InvoiceIssuerName: Alliance Resource Partners, L.P.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: data_feed_subscription\n    description: Annual data-feed subscription value\n    unit: contract-year\n    aggregation: sum\n    dimensions:\n      - feed\n      - partner\nprinciples:\n  - name: Visibility\n    description: Track data-feed costs through the bilateral integration agreement; ARLP does not provide\n      a public usage console.\n  - name: Allocation\n    description: Allocate feed cost to operations (logistics, royalty, customer EDI) consuming the data.\n  - name: Optimization\n    description: Right-size feeds during renewal;\
  \ consolidate redundant integrations.\n  - name: Accountability\n    description: Owned by the partner-side operations or commercial owner of the integration.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/alliance-resource-partners/refs/heads/main/finops/alliance-resource-partners-finops.yml
sources:
- https://www.arlp.com
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Coal
- Mining
- Energy
- FinOps
- FOCUS
---
