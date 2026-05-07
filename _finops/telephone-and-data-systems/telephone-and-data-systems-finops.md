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
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps shape for Telephone and Data Systems. TDS bills connectivity services (broadband, voice, video, business connectivity, wireless infrastructure) on a recurring subscription basis rather than as developer-API consumption.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Telephone and Data Systems, Inc.
  ProviderName: Telephone and Data Systems
  PublisherName: Telephone and Data Systems, Inc.
  ServiceCategory: Telecommunications / Connectivity
  ServiceName: TDS Telecom
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  - market
  name: connectivity_subscriptions
  unit: month
name: Telephone And Data Systems Finops
provider_name: Telephone and Data Systems
provider_slug: telephone-and-data-systems
publisher_name: Telephone and Data Systems, Inc.
service_category: Telecommunications / Connectivity
slug: telephone-and-data-systems-finops
source_filename: telephone-and-data-systems-finops.yml
source_heading: FinOps Profile
source_url: https://www.tdstelecom.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Telephone and Data Systems\nproviderId: telephone-and-data-systems\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Broadband\n  - Fiber Internet\n  - Fortune 500\n  - Rural Connectivity\n  - Telecommunications\n  - Wireless Infrastructure\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Telephone and Data Systems. TDS bills connectivity\n  services (broadband, voice, video, business connectivity, wireless infrastructure) on a recurring\n  subscription basis rather than as developer-API consumption.\nsources:\n  - https://www.tdstelecom.com/\nnotes: TDS does not operate a usage-priced developer API. FOCUS columns capture the publisher\n  identity; meters describe connectivity-service subscriptions rather than API requests.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Telephone and Data Systems, Inc.\nserviceCategory: Telecommunications / Connectivity\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: TDS Telecom\n  ServiceCategory: Telecommunications / Connectivity\n  ProviderName: Telephone and Data Systems\n  PublisherName: Telephone and Data Systems, Inc.\n  InvoiceIssuerName: Telephone and Data Systems, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: connectivity_subscriptions\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n      - market\nprinciples:\n  - name: Visibility\n    description: Spend is observed through TDS Telecom invoices and account portals; no developer\n      consumption export exists.\n  - name: Allocation\n    description: Allocation is by service line (residential\
  \ broadband, business broadband, voice,\n      wireless infrastructure) and market.\n  - name: Optimization\n    description: Optimization is procurement / contract-driven (term length, bundle selection)\n      rather than API-cost driven.\n  - name: Accountability\n    description: The contracting customer (residential household or business owner) is the\n      accountable cost owner of the connectivity subscription.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/telephone-and-data-systems/refs/heads/main/finops/telephone-and-data-systems-finops.yml
sources:
- https://www.tdstelecom.com/
specification: FinOps Framework
tags:
- Broadband
- Fiber Internet
- Fortune 500
- Rural Connectivity
- Telecommunications
- Wireless Infrastructure
- FinOps
- FOCUS
---
