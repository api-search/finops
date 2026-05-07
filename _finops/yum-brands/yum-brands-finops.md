---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: 'Yum! Brands does not operate a metered API; this artifact is a Contact Sales

  placeholder rather than a billable cost surface.

  '
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Yum! Brands, Inc.
  ProviderName: Yum! Brands
  PublisherName: Yum! Brands, Inc.
  ServiceCategory: Quick Service Restaurants
  ServiceName: Yum! Brands
layout: finops
meters:
- aggregation: count
  description: Negotiated brand / franchise / supplier agreement line items; not a metered API meter.
  name: partnership_agreements
  unit: varies
name: Yum Brands Finops
provider_name: Yum Brands
provider_slug: yum-brands
publisher_name: Yum! Brands, Inc.
service_category: Quick Service Restaurants
slug: yum-brands-finops
source_filename: yum-brands-finops.yml
source_heading: FinOps Profile
source_url: https://www.yum.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Yum Brands\nproviderId: yum-brands\npublisherName: Yum! Brands, Inc.\nserviceCategory: Quick Service Restaurants\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Restaurants\n  - Fast Food\n  - FinOps\n  - FOCUS\ndescription: |\n  Yum! Brands does not operate a metered API; this artifact is a Contact Sales\n  placeholder rather than a billable cost surface.\nsources:\n  - https://www.yum.com/\nnotes: |\n  No public API or invoice line-item documentation exists for Yum! Brands. Any\n  partner-side spend (royalties, supplier fees, advertising co-op contributions)\n  flows through brand-level franchise / supplier contracts,\
  \ not a developer billing\n  surface.\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Yum! Brands\n  ServiceCategory: Quick Service Restaurants\n  ProviderName: Yum! Brands\n  PublisherName: Yum! Brands, Inc.\n  InvoiceIssuerName: Yum! Brands, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: partnership_agreements\n    description: Negotiated brand / franchise / supplier agreement line items; not a\n      metered API meter.\n    unit: varies\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Spend visibility flows through the partner's own AP / contract management\n      system; Yum! Brands does not expose a usage API.\n  - name: Allocation\n    description: Allocate by brand (KFC / Pizza Hut / Taco Bell / Habit Burger) and by\n      contract type (franchise royalty, supplier, marketing co-op).\n  - name: Optimization\n    description:\
  \ Optimization happens at contract renewal (volume tiers, exclusivity, term\n      length) rather than via runtime levers.\n  - name: Accountability\n    description: Spend ownership sits with the franchisee / supplier finance lead who is\n      counterparty to the Yum! Brands agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/yum-brands/refs/heads/main/finops/yum-brands-finops.yml
sources:
- https://www.yum.com/
specification: FinOps Framework
tags:
- Restaurants
- Fast Food
- FinOps
- FOCUS
---
